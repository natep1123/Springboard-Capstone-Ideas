# Capstone Step One: Project Ideas
_Collecting and refining ideas while I finish Springboard curriculum, then I will complete the full project in its entirety._

---

## Capstone Project Proposal: Trail Incident Reporter

### Project Overview
The **Trail Incident Reporter** is a full-stack web application built with the MERN stack (MongoDB, Express.js, React, Node.js) that enables park rangers, hikers, and managers to report and track incidents on park trails, such as fallen trees, wildlife sightings, or trail damage. Inspired by my background in parks and recreation natural resource management, this app provides a practical tool for trail maintenance while showcasing my skills in full-stack development.

### Objectives
- Deliver a functional MERN application within a 1-2 week timeline as a junior developer.
- Demonstrate proficiency in user authentication, CRUD operations, and geospatial data visualization.
- Create a portfolio piece that reflects my domain knowledge and technical abilities for entry-level software engineering roles.

### Key Features
1. **User Authentication**: Secure login/register system using JWT to manage user access.
2. **Incident Reporting**: Form to submit incidents (title, description, location), stored in MongoDB.
3. **Map View**: Interactive map (via Mapbox) displaying incident locations as pins.
4. **Incident List**: Filterable list of reported incidents for easy tracking.

### Technical Details
- **Frontend**: React for a responsive UI with forms, a map component, and an incident list.
- **Backend**: Node.js/Express.js for RESTful API handling user auth and incident CRUD operations.
- **Database**: MongoDB with two collections—users and incidents (title, description, lat/long, userId).
- **External Libraries**: Mapbox API (free tier) for lightweight geospatial visualization.

### Timeline
- **Days 1-4**: Set up backend (auth, API, MongoDB) and basic frontend (login, reporting form).
- **Days 5-8**: Integrate Mapbox map and incident list; style UI.
- **Days 9-10**: Test, deploy (Heroku/Netlify, MongoDB Atlas), and document.

### Stretch Goals (Time Permitting)
- Add input sanitization for basic cybersecurity.
- Enable map-click location selection for incident reporting.
- Implement a simple severity indicator based on description keywords.

### Relevance
This project fulfills Springboard’s full-stack requirements while leveraging my parks and rec experience. It also introduces me to geospatial data and secure coding practices, aligning with my long-term interests in cybersecurity and mapping technologies.
