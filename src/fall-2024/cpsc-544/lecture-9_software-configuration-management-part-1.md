# Lecture 9: software configuration management (part 1)

## The need for configuration management

**Software configuration management**

- One of the most fundamental activities in software engineering
- Changes to requirements drive changes in design which affects code
- Even modest sized project require a *formal change management system*
- Key objective of the software process
  - Have change activity converge
  - Leads to a stable product that is stable enough to ship
  - Managing all changes is important to achieve this goal
- Focuses on code control
  - Control requirements and design changes
  - Can often be handled as enhancements to a code management system
- Change management is a set activities to help manage change by
  - Identifying work products that are likely to change
  - Establishing relationships among them
  - Defining mechanisms for managing different versions
  - Controlling changes imposed
  - Auditing and reporting and changes made

**Problems fixed with configuration management**

- Problems are frustrating because
  - They take time to fix
  - Often happen at the worst times
  - Are totally unnecessary
- Configuration management addresses these by
  - Coordinating the work product of many different people
  - Preventing conflicts that result in problems

| Problem   | Definition    |
|--------------- | --------------- |
| Simultaneous update   | Two or more programmers work separately on the same program   |
| Shared code   | Bug is fixed in code shared by several programmers   |
| Common code   | Common program functions are modified   |
| Versions   | Evolutionary releases   |

**Control system to answer**

1) What is my current software configuration?
2) What is its status?
3) How do I control changes to my configurations?
4) How do I inform everyone else of my changes?
5) What changes have been made to my software?
6) Does anyone else's changes affect my software?

## Software product nomenclature

- Role of configuration management
  - Control the development of elements as they are built
  - Combine into a full system
  - Important to use common system terminology
- Start the design process by
  - Partitioning the system
  - Repeat until a satisfactory level of detail is achieved
- Implementation begins with the smallest pieces
  - Each is assembled and tested progressively
  - Eventually, the total system is completed

| Name   | Definition    |
|--------------- | --------------- |
| System   | Package of all software (and hardware) meeting user requirements   |
| Subsystem   | Piece of a whole system dedicated to meet a subset of user requirements, such as display   |
| Product   | Useable program included in a subsystem   |
| Component   | Specific program made of abstract entities like a scheduler or an I/O controller |
| Module | Building blocks of system components |

| Test name   | Definition    |
|--------------- | --------------- |
| Unit test   | Test of an individual module   |
| Integration test   | Test of interface and interdependencies of integrated modules (between them)   |
| Function test   | Test a fully operational build of a component, product, subsystem and full system test   |
| Regression test   | Test against new builds to ensure that it has not regressed   |


## Basic configuration management functions

- With a stable initial product, establish a first baseline
- With each successive set of enhancements, establish a new baseline in step with development
- Retain each baseline in a database along with all changes that produced it
- The baseline is
  - The official repository of the product containing the most current version
  - Only tested code and approved changes are put into the baseline
  - Acts as the official source for all programmers to use

**Configuration control**

- Revolves around **1** official copy of the code
- Protect every system revision by keeping a separate official copy of each revision level
- Can take a lot of storage, but most serious issues concern *code divergence*

**Revisions**

- Keep track of revisions
- Large systems may involve a program that provides essential functionality for all others
- Once a module is integrated into a testable unit, it is tested with the latest control program level
- Previous tests can be re-run to trace new problems to the source
- Early driver modules can differ, so exact reproduction of prior test is not possible
- Key is to track every change to every module and every test case
- There is one latest official version and all others are retained
- Obsolete copies can be used to trace problems

**Derivations**

- A derivation record can show
  - Test A was run on control program level 116
  - And re-run was attempted on level 117
  - Changes X and Y can be identified readily
- Information in a derivation record include
  - Revision level of each module
  - Revision level of tools used
  - Test cases used and their revision level
  - Test data employed
  - Files used
  - Software (and hardware) configuration
  - Operational procedures
  - If not a stand-alone test, a record of job streams being executed

**Versions**

- Several different functions can be implemented by the same module with modest differences in code
- Project progression leads to many versions of work product
- Repository must save all of these
  - Enables effective management of product releases
  - Permits developers to go back to previous versions during testing and debugging

**Deltas**

- Multiple versions introduce the problem of multiple copies of the same code
  - Most of the code in the two memory management modules are identical
  - One would have an additional routine to handle memory limits testing and mode switching
- Stored separately, there is no way to ensure changes made to one are incorporated into the other
- Deltas solves this by storing the base module along with the changes required to make it into another version

**Conditional code**

- Another way to handle slight variations is conditional program construction
- Source program contains different versions constructed based on different conditions
  - None are included in the final system unless called for during installation
- Conditional code is done using system generation options
  - Conditionally select optional modules based on the particular condition
  - All modules are included in the source library, but only one is used at anytime

## Baselines

- A baseline is the foundation for configuration management
  - Provides the official standard on which subsequent work is based on
  - Only allows authorized changes to be made
- After an initial baseline, subsequent changes are recorded as deltas until the next one is set
- Baselines should be established early in a project
- But not *too early* as to impose unnecessary procedures and slow programmers work down
- As long as individual modules work with little interaction, a baseline is not needed
- As soon as integration begins, formal control is needed

**Scope**

- Current level of each module
- Current level of each test case
- Current level of each tool used
- Current level of any special test or operational data
- Current level of all macros, libraries, and files
- Current level of any installation or operating procedure
- If project involves OS or change control program, retain computing system information and its change level

**Control**

- Ensure appropriate baseline control while providing a flexible service to programmers
  - Must protect against unauthorized changes
  - Must allow programmers to readily test their code
- Controlled flexibility is done by providing private working copies of any part of the baseline to programmers
  - Enables programmers to try out changes
  - Doesn't disturb anyone else
- When ready to incorporate changes
  - Ensure new code changes are compatible
  - New code does not cause regression

**Configuration management records**

- Code change procedure
  1) Change proposal is documented and must be authorized before being made
  2) As change is made, record of what was done is kept
  3) Test results should also be documented
- Detailed test records are crucial for simultaneous software and hardware changes
- Problem reports
  - FIXME!
- Expect lists
  - List of every function and feature planned for the next baseline
  - Developers should maintain a list of functions, features, fixes, and interfaces to implement before attempting integration
  - Information is made available to all development groups so they can evaluate impact on their own work

## Configuration management responsibilities

- Needed to implement necessary controls and procedures
- May be handled by a single person, a few, or an entire organization

**Module ownership**

- Maintaining design integrity is difficult in large systems
- Designate a programmer to "own" each module
  - Many programmers will end up owning more than one module
- Module owners must
  - Know and understand module design
  - Provide advice to everyone who works on or interfaces with the modules
  - Serve as a technical control point for module modification (enhancement and repair)
  - Ensure module integrity by reviewing changes and conducting periodic regression tests

**Change control board**

- Required on large projects to ensure change is properly considered and coordinated
- Purpose is to ensure baseline changes are considered by all involved parties and is authorized before implementation
- To consider a proposed change, the following information is needed
  - Size
  - Alternatives
  - Complexity
  - Schedule
  - Impact
  - Cost
  - Severity
  - Relationship to other changes
  - Test
  - Resources
  - System impact
  - Benefits
  - Politics
  - Change maturity
- To fix customer reported problems, the following additional information is needed
  - Problem change is intended to fix
  - Conditions under which the problem was observed
  - Copy of the trouble report
  - Technical description of the problem
  - Names of any other programs affected
- Prior to release, additional information should be made available
  - Final source and/or object code
  - Final documentation changes
  - Evidence of successful inspection and test of code and documentation
- Change should then be authorized or denied and controls conditions under which code can be released
- Problems with the change control board
  - Workload can be excessive, especially during final testing and release phases of large project
  - Can establish multiple change control boards for specific components/test phases
  - Board members must be selected with care
  - Board members have the power to block any part of the project
  - Generally, the project manager should chair the highest-level change control board

**Configuration management organization**

- Primarily responsible for project-unique changes
- Must coordinate with computer operations to replicate every program and test environment

## The need for automated tools

- Final development stages involve a lot of details
- Sloppiness in last minute changes can destroy quality
- Overlooked changes can lead to unpleasant problem during test or customer use

**Change management system**

- Tracks change requests, problem reports, board actions, and activity logs
- Data on what was done, by whom, when, what remains to be done, any special conditions, and current status
  - Changes not closed
  - Changes to particular components
  - Oldest outstanding changes
- Track mean time to change closure and maintain statistics on the change backlog
- Change activity is a powerful indicator of project status
  - Enables management to pin point problems and address them in a timely manner

**System library**

- Stores development work products
  - Source and object code for every baseline
  - Test cases
  - Development tools
- Provides locks to prevent unauthorized changes
  - Can build various system configurations
  - Test drivers, scenarios, and buckets required for development
- Primary functions include
  - Retrieving objects by name, date of creation, author, component, and development status
  - Identifying object relationships
  - Executing a make function (build product release)
  - Performing service functions like checking status, verifying presence of build items
  - Providing required levels of control and protection
  - Gathering and reporting any desired statistical and accounting information
