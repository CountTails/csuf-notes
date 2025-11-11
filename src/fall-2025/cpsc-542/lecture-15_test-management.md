# Lecture 15: test management

- ISO 29119: viewpoint that empashizes overall, academic, or conceptual
- ISTQB: advanced-level-test-manager

## Testing process

### Test planning, monitoring and control

- Test planning
  - Involves identifying activities and resources required to meet mission and objectives identified in the test strategy
- Monitoring and control
  - Establish a testing schedule and monitoring framework
  - Enables tracking of test work products and resources against the plan

### Test analysis

- An activity the defines *what* is to be tested in the form of test conditions
- Test conditions are found by analysis of the test basis, test objectives, and product risks
  - Viewable as the detailed measures and targets for success
  - Should be traceable back to the test basis and defined strategic objectives
  - Should also be traceable forward to test designs and other test work products

### Test design

- The activity that defines *how* something is to be tested
- Involves identification of test cases by stepwise elaboration of identified test conditions or test basis
- Uses techniques identified in the test strategy and/or the test plan

### Test implementation

- The activity during which tests are *organized and prioritized* by test analysts
- Test designs are implemented as concrete test cases, test procedures, and test data
- Inputs are defined and their associated expected results in test case specifications and test steps in test procedure specifications

### Test execution

- Begins once the test object is delivered and the *entry criteria* to test execution are satisfied
- Test manager monitors progress according to the test plan
- Initiate and carry out control actions to guide testing toward a successful conclusion

### Evaluating exit criteria and reporting

- Ensure effective processes are in place to provide the source information for evaluating exit criteria and reporting

### Test closure activities

- Test execution is determined to be complete
- Key outputs should be captured and either passed to the relevant person or archived
- Collectively, these are test closures activities

## Test management

### Test management in context

- Manager's central responsibility involves
  - Secure and utilize resources
  - Carry out a value-adding processes
- Understand testing stakeholders
  - Developers, managers,and architects
- Align of test activities and other lifecycle activities
  - Testing should be integral to a project
  - Disregards the software development models used

### Managing non-functional testing

- The testing of non-functional requirements of a software application
  - Includes compliance, usability, load, and security testing
- How to integrate functional tests into the software development lifecycle
  - Common mistake to wait until *all* functional tests are complete to starting non-functional tests
  - Can result in late discovery of critical non-functional defects

### Risk-based testing

- Risks exist whenever some problem may occur which would decrease perceptions of product quality or project success
  - Identify quality risks and assess risk to product quality with stakeholders
  - Test team designs, implements and executes tests to mitigate the quality risks
- Quality includes the totality of features, behaviors, characteristics, and attributes that affect customer, user, and stakeholder satisfaction

### Test documentation

**Test policy**

A short, high-level document that

- Summarizes the value that the organization derives from testing
- Defines the objectives of testing
  - Building confidence in the software
  - Detecting defects in the software
  - Reducing the level of quality risk
- Describes how toe evaluate effectiveness and efficiency of testing in meeting objectives
- Outlines the typical test process, perhaps using ISTQB fundamental test process as a basis
- Specifies how the organization will improve its test processes

**Test strategy**

- Describes the organization's general test methodology
- Includes the way testing is used to manage product and project risks
- Covers division of testing into levels and high-level activities associated with testing

**Master test plan**

- Covers all of the testing work to be done on a particular project
- Includes the particular levels to be carried and the relationships among those levels
- Corresponds the test levels and the development activities

**Level test plan**

- Describe the particular activies to be carried out within each
  - Test level
  - Test type

### Project risk management

- Project risks can and should be mitigated successfully by the test manager
  - Test environment and tools readiness
  - Test staff availability and qualification
  - Lack of standards, rules and techniques for the testing effort
- Once a project risk has been identified and analyzed, there are 4 main options to manage that risk
  - Mitigate the risk through preventive measures to reduce likelihood and/or impact
  - Make contingency plans to reduce impact if the risk becomes an actuality
  - Transfer the risk to some other party to handle
  - Ignore or accept the risk

### Test estimation

- A management activity is the creation of an approximate target for cost and completion dates
- Associates them with activities involved in a particular operation or project

### Defining and using test metrics

- What gets measures gets done
- What doesn't get measures does not get done
- Testing metrics can be classified as belonging to one or more of the following categories
  - Project metrics: measures progress toward established project exit criteria, such as the percentage of test cases executed, passed, and failed
  - Product metrics: measures some attribute of the product, such as the extent to which it has been tested or the defect density
  - Process metrics: measure the capability of the testing or development process, such as the percentage of defects detected by testing
  - People metrics: measure the capability of individuals or groups, such as the implementation of test cases within a given schedule
- A test manage may want to perform the following
  - Definition of metrics
  - Tracking of metrics
  - Reporting of metrics
  - Validity of metrics

### Metrics road rap

**Risk metrics**

- Percentage of risks completely covered by passing tests
- Percentage of risks for which some or all tests fail
- Percentage of risks not yet completely tested
- Percentage of risks covered, sorted by risk category
- Percentage of risks identified after the initial quality risk analysis

**Defects metrics**

- Cumulative number reported (found) versus cumulative number resolved (fixed)
- Mean time between failure or failure arrival rate breakdown of the number or percentage of defcts categorized by the following
  - Particular test items or components
  - Root causes
  - Source of defect
  - Test releases
  - Phase introduced, detected, and removed
  - Priority/severity
  - Reports rejected or duplicated trends in the lag time from defect reporting to resolution number of defect fixed that introduced new defects

**Test metrics**

- Total number of tests planned, specified (implemented), run, passed, failed, blocked, and skipped
- Regression and confirmation test status, including trends and totals for regression test and confirmation test failures
- Hours of testing planned per day versus actual hours achieved
- Availability of the test environment (percentage of planned test hours when the test environment is usable by the test team)

**Test coverage metrics**

- Requirements and design elements coverage
- Risk coverage
- Environment/configuration coverage
- Code coverage

**Test planning metrics**

- Risk, requirements, and other test basis element coverage
- Defect discovery
- Planned versus actual hours to develop testware and execute test cases

**Test analysis metrics**

- Number of test conditions identified
- Number of defects found during test analysis

**Test design activity metrics**

- Percentage of test conditions covered by test cases
- Number of defects found during test design (by developing tests against the test basis)

**Test implementation activity metrics**

- Percentage of test environments configured
- Percentage of test data records loaded
- Percentage of test cases automated

**Test execution activity metrics**

- Percentage of planned test cases executed, passed, and failed
- Percentage of test conditions covered by executed (and/or passed) test cases
- Planned versus actual defects reported/resolved
- Planned versus actual coverage achieved

## The rest

### Review

- Management reviews and audits: understand key characteristics of management reviews and audits
- Managing reviews
  - Analyze a project to select appropriate review type and define a plan for conducting reviews
  - Understand the factors, skills, and time required for participation in reviews
- Metrics for reviews: define process and product metrics to be used in reviews
- Managing formal reviews: explain, using examples, the characteristics of a formal review

### Defect management

- Defect lifecycle and the software development lifecycle
- Defect report information
- Assessing process capability with defect report information

### Improving the testing process

- Test improvement process
- Improving the test process
  - With TMMI
  - With TPI next
  - With CTP
  - With STEP

### Test tools automation

- Test tool selection
- Tool lifecycle
- Tool metrics

### People skills

- Individual skills
- Test team dynamics
- Fitting testing within an organization
- Motivation
- Communication

