# 📦 Logistics Platform – UI/UX Requirements for Figma Design

## 🔄 1. Buyer Journey – Guided Booking Flow

### 🔘 Step 1: Vehicle Selection
- **Component:** Icon Cards (3-grid)
- **Options:**
  - 🚛 Truck
  - 🚗 Auto
  - 🚚 Chhota Hathi

### 🔘 Step 2: Trip Info
- **Form Fields:**
  - 📍 From Location (Auto-suggest + Map pin)
  - 📍 To Location (Auto-suggest + Map pin)
  - 📱 Phone Number (Required)
  - 📧 Email (Optional)

### 🔘 Step 3: Authentication
- If not logged in:
  - Check if user exists via phone
  - **Login:** Phone + OTP
  - **Signup:** Name, Phone, OTP

### 🔘 Step 4: Vehicle & Pricing Summary
- **UI Card Includes:**
  - 🚛 Vehicle Type
  - ₹ Estimated Price
  - 🕒 ETA
- **CTA:** `Confirm & Proceed`

---

## 💳 2. Payment Flow

### Choose Payment Option
- 💳 **Pay Now** → UPI/Card/Wallet Integration
- 💸 **Pay Later** → Skip payment, mark as “Pending”

### Pay Now Path
- On success:
  - ✅ Show "Payment Complete"
  - 📦 Show Pickup OTP

### Pay Later Path
- 🕓 Show Pickup OTP with “Pending Payment” banner

---

## 🚚 3. Vehicle Assignment

### Buyer View
- Card with:
  - 👤 Driver Name
  - 🚚 Vehicle Type
  - 📞 Driver Mobile
  - 🗺️ Map Link

### Driver View
- Assigned Trip Card:
  - 📍 Pickup & Delivery Info
  - 🔐 Awaiting Pickup OTP

---

## 🔐 4. OTP Flows

### Buyer Enters Pickup OTP
- 6-digit PIN Input
- ✅ If correct:
  - Unlock destination
  - Generate Delivery OTP
- ❌ If incorrect:
  - Show toast: “Invalid OTP. Try again.”

### Receiver Enters Delivery OTP
- ✅ If correct:
  - **Pay Now:** Mark Complete, Auto-pay Driver
  - **Pay Later:** Trigger Payment, Then Pay Driver
- ❌ If incorrect:
  - Show error toast

---

## 📊 5. Dashboards

### Buyer Dashboard
- Booking History Cards
- Filters: Date, Vehicle Type, Status
- Payment + OTP logs
- CTA: View Details / Download Invoice

### Driver Panel
- Assigned Trips
- OTP Status
- Map Integration
- Trip & Earnings Summary

### Admin Panel
- All Trip Records
- Real-Time Status
- Driver & Buyer KYC
- Payment Controls

---

## 🎨 UI Design System

| Component | UI Element |
|----------|-------------|
| Vehicle Selector | Icon Cards |
| OTP Entry | 6-digit PIN Input |
| Payment Options | Toggle / Buttons |
| Status Feedback | Toasts / Banners |
| Assignment | Info Card |
| Delivery | Timeline UI |
| Style | Rounded Cards, Clean Layout |

### Fonts
- Inter / Poppins / Open Sans

### Colors
- **Primary:** Navy Blue `#1E3A8A`
- **Secondary:** Slate Gray `#64748B`
- **Success:** Green `#22C55E`
- **Error:** Red `#EF4444`
- **Accent:** Amber `#F59E0B`

### Microinteractions
- Loading Skeletons
- OTP Animations
- Hover / Press Effects

---

## 👷‍♂️ 6. Driver/Partner Onboarding

### 5-Step Wizard
1. Basic Info + Mobile Verification
2. Vehicle Details (Multi-type)
3. Availability & Region
4. Upload License & Insurance
5. Accept Terms → Submit

---

## 🤖 7. Optional AI Matchmaking (Future)

### Input
> “Describe your delivery need”

Example: “Need a mini truck to deliver furniture from Chennai to Coimbatore”

### Output
- “3 Vehicles Matched”
- Vehicle Cards with Price & ETA
- CTA: `Book Now`
