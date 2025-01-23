# Lecture 1: project management process framework

## The modern software process

- Supports evolution of plans, requirements, and architecture together with well-defined synchronization points
- Enables risk management and objective measures of progress and quality
- Allows for the evolution of system capabilities through demonstrations of increased functionality

### Engineering and production stages

- The engineering stage: driven by less predictable but smaller teams doing design and synthesis activities
- The production stage: driven by more predictable but larger teams doing construction, test, and deployment activities

### Phases of the life-cycle process

- Engineering stage can be broken into the inception and elaboration phases
- Production stage can be broken down into construction and transition phases

#### Inception phase

**Primary objectives**

- Establish project's scope and boundary conditions
  - Operational concept
  - Acceptance criteria
  - Clear understanding of intended product (and what it is not)
- Discriminating critical use cases of the system that will drive major design trade-offs
- Demonstrating at least one candidate architecture against primary scenarios
- Estimate cost and schedule for entire project
- Estimate potential risks

**Essential activities**

- Formulating scope of the project
  - Capturing requirements
  - Defining operational concept
  - Deriving acceptance criteria
- Synthesizing the architecture
  - Evaluate design trade-offs
  - Resolving problem ambiguities
  - Selecting solution space assets
- Planning and preparing a business case
  - Managing risk
  - Evaluating staff, iteration plans, and cost/schedule/profitability trade-offs
  - Determining infrastructure sufficient to support the life-cycle development task

**Primary evaluation criteria**

- Do all stakeholder concur on the scope definition and cost and schedule estimates?
- Are requirements understood, as evidenced by the fidelity of the critical use cases?
- Are the cost and schedule estimates, priorities, risks, and development processes credible?
- Do the depth and breadth of an architecture prototype demonstrate the preceding criteria?
- Are actual resource expenditures versus planned expenditures acceptable?

#### Elaboration phase

**Primary objectives**

- Baselining the architecture as rapidly as practical
- Baselining the vision
- Baselining a high-fidelity plan for the construction phase
- Demonstrating that the baseline architecture will support the vision at a reasonable cost in a reasonable time

**Essential activities**

- Elaborate the vision
  - Establish high-fidelity understanding of critical use cases
  - Make architectural and/or planning decisions
- Elaborate the process and the infrastructure
  - Establish the construction process
  - Select tools and process automation support
  - Choose intermediate milestones and their respective evaluation criteria
- Elaborating the architecture and selecting components

**Primary evaluation criteria**

- Is the vision stable?
- Is the architecture stable?
- Does the executable demonstration show that the major risk elements have been addressed and credibly resolved?
- Is the construction phase plan of sufficient fidelity, and is it backed up with a credible basis of estimate?
- Do all stakeholders agree that the current version can be met if the current plan is executed to develop the complete system in the context of the current system architecture?
- Are actual resource expenditures versus planned expenditures acceptable?

#### Construction phase

**Primary objectives**

- Minimizing development costs by optimizing resources and avoiding unnecessary scrap and rework
- Achieving adequate quality and rapidly as practical
- Achieving useful versions as rapidly as practical

**Essential activities**

- Resource management, control, and process optimization
- Complete component development and testing against evaluation criteria
- Assessment of product releases against acceptance criteria of the vision

**Primary evaluation criteria**

- Is this product baseline mature enough to be deployed in the user community?
  - Existing defects are not obstacles to achieving the purpose of the next release
  - Pending changes are not obstacles to achieving the purpose of the next release
- Are the stakeholders ready for transition to the user community?
- Are actual resource expenditures versus planned expenditures possible?

#### Transition phase

- Beta testing to validate the new system against user expectations
- Beta testing and parallel operation relative to legacy system it is replacing
- Conversion of operational database
- Training of users and maintainers

**Primary objectives**

- Achieving user self-supportability
- Achieving stakeholder concurrence that development baselines are complete and consistent with the evaluation criteria of the vision
- Achieving final product baselines as rapidly and cost effectively as practical

**Essential activities**

- Synchronization and integration of concurrent construction increments into consistent development baselines
- Development specific engineering
- Assessment of development baselines against the complete vision and acceptance criteria in the requirement set

**Primary evaluation criteria**

- Is the user satisfied?
- Are actual resource expenditures versus planned expenditures possible?

## Artifacts of the process

- Process artifacts are organized into five set
  1) Management
  2) Requirements
  3) Design
  4) Implementation
  5) Deployment
- Management artifacts capture information necessary to synchronize stakeholder expectations
- Other artifacts are captured in rigorous notations that support automated analysis and browsing

### Management set

- Relevant stakeholder reviews
- Analysis of changes
  - Current version and previous version of artifacts
  - Identifies management trends
  - Validates performance changes in terms of cost schedule and quality
- Major milestones demonstrations of the balance among all artifacts and, in particular, the accuracy of the business case and vision artifacts

### Engineering set

**Requirements**

- Analysis of consistency with the release specifications of the management set
- Analysis of consistency between the vision and the requirements model
- Mapping against the design, implementation, and deployment sets to evaluate the consistency and completeness and the semantic balance between information in the different sets
- Analysis of changes between current version of requirements artifacts and previous versions
- Subjective review of other dimensions of quality

**Design**

- Analysis of the internal consistency and quality of the design model
- Analysis of consistency with requirement models
- Translation into implementation and deployment sets and notations to evaluate the consistency and completeness and semantic balance between information in the sets
- Analysis of changes between the current version of the design model and previous versions
- Subjective review of other dimensions of quality

**Implementation**

- Analysis of consistency with the design models
- Translation into deployment set notations to evaluate the consistency and completeness among artifacts sets
- Assessment of component source or executable files against relevant evaluation criteria through inspection, analysis, demonstration, or testing
- Execution of stand-alone component test cases that automatically compare expected results with actual results
- Analysis of changes between the current version of the implementation set and previous versions
- Subjective review of other dimensions of quality

**Deployment**

- Testing against the usage scenarios and quality attributes defined in the requirements set to evaluate the consistency and completeness and the semantic balance between information in the two sets
- Testing the partitioning, replication, and the allocation strategies in mapping components of the implementation set to physical resources of the deployment system
- Testing against the defined usage scenarios in the user manual such as installation, user-oriented dynamic reconfiguration, mainstream usage, and anomaly management
- Analysis of changes between the current version of the deployment set and previous versions
- Subjective review of other dimensions of quality

## Software development tools and the artifact set

- Most of today's software development tools map closely to one of the five artifact sets

**Management**

- Scheduling
- Workflows
- Defect tracking
- Change management
- Documentation
- Spreadsheet
- Resource management
- Presentation tools

**Requirements**

- Requirements management tools

**Design**

- Visual modeling tools

**Implementation**

- Compiler/debugger tools
- Code analysis tools
- Test coverage analysis tools
- Test management tools

**Deployment**

- Test coverage and test automation tools
- Network management tools
- Commercial components
- Installation tools

## Workflows of the process

- Activities of the process are organized into 7 major workflows
  1) Management: controlling the process and ensuring win conditions for all stakeholder
  2) Environment: automating the process and evolving the maintenance environment
  3) Requirements: Analyzing the problem space and evolving the requirement artifacts
  4) Design: modeling the solution and evolving the architecture and design artifacts
  5) Implementation: programming the components and evolving the implementation and deployment artifacts
  6) Assessment: assessing the trends in process and product quality
  7) Deployment: transitioning the end products to the user
- Activities are performed concurrently
  - Levels of effort and emphasis as project progresses
  - Management concerned with planning, project control, and organization

## Checkpoints of the process

- Used to synchronize stakeholder expectations throughout the life-cycle
  - Major milestones
  - Minor milestones
  - Status assessments
- Most important major milestones transitions the project from elaboration to construction phase
- Minor milestones depend on the project and organization culture
- Periodic status assessments help focus continuous attention on the evolving health of the project

### Objectives

- Synchronize stakeholder expectations and achieve concurrence on three evolving perspectives
- Synchronize related artifacts into a consistent and balanced state
- Identify important risks, issues, and out-of-tolerance conditions
- Perform global assessment for the whole life-cycle

### Joint management reviews

1) Major milestones: system wide events held at the end of each development phase
  - Provide visibility into system-wide issues
  - Synchronize management and engineering perspectives
  - Verify aims of the phase have been achieved
2) Minor milestones: iteration focused events conducted to review the content of an iteration in detail and authorizes continued work
  - Iteration readiness review: informal milestone conducted at the start of each iteration to review the iteration plan and evaluation criteria allocated to the iteration
  - Iteration assessment review: informal milestone conducted at the end of each iteration to assess the degree iteration met evaluation criteria and review impact of iteration results on the plan for subsequent iterations
3) Status assessments: periodic events that provide management with frequent and regular insight into progress being made
  - Mechanism for openly addressing, communicating, and resolving management issues, technical issues and project risks
  - Objective data derived directly from ongoing activities and evolving product configurations
  - Mechanism for disseminating process, progress, quality trends, practices, and experience information to and from all stakeholders in an open forum

### Stakeholders and their concerns

**Customers**

- Schedule and budget estimates
- Feasibility and risk management
- Requirements understanding
- Progress
- Product line compatibility

**Users**

- Consistency with requirements and usage scenarios
- Potential for accommodating growth
- Quality attributes

**Architects and system engineers**

- Product line compatibility
- Requirements changes
- Trade-off analysis
- Completeness and consistency
- Balance among risk
- Quality and usability

**Developers**

- Sufficiency of requirements detail and usage scenario descriptions
- Frameworks for component selection or development
- Resolution of development risk
- Product line compatibility
- Sufficiency of the development environment

**Maintainers**

- Sufficiency of product and documentation artifacts
- Understandability
- Interoperability with existing systems
- Sufficiency of maintenance environment

**Others**

- Possibly other perspectives by stakeholders
  - Regulatory agencies
  - Subcontractors
  - Associate contractors
  - Sales and marketing team
