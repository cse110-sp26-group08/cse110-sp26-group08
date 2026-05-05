# Standup Meeting for Team 08 - Seven Ate Nine

**Date: April 28, 2026**\
**Location: Catalyst In-Person**\
**Start Time:** 6:20\
**End Time:** 6:30

**Present:** Himir Desai, Felix Tong, John Bolibol, Matthew Bozoukov, Matthew Beaudin, Vinh Tong, William Ayoade, Yang Bie, Yusuf Damda Nikita Jos, Ki Diaz\
**Late:** \
**Absent:**

## Meeting Outline and Goals

In this standup, the team discusses project architecture based on research, clarifies the Watchtower system design, and shares individual research findings on observability systems and competitive analysis. The team also finalizes team structure and initial sprint planning.

- [Standup Meeting for Team 08 - Seven Ate Nine](#standup-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Watchtower Architecture Deep Dive](#watchtower-architecture-deep-dive)
    - [Versioning and Multi-App Tracking](#versioning-and-multi-app-tracking)
    - [Team Structure and Roles](#team-structure-and-roles)
    - [Research Findings](#research-findings)
    - [Feature Prioritization](#feature-prioritization)
    - [Next Steps and Sprint Planning](#next-steps-and-sprint-planning)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Watchtower Architecture Deep Dive

Himir consulted with ChatGPT and the professor to clarify the system design. The professor confirmed we do not need to emulate the entire test tab. The architecture consists of three main layers:

1. **Dashboard UI** - The user-facing interface for viewing metrics and errors
2. **Storage** - Database layer storing collected metrics (JSON files or database)
3. **Collector and API** - JavaScript file that acts like a library import

The key insight is that the collector can be implemented as a JavaScript file that gets added to test applications as a script tag (similar to how CSS files are imported). This file will:

- Automatically collect page load times and errors
- Run automatically when the test app loads the script
- Send collected data to storage

Teams can also manually add timers to measure specific functions or features. When the timer ends, the data is sent to storage.

**Data Collection Features:**

- **Automatic:** Page load times, errors, network events
- **Manual:** Custom timers for specific functions/features, labeled with descriptions (e.g., "API calls", "button clicks")
- **Handled Errors:** Errors caught by the application but not surfaced to the frontend—these can be manually reported to Watchtower

### Versioning and Multi-App Tracking

The system tracks different versions of applications. When a developer updates their app from version 1.0 to version 1.1, they update the version number. In Watchtower:

- Multiple test apps can report metrics to the same Watchtower instance
- The dashboard can show app-level and version-level metrics
- Developers can see how errors and performance changed between versions (e.g., "errors increased 5x from v1 to v2")
- This helps identify which deployments or updates introduced issues

### Team Structure and Roles

The team will be organized into functional teams for the project:

1. **Product and UX Team** (Weeks 1-2)
   - Define user personas and user stories
   - Determine which features to implement
   - Identify core functionality needed for MVP

2. **Backend/Data Team**
   - Develop the JavaScript collector file
   - Handle automatic error and performance tracking
   - Manage data storage and collection pipeline
   - Build API endpoints for data retrieval

3. **Dashboard/UI Team**
   - Design the frontend website appearance
   - Create buttons, animations, and UI components
   - Build the dashboard interface for viewing metrics

4. **DevOps/Infrastructure Team** (Week 1-2 setup)
   - Set up GitHub repository and workflows
   - Configure automated testing
   - Set up linting and documentation tools
   - Establish CI/CD pipeline

### Research Findings

**User Reviews Analysis:**
One team member researched user reviews for similar tools and found:

- Users appreciate specific key features and value their implementation
- Tools like Google Analytics are compared favorably for certain capabilities
- Major complaint: Recent updates that broke backwards compatibility forced users to relearn workflows
- Lesson: Backwards compatibility should be a priority when releasing updates

**Developer-Focused Requirements:**

- Primary users will be developers integrating Watchtower
- Key requirement: Reliability and trustworthiness
- Developers need to feel confident using the tool in production

**Technical Implementation Options:**

- Can use Playwright to access browser without full emulation
- Watchtower can monitor network requests (e.g., checking if requests return HTTP 200)
- Availability metrics can be tracked and monitored

**PostHog Competitive Analysis:**
One team member researched PostHog (a competitor):

- Uses JavaScript snippets for data collection (confirms our approach)
- Core features include:
  - Session replay
  - Error tracking
  - Web analytics
  - User behavior tracking
- Session replay appears to be a highly popular/valuable feature

**PostHog Feature Evaluation:**
Another team member categorized PostHog's functionality into 5 categories and evaluated which should be prioritized for our MVP:

- Key takeaway: We should implement a reduced version of PostHog, not attempt feature parity
- Focus on core functionality rather than extensive feature set

**CSC 135 Analytics Experience:**
Nikita Jos drew from CSC 135 course experience:

- Separate analytics infrastructure was used
- Analytics platform collected user data and displayed metrics
- This experience validates the architecture we're designing

### Feature Prioritization

Based on research, potential features for Watchtower include:

- Overview dashboard
- Alert system
- Performance warnings
- User feedback panel
- Deployment timeline

**Important:** The team consensus is to keep the project scope small and avoid feature bloat. This aligns with the project philosophy that stability and process are more important than extensive features.

**A/B Testing Consideration:**
One team member researched A/B testing use cases, noting that Watchtower could help track which versions of apps users prefer and provide user metrics for analysis.

### Next Steps and Sprint Planning

- **By tonight or tomorrow:** Divide into functional teams
- **By Thursday:** Team discussion and refinement of research findings
- **Friday & Saturday:** Document research findings and technical decisions
- **Following week:** Finalize prototypes based on research (prototyping is Week 2, not Week 1)

Each team should use the research to create detailed summaries and potentially generate prototype mockups using ChatGPT or similar tools to visualize concepts.

## Takeaways and Summary

- Watchtower architecture consists of Dashboard UI, Storage, and a JavaScript Collector
- The collector works by being included as a script tag in test applications
- Automatic collection includes errors and page load times; manual features include custom timers and error reporting
- Versioning allows tracking how metrics change across app versions
- Similar tools like PostHog use comparable architectures (JavaScript collection), validating our approach
- Team organization will be by function (Product/UX, Backend/Data, Dashboard/UI, DevOps)
- Backwards compatibility is critical—updates that break existing functionality damage user trust
- Core focus should be reliability and simplicity over extensive feature set
- Session replay may be a valuable feature to consider
- Functional teams should meet by Thursday to discuss and refine findings
