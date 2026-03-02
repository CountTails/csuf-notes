# Lecture 7: building and sustaining maintainability

## Ways of building the maintainability

### Quality factors and setting quality objectives and priorities

**Quality factors**

- Fitness for purpose: deals with whether the product meets the requirements as it was intended
- Correctness: use of SLC models and methods can help build in correctness
- Portability: between different platforms (hardware, software, and even different languages)
- Testability: a system that is easy to test is also easier to change effectively because it is easier to test the changes that are made
- Usability: if a system is not used, then it is useless
- Reliability: builds in the trust into system (safety critical systems need higher degrees of reliability)
- Efficiency: deals with how it makes use of a computer resource
- Integrity: system is safe from unauthorized access and is built from consistent and reproducible set of modules
- Reusability: central to maintainability of a system
- Interoperability: the ability of a system to interact with other systems

**Setting quality objectives and priorities**

- Achieving all quality characteristics is almost impossible
- Tell developer what is expected in terms of quality characteristics
- Clearly state to the developer your objectives and priorities

### Choice of programming language

**Language classes**

- First generation
  - Low level languages developed in the early 1950s
  - Machine and assembly languages mostly
- Second generation
  - Static high level languages (Fortran, Cobol, Algol, Basic)
  - Programmer has no direct control over machine level operations
  - All memory allocation must be known at compile-time (no dynamic allocations)
  - Good: broad usage, large software library, wide acceptance
  - Bad: poor data typing, No argument passing
- Third generation (late 1960s)
  - Structured/limited dynamic hi-level languages
  - Block structured, strong procedural, complex data structures and abstract data types
  - Object oriented languages (Java, C++)
  - All memory management is carried out during program execution (statement may cause allocation or deallocation)
- Fourth generation (late 1980s to present)
  - Usually non-procedural (provides *what* results to be achieved not *how* to achieve it)
  - User friendly (easy to understand)
  - Non-professionals can obtain results with it (simple and easy to change)
  - Program size is orders of magnitude lower
    - Prototype can be created and modified quickly
    - Ease of understanding the code
    - Easy to debug
  - Examples include: SQL, report generators, graphic languages, specification languages
  - Impacts on maintenance
    - Increased productivity: more rapid change implementation
    - Cost reduction: due to increased productivity
    - Ease of understanding: property of languages of this class
    - Automatic documentation: large portion of documentation is automatically generated
    - Reduction in workload: end-user implementation allows reduction of workload for maintenance personnel
  - Weaknesses of fourth generation languages
    - Application specific: usually target a specific domain
    - Hyped ease of use: easy use by end-user may lead to unmaintainable software
    - Poor design: easy use by the end-user may lead to poor design of the software

**Application area**

- Numeric/scientific: generally dealt with computation on single variable or arrays
- Business data processing: primarily concerned with processing files and records with complex data structures
- Military: numeric/scientific computation with complex data structures in real-time systems
- AI: arbitrary recursion on a list structure

**Engineering features**

- Ease of design-to-code translation: how easily a program language mirrors the design representation
  - Sophisticated data structures such as records and user-defined data types
  - Specialized I/O
  - Object oriented constructs
  - Source code portability (dialect, ISO/ANSI, OS calls supported)
- Source code transported from one platform to another
  - Bit manipulations necessary
  - Availability of supporting tools (debugger, formatter, etc.)

**Psychological features**

- Focus on human concerns such as ease of use and simplicity of learning
  - Uniformity: the degree to which a language uses consistent notation, applies arbitrary restrictions and supports syntactic/semantic exceptions
  - Ambiguity: indicates the difference between the way a human and computer interprets an expression

**Language features**

- Readability: how easy a program is to read and understand
  - Naming convention: variables/identifier/function names
  - Use of user-defined data types
  - Macroscopic structures (if-then-else, while, etc.)
- Control of side-effect: allows features to control side-effects
- Data abstraction: hiding unnecessary details of data and functions
- Dynamic memory allocation
- Exception handling: provides to handle exception values, such as `ValueOutOfRange`, `IndexError` rather than just halt execution
- Consistency checks
  - Level of type consistency check in arithmetic operations
  - Strong type checking (only operations of same type allowed)
  - Truthy/Falsy values (`x=5+yes`) yields 6 if `yes==true` otherwise yields 5

### Using quality enhancing techniques

**Modularization**

- Dividing the program into a set of modules which put together will satisfy the problem
- Advantages:
  - Localization of change: no need to change entire program
  - Features are added with new modules
  - Errors are easier to locate

**Structured techniques**

- New systems
  - Structured analysis and specification
  - Data flow oriented: functional modeling approach uses the concept of functional abstraction
  - Data structure oriented: entity-relationship diagram
  - Structured design: DFD to PSD conversion
  - Data structured design
  - Structured programming: takes the concepts of modularization further into module interactions
- Old systems
  - Spare parts approach: replace whole module (need not to know details of the code)
  - Structurally retrofit: transform unstructured code into structured code with help from automated tools
  - Reformatting: sometimes is enough to improve structure without risky rewriting

**Reuse: use of existing and tested code**

- Advantages
  - More reliable software
  - Overall risk is reduced
  - Cost saving
  - Time saving
  - Enforcement or organizational standards
- Disadvantages
  - Initialization cost (creating components and cataloguing) qualification necessary
  - Some studies suggest that break-even may occur after 2-3 years
  - Maintenance of components
  - Classification may not be trivial (generalization necessary)

- Reuse driven software development process
  - Outline system requirements
    - Search for reusable requirement components
    - Modify the requirements according to the discovered components
  - Architectural design
    - Search for reusable design components
    - Specify system components based on reusable components
    - Search for reusable code components
  - Implement the code
- Levels of reusability
  - Application system reuse: whole system may be reused
  - Subsystem reuse: major subsystem of an application may be reused
  - Module and object reuse: component of a system reflecting a collection of functions reused
  - Function reuse: a single function may be reused
- Generalize for greater reusability
  - Name generalization: choose a neutral name rather then reflection of specific application area
  - Operation generalization: adding some operations or removing some which are application specific
  - Exception generalization: check each component to see what exceptions it might generate and include theses exceptions in the component interface

**Use of templates/macros**

> Class templates allow us to use a single class of function that operates on many types instead of creating a separate class of function for each type

```C
// Minimum function for integers
int min(int a, int b) {
  return (a < b) ? a:b;
}

// Minimum function for long
long min(long a, long b) {
  return (a < b) ? a:b;
}

// Build a function template to specify it once and create type specific instances
template<class T>
T min(T a, T b) {
  return (a < b) ? a:b;
}

// Instantiate with the `int` type
min<int>(a, b)
```

```c
template <class T>
class stack {
  T *stackp
  int size
  int index

public:
  T pop(void) {return stackp[--index]}
  void push(T item){stackp[index++] = item}
  stack(int sz) {stackp = new T[size=sz]}
  ~stack() {delete []stackp}
}

stack<int> things(30); // Stack of integers
stack<string> strings(20); //Stack of strings
strings.push("A string");
cout << strings.pop();
```

- Makes code easier to reuse
- Reduces the amount of duplicated code

> Macros are used to replace one text string with another during pre-compilation time

```C
#define NUM_CARDS 52
#define DIM(a) (sizeof(a)/sizeof(a[0]))
```

- Reuse of macros is encouraged
- Makes code more compact
- Careful of pitfalls

```C
#define mult(a,b) a*b

mult(y+1, x+3) // will be replaced as y+1*x+3

#define mult(a,b) ((a)*(b))
mult(y+1, x+3) // will be replaced as (y+1)*(x+3)
```

**Programming style and standards**

- Style (personal choice)
  - Use of consistent and meaningful names
  - Use one statement per line to avoid unnecessary complexity
- Good formatting of the program
  - Show logical structure of the program
- Commenting
  - Header: module name, description, author, date of code, modifications
  - Body: comment important blocks of code
- Team standards: typically imposed by organizations and reviewed by SQA teams
  - Functions should have 50 or fewer lines
  - Nesting should not exceed three levels
  - Use of `goto` needs approval
  - No more than 5 formal parameters for a subroutine/function

**OO paradigms**

- Decomposition aids comprehension
  - Algorithmic decomposition: process is broken down into subprocesses
  - OO decomposition: system is viewed as a collection of objects which communicate through messages
- Techniques in software maintenance
  - Use cases
  - Class diagrams
  - Design patterns
  - Object reuse
- Impact on maintenance
  - Less error prone -> less maintenance
  - High reusability (high cohesion and low coupling)
  - Risk associated with complex systems are reduced

## Ways of sustaining maintainability

### Impact analysis

- More important to sustain maintainability
- Handles planning and managing software change and has effect of making changed system more maintainable
  - What is affected by change
  - Where changes are needed
  - How the changes are carried out
- Traditional approaches concentrate on analysis of source code (program slicing)
- Approaches with wider views also look at changes in design and implementation documents

### SQA practices

- Powerful technique for introducing and maintaining software quality
- Up to 20% of cost of development and maintenance should go to SQA
- Code walkthroughs
  - Inspection: 5 roles (reader, moderator, reviewer, author, scribe)/ 3 persons
  - Clear steps (preparation, meeting, follow-up)

**Checkpoint reviews**

- Conducted at the end of each software development activity
- Demonstrates the required procedure performed and software deliverables have been produced

**Acceptance reviews**

- Special checkpoint at the end of a software development project before delivery to customer
- Denotes the transfer of responsibility from the developer to the maintainer
  - Acceptance criteria must be clearly defined
  - Items: All documentation (requirements to user manuals)
  - Tests: change exercise
  - Bebugging: reliability (9/10 seed errors found within 5 hours)

**Periodic maintenance audits**

- Done to ensure the quality of the operational software
- If deterioration is detected, measure must be taken to enhance the quality
- Same quality checks and audits can be performed as during the check point reviews
- Compared with previous results
