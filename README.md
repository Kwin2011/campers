# TravelTrucks — Frontend Test Project

This project is a frontend implementation for **TravelTrucks**, a camper rental service.  
The goal is to build a multi-page React application with catalog browsing, filtering, camper details, reviews, and a booking form.

## 🔧 Tech Stack

- **React + Vite**
- **Redux Toolkit**
- **React Router**
- **Axios**
- **CSS solution of choice** (CSS Modules, Styled Components, MUI etc.)

## 🚀 Features

### 📌 Pages

| Route | Description |
|-------|-------------|
| `/` | Home page with a banner and CTA button “View Now” |
| `/catalog` | Catalog of campers with filtering and “Load More” |
| `/catalog/:id` | Detailed camper page with gallery, characteristics, reviews, and booking form |

## 📂 API

Backend is provided via MockAPI:

https://66b1f8e71ca8ad33d4f5f63e.mockapi.io/campers


### Endpoints:

- **GET** `/campers` — list of campers (supports query params)
- **GET** `/campers/:id` — camper details

## 🧭 Requirements Implemented

### ▶ Home Page
- Banner with CTA
- Button **“View Now”** navigates to `/catalog`

### ▶ Catalog Page
- List of campers with:
  - image  
  - name  
  - description  
  - rating  
  - location  
  - price formatted as `8,000.00`
- Filters:
  - location (text input)
  - vehicle type (single choice)
  - features (AC, kitchen, bathroom, etc.)
- Add/remove from Favorites (saved in localStorage)
- “Show More” on card → opens camper in **new tab**
- “Load More” button → loads more results with the same filters

### ▶ Camper Details Page
- Photo gallery
- Overview + full characteristics:
  - `transmission, engine, AC, bathroom, kitchen, TV, radio, refrigerator, microwave, gas, water`
- Detailed info:
  - `form, length, width, height, tank, consumption`
- Reviews (1–5 stars)
- Booking form + success notification

## 🗄 State Management (Redux)

Global state stores:
- campers list
- filters
- favorites
- pagination
- selected camper details

When filters change:
- previous results are cleared before fetching

## 📁 Project Structure (example)

src/
├─ api/
│ └─ campersApi.js
├─ components/
├─ pages/
│ ├─ Home/
│ ├─ Catalog/
│ └─ CamperDetails/
├─ redux/
│ ├─ store.js
│ ├─ campersSlice.js
│ ├─ filtersSlice.js
│ └─ favoritesSlice.js
├─ utils/
├─ styles/
└─ App.jsx


## 📦 Installation

```bash
npm install
npm run dev

## 📦 Installation

```bash
npm install
npm run dev
🌐 Deployment
Deploy on Vercel or Netlify.

Add your link here:

https://your-project-url.com
📝 Notes
Desktop layout required; adaptive optional.

DRY principle, clean structure.

Axios for all API calls.

Comments added where needed.