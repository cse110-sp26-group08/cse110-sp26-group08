# Weekly Meeting for Team 08 - Seven Ate Nine

**Date: April 27, 2026**\
**Location: Zoom Meeting**\
**Start Time:** 4:02 PM\
**End Time:** 4:21 PM

**Present:** Himir Desai, Matthew Bozoukov, John Bolibol, Yusuf Damda, Vinh Tong, Felix Tong, Ki Diaz, Matthew Beaudin, William Ayoade, Yang Bie\
**Late:** \
**Absent:** Nikita Jos

## Meeting Outline and Goals

In this meeting we review the Watchtower project requirements and discuss how we will approach the project using Agile methodologies. We cover sprint planning, process requirements, technical constraints, and team organization strategy.

- [Weekly Meeting for Team 08 - Seven Ate Nine](#weekly-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Agile Methodology Overview](#agile-methodology-overview)
    - [Project Overview: Watchtower](#project-overview-watchtower)
    - [Agile Process Requirements](#agile-process-requirements)
    - [Repository Process and Tooling](#repository-process-and-tooling)
    - [Technical Constraints](#technical-constraints)
    - [Project Timeline](#project-timeline)
    - [AI Usage Strategy](#ai-usage-strategy)
    - [Team Organization](#team-organization)
  - [Takeaways and Summary](#takeaways-and-summary)
  - [Action Items](#action-items)

## Discussion

### Agile Methodology Overview

We discussed the importance of sprints as time-bound goals with defined task sets to organize team efforts. Agile retrospectives will be used to evaluate sprint performance. Scrum meetings are 15-minute check-ins to monitor progress and identify who needs help. The requirement states we must have at least 3 standard meetings per week.

Himir will clarify with the TA whether meetings can be conducted asynchronously via Slack announcements (similar to other UCSD club practices) instead of synchronous Zoom calls, as not all members may be available for 3 weekly Zoom meetings.

### Project Overview: Watchtower

The Watchtower project is a centralized observability system that:

- Reports errors being thrown in software
- Identifies performance degradations
- Captures upset user signals through rating widgets and feedback forms
- Integrates with build systems to track which deployments caused issues

Our job is to create a simplified version of this system suitable for software that is just starting out. We are building operational-facing software with stability requirements—more features mean more risks.

### Agile Process Requirements

- **Sprint Planning:** Must conduct documented sprint planning meetings before each sprint begins
- **Stand-ups:** Must hold stand-ups virtually on Slack and/or in-person at least 3 times per week, with information captured in GitHub Issues
- **Sprint Reviews & Retrospectives:** Must perform these at least 2 times before project conclusion. All team members must attend retrospectives.
- **TA Meetings:** Must work with the TA weekly and meet with the professor at least once before quarter end
- **Retrospective Form:** All team members must fill out a retrospective Google form (deadline: next Monday)

### Repository Process and Tooling

- All work (planning, meetings, documentation, tests) should be in GitHub incrementally
- GenAI usage must be exposed and discussed
- Pull requests required for work batches above 300 lines of code with human review
- Git branching should be demonstrated and used throughout the project
- Semantic versioning (SEMVER) must be employed
- CI/CD pipeline must be built using GitHub Actions
- Testing: Unit and E2E testing must be demonstrated, not just at project conclusion
- Code documentation must be maintained
- Linting and quality checks performed both manually and via CI pipeline
- `.gitignore` must be used
- Commits must be consistent and follow a format like conventional commits
- Changelog should be kept (manual, automatic, or hybrid)

### Technical Constraints

- Technology stack restricted to: Markdown, standard HTML/CSS (no frameworks like React)
- Only JavaScript for interactivity (no other frameworks)
- Side technologies limited to: Mastodon, Cloudflare, or GitHub Pages only
- All major technical decisions must be captured as architectural design records (ADRs)
- Dependencies can only be added with TA approval
- Project deliverables can include: web apps, progressive web apps, mobile apps, desktop apps, Chrome extensions, VS Code extensions, or REST endpoints
- All projects must have a website documenting what was produced for end users

### Project Timeline

**Week 1 - Orienting Sprint (April 26 - May 3):** Light work week due to midterm

- Research the project prompt
- Create user personas
- Write user stories
- Create design brief
- Create wireframes

**Week 2 - Design & Prototyping Sprint:** Initial exploration with TA guidance. If not completed before Week 3, we will be forced to repeat it.

**Week 3 onwards:** Heavy coding begins after design/prototyping sprints are complete

**Week 9:** Review break with another team for feedback
**Week 10:** Must have interaction with professor before end of week

### AI Usage Strategy

We discussed a structured approach to using AI for code generation:

- Create file structure first (HTML, CSS, JavaScript files) as a team
- Assign specific functions to team members
- Each person creates skeleton files for their assigned functions
- Use AI to generate code for specific functions within those files, not entire projects
- Manually test generated functions before submission
- Consider having AI generate tests or writing tests manually
- Submit pull requests for code review
- Team reviews code and tests it on the website before merging

This approach differs from the slot machine project where AI generated everything at once, making code harder to understand and manage.

### Team Organization

Instead of assigning individual features to all 11 members, we will organize into 3 teams:

- **Front-end team**
- **Back-end team**
- **Additional team** (TBD)

Each team manages itself and assigns work internally. This approach:

- Reduces coordination complexity
- Increases team accountability
- Allows flexibility to switch teams between sprints if needed
- Enables everyone to experience different roles throughout the project
- Prevents bottlenecks from waiting on individual contributors

## Takeaways and Summary

- Watchtower is an observability system for monitoring application health and user feedback
- Process is more important than features—a quality-focused, organized process produces better grades than feature-rich code done without clear process
- We must complete design/prototyping before heavy coding begins
- Team structure will be organized by function (front-end, back-end, etc.) rather than individual features
- AI should be used strategically at the function/component level, not for entire project generation
- Agile requirements include sprints, stand-ups, retrospectives, and comprehensive documentation
- Meeting with TA after this session to clarify remaining questions about sprint requirements and project details

## Action Items

| Action Item                                             | Owner       | Due Date                  |
| ------------------------------------------------------- | ----------- | ------------------------- |
| Clarify meeting format options with TA (Slack vs. Zoom) | Himir Desai | TA Meeting (April 27)     |
| Determine exact project scope after TA meeting          | Himir Desai | After TA Meeting          |
| Conduct team research on Watchtower project             | All Members | Within 2 days             |
| Fill out retrospective Google form                      | All Members | Next Monday               |
| Schedule sprint planning meeting                        | Himir Desai | Before next sprint starts |
