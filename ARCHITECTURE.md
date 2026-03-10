# BloodLink Emergency Donor System Architecture

This project utilizes a Serverless architecture powered by Firebase, mapped to the requested folder layout:

## 🌐 Frontend
- `frontend/pages/` - Future home for discrete HTML logic chunks.
- `frontend/components/` - Future home for reusable UI components (e.g. Nav, Footer snippet).
- `frontend/dashboard/` - Contains dashboard rendering logic and stats logic.
- `frontend/map/` - Contains Leaflet.js rendering logic.

## ⚙️ Backend
As a serverless platform, the backend logic runs directly via Firebase SDK in `js/` or via Cloud Functions.
- `backend/routes/` - Handled via Firebase native routing.
- `backend/controllers/` - Reflected in Javascript handlers (e.g., `admin.js`, `dashboard.js`).
- `backend/models/` - Firebase NoSQL data definitions.
- `backend/services/` - Firestore SDK API configurations (`firebase-config.js`).

## 🗄️ Database
- `database/donors/` - Represents the Firestore `donors` collection handling active users, locations.
- `database/blood_requests/` - Represents the Firestore `requests` collection storing Hospitals, Patient Names, Priorities, and exact Geospatial Coordinates.
