# Lecture 18: verification and validation

## Definitions

### Verification

- The process of evaluating a system or component to determine whether the products of a given development phase satisfy the conditions imposed at the start of that phase
- The process of providing objective evidence that the system software, or hardware and its associated products conform to the requirements
  - For all life cycle activities during each life cycle process
  - Satisfy standards, practices, and conventions during life cycle processes
  - Successfully complete each life cycle activity and satisfy all the criteria for initiating succeeding life cycle activities
- Verification of interim work products is essential for proper understanding and assessment of life cycle phase product(s)

### Validation

- The process of evaluating a system or component during or at the end of the development process to determine whether it satisfies specified requirements
- The process of providing evidence that the system, software, or hardware, and its associated products satisfy requirements allocated to it at the end each life cycle activity, solve the right problem, and satisfy intended use and user needs

### Takeaways

- Time related terms
  - "the start of..."
  - "at the end..."
- Action related terms
  - "process"
  - "activities"
- Goals related terms
  - "requirements"
  - "conditions"
  - "intended use and user needs"

## Processes

- V&V processes have activities and tasks defined for the processes
- V&V activities that are associated with software life cycle processes in clause 9 of ISO12207

### V&V and testing

| Software | V&V testing by integrity level |
| -------- | ------------------------------ |
| | 4 \| 3 \| 2 \| 1 |
| V&V software component testing | Perform \| Perform \| Review \| No action |
| V&V software integration testing | Perform \| Perform \| Review \| No action |
| V&V software qualification testing | Perform \| Perform \| Review \| No action |
| V&V software acceptance testing | Perform \| Perform \| Review \| No action |

> The term **perform** means that the V&V organization specifies and creates its testing product and either conducts that testing or analyzes the results of that testing if it is conducted by another organization. The term **review** means that the V&V organization reviews the testing plans and analyzes the results of tests

### Integrity levels

| Level | Description |
| ----- | ----------- |
| 4 (catastrophic) | Software must execute correctly or grave consequences will occur. No mitigation is possible |
| 3 (critical) | Software must execute correctly or the intended use of system/software will not be realized casuing serious consequences. Partial to complete mitigation is possible |
| 2 (marginal) | Software must execute correctly or an intended function will not be realized causing minor consequences. Complete mitigation possible |
| 1 (negligible) | Software must execute correctly or intended function will not be realized causing negligible consequences. Mitigation not required |

## Activities

### Common

- V&V management
  - Monitors and evaluates all V&V outputs
- Acquisition V&V
  - Addresses project initiation
  - Contract preparation
  - Supplier monitoring
  - Acceptance and completion
- Supply planning V&V
  - Address the initiation
  - Preparation of response
  - Contract and planning
  - Execution and control
  - Review and evaluation
  - Delivery and completion activities
- Project planning V&V
  - Determines scope of the project management and technical activities
  - Identifies process outputs, project tasks and deliverables
  - Establishes schedules for project task conduct
- Configuration management V&V
  - Use and provide inputs to the configuration management process throughout the project life cycle

### Software

- Software concept V&V
- Software requirements V&V
- Software design V&V
- Software construction V&V
- Software integration test V&V
- Software qualification test V&V
- Software acceptance test V&V
- Software installation and checkout V&V
- Software operation V&V
- Software maintenance V&V
- Software disposal V&V

## Explanation

- Verify and validate that the software requirements satisfy the system requirements allocated to software within the assumptions, constraints, and operating environment for the system
- Verify that the software requirements comply with standards, references, regulations, policies, physical laws, and business rules
- Validate the sequence of states and state changes using logic and data flows coupled with domain expertise, prototyping results, engineering principles, or other basis
- Validate the flow of data and control satisfy functionality and performance requirements
- Validate data usage and format


