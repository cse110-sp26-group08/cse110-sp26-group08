# Weekly Meeting for Team 08 - Seven Ate Nine

**Date: May 11, 2026**  
**Location:** Team Notes / Sprint Planning  
**Start Time:** 4:00  
**End Time:** 4:25 

**Present:** Himir Desai, John Bolibol, Yusuf Damda, Ki Diaz, Yang Bie, Matthew Bozoukov, Vinh Tong, Nikita Jos, William Ayoade   
**Late:**  
**Absent:**  

## Meeting Outline and Goals

This weekly meeting note captures Sprint 1 expectations and team workflow guidance based on Himir's notes. The discussion focused on the minimum front-end deliverables for Sprint 1, required project organization, expected Git and branch workflow, pull request practices, and team rules for handling requested changes and merge conflicts.

- [Weekly Meeting for Team 08 - Seven Ate Nine](#weekly-meeting-for-team-08---seven-ate-nine)
  - [Meeting Outline and Goals](#meeting-outline-and-goals)
  - [Discussion](#discussion)
    - [Sprint 1 Front-End Requirements](#sprint-1-front-end-requirements)
    - [Project Structure Expectations](#project-structure-expectations)
    - [Git and Branch Workflow](#git-and-branch-workflow)
    - [Commit Message Standards](#commit-message-standards)
    - [Pull Request Expectations](#pull-request-expectations)
    - [Important Team Rules](#important-team-rules)
    - [Sprint 1 Deadline](#sprint-1-deadline)
  - [Takeaways and Summary](#takeaways-and-summary)

## Discussion

### Sprint 1 Front-End Requirements

Sprint 1 should include a minimal front-end foundation for the project. The initial expectations are:

- Create a simple front-end structure
- Build around 3 basic pages
- Include a shared or common navigation bar across pages
- Keep the design clean and simple for Sprint 1

The emphasis for this sprint is on having a usable structure in place rather than polishing the final visual design.

### Project Structure Expectations

The project should be organized clearly from the start so the team can scale development more easily in later sprints.

Expected structure includes:

- At least 1 dedicated `frontend` folder
- Files grouped in a way that is organized and readable
- A clear separation of responsibilities as the codebase grows

### Git and Branch Workflow

For each issue, the expected workflow is:

1. Create a new branch
2. Name the branch based on the issue or task
3. Write the code for that issue
4. Commit the changes
5. Push the branch
6. Open a Pull Request

Each issue should have its own branch rather than combining multiple unrelated tasks into one branch.

### Commit Message Standards

All commit messages should follow Conventional Commit formatting.

Examples discussed:

- `feat: add navigation bar`
- `fix: resolve button alignment`
- `style: update dashboard layout`

Using a consistent commit format will make project history easier to read and help the team track work more clearly.

### Pull Request Expectations

When opening a Pull Request:

- Reference the related issue directly in the PR description
- Use issue-closing keywords when appropriate

Examples:

- `Resolves #1`
- `Closes #2`

This ensures issues stay connected to implementation work and can automatically close once the PR is merged.

### Important Team Rules

The following team rules were emphasized:

- If changes are requested on a PR, make updates on the same branch
- Do not create a new branch for PR revisions unless specifically instructed
- Do not resolve merge conflicts independently
- Notify the group leader or team first if merge conflicts occur

These rules are intended to keep collaboration predictable and avoid accidental integration mistakes.

### Sprint 1 Deadline

The target for Sprint 1 completion is Saturday.

The team should aim to have the required front-end structure, branch workflow, and PR process in place by that deadline.

## Takeaways and Summary

This meeting established the basic expectations for Sprint 1 and clarified how the team should manage implementation work.

1. **Front-end foundation comes first:** Sprint 1 should include about 3 basic pages and a shared navigation bar
2. **Project organization matters early:** the repository should include a dedicated frontend structure and readable file layout
3. **Each issue needs its own branch:** branch naming should reflect the task being worked on
4. **The full Git workflow is required:** branch, code, commit, push, and PR should be followed for every issue
5. **Conventional Commits are expected:** commit history should use standard prefixes like `feat`, `fix`, and `style`
6. **PRs must reference issues:** issue keywords like `Resolves #...` and `Closes #...` should be used
7. **PR revisions stay on the same branch:** requested changes should not be moved to a new branch unless instructed
8. **Merge conflicts should be escalated:** teammates should notify leadership rather than resolving conflicts alone

**Next Steps:**

- Set up the initial front-end folder structure
- Create the basic Sprint 1 pages
- Add a shared navigation bar
- Follow the agreed branch and PR workflow for all assigned issues
- Complete Sprint 1 work by Saturday
