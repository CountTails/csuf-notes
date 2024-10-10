# Lecture 16: software testing

## Software testing definitions

- Software testing is the execution of a program to find its results
- Most time of the software development process is spent here
- Many software professionals believe testing is done to show that the program works (Incorrect)
- Testing is done to learn about a program's faults
- Testing is an *inefficient way* to find most bugs
  - Software inspections offer the same quality improvement benefits
  - Despite limitations, testing still remains a critical part of software development

| Term   | Definition    |
|--------------- | --------------- |
| Testing   | The process of executing a program (or part of a program) with the intention of finding errors |
| Verification   | The set of activities that ensure the software correctly implements a specific function. Are we building the *product right*?   |
| Validation   | A different set of activities that ensures that the software that has been built is traceable to customer requirements. Are we building the *right product*?  |
| Debuggging   | Diagnosing the precise nature of a *known error* and then *correcting* it   |

**Seven types of software test**

1) Unit or module tests
2) Integration tests
3) External function tests
4) Regression tests
5) System tests
6) Acceptance tests
7) Installation tests

**Testing methods**

- White box testing: internal design of a program is available and tester uses detailed knowledge to create tests
- Black box testing: tests are designed without knowledge of the program's internals (based on functional requirements)

## Software testing principles

- Software testing presents an economic problem
  - In large systems, more tests will always find more bugs
  - The question is whether all bugs have been found, but whether the program is sufficiently good enough to stop testing
- The trade-off between more testing or stopping should be based on
  - Probability of finding more bugs in tests
  - Marginal costs of doing more tests
  - Probability of users encountering the remaining bugs
  - Resulting impact of these bugs on users

### The axioms of testing

- A good test case is one that
  - Has a high probability of detecting a previously undiscovered defect
  - Not one that shows the program works correctly
- One of the most difficult problems in testing is knowing when to stop
- It is impossible to test your own program
- A necessary part of every test case is the description of the *expected output*
- Avoid non-reproducible or on-the-fly testing
- Write test cases for *invalid* and *valid* input conditions
- Thoroughly inspect the results of each test
- As the number of detected defects in a piece of software increases, the probability of the existence of more undetected defects also increases
- Assign your best programmer to testing
- Ensure that testability is a key objective in your software design
- The design of a system should be such that each module is integrated into the system only once
- Never alter the program to make testing easier
- Testing, like most other activities, must start with objectives

### The proper role of testing

- Exhaustive testing, even for relatively simple programs, is generally impossible
- Test design reduces this to a small subset of conditions that will reveal characteristics of a program

## Types of software tests

### Unit testing (white box)

- Unit tests are essentially path tests
  - A path is an instruction sequence that threads through the program, from entry to final exit
  - Focuses on a small segment of code and aims to cover a high percentage of internal paths
- These tests are often designed by the programmer who produced the code 
  - Tester may be biased by previous experience
  - Those who create the program's faults are least likely to recognize them
- Unit testing generally has the highest error yield rate of all testing techniques

### Integration testing

- Proper approach depends on 
  - The kind of system being built
  - Nature of the development project
- Large systems should approach integration is a step-wise manner
  - Such system may have several components that can be built and integrated separately

**Bottom-up testing**

1) Modules are individually tested, with stub drivers implementing system functions
2) As more modules are integrated, stub drivers are replaced by modules performing those functions

**Top-down testing**

1) Initial tests establish a basic system skeleton and each new module add capability
2) Lower-level functions are simulated with stubs

### System build

- Build experts
  - Integrate components in the system builds
  - Maintain configuration management
  - Distribute builds back to development for module and component test
- Developers and build experts
  - Establish the integration plan
  - Build the drivers
  - Integrate the system

### Function testing (black box)

- Designed to exercise the program to its *external specification*
- Testers are not biased by knowledge of program's design
  - Likely provide tests that resemble the user's environment
  - Requires explicitly stated requirements and ability for tests to cover only small portions of the possible test conditions

### Regression testing

- Testing is both progressive and regressive
  - Progressive introduces tests and new functions, uncovering problems with newly added or modified modules and their interfaces
  - Regressive concerns the effects of newly introduced changes on all previously integrated code 
- Problems arise when errors made in incorporating new functions affects previously tested functions
- This testing is particularly important with software maintenance
  - Incorporate selected test cases into a regression test bucket
  - Run the test bucket periodically to attempt to detect regression problems

### System testing

- Find the cases where the system does not work as intended
  - Regardless of contract, if system does not meet user's real needs, everyone loses
  - Special attention should be paid to operational errors and intentional misuse
- Program objectives should specify what is to be done for the end users
  - Non-specific objectives cause testing, system design, and implementation planning issues
  - Systems build without good objectives often have to be rebuilt before use
- System test planning often discovers issues undiscovered through the entire development process

### Acceptance and installation tests

- Try the system in a real user environment
  - A field test like this requires special support, but are invariably worth more than the costs
  - Only required when software is developed under contract
- For non-contracted development, special users can access beta test sites
  - Compensate users with special installation support or early program availability
  - If end user testing is not possible, it may be possible to try the system in an internal application environment

## Test planning

- Starts with an overall development plan
  - Defines all functions, roles, and methods for all test phases

### The test files

- Establish a development file system
  - Retains information for the test plan
  - Retains information for each test and test case
- Should be defined and provisioned as part of the configuration management plan
- Helps relate all materials to each test and helps establish a test database

### Test success criteria

- Developers view success as executing a test case without any problems
- Testers measure success based on bugs found
- Tests should be planned against yield criterion (bugs per test run) determined from previous experience
  - Tester's goal is to increase the test case yield
  - Developer's goal is to produce code that will reduce test yield
- If tester cannot meet yield objectives, work should be technically reviewed for adequacy
- Testers should determine why did not catch bugs found later to help improve test design for the future

## Test development

- Deciding what test cases to develop is based on
  - Full test coverage is generally impossible
  - There is **no** proven comprehensive method to select the highest yielding test conditions
- Because errors are inevitable, hold walkthroughs of the test plan and inspections of the test cases
- It is reasonable to test
  - All valid classes for normal operations
  - Exhaustively test behavior under unusual or illegal conditions

### Test coverage techniques

- Program as a graph
  - Statement are nodes, flow are paths
  - Ensure that nodes and the paths between them are adequately covered by tests
  - Test coverage is determined by comparing the number of test paths executed with the complexity of the program graph
- In unit tests
  - Pick requirement functional paths that connect entry to exit
  - Pick additional paths as small variations
  - Pick additional paths that have no obvious functional meaning
- In functional testing
  - Program functions are considered as a set of transaction flows that form functional paths
  - Transaction flows can be reduced to graphs of nodes and paths
  - Tests are designed to achieve coverage of these nodes and paths

### Path selection

1) Establish equivalence classes based on various parameters and conditions for the program
2) An equivalence class covers all valid cases
3) An equivalence class would also be established for invalid classes (too low or too high)

### Test case design guidelines

- Consider common types of errors
  - Missing control flow paths
  - Inappropriate path selection
  - Inappropriate or missing action
- Some general guidelines
  - Do it wrong
  - Use wrong combinations
  - Don't do enough
  - Do nothing
  - Do too much
- Overall considerations
  - Don't forget about normal test cases
  - Don't go overboard with test cases
  - Don't ignore structure
  - Remember that there is more than one kind of test

## Test execution and reporting

- Tests should be treated as experiments
  - Carefully controlled and recorded
  - Reproducible
- All anomalous behavior should be noted and investigated

### Test reports

- Each test should produce a test report
- Detail depends on purpose and audience of the report

### Bug classification

- Should have standard definitions for bug severity
  - Allows follow-up actions to be prioritized
  - Helps track critical items

### Test analysis

- Tests gather data on programs
  - Analyze resulting information
  - Use it to make decision

## Test tools and methods

FIXME! Test tools

## Real-time testing

- Difficult because
  - Development done on a host system
  - Compiled for execution on a target system
- Test and debug facilities are available on the host system
- Target system is generally much more sparsely equipped

## The test organization

- Programmers are inherently incapable of effectively testing their programs
  - Feel guilty about the existence of bugs
  - Biased by the creative work they have done
- Can be remedied by separating testing from program design and implementation
  - Such test groups assume test responsibility *after* unit testing
  - Group tries to find as many bugs as possible
  - With experience, these groups can find odd pathological cases
