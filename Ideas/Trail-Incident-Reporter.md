# Trail Incident Reporter

_A full-stack MERN (MongoDB, Express.js, React, Node.js) web app for park rangers, hikers, and managers to report and track trail incidents (e.g., fallen trees, wildlife sightings), inspired by my parks and recreation background._

## Overview

- **Purpose**: Enable users to report incidents with locations, view them on a map, and browse a list, even in remote areas with spotty service.
- **Target**: Built in 1-2 weeks by a junior developer for Springboard capstone, aligning with goals in geospatial data and cybersecurity.

## User Flow

1. **Access**: Open app (Netlify/Heroku) on desktop/mobile; see login page if not authenticated.
2. **Login/Register**: Enter email/password or create account; redirected to dashboard.
3. **Dashboard**: View map with incident pins and filterable list; layout splits (desktop) or stacks (mobile).
4. **Report Incident**: Fill title/description, pick location via map click (modal on mobile), submit online or cache offline.
5. **Browse**: Explore incidents on map (click pins) or list (filter by keyword).
6. **Logout**: End session, return to login.

## Features

- **Authentication**: Secure login/register with JWT; email/password stored in MongoDB.
- **Incident Reporting**: Form with title, description, and map-click location (lat/long); saves to backend or caches offline.
- **Map View**: Mapbox displays incidents as pins; popups show details; touch-friendly on mobile.
- **Incident List**: Filterable list of incidents in cards; responsive for all screens.

## Design

- **UI**: Clean, responsive (Bootstrap); desktop split (map 7/12, list/form 5/12), mobile stacked (map -> form -> list).
- **Form**: Stacked fields, full-width buttons on mobile; location via inline map (desktop) or modal (mobile).
- **Map**: Full-width on mobile (50vh), zoom/pan enabled; pins tappable with legible popups.
- **Feedback**: Success messages for reports/syncs; errors for failed logins.

## Technologies

- **Frontend**: React (UI), Bootstrap (styling), Mapbox GL JS (maps), Axios (API calls).
- **Backend**: Node.js/Express.js (REST API), MongoDB/Mongoose (data), bcrypt (hashing), JWT (auth).
- **Deployment**: Netlify (frontend), Heroku (backend), MongoDB Atlas (database).

## Location Handling

- **Method**: Users click Mapbox map to set incident location (lat/long); optional “Use My Location” (Geolocation) as stretch goal.
- **Trail ID**: No auto-detection; relies on map click or optional trail name field; preloaded trail data possible later.
- **UX**: Intuitive, no manual lat/long entry; mobile uses full-screen map modal.

## Offline Support

- **Caching**: If no service, incidents save to `localStorage` with “Saved offline” message.
- **Sync**: Auto-checks every 30s; uploads cached data to `POST /incidents` when online, refreshes UI.
- **Limits**: UI loads if cached (stretch: service worker); no live updates offline.

## Mobile-Friendliness

- **Layout**: Stacked (map, form, list); full-width elements adjust via Bootstrap grid.
- **Form**: Modal for location picking; large buttons/text for touch.
- **Map**: Touch gestures (zoom/pan) via Mapbox; sized for scrolling.

## End-to-End

- **Start**: Login -> JWT -> Load incidents (`GET /incidents`).
- **Report**: Submit form -> Save online (`POST /incidents`) or cache offline -> Sync later.
- **Browse**: Map/list update dynamically; logout clears session.

## Why It Works

- **Capstone**: Hits MERN goals (API, UI, DB) in 1-2 weeks; showcases geospatial/security basics.
- **Real-World**: Practical for trails, leverages my parks and recreation background, handles offline use.
