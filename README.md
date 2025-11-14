# MaidEase Frontend (React PWA)

The MaidEase frontend is a **React-based Progressive Web App (PWA)** that provides a smooth, mobile-friendly experience for both customers and maids.  
It communicates with the backend via REST APIs and supports offline caching through PWA features.

---

## Tech Stack
- React (with Vite)
- Redux Toolkit (state management)
- React Router
- Axios
- TailwindCSS
- PWA Service Worker
- Jest + React Testing Library

---

## How the Frontend Works (System Flow Explained)

### 🏁 1. Landing Page → Login / Signup
- New users can register as Customer or Maid.
- Existing users log in and receive a JWT token.
- The token is stored in `localStorage`.

### 2. Role-Based Dashboards
After login, the UI redirects based on role:

#### **Customer Dashboard**
- Browse maids  
- Apply filters (skills, rate, availability)  
- Create booking requests  
- View booking statuses  
- Leave reviews for completed jobs  

#### **Maid Dashboard**
- Manage profile and skills  
- Set available time slots  
- View booking requests  
- Accept or reject requests  
- View job history and customer reviews  

### 3. API Communication
- Axios handles API calls.
- JWT token added automatically to request headers.
- API errors are displayed as user-friendly messages.

### 4. PWA Features
- Add to Home Screen  
- Offline caching for static assets  
- Faster load times even on slow networks  

---

## Project Structure
src/
├─ components/
├─ pages/
├─ store/
├─ hooks/
├─ utils/
├─ tests/
└─ main.jsx
