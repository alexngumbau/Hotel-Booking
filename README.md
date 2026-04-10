# Hotel Booking Platform

🌐 **Live Demo:** [https://hotel-booking-cyan-psi.vercel.app](https://hotel-booking-cyan-psi.vercel.app)

A full-stack hotel booking platform where users can browse hotels, view room details, and manage their bookings, alongside a hotel owner dashboard for listing and managing rooms.

## Features

### Guest / User
- Browse featured destinations and exclusive offers
- Search rooms by destination, check-in, and check-out dates
- View detailed room information and ratings
- Book rooms securely with authentication via Clerk
- View and manage personal bookings

### Hotel Owner
- Dedicated owner dashboard with booking statistics and revenue overview
- Add and list rooms with images and details
- Track recent bookings in real time

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | React 19 |
| Routing | React Router DOM v7 |
| Styling | Tailwind CSS v4 |
| Authentication | Clerk |
| Build Tool | Vite v7 |
| Deployment | Vercel |

## Project Structure

```
client/
├── public/
├── src/
│   ├── assets/          # Static assets and dummy data
│   ├── components/      # Reusable UI components
│   │   ├── hotelOwner/  # Owner-specific components (Navbar, Sidebar)
│   │   ├── Hero.jsx
│   │   ├── Navbar.jsx
│   │   ├── Footer.jsx
│   │   ├── HotelCard.jsx
│   │   ├── StarRating.jsx
│   │   ├── ExclusiveOffers.jsx
│   │   ├── FeaturedDestination.jsx
│   │   ├── Testimonial.jsx
│   │   └── NewsLetter.jsx
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── AllRooms.jsx
│   │   ├── RoomDetails.jsx
│   │   ├── MyBookings.jsx
│   │   └── hotelOwner/
│   │       ├── Layout.jsx
│   │       ├── Dashboard.jsx
│   │       ├── AddRoom.jsx
│   │       └── ListRooms.jsx
│   ├── App.jsx
│   └── main.jsx
├── .env
├── package.json
└── vite.config.js
```

## Getting Started

### Prerequisites

- Node.js >= 18
- A [Clerk](https://clerk.com) account for authentication

### Setup

1. **Clone the repository**

   ```bash
   git clone https://github.com/alexngumbau/Hotel-Booking.git
   cd Hotel-Booking/client
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Configure environment variables**

   Create a `.env` file in the `client/` directory:

   ```env
   VITE_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
   ```

4. **Start the development server**

   ```bash
   npm run dev
   ```

   The app will be available at `http://localhost:5173`.

### Build for Production

```bash
npm run build
```

## Deployment

The project is configured for deployment on **Vercel**. The `vercel.json` file includes SPA rewrite rules to handle client-side routing:

```json
{
  "rewrites": [{ "source": "/(.*)", "destination": "/" }]
}
```

## Live Demo

[https://hotel-booking-cyan-psi.vercel.app](https://hotel-booking-cyan-psi.vercel.app)
