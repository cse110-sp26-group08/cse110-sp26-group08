# Weekly Standup for Team 08 - Seven Ate Nine

**Date: May 21, 2026**  
**Location:** Team Standup Meeting  
**Start Time:** 6:20 
**End Time:** 6:30 

**Present:** Himir Desai, John Bolibol, Yusuf Damda, Ki Diaz, Yang Bie, Matthew Bozoukov, Vinh Tong, Nikita Jos, William Ayoade,Felix Tong, Matthew Beaudin  
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This standup focused on backend progress after the SQL migration, the current uptime notification design, frontend dashboard and docs-page progress, and how frontend integration should proceed now that the backend API contract is mostly unchanged.

- [Weekly Standup for Team 08 - Seven Ate Nine](#weekly-standup-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Backend SQL Migration Update](#backend-sql-migration-update)
    - [Scheduler and Triple-Check Notification Plan](#scheduler-and-triple-check-notification-plan)
    - [Frontend Progress Updates](#frontend-progress-updates)
    - [Dashboard Design Direction](#dashboard-design-direction)
    - [Frontend and Backend Integration Notes](#frontend-and-backend-integration-notes)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Backend SQL Migration Update

The backend team reported that the database layer had been migrated from MongoDB to SQL based on professor guidance.

According to the update:

- Backend controllers and schemas were changed to be SQL-based
- The frontend should require little to no major refactoring
- The main frontend-facing difference is that `_id` becomes `id`
- Function names, return types, and general backend behavior remain the same

This was framed as a low-impact backend architecture change from the frontend team's perspective, since the API contract is largely preserved.

### Scheduler and Triple-Check Notification Plan

The backend team also reviewed the notification system and uptime-check workflow that is currently being built.

The design described in the standup includes:

- A scheduler that checks each website every 5 minutes
- Recording the current result along with the previous two checks
- Keeping only the last three check records and deleting older ones
- Marking backend status values when the website's state changes
- Sending an email notification only if all three recent checks show the site is down

This triple-check design is intended to avoid false alarms while still notifying app owners about real downtime events.

### Frontend Progress Updates

The frontend team shared a few current work items during the standup.

Progress mentioned included:

- William finishing the outline for the docs page
- Ongoing backend/frontend integration work still needed before the docs page is fully complete
- A pull request that fixed some card sizing issues
- Continued work on dashboard design and layout changes

The frontend side appears to be moving from page scaffolding toward refinement and integration.

### Dashboard Design Direction

Feedback was also given on proposed dashboard changes.

The main guidance was to keep the dashboard simple. Although the current proposals were viewed as reasonably simple already, comments were made to avoid overcomplicating the design while the team continues iterating.

This means the main dashboard effort right now is less about changing backend behavior and more about:

- Simplifying presentation
- Refining the page layout
- Preserving compatibility with the data already exposed by the backend

### Frontend and Backend Integration Notes

The standup ended with a brief clarification about how frontend work should proceed alongside the SQL migration.

The response given was that frontend integration does not need to wait for a major API rewrite. Since the functions remain the same, frontend contributors can continue integrating against the backend with only the `id` versus `_id` adjustment where needed.

This was useful because it reduced uncertainty about whether new branches or major integration changes would be required after the database migration.

## Takeaways and Summary

This standup emphasized that backend infrastructure changed significantly under the hood, while frontend integration should remain mostly stable.

1. **The backend has now been migrated to SQL:** controllers and schemas were updated to match professor guidance
2. **Frontend impact from the migration is minimal:** the main expected change is replacing `_id` with `id`
3. **The notification system is being designed around a scheduler:** uptime will be checked every 5 minutes and stored as rolling recent history
4. **Three failed checks are required before emailing users:** this reduces false positives and unnecessary alert spam
5. **Frontend work is shifting toward polish and integration:** docs page progress, dashboard redesign work, and card sizing fixes were all mentioned
6. **Dashboard design should remain simple:** feedback pushed for a straightforward layout rather than a more complex redesign

**Next Steps:**

- Finish the backend scheduler and rolling three-check uptime storage
- Complete the email notification logic for confirmed outages
- Update frontend integration points to use `id` instead of `_id` where necessary
- Continue dashboard simplification and design refinement
- Integrate frontend pages with the updated backend now that the SQL migration PR is available
