# Weekly Standup for Team 08 - Seven Ate Nine

**Date: May 19, 2026**  
**Location:** Team Standup Meeting  
**Start Time:** Not recorded  
**End Time:** Not recorded  

**Present:** Team 08  
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This was a short standup held the day after the previous meeting. The team focused on updated backend issue assignments for uptime monitoring and notifications, current frontend page ownership, dashboard and error-page graph planning, and ongoing UI standardization work.

- [Weekly Standup for Team 08 - Seven Ate Nine](#weekly-standup-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Backend Uptime and Notification Plan](#backend-uptime-and-notification-plan)
    - [Database Direction](#database-direction)
    - [Frontend Page Ownership](#frontend-page-ownership)
    - [Dashboard and Error Graph Discussion](#dashboard-and-error-graph-discussion)
    - [Shared Component and UI Cleanup Work](#shared-component-and-ui-cleanup-work)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Backend Uptime and Notification Plan

The backend team received new issues related to uptime monitoring and email notifications.

The plan discussed in the standup was:

- Check whether each app URL is up every 5 minutes
- Save the last three uptime check records in the database
- Treat three consecutive failed checks as a confirmed downtime event
- Send an email to the app owner only after those three failures
- Avoid sending repeated emails while the site remains down
- Allow another alert only after the site comes back up and later fails again

This logic was intended to reduce false alarms and prevent email spam during longer outages.

### Database Direction

It was also mentioned that the backend storage approach may change based on professor feedback.

The team is currently considering switching from MongoDB to SQL. This was not presented as finalized during the standup, but it was described as an active possibility that could affect backend implementation choices.

### Frontend Page Ownership

The frontend team briefly reviewed who was handling which interface areas.

Current work mentioned included:

- Dashboard work continuing in stages, starting with the top section before preserving the graph area
- Error page development
- Performance page work assigned to John
- Homepage work in progress

This helped clarify ownership while the frontend team continues splitting work across pages.

### Dashboard and Error Graph Discussion

The team also discussed how graphs should differ between the main dashboard and the error page.

One concern raised was that the error page should not simply reuse the same graph structure as the main page. Since errors occur at different timestamps, the graph likely needs to represent error counts across time ranges rather than a flat or misleading line.

This means the error visualization may need:

- Timestamp-based grouping
- A line chart or similar chart tied to error frequency over time
- Different logic from the dashboard's existing summary graphs

### Shared Component and UI Cleanup Work

The standup included a quick frontend update on reusable components and UI consistency.

It was reported that:

- The navigation bar was turned into a reusable component
- That component was already being reused on the standup and login pages
- Additional work was underway to standardize the navigation bar across the site
- Dashboard HTML and styling work was still actively in progress
- There was also minor discussion about possibly changing button text and redirect behavior

These updates showed that part of the frontend effort is now shifting from one-off page work toward consistency and reuse.

## Takeaways and Summary

This standup centered on narrowing backend alert behavior and clarifying current frontend implementation work.

1. **Backend uptime logic is now more concrete:** the team discussed a 5-minute polling system with three stored checks before sending an alert
2. **Email spam prevention is part of the design:** alerts should not repeat until a site recovers and then fails again
3. **Database plans may still shift:** the team is considering moving from MongoDB to SQL based on professor guidance
4. **Frontend ownership is split across pages:** dashboard, error page, performance page, and homepage work are proceeding in parallel
5. **Error graphs need separate thinking:** error data should likely be charted by time-window counts rather than copied directly from the main dashboard
6. **UI standardization is underway:** the navigation bar has been componentized and is being reused across pages

**Next Steps:**

- Implement the uptime polling and last-three-check backend logic
- Build the email notification flow with outage-state tracking
- Decide whether the backend will remain on MongoDB or move to SQL
- Continue dashboard and error page implementation with clearer graph requirements
- Keep standardizing shared frontend components across the app
