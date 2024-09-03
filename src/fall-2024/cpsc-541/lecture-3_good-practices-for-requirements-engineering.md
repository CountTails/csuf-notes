# Good practices for requirements engineering

![Good Requirements Engineering Practices](figures/requirements-engineering-good-practices.png)

## Elicitation

### Process outline

- Define a requirements development Process
  - Outline the steps
  - Determine activities
- Write a vision and scope document
  - Define project objectives
  - Set boundaries
  - Focus on the project

### User classes

- Roles
- Goals
- Features used
- Frequency of use
- Knowledge and skill levels
- Location and attitude

### Commitments

- Long-term
  - Identify a product champion to be a representative of the user group
  - Representative speaks for and decides on behalf of the user group
- Short-term
  - Gather focus groups from user classes
  - Describe functionality and quality needs

### Use cases and event tables

- Use cases
  - Tasks to be accomplished
  - Goals and purposes
  - User and system interactions
- Event tables
  - Describe external signals and data
  - Categorize events as temporary or a business event

### Workshops and observation

- Workshops
  - Collaboration between analysts and users
  - Discuss and draft documents
- Observation
  - Current tasks establish context for new system
  - Data flow can be captured

### Problems and reuse opportunities

- Examine problem reports
  - Difficulties with old systems reveal needs for new one
  - Enhancements that are explicitly requested
- Reuse opportunities
  - Look for similarities to previous projects or existing solutions

## Analysis

- Draw context diagram
  - Show environment and system boundaries
  - Show interfaces into and out of the system
- Create prototypes
  - User interfaces: get feedback on a tangible entity
  - Technical: explore feasibility of potential problem areas
- Prioritize
  - Allocate requirements to releases
  - Adjust to change in resources, needs, goals, or market conditions
- Model
  - Use abstract and flexible representations
  - Use rigorous notations to reveal problems
- Identify interfaces to other systems
- Identify requirements to other subsystems

## Specification

- Make documentation that is
  - Consistent
  - Accessible
  - Reviewable
- Adopt a SRS template (such as IEEE 830)
- Identify sources
  - Justify presence of requirements
  - Support future clarification
- Label requirements (with a unique ID) for traceability and management
- Record business rules
  - Keep separate from SRS
  - Exist outside the scope of a single project
- Specify quality attributes that can affect customer/user satisfaction

## Validation

- Inspect documents
  - Formal examinations by people with different perspectives and expertise
  - Informal reviews of drafts in progress
- Define test cases
  - Describe expected behavior
  - Review with customer/user
  - Trace to specification
  - Define acceptance criteria

## Management

- Define a change control process (proposal => analysis => resolution)
- Establish a change control board (small, competent, and empowered group)
- Perform impact analysis
  - Scope of change (other artifacts affected)
  - Effort and cost
- Establish a baseline and use version control
  - Distinguish between release baselines
  - Distinguish between previous and current versions
- Maintain change history (who, what, when, why)
- Track change status (know every requirement's condition)
- Measure volatility
  - Know the rate of change
  - Identify problems
- Use a tool to automate management tasks
- Create a traceability matrix
  - Connect requirements, code, and tests
  - Ensure no requirements are missed
  - Prevent extraneous features from appearing

