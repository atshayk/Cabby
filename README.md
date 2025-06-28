# 🚕 Cabby – Corporate Cab Booking Platform

**Cabby** is a full-stack web application designed to streamline and manage cab bookings for corporate offices through a network of registered vendors. It facilitates real-time booking management, vehicle/driver coordination, and open market fallback systems for unfulfilled rides.

## 🧩 Project Overview

Cabby allows companies to book rides for employees or clients using associated vendors. Vendors can accept, reject, or place requests into an open market system, enabling first-come-first-serve fulfillment across their network.

The platform includes dashboards for companies and vendors, full trip lifecycle tracking, driver and vehicle management, invoicing, and real-time messaging via RabbitMQ.

## 🌟 Features

### 🏢 Company Dashboard
- Book rides with guest and trip details.
- Track bookings by status: Upcoming, Ongoing, Completed, Cancelled.
- View history and trip information.

### 🧑‍🔧 Vendor Dashboard
- Receive and respond to real-time booking requests.
- Assign drivers and vehicles upon acceptance.
- Manage driver and vehicle records.
- Submit manual bookings (offline/phone requests).
- Submit and track invoices and payments.
- Create and save custom data views/tables.

### 🔁 Open Market Logic
- Unfulfilled bookings can be placed in the Open Market.
- 30 min: visible only to associated vendors.
- After 30 min: opens to all eligible vendors.
- First vendor to accept gets the booking (SLA tracked).

### 🛣️ Trip Lifecycle
- Statuses: `requested → accepted → ongoing → completed/cancelled`.
- Trip start and end simulated via action buttons.

## 🛠️ Tech Stack

| Layer       | Technology                        |
|------------|------------------------------------|
| Frontend   | Next.js (TypeScript), TailwindCSS, Shadcn/UI |
| Backend    | Node.js (Express.js)               |
| Database   | Supabase              |
| Messaging  | RabbitMQ (via CloudAMQP)           |
| Auth       | JWT-based, Role-based Access       |
| Deployment | Vercel (Frontend), Railway/AWS/Docker (Backend) |


## 🤝 Contributing

Pull requests are welcome! Please open an issue first to discuss what you'd like to change.
