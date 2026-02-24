# Lecture 6: maintenance measures

## Software measurement

- The process of objectively and empirically
  - Quantifying an attribute of a software system
  - Quantifying the process connected with a system's development, use, maintenance, and evolution
- Process: any software related activity (analysis, specification, design, coding, testing)
- Resource: input to a process (personnel, hardware, software)
- Product: any intermediate or final output resulting from a software process (system documentation, test data, source code)
- In software measurement, there are 2 types of attributes
  - Internal: measured in terms of process, product, or resource itself
  - External: measured with respect to the relation of a process, product, or resource to its environment
- The result of a measurement process is known as a metric

## Objectives of software measurement

1) Evaluation: evaluate different methods, program libraries, and tools before deciding which is best for a given task
2) Control: control the process to ensure change requests are dealt with promptly and within budget
3) Assessment (capability): assessing a process in the first step in controlling it
4) Improvement: improve characteristics of a software process (quality and productivity) and track progress with measures
5) Prediction: make predictions about aspects of a software product that assist management with resource allocation

## Types of measurement

### Process metrics

- Measures of the software development process
  - Overall development time
  - Type of methodology used
- Collected across all projects over long periods of time
- Intended to provide indicators that lead to long-term software process improvement
- To improve a software process
  - Measure a specific attribute of the process
  - Derive meaningful metrics from these attributes
  - Use metrics to provide indicators
  - Indicators hint at a strategy for improvement
- To measure effectiveness of a software process
  - Must be measured indirectly
  - Set of metrics is derived from the outcomes of the process
  - Outcomes include:
    - Errors uncovered before release of the software
    - Defects delivered to and reported by end-users
    - Work products delivered
    - Human effort expended
    - Calendar time expended
    - Conformance to schedule

### Project metrics

- Measures of the software project used to monitor and control a project
- Enable a software project manager to:
  - Minimize development time by accounting for delays and potential risks
  - Assess product quality on an on-going basis
- Used in estimation techniques and other technical work
  - Metrics from past projects provide a basis for effort and time estimations for current projects
  - Actual values of effort and time expended can be compared to original estimates
  - Used by project manager to monitor and control the project

### Product metrics

- Measures of the software product at *any* stage of its development
- Product metrics may measure:
  - Complexity of the software design
  - Size of the final program
  - Number of pages of documentation produced
- Direct measures
  - Easy to collect
  - Cost, effort, Lines of Code, Execution speed, Memory size, Defects, etc.
- Indirect measures
  - More difficult to assess & can be measured indirectly only
  - Quality, Functionality, Complexity, Reliability, Efficiency, Maintainability

## Normalization of measurement

- Example scenario
  - 2 different project terms record errors in a software process
  - Team A finds 342 errors before release
  - Team B finds 184 errors before release
  - Which team is more effective at finding errors?
- To answer this question, the size and complexity of the project must be known
- But normalizing allow for direct comparison of the 2 metrics

### Size-oriented metrics

- Based on the "size" of the software produced

| Project | Effort (man months) | Cost ($) | kLOC | Documentation (pages) | Errors | People |
| ------- | ------------------- | -------- | ---- | --------------------- | ------ | ------ |
| A | 24 | 168,000 | 12.1 | 365 | 29 | 3 |
| B | 62 | 440,000 | 27.2 | 1224 | 86 | 5 |

- Advantages of size-oriented metrics
  - Lines of code are easily countable
  - Many software estimation models use lines of code as input
- Disadvantages of size-oriented metrics
  - Lines of code measures are language and programmer dependent
  - Use in estimation requires a lot of detail which can be difficult to achieve

### Function oriented metrics

- Based on "functionality" delivered by the software
- Functionality is measured indirectly using a measure called the *function point*
- FP are derived using an empirical relationship based on countable measures of software and assessments of software complexity

**Calculating FP**

1) Count the measurement parameters
2) Assess the complexity of the values
3) Rate the complexity factors to produce the complexity adjusted value (CAV)
4) Calculate the adjusted FP as follows: $\text{FP} = \test{FP}_{raw} * (0.65 + 0.01 * \text{CAV})$

**Complexity adjustment factors**

1) Does the system require reliable backup and recovery?
2) Are data communications required?
3) Are there distributed processing functions?
4) Is performance critical?
5) Will the system run in an existing, heavily utilized operating environment?
6) Does the system require online data entry?
7) Does the online data entry require the input transaction to be built over multiple screens or operations?
8) Are the master files updated online?
9) Are the inputs, outputs, files, or inquiries complex?
10) Is the internal processing complex?
11) Is the code designed to be reusable?
12) Are conversion and installation included in the design?
13) Is the system designed for multiple installations in different organizations?
14) Is the application designed to facilitate change and ease of use by the user?

- The rating for all factors ($F_{1}$ to $F_{14}$) are summed to produce the CAV
- Each factor receives a rating on the 0-5 scale with 0 being no influence and 5 being essential

**Relation between LOC and FP**

$$
  \text{LOC} = \text{Language Factor} * \text{FP}
$$

| Language | LOC/FP |
| -------- | ------ |
| Assembly | 320 |
| C | 128 |
| Cobol | 105 |
| Fortran | 105 |
| Pascal | 90 |
| Ada | 70 |
| OO languages | 30 |
| 4GL languages | 20 |

## Examples of software measurement

### Size

- One way to measure size is in lines of code
- Usually measures in thousands of lines at a time
- During maintenance, focus in the number of lines added or modified

### Complexity

**McCabe**

- Cyclomatic complexity measures logical complexity
- Represent the code as a control flow graph
  - Nodes stand in for a sequence of one or more procedural statements
    - Nodes containing conditional expressions are known as predicate nodes
    - Predicate nodes have 2 edges leading out from it
  - Edges represent flow of control in a specific direction
    - Edge must start and terminate at nodes
    - Do not intersect or cross over other edges
  - Areas bounded by a set of edges and nodes are called regions
    - Area outside of the graph is also a region
- Complexity is computed as $R = E - N + 2$
  - R is the number of region in the control graph
  - E is the number of edges
  - N is the number of nodes

**McClure**

- A variation of cyclomatic complexity
- Accounts for the complexity of the variables used in predicates
- Computed as $C(M) = C + V$ where
  - C is the number of comparisons
  - V is the number of control variables

**Halstead**

- Proposed many measures, including
  - $n_{1} =$ Number of unique operators used
  - $n_{2} =$ Number of unique operands used
  - $N_{1} =$ Total number of operators used
  - $N_{2} =$ Total number of operands used
  - $n = n_{1} + n{2}$ (program vocabulary) 
  - $N = N_{1} + N_{2}$ (program length)
- An operand is a variable or constant
- An operator is an entity that can change the value of an operand
  - Computed program length: $\text{PL} = n_{1} \log{n_{1}} + n_{2} \log{n_{2}}$
  - Program volume: $V = N \log{n}$
  - Program difficulty: $D = \frac{n_{1}}{2} + \frac{N_{2}}{n_{2}}$
  - Program effort: $E = D * V$
  - Time: $T = \frac{E}{18}$ seconds

### Quality

**Product quality**

- Measurable by
  - Number of change requests per thousand lines of code after release
  - Number of faults detected after release
- Idea is that lower is better

**Process quality**

- Describes the degree the maintenance process is assisting personnel in satisfying change requests
- Measurable by
  - Schedule (difference between planned work and actual work divided by planned work (close to 0 is better))
  - Productivity (lines of code added or modified divided by effort is days required to make changes)

### Maintainability

- Ease with which software can be understood, corrected, adapted, and/or enhanced
- No exact model, but can depend on external factors
  - Mean time to repair (reliability)
  - Modularity (cohesion and coupling)
  - Complexity and readability can serve as indicators
- A maintainable software system implies characteristics of
  - Testability
  - Understandability
  - Modifiability
  - Portability
  - Reliability
  - Efficiency
  - Usability

**Understandability**

- The ease with which the program can be understood
- Ability to determine what a program does and how it works by reading source code and documentation
- Modularity
  - Divide the solution into smaller pieces (modules) with minimum cost
  - Construct modules single-mindedly and avoid excessive interaction with other modules
  - Aim for high cohesion and low coupling
  - Cohesion is a measure of relative functional strength of a module
    - Coincidental: performs multiple completely unrelated actions
    - Logical: performs a series of related actions
    - Temporal: performs a series of actions related in time
    - Procedural: performs a series of actions related by the sequence of steps
    - Communcational: performs a series of actions related by the sequence of steps and all actions are performed on the same data
    - Informational: performs a number of actions, each of its own entry point, with independent code for each action, all performed on the same data structure
    - Functional: performs exactly one function
  - Coupling is a measure of interconnection/interdependence among modules (lower is better)
    - Call coupling: one operation invokes another
    - Type use coupling: component A uses a datatype defined in component B
    - Data coupling: all arguments are homogeneous data items
    - Stamp coupling: a data structure is passed as an argument but the called module operates only some of the individual components of the data structure
    - Control coupling: one passes an element of control to another module
    - Common coupling: access to same global variable allowed
    - Content coupling: one directly references the content of the other (uses `goto` statements)
- Consistency
  - Indentation style (spaces vs tabs) used throughout the program
  - One executable statement per line of code
  - Variable and procedure names are unique, descriptive, and compliant with company standards
  - Each variable and procedure has one and only one unique name in the program
  - Each variable used to represent one and only one quantity and each procedure used to represent one and only one logical function
  - Program is a true representation of design

**Modifiability**

- Defined as the ease with which a program can be changed
- Lower difficulty means more modifiable
  - $D = A / C$
  - $A$ is the average complexity of modules to be changed
  - $C$ is the average complexity of all modules in the program

**Reliability**

- Mean time between errors (should be high)
- Mean time to repair (should be low)
- Percentage uptime (should be high)
- Bebugging: assumes the number of errors removed from a program is related to the reliability of a program
  - $E_{\text{remain}} = N_{\text{real_found}} / N_{seed_found} * N_{seed}$
  - If reliability is above 95% (seed errors found), then stop

### Cost estimation

- Can be computed
  - Based on historical data
  - Using COCOMO or COCOMO 2 frameworks
  - Time in person-months

## Guidelines for selecting maintenance measures

- Qualities of a good metric
  - Simple, precisely defined, and clear how the metric can be evaluated
  - Objective, to the extent possible
  - Easily obtainable
  - Valid (metric should measure what it intends to measure)
  - Robust (relatively insensitive to insignificant changes in process or product)
- Good measurements should have
  - Clearly defined objectives: what measures to use and data to be collected
  - Personnel involvement: measurement purpose should be clear to personnel else it could be misinterpreted or misguided
  - Ease of use: selected measures should not take too much time to administer
