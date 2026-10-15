# RideSync

RideSync is a full-stack ride-booking application built with the MERN stack. It brings riders and captains together through separate user experiences: riders can enter pickup and destination details, view estimated fares, and request a ride, while captains can review ride requests, confirm trips, and complete rides. Google Maps services power address suggestions and route information, and Socket.IO supports real-time ride events. The project combines a React and Vite frontend with an Express and Node.js API, MongoDB persistence, and JWT-based authentication.

> Independent educational project; not affiliated with or endorsed by Uber.

## Features

- Rider and captain registration, login, and protected pages
- Ride requests, fare estimates, captain confirmation, and ride completion
- Google Maps address suggestions, route information, and map display
- Real-time ride events and captain location updates with Socket.IO
- JWT-based authentication backed by MongoDB

## Tech Stack

- Frontend: React, Vite, Tailwind CSS, React Router
- Backend: Node.js, Express, Mongoose
- Database: MongoDB
- Real-time communication: Socket.IO
- Maps: Google Maps Platform

## Prerequisites

- Node.js and npm
- A MongoDB database, local or hosted
- A Google Maps Platform API key with the required Maps JavaScript, Places, Geocoding, and Distance Matrix APIs enabled

## Getting Started

### 1. Configure the backend

```powershell
cd Backend
npm install
npm install socket.io
```

Create `Backend/.env`:

```env
PORT=3000
DB_CONNECT=mongodb://127.0.0.1:27017/ridesync
JWT_SECRET=replace_with_a_long_random_secret
GOOGLE_MAPS_API=your_google_maps_api_key
```

The backend currently imports Socket.IO without listing it in `Backend/package.json`, so the additional install command is required for a fresh setup.

### 2. Configure the frontend

In a second terminal:

```powershell
cd frontend
npm install
```

Create `frontend/.env`:

```env
VITE_BASE_URL=http://localhost:3000
VITE_API_URL=http://localhost:3000
VITE_GOOGLE_MAPS_API_KEY=your_google_maps_api_key
```

Both URL variables are used by the current frontend code. Use the deployed backend URL instead when running against a hosted API.

### 3. Start the application

Start the backend from `Backend/`:

```powershell
node server.js
```

Start the frontend from `frontend/`:

```powershell
npm run dev
```

Open the local URL printed by Vite, usually `http://localhost:5173`.

## Project Structure

```text
Backend/   Express API, MongoDB models, authentication, rides, maps, and sockets
frontend/  React application, rider and captain pages, and UI components
```

## Author

Tayyaba
