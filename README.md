# Movie Ticket Booking Management Application

Pega Platform project built for **CineWave Entertainment** as part of the National Internship Program (NIP), Pega Academy 2026.

## Overview

CineWave Entertainment manages movie ticket bookings across multiple theatres and locations. This application replaces manual, email-based booking tracking with a structured Pega case management workflow — allowing customers to request bookings, staff to manage show availability, and the system to automatically calculate cost, allocate seats, generate tickets, and notify customers.

## Application Details

- **Application Name:** NIP-MovieTicket-MahalakshmiM
- **Case Type:** Movie Ticket Request
- **Built With:** Pega Infinity (Pega Blueprint + App Studio)

## Case Lifecycle

1. **Initial Request** — Customer submits Movie Name, Show Date, Show Time, and Number of Tickets. All fields are required and validated.
2. **Availability** — System captures Seat Availability Status and Available Seats Count. Booking cannot proceed unless seats are marked available. Booking cost is calculated automatically as Ticket Price × Number of Tickets.
3. **Approval** — Customer reviews Movie Name, Show Time, Number of Tickets, and Total Cost, then confirms or cancels the booking. Cancelled bookings resolve immediately without further processing.
4. **Booking Execution** — System sets Booking Confirmation Status, Seat Numbers, and Ticket ID, and routes the case to PremiumShowQueue or StandardShowQueue based on Show Type.
5. **Resolved** — Booking is finalized and a confirmation notification is sent to the customer.

## Key Features

- Reusable **Movie** and **Show** data objects for consistent movie/show information across bookings
- Automatic **Total Cost** calculation via a Data Transform (CalculateTotalCost)
- Validation logic preventing booking progress when seats are unavailable
- Conditional stage-skipping for cancelled bookings
- Automated correspondence on case resolution
- Service Level Agreement: 1-day goal, 2-day deadline, with automatic urgency escalation
- Automatic work-queue routing based on Show Type (Premium vs Standard)

## Repository Contents

- `Ticketing_and_Booking_*.blueprint` — Exported Pega Blueprint file used to scaffold this application
- `README.md` — This file

## Author

**Mahalakshmi M**
BTech Computer Science and Business Systems
VSB Engineering College
