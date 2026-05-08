# Standup Meeting for Team 08 - Seven Ate Nine

**Date: May 5, 2026**\
**Location: Catalyst In Person**\
**Start Time:** 6:22 PM\
**End Time:** 6:30 PM

**Absent:** Nikita Jos
**Present:** Matthew Beaudin, Himir Desai, Matthew Bozoukov, Felix Tong, Yang Bie, Vinh Tong, William Ayoade, Ki Diaz, John Bolibol, Yusuf Damda\
**Late:** \
**Absent:** Nikita Jos

## Meeting Outline and Goals

This standup focuses on finalizing system architecture decisions across frontend, backend, and data collection. The team discusses dashboard design principles, data visualization research, backend technology stack, database selection, authentication system, and upcoming interview with the professor. Key outcomes include confirming technology choices (Express TS, MongoDB), establishing data visualization strategy, and scheduling the professor interview.

- [Standup Meeting for Team 08 - Seven Ate Nine](#standup-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Dashboard Design and Data Visualization](#dashboard-design-and-data-visualization)
    - [Dashboard Design Principles](#dashboard-design-principles)
    - [Data Visualization Implementation](#data-visualization-implementation)
    - [Frontend Theme and Channel Updates](#frontend-theme-and-channel-updates)
    - [Interview Planning with Professor](#interview-planning-with-professor)
    - [Backend Architecture and Technology Stack](#backend-architecture-and-technology-stack)
    - [Database Selection](#database-selection)
    - [Authentication System](#authentication-system)
    - [Data Collection Methods](#data-collection-methods)
    - [Next Sprint Goals](#next-sprint-goals)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Dashboard Design and Data Visualization

Himir shared research findings from a comprehensive document (condensed from CSE 135) covering data visualization principles and best practices. This document provides a foundational reference for dashboard design decisions across the team.

### Dashboard Design Principles

Key design patterns identified for the dashboard:

- **Progressive Disclosure:** Display an overview first, then allow users to zoom in and filter for specific metrics
- **Chart vs. Table Selection:** Simple heuristics for determining when to use charts versus tables for data presentation
- **Data Flow Considerations:** Understanding problems and considerations specific to JSON data handling

These principles will guide UI design decisions for the dashboard interface.

### Data Visualization Implementation

**Visualization Library:** Chart.js

- Used for generating graphs and visual representations of metrics
- Receives JSON data from the backend API
- Coordinates between backend and frontend teams on data format

**Rendering Technology:**

- **Canvas:** HTML5 Canvas for rendering visualizations
- **SVG:** Scalable Vector Graphics as an alternative format

**Frontend Coordination:** The frontend team will specify the JSON data format needed for Chart.js integration. The backend team will implement the API to return data in the requested format to ensure smooth integration.

### Frontend Theme and Channel Updates

The frontend team has settled on a **blue and white color scheme** for the dashboard. This theme is visible in the frontend Slack channel and will be applied consistently across all UI components.

### Interview Planning with Professor

The team is preparing for an interview with the professor to validate understanding and gather requirements:

**Meeting Details:**

- Meeting with Audrey confirmed both survey and interview are possible
- Scheduled for the professor's office hours (tomorrow, May 6)

**Preparation:**

- Created a slide deck for the interview presenting:
  - Current understanding of the system
  - System flow architecture
  - Possible MVP features
- Researched data collection requirements and possible metrics
- Summary of findings documented in team channel for reference

**Next Steps:**

- Complete the professor interview to gather authoritative requirements
- Create a summary document with findings to share with the entire team before the next standup

### Backend Architecture and Technology Stack

The backend team decided on the following technology stack:

**Framework:** Express TS

- Runs the website application
- Provides endpoint routing for both page serving and API requests
- Handles requests from frontend and data collection endpoints

**Endpoint Structure:**

1. **Page Endpoints:** `/home`, `/app`, etc.
   - Routes that serve frontend pages to users

2. **API Endpoints:**
   - `/api/collect` - Receives collected data from test applications
   - `/api/get-data/:app-id` - Retrieves data for a specific application by app ID
   - Backend team will implement data format based on frontend specifications

### Database Selection

**Database System:** MongoDB

- Chosen as the primary data storage solution
- Stores all collected metrics and application data
- Integrates with Express TS backend

### Authentication System

The team designed a simplified login system to minimize complexity:

**Signup Process:**

- Username
- Email
- Password

**Login Process:**

- Username OR Email (either credential can be used)
- Password

**Collector App Configuration:**

For test applications using Watchtower, developers add a configuration file (e.g., `watchtower-config.js`) to their target application containing:

- User's email
- Password (if necessary)
- This configuration links the test app to the developer's Watchtower account on the backend

### Data Collection Methods

The team will finalize exact data collection implementation details before the next standup.

**Built-in Browser APIs:** The professor indicated that JavaScript provides built-in functions for collecting performance metrics:

- **Example:** `window.getLoadTime()` - Built-in browser API for page load times
- Most performance data can be collected using these browser APIs without custom implementation

**Next Action:** Determine which specific browser APIs and JavaScript functions to prioritize for data collection.

### Next Sprint Goals

**Frontend Team:**

- Finalize specific UI features and layout for each page (login page, dashboard, etc.)
- Determine exact JSON data format needed from backend for Chart.js integration
- Define specific features and requirements for each interface component

**Backend Team:**

- Clarify exact data format requirements from frontend team for `/api/get-data/:app-id`
- Determine specific JavaScript browser APIs to use for data collection
- Define data collection pipeline and storage structure

**Full Team:**

- Complete professor interview and document findings
- Create summary document for team-wide review

## Takeaways and Summary

The team has made significant progress on architecture decisions:

1. **Data Visualization Strategy Established:** Chart.js selected with Canvas/SVG rendering options; progressive disclosure principle adopted
2. **Technology Stack Confirmed:** Express TS backend with MongoDB database
3. **API Design Clarified:** Page endpoints and API endpoints defined with clear separation of concerns
4. **Authentication Simplified:** Basic username/email and password system approved
5. **Collector Configuration:** Config file approach established for linking test apps to developer accounts
6. **Frontend Theme Finalized:** Blue and white color scheme established in Slack channel
7. **Professor Interview Scheduled:** Slide deck prepared with system flow and MVP features for validation

**Key Dependencies:**

- Frontend team must specify JSON data format for backend implementation
- Backend and frontend must coordinate on `/api/get-data/:app-id` response structure
- Browser API selection must be finalized before data collection implementation

The next standup should follow the professor interview and focus on requirements gathering outcomes, finalized data format specifications, and specific browser API selections.
