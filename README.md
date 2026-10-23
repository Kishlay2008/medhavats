# 🚀 SmartBook — AI-Powered Appointment & CRM Platform for Micro-Businesses

> **Google Gemini Hackathon 2026** | **Team Medhavats** (Rungta University)  
> *Track: Open Track*

---

## 📌 Problem Statement

Small service businesses in India (salons, spas, clinics, gyms) face massive operational friction:
* **Appointment Chaos:** Bookings are managed manually over fragmented WhatsApp chats, leading to double-bookings and schedule conflicts.
* **Heavy Revenue Leakage:** A **25% customer no-show rate** costs individual micro-businesses between **₹50,000 to ₹2,00,000** every month.
* **Manual Operational Toll:** Store owners waste **15+ hours per week** manually answering booking calls and coordinating schedules.
* **Zero Customer Retention:** Over **68% of first-time customers never return** due to the complete lack of automated follow-ups or loyalty systems.

---

##💡 Our Solution

**SmartBook** is an AI-driven, WhatsApp-native appointment and customer management platform designed specifically for Indian micro-businesses (under 10 staff members) that sets up in under **5 minutes**.

### Key Features:
* **WhatsApp-Native Scheduling:** Customers book, reschedule, or cancel appointments directly via WhatsApp chats or a sleek web link.
* **Automated UPI Deposits:** Collects small advance deposits via UPI to eliminate no-shows entirely.
* **AI Conversational Intelligence:** Powered by **Gemini 2.5 Flash** to parse natural language messages, screenshots, and voice notes into structured calendar events.
* **Smart Waitlist & Slot Recovery:** Automatically offers canceled slots to waitlisted customers via WhatsApp.
* **Real-Time Analytics Dashboard:** Business owners get live occupancy graphs, daily revenue analytics, and automated retention alerts.

---

## 🧠 How Gemini Powers SmartBook

SmartBook utilizes Google's Gemini API at three critical levels:

1. **Multimodal Chat Parsing:** Processes raw text, voice notes, and chat screenshots sent by customers on WhatsApp to extract desired dates, times, and service requests.
2. **Structured Data Generation (JSON Mode):** Transforms messy customer conversations into clean, structured JSON objects for seamless calendar synchronization.
3. **Agentic Function Calling:** Automatically invokes backend functions to verify slot availability, dispatch WhatsApp notification payloads, and manage waitlists.

---

## 🛠️ Tech Stack

* **Frontend:** React, Tailwind CSS, Chart.js (for analytics & dashboard visualizations)
* **Backend & Hosting:** Node.js, Express, Firebase (Firestore & Authentication)
* **AI Engine:** Google Gemini 2.5 Flash API (via Google AI Studio)
* **Payments & Messaging:** Razorpay / UPI API, Twilio / Gupshup WhatsApp Business API

---

## 📂 Repository Structure

```text
smartbook/
├── public/
│   ├── index.html        # Landing Page
│   ├── book.html         # Public Customer Booking Page
│   ├── admin.html        # Admin Real-Time Dashboard & Analytics
│   ├── manage.html       # Customer Appointment Management & Loyalty Portal
│   └── js/
│       └── firebase.js   # Firebase & Realtime Firestore Configuration
├── functions/
│   ├── index.js          # Node.js Backend & Gemini API Function Calling
│   └── whatsapp.js       # Webhook Handlers for WhatsApp API
├── README.md
└── package.json
