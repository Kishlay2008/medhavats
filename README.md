# SmartBook — Universal B2B2C Reservation & Appointment Engine

A hackathon-ready, full-stack web application for service-based enterprises to manage bookings, payments, and customer communication.

## Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | Next.js 14 (App Router), TypeScript, Tailwind CSS, Shadcn UI |
| Backend | Node.js, Express, TypeScript, Prisma ORM |
| Database | PostgreSQL (via Prisma) |
| Real Integrations | Gemini API, Google Maps API, FamPay API, Twilio API |
| Mocked Integrations | Google Calendar API, Google Meet API, Cloud Storage |

## Repository Structure

```
smartbook-web/
├── client/                 # Next.js Frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   └── app/            # App Router pages
│   └── .env.local          # Frontend env vars (Google Maps)
└── server/                 # Express Backend
    ├── src/
    │   ├── controllers/    # Request handlers
    │   ├── services/       # Business logic & external APIs
    │   ├── models/         # Prisma schema
    │   └── server.ts       # Express entry point
    └── .env                # Backend env vars (Gemini, Twilio, FamPay)
```

## Environment Variables

### Backend (`server/.env`)
```bash
GEMINI_API_KEY=AQ.Ab8RN6LJVbTffUvi5VhDK6GcdIoOT-McPWiS-0vLCZoiSMIcGA
TWILIO_ACCOUNT_SID=AC8bc34dc8ac3b3a5a336207551ee2c846
TWILIO_AUTH_TOKEN=6cd5e076962270e1f6a74d46cf0728ce
FAMPAY_API_KEY=fam_af8dcc8ae13251889832052c048b6ab8ee221671
DATABASE_URL="postgresql://user:password@localhost:5432/smartbook?schema=public"
PORT=3001
```

### Frontend (`client/.env.local`)
```bash
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=AIzaSyDu147TPWah4EemvOAVwVz-w9DkZw-EPGQ
NEXT_PUBLIC_API_URL=http://localhost:3001
```

## Getting Started

### Prerequisites
- Node.js 18+
- PostgreSQL 14+
- npm or pnpm

### Backend Setup
```bash
cd server
npm install
npx prisma generate
npx prisma db push
npm run dev
```

### Frontend Setup
```bash
cd client
npm install
npm run dev
```

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/bookings` | Create a new booking |
| GET | `/api/bookings/:id` | Get booking details |
| POST | `/api/payments` | Process payment via FamPay |
| POST | `/api/media/upload` | Upload media to local storage |
| POST | `/api/ai/chat` | Chat with Gemini assistant |
| POST | `/api/waitlist/notify` | Trigger SMS notifications |

## Mocked Integrations

- **Google Calendar**: `services/calendarSync.ts` returns `200 OK` without OAuth
- **Google Meet**: `controllers/bookingController.ts` generates `https://meet.google.com/mock-xyz-abc`
- **Cloud Storage**: `controllers/mediaController.ts` saves to `server/uploads/`

## License

MIT