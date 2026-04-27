# Lecture 14: maintenance tools

## Criteria for selecting tools

**Criteria**

- Capability: tool must be able to support the tasks to be performed
- Features: all features of any potential tool need to be considered
- Cost and benefits: the cost of introducing a new tool must be weighed against the benefits
- Platform: the platform where the tool is mounted need to be considered
- Programming language: important to obtain a tool that supports a programming language that is already an industry standard
- Ease of use: gain quick and wide acceptability among users
- Openness of architecture: ability to integrate a tool with others from different vendors
- Stability of vendor: consider the reputation of the vendor
- Organizational culture: take the work pattern of an organization into consideration

**Categories**

- Program understanding and reverse engineering
- Testing
- Configuration management
- Documentation and complexity measurement

## Tools for program understanding

**Program slicers**

- Divide up a software program by marking all sections of a program that will influence a variable during normal program execution
- Three types of program slicing available
  - Static
  - Dynamic
  - Amorphous
- Commercially available program slicers
  - Sprite
  - Code Surfer
  - Kaversi
  - ConSIT

**Static analyzers**

- Used to analyze different parts of a program (such as modules, procedures, variables, data elements, objects, and classes)
- Commercially available static analyzers
  - Splint
  - Extended Static Checker
  - Cleanscape LintPlus
  - ASTREE

**Dynamic analyzers**

- Used to profile executing software on simulated or actual hardware environments
- Goal is to reduce debugging time by automatically pinpointing and flagging errors as they occur
- Commercially available dynamic analyzers
  - Purify
  - Valgrind

**Data flow analyzers**

- A technique for gathering information about the possible set of values calculated at various points during program execution
- Commercially available data flow analyzers
  - EDSA

**Cross-referencers**

- Generate usage indexes for any given program entity
- Main feature of the indexer is the ability to jump easily to the declaration of any global identifier
- Commercially available cross-referencers
  - LXR Cross Referencer
  - Spxref (a Prolog cross-referencer)
  - Cxref
  - GNU GLOBAL

**Dependency analyzers**

- Assist the maintainer in analyzing and understanding the interrelationships between entities and a program
- Commercially available dependency analyzers
  - Ada system dependency analyzer
  - Class dependency analyzer

**Transformation tools**

- Represent program entities in different formats, usually between graphical and text
- The visual representation can help program understanding and convey information not possible as stand alone text
- Commercially available Transformation tools
  - Stratego/XT

## Tools for testing

- Testing is one of the most expensive and demanding tasks in software development and maintenance
- Depending upon what point during the software life-cycle errors are found, the cost can be staggering
- Testing is the process used to help identify the correctness, completeness, security, and quality of developed computer software
  - Simulators: system to be tested is simulated in a controlled environment and appropriate set of tests are carried out
  - Test case generator: generates data sets to test the functionality of the system undergoing the modification
  - Test path generator: provides potential data flow and control flow paths that are affected by a change
- Commercially available testing tools
  - T-SCOPE
  - Semantic designs test coverage tools
  - McCabe IQ test team edition

## Tools for configuration management

- An essential activity during software maintenance
- Used for identification of the components and changes
  - Control the way changes are made
  - Auditing changes
  - Recording and documenting all activities that have taken place
- Commercially available CM tools
  - Revision control system (RCS)
  - Visual Source Safe
  - IBM Rational ClearCase
  - SCCS (Source Code Control System)

## Tools for documentation

- Software documentation is a critical and sometimes overlooked component of any software system
- Two broad categories of software documentation: user and system
- Broad categories can be broken down further: architecture/design, technical/user/marketing
- Commercially available documentation tools
  - JavaDoc
  - Doxygen
  - Classdoc
  - JSDoc

## Tools for complexity assessment

- Software complexity is a factor that needs to be considered before any change is to be implemented
- The more complex a program is, the more likely it is for the maintainer to make an error when implementing a change
- Commercially available complexity assessment tools
  - McCabe IQ Developers Edition
  - CyVis
  - Journyx
