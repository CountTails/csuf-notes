# Lecture 9: reverse engineering

> Reverse engineering is a technique to abstract higher levels of abstractions from source code

## Types of abstraction

- Functional abstraction: also known as procedural abstraction, means the functions from the target system
- Data abstraction: data objects are manipulated by functions
- Process abstraction: means the exact order in which operations are manipulated

## Goals and benefits of reverse engineering

- Aims to facilitate change by allowing software system to be understood in terms of 
  - What it does
  - How it works
  - Its architectural representation (and possible requirements specification)
- Generally helps with the understanding of the target software to benefit maintenance
  - Corrective change: the abstraction of unnecessary detail gives greater insight into parts of the program to be corrected (easier to identify defects and error sources)
  - Adaptive/perfective change: higher abstraction can be used to see how additional requirements fit and also as a basis for new development
  - Preventive change: better understanding gives benefits to future maintenance
  - Software reuse: components resulting from reverse engineering can be reused with some modifications
  - Quality: improves quality of software by building in quality factors (lower complexity, side effects)

## Conditions for reverse engineering

1) Missing or incomplete design/specification
2) Out-of-date, incorrect, or missing documentation
3) Increased program complexity
4) Poorly structured source code
5) Need to translate programs into a different programming language
6) Need to make compatible products
7) Need to migrate between different software or hardware problems
8) Static of increasing bug backlog
9) Decreasing personnel productivity
10) Need for continuous and excessive corrective change
11) Need to extend economic life of a system
12) Need to make similar but non-identical products

## Levels of reverse engineering

**Re-documentation (restructuring)**

- Creation of *semantically equivalent* representation with the same relative abstraction level
- Goals of restructuring
  - Create alternative views of a system
  - Improve the documentation
  - Generate documentation for newly modified program
- Types of restructuring
  - Control-flow driven: involves the imposition of clear control structure within source code and can be intra or inter modular in nature
  - Efficiency driven: involves making functions or algorithms more efficient
  - Adaptation driven: involves changing the coding style in order to adapt a program to a new language or operating system

**Design recovery**

- Entails the identification and extraction of meaningful higher level abstraction from source code
- Can be used as a basis for new development
- Different approaches to design recovery exist

**Specification recovery**

- Involves higher level abstractions beyond the design
- Formal specification and object-oriented modeling

**Re-engineering**

- Recovered higher level abstraction can be a basis for new development
- Involves reverse engineering and then forward engineering

## Design architecture recovery

- Structures which compose software elements, externally visible properties of those elements, and the relationship among them
- Promotes the development of accurate detail and information about the system's architecture and this is done to enhance or include maintenance, re-engineering or reuse
- Expresses how things interact within the system architecture
- Different types of design techniques work of different domains (legacy systems or object-oriented systems)
- Commonly used analysis methods in design recovery technique are structural analysis, dynamic analysis, and static analysis

### Desire

- Method produced at Microelectronics and Computer Technology
- Main focus is to directly address the issues of domain analysis in the context of reverse engineering
- To form a view, recreate design abstractions from source code, available documentation, and domain knowledge from individuals
- Model attempts to weave together the recovered abstractions to help software engineers understand a specific target system
- System attempts to bridge the gap between conceptual abstraction and source code
  - Parser recursively processes a set of files an constructs a relational diagram
  - Data dictionary created from the diagrams
  - Structured relationship are discovered in source code
  - Results are reviewed with an end user

### Reconstruction through design patterns

- Modern software architecture relies heavily on design patterns to facilitate object-oriented programming
- Design patterns play an essential role in comprehension of software re-engineering
- Typically classes that utilize design patterns often encapsulate other classes or behaviors
- Recognition of patterns requires analysis of software's structure and behavior to create abstract views of the source code in a bottom-up manner

## Object oriented reverse engineering

### Implementation/construction and recovery

- Lowest level of abstraction is the actual code, created during the implementation phase of development
- Software maintainer may find themselves without source code for a variety of reasons
  - Binary distributions can be decompiled to recover the majority of source code
  - Converts the byte code contained within binary files into source code

### Elaboration

- The software architecture is created in the elaboration phase of the universal process
- Work products include UML diagrams, architecture documentation and data models
- Existing work products can be used for design recovery
  - Target of this phase is the recovery of the design
  - More difficult to achieve than source code recovery
  - Effective design recovery requires more input than just original byte code distributions
  - Also calls on existing documentation, domain knowledge and personal experience
- Process can be more labor intensive and require addition training to interpret results

### UML recovery from object-oriented source code

- In design recovery
  - Choose the diagrams to represent the output of the RE
  - Choice of UML is not limited
  - UML has 14 diagrams which can either be classified as structural or behavioral
- What to recover from the source code
  - Class diagrams
  - Package diagrams
  - Sequence diagrams

**Manual design recovery**

- Recovery of the class diagram
  - Obtained by analyzing the source code
  - Process in incremental and iterative
  - Identify classes -> recover internal features -> recover relationships among classes
- Recovery of the sequence diagram
  - Shows object interactions arranged in time sequence within the scope of a method
  - Identify object -> Identify constructors -> Identify interactions between objects (in sequential order) -> Identify scope of objects -> Identify conditional branching and loops
- Recovery of the package diagram
  - Decompose the larger system into smaller units called packages
  - Package diagrams show packages of the system with relationships between them
  - Look for keyword namespaces -> List all class declarations and package declarations within the scope of the package

**Automatic design recovery**

- Tools like Visual Studio provide ways to recover design directly from source code

### Inception

- The next level of abstraction up from elaboration
- Represents the highest level of abstraction in the process
- Establishes requirements, vision, and business rules
- Target of this phase is recover the specification
- Work artifacts include requirements specification and vision document

## Reverse engineering tools

- Recover software architecture and design patterns
- Re-document programs and databases
- Restructure/Re-modularize existing systems

### Documentation generators

- Javadoc: parses declarations and documentation comments in source code and produces HTML documentation
- Doxygen: generates documentation from annotated C++ sources and many other programming languages
- RDOC: generates structured HTML documentation for Ruby source

### UML modeling tools

- Objectaid: analyzes Java source code or byte code to build a Java model and then UML diagrams
- Visual Paradigm for UML: generates UML diagrams from source code for systems developed in popular programming languages

### Binary reverse engineering tools

- Disassemblers: binary to assembly code
- Decompilers: binary to HLL source

### Other reverse engineering tools

- AgileJ: reverse engineering tool in an agile environment for program comprehension of code written in Java
- Imagix4D: program comprehension tool for C, C++, and java that provides easier source code analysis of legacy systems
