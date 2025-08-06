# 🎯 Logistics UI/UX Design – Consignee & Admin Panels

Designed for Figma UI/UX Design Team

---

## 🧑‍💼 1. CONSIGNEE (BUYER) PANEL

### 🔹 Entry Point: "Book a Vehicle" CTA

#### Modal-Based 4-Step Booking Flow
| Step | UI Component | Notes |
|------|--------------|-------|
| 1. Vehicle Type | Icon Card Selector | 🚛 Truck, 🚗 Auto, 🚚 Chhota Hathi |
| 2. Trip Info | Form + Map Pins | Origin, Destination, Phone, Email |
| 3. Auth | Modal (Login/Signup) | OTP-based flow |
| 4. Price Summary | Card UI | Vehicle, ETA, Estimated Price, Confirm CTA |

---

### 🔹 Payment Flow (After Confirming Booking)
| Option | UI | Action |
|--------|----|--------|
| 💳 Pay Now | UPI/Card/Wallet | Generate Pickup OTP |
| 💸 Pay Later | Skip Payment | Mark as Payment Pending + Generate Pickup OTP |

**After OTP generation:**
- Show Assigned Driver Card:
  - 👤 Name, 📞 Phone, 🚚 Vehicle Type, 🗺️ Live Location

---

### 🔹 Pickup OTP Screen
- Enter 6-digit PIN-style OTP
- ✅ Success: Generate Delivery OTP
- ❌ Failure: Show Error Toast

---

### 🔹 Delivery OTP Flow (Receiver’s End)
- Receiver enters OTP
- If correct:
  - 💳 **Pay Now**: Mark complete, notify marketplace, auto-pay driver
  - 💸 **Pay Later**: Trigger buyer payment, then pay driver

---

### 🔹 Consignee Dashboard (Home Screen)
#### Cards Grid or Table View:
| Element | UI Component |
|---------|---------------|
| Trip ID / Status | Badge + Icons |
| Date / Time | Text |
| Vehicle Type | Icon |
| Pickup & Drop | Address Chips |
| OTP Logs | View OTP |
| Payment | Paid / Unpaid Status |
| Action | View Details / Invoice / Cancel |

#### Filters:
- Date Range, Vehicle Type, Status (Booked / In Transit / Delivered)

---

## 🛠️ 2. ADMIN PANEL

### 🔹 Trip Management Dashboard

#### List or Table View:
| Field | Description |
|-------|-------------|
| Trip ID | Unique ID |
| Buyer Info | Name + Phone |
| Vehicle Type | Icon |
| Driver Assigned | Name + Contact |
| Pickup/Drop | Address |
| Status | OTP Pending / Pickup Done / Delivered |
| Payment | Paid / Pending |
| Action | View / Force Complete / Flag |

#### Filters:
- Date, Status, Buyer, Vehicle, Driver

---

### 🔹 Live Tracking (Map View)
- Display live locations of all in-transit trips
- Color-coded markers:
  - Green: On-time
  - Yellow: Delayed
  - Red: Issue/Error
- Trip Card shown on marker click

---

### 🔹 Payment Management
| Buyer Payment Mode | Action |
|--------------------|--------|
| 💳 Paid | Auto-release driver payout |
| 💸 Pay Later | Trigger payment collection |
- Dashboard for unsettled payments
- Trigger reminders / force collection

---

### 🔹 Driver & Buyer KYC Review
| Section | Feature |
|---------|---------|
| Driver Verification | Docs Upload (License, PAN, etc.) |
| Buyer Verification | OTP, Basic Info |
| KYC Status | Verified / Pending / Flagged |
| Admin Action | Approve / Reject / Comment |

---

### 🔹 Notifications & Error Handling
- Trip OTP Failures
- Missed Deliveries
- Auto Flags for:
  - ⏳ Delayed trips
  - ❗ Invalid OTP attempts
  - 🔁 Repeated booking cancellations

---

## 🎨 UI STYLE SYSTEM

| Element | Suggestion |
|--------|------------|
| Design System | Clean, industrial dashboard layout |
| Fonts | Inter / Poppins / Open Sans |
| Color Palette |
  - Primary: Navy Blue `#1E3A8A`
  - Secondary: Slate Gray `#64748B`
  - Success: Green `#22C55E`
  - Error: Red `#EF4444`
  - Accent: Amber `#F59E0B` |
| Components | Cards, Tables, Tag Chips, Modals, Status Badges |
| Animations | Microinteractions for OTP / Transitions / Error Toasts |

---

## 🧠 UX Notes
- Every step should guide clearly: feedback → action → confirmation
- Modular screens (for dashboard design)
- Minimize manual admin input via automation
