# JERRY HOTEL — Luxury 5-Star Hotel & Suites Website

> **Tagline:** "Experience Luxury. Discover Comfort."  
> **Aesthetic:** Elegant 5-star luxury hotel design crafted using pure **HTML5, CSS3, and Vanilla JavaScript**.

---

## 1. Project Overview

**Jerry Hotel** is a multi-page, high-end luxury hospitality website engineered with zero external JavaScript frameworks, zero CSS utility dependencies, and pure web standards. It features a bespoke champagne gold, deep obsidian black, and ivory design system, responsive layouts, a 4-step booking engine with live INR price calculations, room filtering, a full-screen image lightbox, and an interactive prototype administration portal.

---

## 2. Project Directory Structure

```
jerry-hotel/
│
├── index.html                  # Luxury Homepage with Hero, Booking Bar, Featured Suites, Dining & Testimonials
├── about.html                  # Hotel History, Five-Star Philosophy, Heritage & Values
├── rooms.html                  # Accommodations Listing with Live Category, Price & Guest Filtering
├── room-details.html           # Dynamic Suite Detail View reading ?id= query param from shared JS
├── booking.html                # 4-Step Booking Engine with Night, Tax (18% GST) & Coupon Calculation
├── booking-confirmation.html   # Printable Reservation Voucher with Unique Reference (JH-2026-XXXX)
├── restaurant.html             # The Grand Palm, L'Amour Bistro & Starlight Sky Lounge with Table Inquiry Form
├── amenities.html              # 12 Five-Star Facilities (Rooftop Pool, Royal Oasis Spa, Chauffeur Fleet)
├── offers.html                 # Special Packages (Weekend, Honeymoon, Corporate) with Live Coupon Validator
├── gallery.html                # Responsive Photo Grid with Multi-Category Filters and Full-Screen Lightbox
├── events.html                 # Imperial Ballroom Weddings, Conferences & Milestone Banquet Inquiries
├── reviews.html                # Verified Guest Testimonials with Live Review Submission Form
├── contact.html                # Contact Form, Concierge Numbers, Interactive Map Placeholder & Directions
├── faq.html                    # Searchable Accordion covering Check-in, Policies, Valet, and Dining
├── blog.html                   # The Jerry Journal Editorial Listing (Gastronomy, Wellness, Heritage)
├── blog-details.html           # Long-Form Editorial Article Reader
├── login.html                  # Jerry Club Guest Portal Sign-In Prototype
├── register.html               # Member Enrollment Prototype
├── my-bookings.html            # Guest Stay History, Profile Points & Demo Cancellation Flow
├── privacy-policy.html         # Data Governance & Client-Side Demonstration Notices
├── terms.html                  # Stay Conditions & Occupancy Guidelines
├── cancellation-policy.html    # Complimentary 24-Hour Cancellation Policy
├── 404.html                    # Luxury Custom Not Found Page
│
├── admin/                      # Administration Demonstration Portal
│   ├── index.html              # Dashboard with 4 Key KPI Metrics, Revenue SVG Chart & Recent Bookings
│   ├── rooms.html              # Suite Inventory Control, Dimensions, Rates & Preview Links
│   ├── bookings.html           # Master Reservation Ledger with Search, Status Toggles & CSV Export
│   ├── guests.html             # Guest Relations Directory with VIP Tiers & CSV Export
│   ├── offers.html             # Active Promo Codes (JERRYLUX, HONEYMOON, WELCOME10) Management
│   ├── reviews.html            # Moderation Queue for Incoming Guest Feedback
│   └── settings.html           # Operational Parameters (Check-in Hours, Tax Rates, WhatsApp Hotlines)
│
├── css/
│   ├── style.css               # Design System: Custom Properties, Typography, Luxury Buttons, Cards, Lightbox
│   ├── responsive.css          # Mobile Navigation Drawer, Breakpoints (1200px, 992px, 768px, 480px) & Print Rules
│   └── admin.css               # Portal Sidebar, Data Tables, Stat Badges, Modal Overlays
│
├── js/
│   ├── main.js                 # Header Scroll, Mobile Nav, Dark/Light Theme, AI Concierge Prototype, Toasts
│   ├── rooms.js                # Master Shared Room Dataset (6 Signature Suites), Listing Filters & Details
│   ├── booking.js              # Multi-Step Engine, Live Calculation (Nights x Rates + Addons - Discount + GST)
│   ├── gallery.js              # Gallery Categories Filter & Lightbox with Next/Prev/Esc Keyboard Controls
│   ├── contact.js              # General Inquiries, Restaurant Table Booking & Event Banquet Forms
│   ├── auth.js                 # Guest Sign In, Registration & My Bookings Synchronization
│   └── admin.js                # Admin Revenue Chart, Booking Status Mutations, Review Moderation & CSV Export
│
└── README.md                   # Complete Documentation, Setup Guide & Backend Roadmap
```

---

## 3. How to Run Locally

Because the project is written strictly in standard **HTML5, CSS3, and modern Vanilla JavaScript**, you do not need Node.js, npm, or any build tool to run or test it.

### Method A: Direct Browser File Open (Easiest)
1. Navigate to the project root directory in File Explorer / Finder.
2. Double-click `index.html` to open it in Google Chrome, Safari, Mozilla Firefox, or Microsoft Edge.
3. Every page navigates seamlessly via standard relative file paths.

### Method B: VS Code & Live Server Extension
1. Open the project folder in **Visual Studio Code**.
2. Install the **Live Server** extension by *Ritwick Dey* (Extension ID: `ritwickdey.LiveServer`).
3. Right-click `index.html` and choose **"Open with Live Server"**.
4. The site will launch automatically at `http://127.0.0.1:5500/index.html`.

### Method C: Local Python HTTP Server
Open a terminal in the project folder and run:
```bash
# Python 3
python3 -m http.server 8000
```
Then visit `http://localhost:8000` in your web browser.

---

## 4. Key Interactive Frontend Features

1. **Smart Multi-Step Booking Engine (`booking.html` & `js/booking.js`)**:
   - **Step 1:** Stay dates & party selection with automatic validation preventing past check-in dates and ensuring check-out is after check-in.
   - **Step 2:** Interactive suite selection showing dimensions, bed configs, and live nightly tariffs.
   - **Step 3:** Guest details validation (email formatting, contact phone, special dietary/arrival requests).
   - **Step 4:** Curated luxury additions (Airport Mercedes Transfer, Dom Pérignon Champagne Welcome, Couple Aromatherapy Spa) and live promo coupon validation.
   - **Step 5:** Accurate mathematical computation of nights, gross subtotal, discounts, 18% luxury GST, and grand total in INR (`₹`).
   - **Confirmation:** Issues unique reference `JH-2026-XXXX`, syncs to session storage, and offers a dedicated print voucher layout (`@media print`).

2. **Rooms Master Controller (`js/rooms.js`)**:
   - 6 Signature Suites: *Deluxe Room (₹12,500)*, *Superior Room (₹16,800)*, *Premium King (₹22,000)*, *Executive Suite (₹34,500)*, *Family Suite (₹42,000)*, and *Presidential Suite (₹75,000)*.
   - Real-time client-side filtering by category, max price slider, guest capacity, and search keywords.
   - Dynamic URL query parser for `room-details.html?id=presidential-suite` with high-res gallery thumbs.

3. **Full-Screen Gallery Lightbox (`gallery.html` & `js/gallery.js`)**:
   - Filters between *Rooms & Suites*, *Architecture*, *Fine Dining*, *Royal Oasis Spa*, and *Events*.
   - Keyboard accessible navigation (`ArrowLeft`, `ArrowRight`, `Escape` to close).

4. **Floating Jerry AI Concierge Prototype (`js/main.js`)**:
   - Virtual hospitality assistant drawer providing instant answers to FAQs (check-in hours, breakfast times, pool policies, airport transfer) with interactive query chips.

5. **Theme Switcher**:
   - Global toggle switching seamlessly between **Obsidian Dark Luxury** and **Ivory Warm Cream Light Mode**, persisted across visits via `localStorage`.

6. **Admin Demonstration Portal (`/admin`)**:
   - Visual KPI metric cards and an SVG bar chart of monthly revenue.
   - Live reservations management with status changes (*Confirmed* ➔ *Checked-In* ➔ *Completed* or *Cancelled*).
   - Review moderation queue allowing administrators to approve or remove reviews.
   - Instant CSV export for reservation records and guest contact lists.

---

## 5. Testing Checklist

- [x] **Cross-Browser Compatibility:** Tested on modern Chrome, Safari, Firefox, Edge, and iOS/Android mobile viewports.
- [x] **Navigation Integrity:** All 22 public pages and 7 admin pages link cleanly via relative paths.
- [x] **Date Validation:** Booking form rejects past dates and check-out dates preceding check-in.
- [x] **Promo Codes:** Test `JERRYLUX` (15% off), `HONEYMOON` (₹5,000 off), and `WELCOME10` (10% off).
- [x] **Room Details Query:** Navigating to `room-details.html?id=executive-suite` renders the exact specifications and gallery for the Executive Suite.
- [x] **Print Styles:** Opening print dialog on `booking-confirmation.html` hides headers, footers, and floating buttons, generating a clean invoice voucher.
- [x] **WhatsApp Widget:** Clicking WhatsApp button opens international chat with pre-filled concierge greeting.
- [x] **Keyboard Accessibility:** Lightbox opens and cycles through pictures with arrow keys; closes with `Escape`.

---

## 6. Features Requiring Future Backend Integration

Because this website is built purely with client-side HTML, CSS, and JavaScript, the following enterprise capabilities are currently simulated as frontend prototypes and are architected for straightforward backend connection:

1. **Real Payment Gateway Integration**:
   - *Requirement:* Integration with Stripe, Razorpay, or Adyen using server-side webhook listeners and PCI-DSS compliant tokenization for live transactions.
2. **Global Distribution System (GDS) & Channel Manager Sync**:
   - *Requirement:* Integration with hotel PMS systems (e.g. Opera Cloud, SynXis) via RESTful APIs to lock actual room availability in real time.
3. **Transactional Email & SMS Service**:
   - *Requirement:* Integration with SendGrid, Amazon SES, or Twilio to dispatch confirmed PDF invoices and SMS check-in reminders upon reservation.
4. **Persistent Multi-Tenant Database**:
   - *Requirement:* Relational database (PostgreSQL / MySQL) or Firebase Firestore to permanently persist reservations, guest profiles, and admin moderation states across multiple devices.
5. **Role-Based Admin Authentication**:
   - *Requirement:* Secure session tokens (JWT / HTTP-only cookies) with bcrypt hashed credentials to restrict `/admin` routes.

---

## 7. How to Publish Online

- **GitHub Pages:** Push the repository to GitHub, go to **Settings > Pages**, and choose the `main` branch.
- **Netlify / Vercel:** Drag and drop the folder into Netlify Drop or import the repository without any build commands.
- **Static Cloud Storage:** Upload directly to an AWS S3 bucket configured for static web hosting or a Google Cloud Storage bucket.

---

*© 2026 Jerry Hotel. All rights reserved. Designed for supreme five-star luxury hospitality.*
