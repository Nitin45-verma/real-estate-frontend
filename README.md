# 🏠 Nitin Real Estate — Frontend

A modern, responsive, and feature-rich web interface for browsing, buying, and selling real estate properties. Built using **React + Vite** with Bootstrap styling, real-time chat, interactive maps, AI-powered chatbot, and Google OAuth authentication.

---

## ✨ Features

- **Property Listings & Search:** Browse, filter, and compare available properties with rich detail pages.
- **Interactive Map View:** Leaflet-powered map to explore properties by location.
- **Google OAuth Sign-In:** Secure one-click user authentication via Google Identity Services.
- **Real-Time Chat:** Socket.IO powered buyer-seller messaging on property pages.
- **AI Chatbot (Aura):** Gemini AI-based assistant for property queries and guidance.
- **EMI Calculator:** Built-in loan EMI calculator for buyers.
- **Visit Booking & Inquiry:** Schedule property visits and submit inquiries directly.
- **Razorpay Payments:** Integrated payment gateway for booking transactions.
- **Poster Generator:** Auto-generate marketing posters for properties.
- **Admin Dashboard:** Full-featured admin panel for managing properties, leads, bookings, and users.
- **Splash Screen & Animations:** Polished UI with Framer Motion page transitions.
- **Responsive UI:** Fully optimized for mobile, tablet, and desktop browsers.

---

## 🛠️ Tech Stack

| Category         | Technology                                      |
| ---------------- | ----------------------------------------------- |
| **Framework**    | React 19 + Vite 8                               |
| **Styling**      | Bootstrap 5 + Bootstrap Icons + Custom CSS      |
| **Routing**      | React Router DOM v7                             |
| **Animations**   | Framer Motion                                   |
| **Maps**         | Leaflet + React Leaflet                         |
| **HTTP Client**  | Axios                                           |
| **Real-Time**    | Socket.IO Client                                |
| **AI**           | Google Generative AI (Gemini)                    |
| **Auth**         | Google OAuth 2.0 (GSI)                          |
| **Deployment**   | Vercel / Docker (Nginx)                         |

---

## 📁 Project Structure

```
frontend/
├── public/                  # Static assets & admin.html
├── src/
│   ├── assets/              # Images, icons, and media
│   ├── components/          # Reusable UI components
│   │   ├── AdminRoute.jsx       # Protected admin route wrapper
│   │   ├── AuraChatbot.jsx      # AI chatbot (Gemini-powered)
│   │   ├── CompareDrawer.jsx    # Property comparison drawer
│   │   ├── EMICalculator.jsx    # Loan EMI calculator
│   │   ├── Footer.jsx           # Site footer
│   │   ├── InquiryModal.jsx     # Property inquiry form modal
│   │   ├── Navbar.jsx           # Navigation bar
│   │   ├── PaymentModal.jsx     # Razorpay payment modal
│   │   ├── PropertiesMap.jsx    # Leaflet map component
│   │   ├── PropertyChat.jsx     # Real-time chat component
│   │   ├── SplashScreen.jsx     # Animated splash screen
│   │   └── VisitBookingModal.jsx # Visit scheduling modal
│   ├── context/
│   │   └── AuthContext.jsx  # Authentication state provider
│   ├── pages/               # Route-level page components
│   │   ├── Home.jsx             # Landing page
│   │   ├── About.jsx            # About us page
│   │   ├── Buy.jsx              # Property listings (buy)
│   │   ├── Sell.jsx             # List your property (sell)
│   │   ├── ConnectUs.jsx        # Contact form page
│   │   ├── Login.jsx            # User login page
│   │   ├── Register.jsx         # User registration page
│   │   ├── PropertyDetails.jsx  # Single property detail page
│   │   ├── AdminDashboard.jsx   # Admin management panel
│   │   └── PosterGenerator.jsx  # Marketing poster tool
│   ├── utils/               # Utility functions & helpers
│   ├── App.jsx              # Root app component with routing
│   ├── App.css              # App-level styles
│   ├── main.jsx             # Vite entry point
│   └── index.css            # Global stylesheet
├── .env.example             # Environment variable template
├── Dockerfile               # Multi-stage Docker build (Nginx)
├── vercel.json              # Vercel rewrite rules & deployment config
├── vite.config.js           # Vite dev server & proxy config
├── eslint.config.js         # ESLint configuration
├── package.json             # Dependencies & scripts
└── README.md                # This file
```

---

## 🚀 Getting Started

### 1. Prerequisites

Ensure you have the following installed on your machine:

- **Node.js** v18+ → [Download](https://nodejs.org/)
- **npm** v9+ (comes with Node.js)

### 2. Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/Nitin45-verma/Nitin-Real-State.git
cd Nitin-Real-State/frontend
npm install
```

### 3. Environment Setup

Create a `.env` file in the `frontend/` directory using the template:

```bash
cp .env.example .env
```

Update the following variables:

```env
# Backend API URL
VITE_API_URL=http://localhost:5000

# Google OAuth Client ID
VITE_GOOGLE_CLIENT_ID=your_google_oauth_client_id.apps.googleusercontent.com
```

### 4. Run Development Server

```bash
npm run dev
```

The app will start at **http://localhost:5173** with hot module replacement (HMR) enabled.

### 5. Build for Production

```bash
npm run build
```

The optimized build output will be generated in the `dist/` folder.

### 6. Preview Production Build

```bash
npm run preview
```

---

## 🐳 Docker Deployment

Build and run the frontend as a Docker container (served via Nginx):

```bash
docker build -t nitin-realestate-frontend .
docker run -p 80:80 nitin-realestate-frontend
```

Or use the root-level `docker-compose.yml` to spin up the full stack:

```bash
cd ..
docker-compose up --build
```

---

## 🌐 Vercel Deployment

The project is pre-configured for Vercel deployment with API proxying:

1. Connect your GitHub repository to [Vercel](https://vercel.com).
2. Set the **Root Directory** to `frontend`.
3. Add environment variables (`VITE_API_URL`, `VITE_GOOGLE_CLIENT_ID`) in Vercel project settings.
4. Deploy — Vercel auto-detects Vite and builds accordingly.

API requests are proxied to the backend via `vercel.json` rewrite rules.

---

## 📜 Available Scripts

| Command             | Description                              |
| ------------------- | ---------------------------------------- |
| `npm run dev`       | Start Vite dev server with HMR           |
| `npm run build`     | Build optimized production bundle        |
| `npm run preview`   | Preview the production build locally     |
| `npm run lint`      | Run ESLint on the project                |

---

## 🔗 Related

- **Backend:** See [`../backend/README.md`](../backend/README.md) for API server documentation.
- **Live Demo:** [nitin-real-state.vercel.app](https://nitin-real-state.vercel.app)

---

## 📄 License

This project is open source and available under the [ISC License](../LICENSE).
