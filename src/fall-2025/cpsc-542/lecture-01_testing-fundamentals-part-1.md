# Lecture 1: testing fundamentals (part 1)

## Definition of testing

### Dictionary definition

> testing (adj.): revealing a person's capabilities by putting them under strain; challenging. "it's been quite a testing time for all of us" by Oxford Dictionaries

### Software testing definition

- According to IEEE std 829-2008
  - 1) An activity in which a system or component is executed under specified conditions, the results are observed or recorded, and an evaluation is made of some aspect of the system or component
  - 2) To conduct an activity as in (1)
- Software testing is
  - An activity
  - An evaluation
- The evaluation part is deeper than it seems
  - How to come up with a proper evaluation?
  - How do you know your "proper evaluation" is proper?
  - How do you assure that you do have a proper evaluation?

## Motivation of software testing

- Software is a necessary part of society
  - Software that does not work properly can cause significant undesired effects
- Has a role in software development, maintenance, and operations
- Improves software quality

## What is testing

- Important terms
  - Error
  - Mistake
  - Bug
  - Defect
  - Failure
- An error/mistake by a developer produces a bug (defect)
- A bug/defect gets executed, the system may (or may not) work and causes a failure

### Software testing principles

- Testing shows the presence of defects
- Exhaustive testing is impossible
- Early testing
- Defect clustering
- Testing is context dependent
- Absence of errors fallacy

## Software testing process

- Test planning and test control (monitoring the plan)
- Test analysis and design
- Test implementation and execution
- Test evaluation (exit criteria and reporting)

### Software development models

- V-model (sequential development model)
- Iterative-incremental development models

### Software testing models

- Testing does not exist in isolation and test models mirror software development models

### Levels of testing

- Unit testing
- Integration testing
- System testing
- Acceptance testing

### How to conduct testing

- White-box testing
- Black-box testing

### Code based testing

- Structural testing
  - Statement coverage
  - Branch coverage
  - Path coverage
  - Cyclomatic complexity
- Static testing
  - Code walkthrough
  - Code inspection
  - Code review

### Specification based testing

- Boundary value analysis
- Equivalence partitioning
- Decision tables

### Test management

- Test organization
- Test planning and estimation
  - Test planning
  - Entry criteria
  - Exit criteria
  - Test estimation
- Test progress monitoring and control
  - Test progress monitoring
  - Test reporting
  - Test control
- Configuration management
- Risk management
- Incident management
