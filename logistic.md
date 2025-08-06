# LogiFlow UI/UX Design Guide

This document provides a structured breakdown of the logistics flow design to be implemented in Figma.

---

## 1. Main Navigation Structure

### Header Component
- **Logo + "LogiFlow" text**
- **Primary navigation**: Dashboard, Orders, Vehicles, Payments, Support
- **User profile dropdown**: Settings, Logout

### Sidebar Navigation (Logged In)
- Dashboard icon
- Orders management
- Vehicle tracking
- Payment history
- Driver management
- Customer support

---

## 2. Core Flow Components

### A. User Authentication Module

**Login Screen:**
- Email/phone + password fields
- "Forgot password" link
- Social login options: Google, Apple
- "New user? Sign up" CTA

**Signup Screen:**
- Progressive form:
  - Basic info (name, email, phone)
  - Business details (optional)
  - Password creation
  - Terms acceptance checkbox
- OTP verification (email/phone)

### B. Trip Booking Flow

**Vehicle Selection Screen:**
- Map view with available vehicles
- Filters: vehicle type, capacity, price range
- Card-based listings:
  - Vehicle image
  - Type (e.g., Thud, Multi-Circuits Helat)
  - Capacity
  - Price estimate
  - Rating (optional)
  - "Select" CTA

**Trip Details Capture:**
- Form with:
  - Origin & Destination (smart autocomplete)
  - Date/time picker
  - Contact info (pre-filled)
  - Special instructions
- "Continue to Payment" CTA

### C. Payment Flow

**Payment Selection:**
- Options:
  - Pay Now
  - Pay Later
  - Saved payment methods
- Secure payment gateway badge
- "Confirm Booking" CTA

**OTP Verification:**
- Modal/popup with OTP input
- Countdown timer + "Resend OTP"
- Visual confirmation on success

### D. Driver Assignment & Tracking

**Driver Matching Screen:**
- Animated "Finding driver" state
- Driver profile card:
  - Photo, Name, Vehicle, Rating, ETA
  - "Contact Driver" button

**Live Tracking View:**
- Interactive map:
  - Driver location pin, Route, ETA counter
- Trip details panel:
  - Pickup/drop points, Vehicle info, Payment status
- "Help" button

### E. Delivery Verification

**OTP Entry for Receiver:**
- OTP field + instruction text
- "Verify" CTA
- Error state (red border, message)

**Delivery Confirmation:**
- Success animation/illustration
- Trip summary
- Rating prompt (stars)
- "Complete" CTA

---

## 3. Special States & Error Handling

**Payment Pending State:**
- Visual indicator in order history
- "Complete Payment" CTA
- Countdown timer

**Error States:**
- OTP mismatch feedback
- Payment failure (retry options)
- Driver assignment delay notice

---

## 4. Admin/Driver Views

**Driver App:**
- Trip acceptance
- Navigation integration
- OTP collection
- Delivery confirmation

**Admin Dashboard:**
- Orders table
- Payment reconciliation
- Driver metrics
- Support interface

---

## 5. UI Style Guide

### Design System

**Fonts:**
- Inter (primary), Roboto (secondary)

**Colors:**
- Primary: #3A86FF
- Secondary: #8338EC
- Success: #06D6A0
- Error: #EF476F
- Warning: #FFD166

**Spacing:** 8px grid  
**Border Radius:** 12px (cards), 6px (buttons)

### Interactive Elements

- Button states: normal, hover, active, disabled
- Form field validation states
- Skeleton loaders
- Micro-interactions

---

## 6. Prototyping Considerations

### Key Transitions
- Vehicle selection → Booking
- Payment → OTP
- Driver assignment → Tracking
- Delivery → Rating

### User Flows
- Signup → Booking → Payment → Delivery
- Login → Repeat booking
- Driver → OTP → Delivery
- Payment failure → Retry

---

## 7. Additional Components

**Notifications:**
- Booking confirmed
- Driver assigned
- Payment receipt
- Delivery updates

**Rating & Feedback:**
- Star rating
- Comment box
- Optional photo upload

---

This structured guide enables fast and clear implementation of the logistics flow in Figma.
