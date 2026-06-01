# Weekly Standup for Team 08 - Seven Ate Nine

**Date: May 28, 2026**  
**Location:** Team Standup Meeting  
**Start Time:** 9:04 PM  
**End Time:** 9:21 PM  

**Present:** Himir Desai, Matthew Bozoukov, Vinh Tong, Yang Bie, Ki Diaz  
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This standup focused on a live walkthrough of the current integrated site, including page design consistency, collector-based performance tracking, login and app-selection behavior, missing app-management features, responsiveness issues, and the team's shift toward bug discovery and final polish.

- [Weekly Standup for Team 08 - Seven Ate Nine](#weekly-standup-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Frontend Reorganization and Design Alignment](#frontend-reorganization-and-design-alignment)
    - [Performance Page and Collector Demo](#performance-page-and-collector-demo)
    - [Errors Page and Alert Testing Gaps](#errors-page-and-alert-testing-gaps)
    - [Login Flow, App Selection, and Missing App Management](#login-flow-app-selection-and-missing-app-management)
    - [Responsiveness, Accessibility, and Testing Workflow](#responsiveness-accessibility-and-testing-workflow)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Frontend Reorganization and Design Alignment

The meeting began with a walkthrough of recent frontend changes. Shadow DOM components were reorganized into a dedicated JavaScript folder, while the broader page structure stayed mostly the same.

The main UI update was an effort to make the other pages visually match the homepage. During the walkthrough, the docs page and apps page were shown as examples of this more consistent design direction.

The docs page now presents a clearer onboarding flow, including:

- Creating an account
- Registering an app
- Adding the collector to a project
- Adding the script tag to the site's HTML
- Supporting more advanced manual error reporting use cases

The team also discussed future navigation structure, with the idea that the homepage would remain distinct while performance, errors, and related product pages could sit under a more product-focused navigation layout.

### Performance Page and Collector Demo

The performance page was demonstrated live using a local lab site with the collector added.

The demo showed that:

- Performance events are being collected successfully
- New visits to the site create additional entries
- The page can display latency, load time, and related event details
- External fetch requests can also be captured and surfaced in the metrics

Examples mentioned during the demo included latency values for requests to external domains such as Google, UCSD, and Amazon. This was used to show that the collector can observe request behavior beyond only the app's own UI events.

The performance page was described as functionally working well overall. The main issue raised was visual rather than functional: the page layout is not centered correctly and leaves noticeable spacing on the right side.

### Errors Page and Alert Testing Gaps

The errors page was identified as not currently working end to end.

The issue discussed was likely not only the page itself, but the error collector path. Manual attempts to trigger errors did not produce visible error events, which suggests either:

- The collector is not capturing those errors correctly
- The test method is not representative of the type of site-generated errors the system expects

The team discussed trying a separate test app to verify this more realistically.

Email alert behavior was also raised. The team acknowledged that the alert system had not yet been fully tested. A plan was mentioned to deliberately stop the local test site, wait for the monitoring interval to pass, and then see whether a downtime email is actually sent.

### Login Flow, App Selection, and Missing App Management

The meeting confirmed progress on login-state behavior.

It was reported that:

- Logged-out users are redirected to the login page when trying to access protected pages
- Logged-in state is preserved while navigating around the site

One remaining product-flow issue was discussed around dashboard access when no app has been selected. In that case, the dashboard currently shows empty data states. The proposed fix was to redirect users to the apps page whenever local storage does not contain a selected app.

The team also identified a larger missing feature area on the projects/apps side: there is currently no way to remove an app.

This led to a proposed app settings page that could eventually support:

- Changing the app name
- Changing the app URL
- Viewing the app API key
- Deleting the app
- Possibly clearing stored app data such as performance history

As an immediate short-term step, the plan was to expose the API key soon so the team could keep testing without having to inspect the database directly.

### Responsiveness, Accessibility, and Testing Workflow

The team briefly reviewed mobile and narrow-width behavior. The standard was not to build a specialized phone experience, but the site should at least avoid breaking at smaller widths.

The performance page was specifically called out as failing this requirement, since its layout overflows on narrower screens. Other pages appeared more stable.

Accessibility was also raised as an open concern. No concrete implementation work was reported yet, but it was identified as something that may need focused cleanup before submission.

The standup closed with a team-wide testing plan for the remaining days:

- Everyone should use the site and try different flows
- Missing features and bugs should be written down as they are found
- The team should build a bug list through Sunday
- The following week should focus on fixing those bugs and preparing the final submission

The group also shared a practical note for testing updated frontend builds: browser cache and service-worker state may cause stale assets to appear after pulling new changes, so clearing site data or disabling cache in the browser may be necessary.

## Takeaways and Summary

This standup centered on validating the integrated product in practice and identifying what still needs to be fixed before submission.

1. **The integrated frontend is becoming more consistent:** docs and apps pages were updated to better match the homepage style
2. **Performance tracking is largely working:** the collector and performance page successfully displayed event, latency, and request data during the demo
3. **The errors flow still needs validation:** error collection and alerting were both described as not yet fully verified
4. **Login protection is improved:** logged-out users are redirected correctly, and logged-in sessions persist across navigation
5. **App management is incomplete:** the lack of an app settings flow currently blocks easier access to API keys and app deletion
6. **The team is now in bug-finding mode:** the immediate plan is to test broadly, document issues, and spend the next stretch on bug fixes and submission prep

**Next Steps:**

- Fix or validate the errors collector and errors page behavior
- Test whether downtime email alerts actually fire after the monitoring delay
- Redirect dashboard users to the apps page when no app is selected
- Add an API-key surface quickly, likely through a settings page or dashboard placement
- Fix the performance page layout bug on narrower widths
- Continue broad team testing, collect bugs, and use the following week for cleanup and submission work
