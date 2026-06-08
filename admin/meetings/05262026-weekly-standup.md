# Weekly Standup for Team 08 - Seven Ate Nine

**Date: May 26, 2026**  
**Location:** Team Standup Meeting  
**Start Time:** 6:20  
**End Time:** 6:30 

**Present:** Himir Desai, Matthew Beaudin, Yusuf Damda, Matthew Bozoukov, Nikita Jos, William Ayoade, Vinh Tong, Ki Diaz, John 
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This standup focused on merging remaining branches, stabilizing the combined site, identifying cross-page design inconsistency, clarifying API-key onboarding behavior, reviewing end-to-end collector testing, and shifting the team toward bug-finding and bug-fixing work.

- [Weekly Standup for Team 08 - Seven Ate Nine](#weekly-standup-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Branch Merging and Integration Status](#branch-merging-and-integration-status)
    - [Design Consistency Across Pages](#design-consistency-across-pages)
    - [Login State and API Key Workflow](#login-state-and-api-key-workflow)
    - [Collector Testing and Endpoint Updates](#collector-testing-and-endpoint-updates)
    - [Team Capacity and Bug-Fix Transition](#team-capacity-and-bug-fix-transition)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Branch Merging and Integration Status

The meeting began with an update on branch status and the plan to merge the remaining work into `main`.

The current plan was:

- Merge the remaining active branches by the end of the day or the following morning
- Resolve any final issues found during merge review
- Get all major pages working in a single integrated site before doing broader polish

One possible branch mismatch was noted around a commit that removed an element, while the merged result still appeared to contain it. This was treated as something to recheck locally before concluding whether it was an actual branch issue or a stale local state problem.

### Design Consistency Across Pages

The team noted that several major pages currently look like they belong to different websites.

Pages specifically called out included:

- Dashboard
- Error page
- Performance page
- Homepage

The immediate decision was not to block integration on design consistency. Instead, the first goal is to make sure the full site works end to end, even if the designs are not yet unified. After that, the homepage design may be used as the visual reference for applying a more consistent style to the remaining pages.

### Login State and API Key Workflow

Two product issues were discussed around user flow after login and app setup.

The first issue was that after logging in and returning to the homepage, the site still prompts the user to log in again. This was described as mostly a backend issue, with some frontend involvement.

The second issue was how to expose the app API key on the dashboard. Two possible approaches were discussed:

- Show the API key directly at the top of the dashboard so the user can copy it
- Provide a more guided setup flow where the user creates a project and receives a JavaScript snippet that already includes the API key

The snippet-based approach was seen as more useful because it reduces setup friction by giving the user something closer to copy-paste integration with the collector file.

### Collector Testing and Endpoint Updates

The meeting also included a report on end-to-end manual testing of the collector.

The collector was tested by:

- Adding it to one of the lab repositories
- Creating a new app
- Taking the API key and connecting the collector flow
- Verifying that performance metrics were successfully recorded

Error tracking could not be fully verified yet because no errors occurred naturally in the lab site during testing. Additional testing was planned to confirm that path.

It was also confirmed that the endpoint changes had already been switched over where needed.

### Team Capacity and Bug-Fix Transition

The deadline for feature completion was relaxed from Thursday to later in the week, with Sunday or the following Tuesday discussed as more realistic cutoffs. After that point, the team plans to focus mainly on bugs, polish, and consistency.

The group then went around and checked current task status. Most contributors reported that they were either finished or only making very small remaining changes, such as:

- Minor adjustments to the error page
- Adding the navbar and sidebar to the performance page
- Waiting on PR review feedback
- Helping test the dashboard and general functionality

Because most people reported that they were no longer actively building large features, the team agreed on the next transition:

- Finish merging everything into `main`
- Have everyone use the website and actively find problems
- Create GitHub issues for each discovered problem
- Label those issues as bugs
- Spend the following week mainly fixing the collected bug list

## Takeaways and Summary

This standup marked a transition from parallel feature work into integration, bug discovery, and final polish.

1. **The immediate priority is merging everything into `main`:** the team wants one working integrated version before doing broader cleanup
2. **Cross-page design consistency is still weak:** dashboard, error, performance, and homepage designs do not yet feel unified
3. **User-flow issues remain:** login state persistence and API-key onboarding still need product and implementation decisions
4. **Collector testing is partly successful:** performance metrics worked end to end, while error testing still needs more validation
5. **Most contributors are finishing feature work:** several team members reported they are done or only have minor remaining changes
6. **The team is moving into bug-fix mode:** once merges are complete, everyone will focus on finding problems, filing bug issues, and fixing them

**Next Steps:**

- Merge the remaining branches into `main`
- Recheck any branch discrepancies discovered during integration
- Decide how the API key or setup snippet should appear in the dashboard flow
- Continue testing collector error handling
- Have the full team use the integrated site, file bug issues, and begin bug-fix work
