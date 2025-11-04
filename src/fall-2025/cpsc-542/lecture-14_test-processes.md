# Lecture 14: test processes

## Motivation

- Is knowing all the test techniques enough in achieving high quality software? No
- When software was not big and complicated
  - Development could be effectively done with a handful of hotshot developers
  - Testers could apply techniques learnt from previous work without bothering colleagues
  - Occasional informal chats were enough to resolve issues
- Time flies and software product size grows
  - Stakeholders in software projects are no longer just developers and testers
  - Failing to communicate among large number of stakeholders
  - Failing to follow through with things
  - Failing to have a systematic way of testing things
  - Good quality software is not achievable with test techniques alone

## What is test process?

- A dictionary definition: *a series of actions or steps taken in order to achieve a particular end*
- With "test" sprinkled in: *a series of test actions or test steps taken in order to achieve a particular end*
- Promoters of IEEE 29119 believe there are multiple test processes falling into one of three main categories
  - Organizational test process
  - Test management processes
  - Dynamic Test processes

### Test processes (IEEE 29119)

- Learning is a bit difficult
  - Consists of 5 parts and 488 pages
  - Costs $100 a copy

**Our approach (1st category)**

- Covers organizational test process
- Addresses high level, over-all issues
  - Test policy
  - Test goals

**How about the 2nd and 3rd category**

- Second category covers test management processes
  - Static type activities involving planning, monitoring, and controlling
- Third category covers dynamic test processes
  - Developing test scripts and executing them

## Definitions

### Organizational test process

> Defining a process for the creation and maintenance of organizational test specifications, such as organizational test policies, strategies, process, procedures and other assets

### Dynamic processes

> Defining generic processes for performing dynamic testing. Dynamic testing may be performed at a particular phase of testing or for a particular type of testing within a test project

### Test management processes

> Defining processes that cover the management of testing for the whole test project or any test phase or test type within a test project

## Strategy

### What are those processes?

1) Organizational test process
2) Test management process (Test planning, test monitoring and control, test completion)
3) Dynamic test process (test design and implementation, environment setup and maintenance, execution and incident reporting)

### Organizing thoughts

- Diving into the 8 processes and learning them all is tempting
- Instead, take the following steps
  - 1) We want to improve the quality of our software products
  - 2) We have learned all those basic and fancy testing techniques
  - 3) Modern software products are so big and complicated and involve many stakeholders. This significant concern threatens the quality of our software products
  - 4) Need a well-defined test process
  - 5) IEEE 29119 comes to the rescue, telling us to implement 8 test processes to get good quality on our software products

## Concerns

- Some readers of IEEE 29119 may not agree or will have concerns
- Maybe agile development is the true answer to the big, complicated, and so-many people problem

### Agile manifesto

- We are uncovering better ways of developing software by doing it and helping others do it
- Through this work, we have come to value
  - Individuals and interactions over processes and tools
  - Working software over comprehensive documentation
  - Customer collaboration over contract negotiations
  - Responding to change over following a plan
- That is, while there is value in the items on the right, we value the items on the left more

### Second thoughts

- Sounds like processes, tools, documentation, and plans are discouraged under agile
- Does not mean we should have ZERO processes, tools, documentation, and plans
- Agile mainly focuses on the issue of "how", while IEEE 29199 focuses on the issue of "what"
- There is no intrinsic conflict between "how" and "what"

### Articulations

- Let's say you are a great Agile pilot
  - Good at responding to change over following a plan
  - Approachable person who interacts well with co-pilot and flight crew
- During take-off, you don't have a process
  - Say, a pre-flight checklist on WHAT needs to be done before take-off
  - After a bad night of sleep, you leave the flaps up....oops!

## Avoiding the oops moment

- Have some process on hand and follow it
- 8 such processes in IEEE 29199 suggested
- Some may seem heavy and not suitable for agile, but take a look before jumping to any conclusions

## The first layer: organizational test process

- Used to develop and manage organizational test specifications
- These specifications typically apply across the whole organization
- Organizational test policy and organizational test strategy are examples of organizational test specifications

**Process steps**

1) Develop organizational test specification
2) Monitor and control use of organizational test specification
3) Update organizational test specification

**Outcomes**

- Requirements for organizational test specification are identified
- Organizational test specifications are developed
- Organizational test specifications are agreed to by stakeholders
- The organizational test specifications are made accessible
- Conformance to the organizational test specifications is monitored
- Updates to organizational test specifications are agreed to by stakeholders
- Updates to the organizational test specifications are made


## The second layer: test management processes

- From a management point of view:
  - Having a plan
  - Monitoring and controlling the execution of that plan
  - See the completion of that plan
- A natural way of managing

### Test planning

**Activities**

- Understand context
- Organize test plan development
- Identify and analyze risks
- Identify risk mitigation approaches
- Design test strategy
- Determine staffing and scheduling
- Record test plan
- Gain consensus on test plan
- Communicate test plan and make available

**Outcomes**

- Scope of work of the test project is analyzed and understood
- Stakeholders who will participate in the test planning are identified and informed
- Risks that can be treated by testing are identified, analyzed, and classified with an agreed level of risk exposure
- Test strategy, test environment, test tool and data needs are identified
- Staffing and training needs to be identified
- Each activity is scheduled
- Estimates are calculated and evidence to justify the estimates is recorded

### Test monitoring and control process

**Activities**

- Setup
- Monitor
- Control
- Report

**Outcomes**

- Means of collecting suitable measures to monitor test progress and changing risk are set up
- Progress against the test plan is monitored
- New and changed test-related risks are identified, analyzed and necessary action(s) invoked
- Necessary control actions are identified
- Necessary control actions are communicated to the relevant stakeholders
- The decision to stop testing is approved
- Test progress and changes to the risks are reported to stakeholders

### Test completion process

**Activities**

- Archive test assets
- Clean up test environment
- Identify lessons learned

**Outcomes**

- Test assets are either archived or passed directly to the relevant stakeholders
- Test environment is in its agreed state
- All test Requirements are satisfied and verified
- Test completion report is recorded

## Third layer: dynamic test processes

### Test design and implementation process

**Activities**

- Identify feature sets
- Derive test conditions
- Derive test coverage items
- Derive test cases
- Assemble test sets
- Derive test procedures

**Outcomes**

- Test basis for each test item is analyzed
- Features to be tested are combined into feature sets
- Test conditions are derived
- Test coverage items are derived
- Test cases are derived
- Test sets are assembled
- Test procedures are derived

### Test environment setup and maintenance process

**Activities**

- Establish test environment
- Maintain test environment

**Outcomes**

- Test environment is set up in a state ready for testing
- Status of the test environment is communicated to all relevant stakeholders
- Test environment is maintained

### Test execution process

**Activities**

- Execute test procedures
- Compare test results
- Record test execution

**Outcomes**

- Test procedures are executed
- Actual results are recorded
- Actual and expected results are compared
- Test results are determined

### Test incident reporting process

**Activities**

- Analyze the test results
- Create/update incident report

**Outcomes**

- Test results are analyzed
- New incidents are confirmed
- New incident report details are created
- Status and details of previously raised incidents are determined
- previously raised incident report details are updated as appropriate
- New and/or updated incident reports are communicated to relevant stakeholders
