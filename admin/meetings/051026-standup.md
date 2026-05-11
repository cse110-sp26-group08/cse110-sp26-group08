# Standup Meeting for Team 08 - Seven Ate Nine

**Date: May 10, 2026**\
**Location: Slack Thread**\
**Start Time:** 7:09 PM\
**End Time:** 5:05 PM (thread activity concluded next day)

**Late:** \
**Absent:** Yang, Nikita, Matthew Buedien
**Present:** Matthew Bozoukov, Felix Tong, Vinh Tong, Himir Desai, Yusuf Damda, Ki Diaz, William Ayoade

## Meeting Outline and Goals

This standup was conducted asynchronously in Slack and focused on collecting team user stories for Sprint 3. Each person was asked to reply with the user stories they contributed toward their team's shared set, and one person per team was expected to share the Google Doc link containing the compiled stories. The thread also set expectations for an upcoming retrospective covering what went well, what should improve, and what should be avoided next sprint.

- [Standup Meeting for Team 08 - Seven Ate Nine](#standup-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Standup Prompt and Shared Document](#standup-prompt-and-shared-document)
    - [Collected User Stories](#collected-user-stories)
    - [Common Themes Across Stories](#common-themes-across-stories)
    - [Retrospective Preparation](#retrospective-preparation)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Standup Prompt and Shared Document

The standup prompt asked everyone to reply in-thread with the user stories they personally contributed to their team’s story set. It also asked one member of each team to share the Google Doc link containing the full set of team user stories.

Matthew Bozoukov shared the compiled user stories document and noted that the doc indicates who wrote which stories.

### Collected User Stories

The following user stories were shared in the thread.

**Felix Tong:**

- As a developer, I would want a performance metric app that does not have any significant performance impact on my own software, so that the metrics that I observe from WatchTower are accurate to the app itself and not affected by the running of WatchTower.
- As a developer who wants to be able to clearly trace the origin of errors, I would want metrics that capture the error origin in extreme detail, including the app version, timestamps, page that the error is from, etc.

**Vinh Tong:**

- As a developer, I want to receive notifications when the application experiences high error rates, downtime, or severe performance degradation so that I can quickly respond before they significantly impact users.
- As a developer, I want to monitor website uptime and service availability so that I can detect outages or inaccessible services and ensure the application remains operational for users.

**Himir Desai:**

- As a developer, I want not make much changes to my existing code and want to just add a single collector file to my repo to collect performance/error data, so that my code stays clean and adding WatchTower is not a cumbersome process.
- As a developer who values security, I want my data to be protected by my email and encrypted password, so that I can be worry free using WatchTower in my apps.
- As a developer, I want to use a performance metric app that doesn't slow down my own app, so that the performance errors I see are due to my app and not WatchTower slowing my app down.

**Matthew Bozoukov (with help from Yusuf):**

- As a user I would want to be able to change how my data is represented through different buttons that can switch between a bar chart, line graph, tabular view, etc., in order to better suit my preferences on how I like seeing data.
- As a developer I would want a widget with a log of different versions of my website and the uptime rate and number of bugs in order to assess which version of my app is most stable.

**Yusuf Damda:**

- As a developer monitoring my project, I want to customize which charts and widgets appear on my dashboard so that I can focus only on the information that is most relevant to me.
- As a developer monitoring my applications, I want important metrics, warnings, and errors to be displayed using clear and distinguishable color-coded indicators so that I can quickly recognize the severity and status of issues on my dashboard.

**Ki Diaz:**

- As a CSE 110 student, I want to check if my website meets the R.A.I.L. (response, animation, idle, load) times specified in class and how I might go about meeting those thresholds for a website to be "good".
- As a developer, I want a documentation tab on the website so that I know how to set up WatchTower in my software and answer any questions I have about how it works.

**William Ayoade:**

- As a developer who values security, I want the UI to hide or redact sensitive user data unless one has the required permissions.
- As a developer, I want error logs (like a stack trace) to be collapsible so I can navigate them easily.

### Common Themes Across Stories

Several priorities appeared repeatedly across the submitted stories:

- **Low-overhead monitoring:** WatchTower should not noticeably slow down the client application
- **Uptime and alerting:** developers want clear notification when websites go down or degrade
- **Detailed debugging support:** error origins, stack traces, versions, and timestamps should be visible
- **Customizable dashboards:** users want control over widget selection and chart format
- **Security and privacy:** authentication, encrypted credentials, and restricted UI visibility matter
- **Usability and onboarding:** setup should be simple and documentation should be accessible

These themes align with the earlier pivot toward a focused MVP centered on uptime monitoring, actionable alerts, and lightweight supporting analytics.

### Retrospective Preparation

The thread closed by reminding the team that a retrospective would happen the following day. Team members were asked to think about:

- What the team did well this sprint
- What could be improved
- What should be avoided in the next sprint

## Takeaways and Summary

This standup produced a concrete pool of user stories for Sprint 3 and helped narrow the product around a few recurring needs:

1. **Uptime monitoring and notifications remain central:** multiple stories focused on outages, availability, and rapid alerts
2. **Performance overhead is a major concern:** several contributors emphasized that WatchTower must not distort app performance
3. **Dashboard flexibility matters:** contributors want configurable widgets, multiple chart views, and clear visual severity cues
4. **Debugging depth is important:** detailed error context, version history, and collapsible logs were all requested
5. **Security and usability are both part of the MVP discussion:** stories covered credential protection, redaction, simple integration, and documentation

**Key follow-up items:**

- Finalize and organize the full team user story document
- Select the highest-priority stories for the MVP
- Prepare retrospective input for the next team discussion

This async standup served as the bridge between broad brainstorming and concrete sprint scoping by turning individual ideas into implementation-oriented user stories.
