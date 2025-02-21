# ASCII Art Gallery

_A full-stack MERN (MongoDB, Express.js, React, Node.js) web app for users to create, share, and rate ASCII art, celebrating retro creativity with a community focus._

## Overview

- **Purpose**: Enable users to craft ASCII art, display it in a gallery, and engage through ratings and comments, fostering a playful creative space.
- **Target**: Built in 1-2 weeks by a junior developer for Springboard capstone, aligning with goals in user interaction and dynamic content.

## User Flow

1. **Access**: Open app (Netlify/Heroku) on desktop/mobile; see login page if not authenticated.
2. **Login/Register**: Enter email/password or create account; redirected to dashboard.
3. **Dashboard**: View top-rated art gallery and leaderboard; tab for “Create Art.”
4. **Create Art**: Fill title, category, and ASCII text in editor; preview and submit.
5. **Browse**: Explore gallery (filter by category/rating), rate art, add comments.
6. **Logout**: End session, return to login.

## Features

- **Authentication**: Secure login/register with JWT; email/password stored in MongoDB.
- **Art Creation**: Form with title, category dropdown, and monospace textarea; saves to backend with live preview.
- **Gallery**: Filterable grid of art cards (title, art, rating); sortable by rating or newest.
- **Interaction**: Rate art (1-5 stars), comment on entries; leaderboard shows top artists.

## Design

- **UI**: Retro, responsive (Bootstrap); desktop split (editor 4/12, gallery/leaderboard 8/12), mobile stacked (editor -> gallery).
- **Form**: Monospace textarea with preview `<pre>` below, category dropdown, full-width submit button.
- **Gallery**: Cards with art in `<pre>`, star rating widget, collapsible comments; leaderboard in a fixed box.
- **Feedback**: Success toast for posted art; errors for failed logins or duplicates.

## Technologies

- **Frontend**: React (UI), Bootstrap (styling), Axios (API calls), React-Star-Rating (ratings).
- **Backend**: Node.js/Express.js (REST API), MongoDB/Mongoose (data), bcrypt (hashing), JWT (auth).
- **Deployment**: Netlify (frontend), Heroku (backend), MongoDB Atlas (database).

## Art Handling

- **Method**: Users type ASCII in a textarea; preview renders live in `<pre>`; saved as plain text in MongoDB.
- **Categories**: Predefined list (e.g., Animals, Sci-Fi, Nature); selected via dropdown.
- **UX**: Intuitive editor with real-time preview; no manual formatting required.

## Offline Support

- **Caching**: If offline, art saves to `localStorage` with “Saved offline” message.
- **Sync**: Checks every 30s; uploads cached data to `POST /artworks` when online, refreshes UI.
- **Limits**: Gallery loads cached art; no ratings/comments offline (stretch: service worker).

## Mobile-Friendliness

- **Layout**: Stacked (editor, gallery, leaderboard); full-width cards via Bootstrap grid.
- **Form**: Large textarea and buttons for touch; preview scrolls if tall.
- **Gallery**: Touch-friendly ratings (tap stars); comments collapse/expand on tap.

## End-to-End

- **Start**: Login -> JWT -> Load gallery (`GET /artworks`).
- **Create**: Submit form -> Save (`POST /artworks`) -> Update gallery.
- **Browse**: Rate (`PATCH /artworks/:id/rate`), comment (`POST /artworks/:id/comments`) -> Refresh UI; logout clears session.

## Why It Works

- **Capstone**: Hits MERN goals (API, UI, DB) in 1-2 weeks; showcases user interaction and community features.
- **Real-World**: Niche but engaging for retro enthusiasts; stands out with its creative, playful focus.
