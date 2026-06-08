# Standup Meeting for Team 08 - Seven Ate Nine

**Date: May 7, 2026**\
**Location: Catalyst In Person**\
**Start Time:** 5:15\
**End Time:** 5:25

**Late:** \
**Absent:** 
**Present:** Matthew Beaudin, Matthew Bozoukov, William Ayoade, Yusuf Damda, John Bolibol, Vinh Tong, Ki Diaz, Felix Tong, Yang Bie, Himir Desai, Nikita Jos

## Meeting Outline and Goals

This standup focused on team progress across backend, frontend, UX, and user story planning. The backend team reviewed its API and database architecture, the data collection subgroup summarized collector flow and payload design, the frontend team shared dashboard structure and navigation work, and the UX update reframed the MVP around uptime monitoring and user notifications. The team also aligned on creating team-specific user stories and selecting MVP stories from that set.

- [Standup Meeting for Team 08 - Seven Ate Nine](#standup-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Backend Architecture and Endpoint Planning](#backend-architecture-and-endpoint-planning)
    - [Database Structure](#database-structure)
    - [Backend Dependencies on Other Teams](#backend-dependencies-on-other-teams)
    - [Data Collection Script and Collector Flow](#data-collection-script-and-collector-flow)
    - [Frontend Dashboard Structure and Navigation Flow](#frontend-dashboard-structure-and-navigation-flow)
    - [UX Guidance and MVP Direction](#ux-guidance-and-mvp-direction)
    - [User Story Planning for Sprint 3](#user-story-planning-for-sprint-3)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Backend Architecture and Endpoint Planning

The backend team split into two temporary subteams to handle separate tasks. One subgroup focused on backend architecture, specifically endpoint planning and database structure. A summary file of planned endpoints was shared in the backend Slack channel.

**Planned account/authentication endpoints:**

- `POST` signup endpoint
- `POST` login endpoint
- `POST` logout endpoint
- `PUT` account update endpoint for actions such as password changes
- `DELETE` account deletion endpoint
- `GET` account data endpoint

**Planned data ingestion and dashboard endpoints:**

- `POST` data collection endpoint used by the target app to send telemetry to the backend
- `GET` performance data endpoint
- `GET` bug data endpoint
- `GET` feedback data endpoint
- `GET` releases data endpoint
- `GET` app data endpoint

**Planned page-serving endpoints:**

- Login page
- Sign-up page
- Homepage
- Individual app pages

### Database Structure

The backend architecture summary currently includes four main tables:

- `users`
- `apps`
- `events`
- `sessions`

These tables are placeholders for the current sprint and may be refined as UX and frontend requirements become more concrete.

### Backend Dependencies on Other Teams

The backend team identified two main dependencies:

**From the frontend team:**

- Exact page names or page routes for homepage and app pages

**From the UX team:**

- Finalized data requirements after Sprint 1
- Clarification on which metrics matter most for the MVP

The backend currently uses placeholder data categories such as performance, bugs, feedback, releases, and apps. During discussion, the team noted that availability or uptime status may also need to be added based on UX direction.

### Data Collection Script and Collector Flow

The second backend subgroup, including Nikita and Welix, reviewed the collector-side implementation plan. This discussion focused on the data collection script, the overall collector flow, and the functions required to capture and send telemetry.

**Main collector responsibilities discussed:**

- Tracking errors
- Tracking performance
- Tracking feedback
- Tracking events

The team also reviewed how collected data will be sent to the backend. The current plan is to use a backend endpoint such as `POST /collect`, along with example payloads for event submission.

For dashboard support, the team also discussed API routes needed by the frontend, including list-style routes for app, event, error, and related metrics data.

### Frontend Dashboard Structure and Navigation Flow

The frontend team also split work into two parts.

**Yusuf and Ki focused on:**

- Deciding where information should appear on the dashboard
- Creating a web skeleton for the interface structure

**Matthew and William focused on:**

- Building a navigation and flow diagram
- Mapping how a user moves from homepage to login and then into the dashboard

The dashboard mock flow includes placeholders for the metrics that will eventually be displayed. The frontend team noted that the exact metrics shown will depend on final UX guidance.

### UX Guidance and MVP Direction

John summarized feedback from office hours, where the main guidance was to shift focus toward solving a concrete user problem rather than trying to show every possible metric.

The strongest recommendation was to focus the MVP on uptime and availability monitoring:

- Notify users when a tracked website goes down
- Track whether the client page is up
- Provide light analytics as supporting information rather than the main focus

An example user story discussed was:

- As a user, I want to be notified when my website goes down so that I do not need to constantly check it myself

Pingdom was referenced as a useful product example to study. The team discussed a simplified workflow where a user provides a URL and the system reports load time and whether the page is currently available.

John also noted that a longer summary message was posted in Slack outlining professor expectations and MVP direction. In addition, the team received a response from Audria, and a comparison document combining feedback from the professor and Audria was planned for completion before midnight.

### User Story Planning for Sprint 3

The third standup topic focused on creating implementation-oriented user stories. Unlike earlier brainstorming, these user stories should map directly to features the team can realistically build.

The team proposed:

- Around 5 to 6 user stories per team
- Approximately 18 total user stories across the three teams

From those, the team would select the most important stories for the MVP:

- 3 to 4 user stories per team
- Around 9 to 12 user stories total for the MVP

Any remaining stories would stay in the backlog for later implementation if time permits.

**Examples discussed by team area:**

- UX: user notification and visibility needs, such as downtime alerts
- Frontend: minimal, readable charts that are not overloaded
- Backend: support for the routes and data required to enable those user-facing features

## Takeaways and Summary

This standup clarified both technical structure and product direction:

1. **Backend API structure expanded:** account, collection, data retrieval, and page-serving endpoints were outlined
2. **Database draft established:** users, apps, events, and sessions remain the current core tables
3. **Collector workflow clarified:** tracking functions and payload submission flow were reviewed
4. **Frontend structure progressed:** dashboard skeleton and user navigation flow were created
5. **MVP direction narrowed:** uptime monitoring and user notifications emerged as the most important feature set
6. **Cross-team dependencies identified:** backend needs finalized routes from frontend and finalized metric requirements from UX
7. **User story process defined:** each team will propose 5 to 6 stories, then narrow to MVP stories

**Key dependencies:**

- UX team must finalize which metrics and alerts are essential for the MVP
- Frontend team must provide exact page routes and dashboard metric requirements
- Backend team must adjust placeholder data categories to reflect final uptime-focused requirements

The next steps are to convert Slack and office-hours guidance into formal user stories, finalize the comparison document from professor and Audria feedback, and align implementation around the uptime-monitoring MVP.
