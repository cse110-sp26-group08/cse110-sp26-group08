# Weekly Meeting for Team 08 - Seven Ate Nine

**Date: May 18, 2026**  
**Location:** Team Weekly Meeting  
**Start Time:** 4:00  
**End Time:** 4:45  

**Present:** Team 08  
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This weekly meeting focused on frontend design consistency, backend API support for metrics collection, backlog review, database planning, and dashboard design feedback. Himir reviewed several current implementation decisions, relayed feedback connected to professor guidance, and helped refine both technical priorities and frontend direction.

- [Weekly Meeting for Team 08 - Seven Ate Nine](#weekly-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Frontend Consistency Feedback](#frontend-consistency-feedback)
    - [Backend Endpoint Updates](#backend-endpoint-updates)
    - [Backlog and Database Discussion](#backlog-and-database-discussion)
    - [Backend Task Adjustments](#backend-task-adjustments)
    - [Dashboard Design Review](#dashboard-design-review)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Frontend Consistency Feedback

Himir pointed out several frontend inconsistencies that still need to be addressed.

The main concerns raised were:

- `app_selection.js` was not fully consistent with the rest of the frontend flow
- The navigation bar design was not visually or structurally consistent with the homepage

This feedback emphasized that the frontend should feel more unified across pages rather than appearing as separate pieces built with different design approaches. The team will need to align navigation and page structure more carefully as the interface continues to develop.

### Backend Endpoint Updates

The backend team reported that post endpoints had now been provided for the frontend team to use.

These endpoints were intended to let the frontend make calls that collect:

- Error data
- Metric or performance data

This support should allow the frontend to begin integrating real backend data into the dashboard rather than relying only on placeholder or hardcoded values.

### Backlog and Database Discussion

Himir reviewed the current backlog and raised an important architectural point from the professor. According to that guidance, a SQL database may be more appropriate than MongoDB for handling non-static data.

This did not necessarily mean an immediate database switch would happen during the meeting, but it did mean the team needed to think more carefully about long-term data structure decisions and how dynamic application data should be stored going forward.

The database discussion was tied directly to backlog review, since backend priorities and future implementation tasks may need to change depending on whether the team continues with MongoDB or moves toward a SQL-based solution.

### Backend Task Adjustments

Himir also went through the backend team’s current task list and adjusted it during the meeting.

This task review helped clarify:

- Which backend items were still active
- Which priorities needed to be changed
- What work should come next based on the updated backlog discussion

The result was a more refined backend plan aligned with the team’s current state and outside feedback.

### Dashboard Design Review

Yusuf presented the current dashboard design during the meeting.

Himir gave direct feedback on what parts of the dashboard design were working and what parts were not. The discussion helped identify both strengths and weaknesses in the current design direction, giving the frontend team more concrete guidance on how to revise the dashboard moving forward.

This review was useful because it moved the dashboard discussion beyond general progress updates and into specific design critique.

## Takeaways and Summary

This meeting focused on tightening consistency, improving backend/frontend coordination, and refining current priorities.

1. **Frontend consistency still needs work:** `app_selection.js` and the navigation bar do not yet match the rest of the site closely enough
2. **Backend integration is moving forward:** the frontend now has post endpoints it can use to send or collect error and metric data
3. **Database planning may need to change:** professor feedback suggested SQL may be a better fit than MongoDB for non-static data
4. **The backlog was actively refined:** current tasks were reviewed in light of new feedback and adjusted accordingly
5. **Dashboard design received targeted critique:** Yusuf’s design presentation gave Himir a chance to identify both strong and weak parts of the current direction

**Next Steps:**

- Make the frontend flow and navigation more consistent across pages
- Begin using the new backend endpoints in frontend dashboard integration
- Reevaluate database direction based on professor feedback
- Continue backend work using the adjusted task list
- Revise the dashboard design based on the review comments
