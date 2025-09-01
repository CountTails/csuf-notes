# Lecture 2: testing fundamentals (part 2)

## Fundamentals of agile software development

### Agile software development

- Individuals and interactions over processes and tools
- Working software over comprehensive documentation
- Customer collaboration over contract negotiations
- Responding to change over following a plan

### Principles

- Our highest priority is to satisfy the customer through early and continuous delivery of valuable software
- Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage
- Deliver working software frequently, at intervals of between a few weeks to a few months, with a preference to the shorter timescale
- Business people and developers must work together daily throughout the project
- Build projects around motivated people. Give them the environment and support they need, and trust them to get the job done
- The most efficient and effective method of conveying information to and within a development team is face-to-face conversation
- Working software is the primary measure of progress
- Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely
- Continuous attention to technical excellence and good design enhances agility
- Simplicity - the art of maximizing the amount of work not done - is essential
- The best architectures, requirements, and designs emerge from self-organizing teams
- At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly

## Fundamentals of agile software testing

- Whole team approach
- Early and frequent feedback

### Extreme programming

- Embraces 5 values to guide development
  - Communication
  - Simplicity
  - Feedback
  - Courage
  - Respect
- Describes a set of principles as additional guidelines
  - Humanity
  - Economics
  - Mutual benefit
  - Self-similarity
  - Improvement
  - Diversity
  - Reflection
  - Flow
  - Opportunity
  - Redundancy
  - Failure
  - Quality
  - Baby steps
  - Accepted responsibility
- Describes 13 primary practices
  - Sit together
  - Whole team
  - Informative workspace
  - Energized work
  - Pair programming
  - Stories
  - Weekly cycle
  - Quarterly cycle
  - Slack
  - 10-minute build
  - Continuous integration
  - Test first programming
  - Incremental design

### Scrum

**Practices**

- Sprints: divides a project into iterations (called sprints) of fixed length (usually 2-4 weeks)
- Product increment: each sprint results in a potentially releasable/shippable product (called an increment)
- Product backlog: A prioritized list of planned product items managed by the product owner. Evolves from sprint to sprint through backlog refinement
- Sprint backlog: At the start of each sprint, the Scrum team selects a set of highest priority items from the product backlog. Since the scrum team, not the product owner, selects the items to be realized within the sprint, the selection is referred to as being on the pull principle rather than the push principle
- Definition of done: To make sure that there is a potentially releasable product at each sprint's end, the Scrum team discusses and defines appropriate criteria for sprint completion. The discussion deepens the team's understanding of the backlog items and the product requirements
- Timeboxing: Only those tasks, requirements, or features that the team expects to finish within the sprint are part of the sprint backlog. If the development team cannot finish a task within a sprint, the associated product features are removed from the sprint and the task is moved back to the product backlog. Timeboxing applies not only to tasks, but in other situations (like meeting start and end times)
- Transparency: The development team reports and updates sprint status on a daily basis at a meeting called the daily Scrum. This makes the content and progress of the current sprint, including test results, visible to the team, management, and all interested parties.

**Roles**

- Scrum master: Ensures that Scrum practices and rules are implemented and followed, and resolves any violations, resource issues, or other impediments that could prevent the team from following the practices and rules. This person is not the team lead, but a coach.
- Product owner: Represents the customer, and generates, maintains, and prioritizes the product backlog. This person is not the team lead
- Development team: Develops and tests the product. The team is self-organized. There is no team lead, so the team makes the decisions. The team is also cross-functional.

### Kanban

- Kanban board: The value chain to be managed is visualized by a Kanban board. Each column shows a station, which is a set of related activities (e.g. development or testing). The items to be produced or tasks to be processed are symbolized by tickets moving from left to right across the board through the stations
- Work-in-progress limit: The amount of parallel active tasks is strictly limited. This is controlled by a maximum number of tickets allowed for a station and/or globally for the board. Whenever a station has free capacity, the worker pulls a ticket from the predecessor station
- Lead time: Kanban is used to optimize the continuous flow of tasks by minimizing the average lead time for the complete value stream

### Other aspects

- Collaborative user story creation
- Retrospectives
- Continuous integration
- Release and iteration planning

## Agile testing

### Difference between testing in traditional and agile approaches

- Testing and development activities are integrated
- Work products, names, entry and exit criteria, and use of tools effectively utilize independent testing

### Testing and development activities

- Developers focus on creating unit tests
- Testers focus on creating automated integration, system, and system integration tests
- Agile teams tend to favor testers with strong technical and test automation background

### Testing levels

- Unit testing (typically done by the developer)
- Feature acceptance testing
  - Feature verification testing tests against the user story's acceptance criteria
  - Feature validation testing determines if the feature is fit for use, improves visibility of progress made, and receives real feedback from business stakeholders
- Regression testing re-runs automated unit tests and feature verification tests from current and previous iterations

### Testing and configuration management

- Often involve heavy use of automated tools to develop, test, and manage software development
- Developers
  - Use tools for static analysis, unit testing, and code coverage
  - Continuously check in the code and unit tests into a configuration management system
  - Use automated build and testing frameworks
- Allows for continuous integration of new software with the system

### Agile tester skills

- Be positive and solution-oriented with team members and stakeholders
- Display critical, quality-oriented, skeptical thinking about the product
- Actively acquire information from stakeholders
- Accurately evaluate and report test results, test progress, and product quality
- Work effectively to define testable user stories, especially acceptance criteria, with customer representatives and stakeholders
- Collaborate within the team, working in pairs with programmers and other team members
- Respond to change quickly, including changing, adding, or improving test cases
- Plan and organize their own work

### Role of a tester in an agile team

- Understanding, implementing, and updating the test strategy
- Measuring and reporting test coverage across all applicable coverage dimensions
- Ensuring proper use of testing tools
- Configuring, using, and managing test environment and test data
- Reporting defects and working with the team to resolve them
- Coaching other team members in relevant aspects of testing
- Ensuring the appropriate testing tasks are scheduled during release and iteration planning
- Actively collaborating with developers and business stakeholders to clarify requirements, especially in terms of testability, consistency, and completeness
- Participating proactively in team retrospectives, suggesting and implementing improvements

### Agile testing methods

- Test-driven development
  - Define the test first
  - Write the *minimal* amount of code to make it pass
  - Evaluate for code smells
  - Repeat
- Acceptance test-driven development
  - Collaborative approach that allows every stakeholder to understand how the software component has to behave
  - Assists developers, testers, and business representatives in understanding what is needed to ensure this bahavior
- Behavior-driven development
  - Given some initial context, when an event occurs, ensure some outcomes

## Tools in agile projects

- Task management and tracking tools
- Communication and information sharing tools
- Software builds and distribution tools
- Configuration management tools
