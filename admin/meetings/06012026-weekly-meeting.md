# Weekly Meeting for Team 08 - Seven Ate Nine

**Date: June 1, 2026**  
**Location:** Team Weekly Meeting  
**Start Time:** 4:04 PM  
**End Time:** 4:29 PM  

**Present:** Himir Desai, Matthew Bozoukov, Yang Bie, Yusuf Damda, Nikita Jos, Ki Diaz, Vinh Tong Matthew Beaudin, John Bolibol, William Ayoade, Felix Tong
**Late:**  
**Absent:** 

## Meeting Outline and Goals

This weekly meeting focused on final bug triage, assigning the remaining GitHub issues, clarifying a few ambiguous issue definitions, and setting a short deadline so the team could finish bug fixes before deployment and final validation.

- [Weekly Meeting for Team 08 - Seven Ate Nine](#weekly-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Bug Triage and Assignment Plan](#bug-triage-and-assignment-plan)
    - [Navbar and Logged-In State Issues](#navbar-and-logged-in-state-issues)
    - [Privacy Policy, CORS, and Missing Issues](#privacy-policy-cors-and-missing-issues)
    - [Homepage Cleanup and Small UX Fixes](#homepage-cleanup-and-small-ux-fixes)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Bug Triage and Assignment Plan

Himir opened the meeting by noting that the team had roughly 17 open GitHub issues, representing the current known bug list.

The main instruction for the week was:

- Everyone should immediately assign themselves a bug on GitHub
- Simple bugs should be finished first before the team moves to more complex fixes
- The goal is to finish all current bugs by Wednesday or, at worst, Thursday

The reasoning was practical: if the team tackles only harder issues first, those changes may introduce additional bugs and create extra cleanup work right before deployment.

During the meeting, team members claimed issues live. Yang took Issue #70, Yusuf took Issue #74, Matthew Bozoukov took Issue #75 and said he could also handle Issue #73, and Nikita initially volunteered for Issues #84 and #85 before Himir took #85 and suggested Nikita instead work on Issue #86.

### Navbar and Logged-In State Issues

One recurring topic was confusion around homepage navigation when a user is already logged in.

Himir explained that the bug was not literally that the Docs or Home buttons log users out. Instead, the homepage navbar always shows `Log In` and `Get Started`, even if the user already has an active session. That creates a misleading experience because a signed-in user can still navigate directly into the dashboard.

The team discussed two related fixes:

- Separating the landing-page navbar from the internal dashboard navbar
- Adding conditional rendering so logged-in users see navigation options such as going directly to the dashboard or apps page

Yang noted that separating internal and landing navigation would likely resolve part of the issue, while Himir clarified that logged-in behavior still needed to be handled explicitly.

### Privacy Policy, CORS, and Missing Issues

The meeting also covered a few issues that were either unclear or not yet properly represented in the bug list.

For Issue #86, Yang pointed out that the team should not remove privacy-policy related links outright. Because the product uses `collector.js` to gather user data, the application needs an actual privacy policy. Himir agreed and reframed the work as creating and wiring up a proper privacy policy instead of deleting those buttons.

Ki and Yusuf then raised a separate local development problem involving CORS blocking requests. Himir showed a quick fix in `app.js` and said he would put that change on a branch so others could proceed with local setup.

This surfaced a broader point that not every problem had been fully captured on the GitHub issues page, so the active bug list still needed some cleanup as the team tested.

### Homepage Cleanup and Small UX Fixes

Later in the meeting, Himir reviewed a few additional interface issues that should be cleaned up alongside the assigned bugs.

These included:

- Removing the unnecessary graph section from the homepage
- Keeping only the essential app information and controls on that page
- Cleaning up the errors page if its current issue owner had not already addressed certain display problems
- Renaming or explaining unclear technical terms such as `TTFB`, potentially with hover text or more descriptive labels
- Fixing a docs-page issue that was briefly shown during the walkthrough

Vinh also asked whether the graphs on the main page were still being removed, and Himir confirmed that they should be removed soon.

The meeting ended with a recap: all current bugs should be completed by midweek so the team can deploy the hosted site, test for any newly introduced issues, and spend the remaining time on final stabilization.

## Takeaways and Summary

This meeting was primarily a bug-assignment and short-term execution meeting focused on getting the product into a stable state before deployment.

1. **The team shifted fully into bug-fix mode:** all current GitHub issues were treated as the immediate priority
2. **Bug ownership was assigned live:** several members claimed issues during the meeting so work could begin immediately
3. **Navbar behavior needs product clarification and implementation cleanup:** logged-in users should not see misleading landing-page actions
4. **Privacy-policy work is required, not removable:** because the app collects user data through `collector.js`, the team needs compliant policy pages
5. **A few additional UX and setup problems remain:** CORS setup, homepage graph cleanup, unclear terminology, and docs-page issues still need attention

**Next Steps:**

- Finish all assigned bug fixes by Wednesday or Thursday
- Separate landing-page and dashboard navigation where needed
- Add conditional logged-in navbar behavior
- Implement Privacy Policy and related legal pages instead of removing those links
- Apply the local CORS fix and continue validating setup issues
- Deploy the hosted site after the current bug list is resolved and test for any new issues
