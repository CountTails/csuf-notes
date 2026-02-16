# Lecture 5: the maintenance process

## The software lifecycle

- Communication
  - What to build
  - REQ/SPEC
- Planning
  - How to build
  - Modeling
  - Designing (architecture, detailed, implementation)
- Construction
  - Implement
  - Integrate
  - Test and validate
- Deploy
  - Operation
  - Maintenance

## 3 traditional software development process models

### 1) Code and fix

- 2 phase model
  - First phase is writing code
  - Second phase is fixing
- Advantages
  - Quickness (fixes can be done quickly)
- Disadvantages
  - Rigidity
  - Does not properly define states for analysis, specification, design and testing

### 2) Waterfall

- Characteristics
  - Each phase is completed before going on to the next phase
  - Each phase is verified by a SQA group
  - Each phase produces a document
  - Changes must be reflected in each step
- Advantages
  - Very simple
  - Each step produces documentation
  - Each documentation is verified
- Disadvantages
  - Sequential (production)
  - Product is "seen" late 
  - Back edges possible for changes

### 3) Spiral

- Characteristics
  - Do risk analysis before engineering
  - In terms of staff, money, technology, and management commitments
- Advantages
  - Evaluates options (alternatives) before building
  - Identify possible risks and solve
  - Stop at any moment
- Disadvantages
  - Project has to be big (RA is done)
  - Internal project
  - Accurate RA measurement is necessary

## A few other software development process models

### Rapid prototyping model

- Characteristics
  - Essentially the same as waterfall, but build prototypes in REQ step
  - Key functionalities shown, but details like error handling and database size are not
  - Must be developed quickly
  - Must be built for change (suggested to use interpreted languages)
- Advantages
  - See earlier versions of the product
  - REQ is clearer (less back edges)
  - More enthusiastic user participation
- Disadvantages
  - Use prototypes for implementation (danger)
  - Could be more expensive
  - Still a sequential model

### Incremental

- Characteristics
  - Construct product in stages
  - Typical product has 10-50 builds
- Advantages
  - Delivery of subset is quicker
  - Can stop at any time
  - Adoption is easier
  - Parallelism is possible
- Disadvantages
  - Integration can be a problem
  - Maintenance may not be done correctly

### Concurrent

- Characteristics
  - Divide REQ into subsets
- Advantages
  - Subset delivered faster
  - More parallelism possible
- Disadvantages
  - Integration becomes more difficult

### Synchronize and stabilize

- Characteristics
  - Initial requirements and specification is done
  - Divide into teams and work in parallel
  - Synchronize everyday
- Advantages
  - Integration becomes less risky
  - Good parallelism
- Disadvantages
  - Integration could still be a problem

### Unified process (OO) iterative

- Inception (communication)
- Elaboration (modeling)
  - Use cases
  - Sequence diagrams
  - Class diagrams
- Construction (implementation)
- Transition (deployment)
- Production (of software increment)

## Maintenance process models

### Quick fix

- Characteristics
  - When a problem occurs, fix will take place (mainly implementation and test)
  - Ad-hoc approach to maintenance
  - Fix will be done without detailed analysis
- Advantages
  - Fast
  - Can be useful for small projects
- Disadvantages
  - Little or no documentation
  - Any design becomes less useful over time

### Boehm's

- Characteristics
  - Process based on economical models and principles
  - Management decisions are the driving force
- Advantages
  - Controlled process
  - Emphasis on feedback
- Disadvantages
  - Slower than quick fix

### Osborne's

- Characteristics
  - Treated as continuous iterations of the software lifecycle activities with provisions for maintenance made for each
  - If good maintenance features do not exists, it is permitted to construct such documnets
- Advantages
  - Involves all lifecycle phases
  - Documentation is updated
- Disadvantages
  - Complicated
  - Lots of overhead

### Iterative enhancement

- Characteristics
  - Based on the view that changes are iterative and process is incremental
  - Model assumes complete documentation each stage
  - Assumes that the software is fully analyzable
- Advantages
  - Relatively simple
  - Allows for analysis
- Disadvantages
  - Management decisions are not explicitly included

### Reuse orientated

- Characteristics
  - Maintenance is viewed as activity involving the reuse of existing software
  - Any phase of the lifecycle can be the starting point
- Advantages
  - Can use components from other projects
  - Code is modular
- Disadvantages
  - Overhead in designing for reuse

## Agile models

### Extreme programming

- Characteristics
  - After *initial communication*, project divided into tasks
  - Tasks are selected by client and completed by small team
  - Each team works on other phases and integrate as soon as finished
- Advantages
  - Quick (on-going) integration
  - Works well even if REQ is not very clear
- Disadvantages
  - Overall integration
  - Lack of documentation for maintenance

### SCRUM

- Three roles
  - Product owner: responsible for business value of a project
  - Scrum master: ensures the team is functional and productive
  - Team: self organizes to get the work done
- Three artifacts
  - Product backlog: prioritized list of desired product features/outcomes
  - Sprint backlog: set of work from the product backlog
  - Burn-down chart: at-a-glance look at the work remaining
- Four ceremonies
  - Sprint planning: team meets with product owner to choose a set of work to deliver during a sprint
  - Daily scrum: team meets each day to share struggles and progress
  - Sprint reviews: team demonstrates to product owner what was completed during the sprint
  - Sprint retrospectives: team looks for ways to improve the product or process

### Agile maintenance

- Maintenance item (bug, feature, refactoring) will be added as a PBI
- Team estimates the PBI
- PBI items chosen for SBI
- Complete a sprint
- Shipped out

