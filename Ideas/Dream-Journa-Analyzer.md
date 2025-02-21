# Dream Journal Analyzer

_A full-stack MERN (MongoDB, Express.js, React, Node.js) web app for users to log dreams, analyze their mood and themes, and reflect on patterns over time, inspired by a curiosity for personal insight._

## Overview

- **Purpose**: Enable users to record dreams, receive simple AI-driven analysis (mood, themes), and visualize trends, offering a unique introspective tool.
- **Target**: Built in 1-2 weeks by a junior developer for Springboard capstone, aligning with goals in data persistence and basic NLP.

## User Flow

1. **Access**: Open app (Netlify/Heroku) on desktop/mobile; see login page if not authenticated.
2. **Login/Register**: Enter email/password or create account; redirected to dashboard.
3. **Dashboard**: View mood trend chart and recent dreams list; tabs for “Log Dream” and “History.”
4. **Log Dream**: Fill text, optional tags, and submit; see instant analysis (e.g., “Positive, Flying”).
5. **Browse**: Explore dream history in a filterable list or trend chart; click entries for details.
6. **Logout**: End session, return to login.

## Features

- **Authentication**: Secure login/register with JWT; email/password stored in MongoDB.
- **Dream Logging**: Form with text, date, and tags; saves to backend with analysis.
- **Analysis Engine**: Sentiment analysis (via `natural`) and theme detection (keyword-based); results displayed inline.
- **History & Trends**: Filterable dream list (date, tag, mood); Chart.js line graph for mood over time.

## Design

- **UI**: Clean, responsive (Bootstrap); desktop split (form 4/12, chart/list 8/12), mobile stacked (form -> chart -> list).
- **Form**: Textarea for dream, tag dropdown, full-width submit button; analysis below in a card.
- **Chart**: Full-width on mobile (40vh), interactive with tooltips; green/red points for mood.
- **Feedback**: Success toast for saved dreams; errors for failed logins.

## Technologies

- **Frontend**: React (UI), Bootstrap (styling), Chart.js (trends), Axios (API calls).
- **Backend**: Node.js/Express.js (REST API), MongoDB/Mongoose (data), `natural` (NLP), bcrypt (hashing), JWT (auth).
- **Deployment**: Netlify (frontend), Heroku (backend), MongoDB Atlas (database).

## Analysis Handling

- **Method**: Backend processes text with `natural` for sentiment (positive/negative) and matches predefined themes (e.g., “flying,” “water”).
- **Themes**: Static list (~10 keywords); no complex AI, just simple matching.
- **UX**: Analysis auto-generates on submit; displayed as a concise summary card.

## Offline Support

- **Caching**: If offline, dreams save to `localStorage` with “Saved offline” message.
- **Sync**: Checks every 30s; uploads cached data to `POST /dreams` when online, refreshes UI.
- **Limits**: UI loads cached dreams; no analysis offline (stretch: service worker).

## Mobile-Friendliness

- **Layout**: Stacked (form, chart, list); full-width elements via Bootstrap grid.
- **Form**: Large textarea and buttons for touch; tags in a dropdown.
- **Chart**: Touch-friendly (zoomable); sized for scrolling below list.

## End-to-End

- **Start**: Login -> JWT -> Load dreams (`GET /dreams`).
- **Log**: Submit form -> Analyze (backend) -> Save (`POST /dreams`) -> Update UI.
- **Browse**: Filter dreams (`GET /dreams?filter=...`) -> Render list/chart; logout clears session.

## Why It Works

- **Capstone**: Hits MERN goals (API, UI, DB) in 1-2 weeks; showcases basic NLP and data visualization.
- **Real-World**: Appeals to users seeking self-reflection; unique twist on personal journaling apps.
