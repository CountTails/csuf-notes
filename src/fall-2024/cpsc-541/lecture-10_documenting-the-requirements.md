# Lecture 10: documenting the requirements

## Specification approaches

**Textual**

- Vision and scope document
- Use case document
- Software requirements specification

**Graphical**

- Structured analysis models
  - Data flow diagrams
  - Entity-relationship diagrams
  - State-transition diagrams
  - Dialog maps
- Object oriented analysis models

**Formal**

- Formal specification languages

## Software requirements specification (SRS)

**Definition**

- A set of precisely stated properties and constraints that a software system must satisfy
- A complete description of the external behavior of a system

**Objectives**

- To achieve agreement regarding the requirements among developers, customers, and other stakeholders
- To provide the basis for design and system testing

**Audiences**

- End users, marketing, and product management
- Project management
- Software, hardware, and systems engineers
- Testing group
- Maintenance and support team

## Course SRS template

### The introduction

**Purpose**

- Delineate the purpose of the SRS document
- Specify the intended audience of the document

**Scope**

- Identify the software products to be produced *by name*
- Explain what the software products will (and will *not* do)
- Describe the application of the software being specified, including relevant benefits, objectives, and goals
- Be consistent with similar statements in higher-level specification

**Definitions, acronyms, and abbreviations**

- Provide the definition of all terms, acronyms, and abbreviations required to properly interpret the SRS

**References**

- Provide a complete list of all documents referenced elsewhere in the SRS
- Identify each document by title, report number, date, and publishing organization
- Specify the sources from which the references can be obtained

**Overview**

- Describe what the rest of the SRS contains
- Explain how the SRS is organized

### Overall description

**Product perspective**

- Describe the context and the origins of the product being specified
  - Follow-on member of existing product family?
  - Replacement for existing system?
  - New or self-contained product?
- If specifying a component of a larger system
  - Relate requirements of larger system to functionality of specified system
  - Identify interfaces between the two

**Product features**

- Summarize the major features the product contains and significant functions it will perform or let the user perform.
- Details provided later, so only a high-level description is needed
- Organize functions to make them understandable to *any* reader

**User classes and characteristics**

- Identify the various user classes you anticipate will use the product
- Describe pertinent characteristics of each user class
- Distinguish favored user classes from those who are less important to satisfy

**Operating environment**

- Describe the operating environment in which the software will operate
  - Hardware platform
  - Operating system and version
  - Other software components or applications that must coexist peacefully

**Design and implementation constraints**

- Describe any issues that will limit the options available to developers

**User documentation**

- List any user documentation components that will be delivered with the software

**Assumptions and dependencies**

- List any assumed factors that could affect requirements list in the SRS
- Identify any dependencies the project has on external factors

### Use cases

- Provide a use case diagram
- Use a template for use case descriptions

### User interfaces

- Describe logical interfaces between software product and users
- Define which software components need a user interface
- Details on user interfaces design should be documented elsewhere

**Hardware interfaces**

- Describe logical and physical characteristics of each interface between the software product and hardware components

**Software interfaces**

- Describe connections between this product and other specific software components
- Identify data items coming into the system and going out, as well as the purpose of each
- Describe services needed and the nature of their communications
- Refer to documentation that describes detailed APIs
- Identify data sharing between software components and any mechanisms that need to be implemented

**Communication interfaces**

- Describe the requirements associated with any communications functions required by the product
- Define any pertinent message formats
- Identify any communication standards that will be used
- Specify any communication security issues, data transfer rates, and synchronization mechanisms

### Other non-functional requirements

**Performance requirements**

- State performance requirements under various circumstances and their rationale
- Specify timing relationships
- Performance requirements should be stated for individual functional requirements or features

**Safety requirements**

- Specify requirements that concern possible loss, damage, or harm that could result from the use of the product
- Define any safeguards, actions to be taken and actions to be prevented
- Define any safety certifications that must be satisfied

**Security requirements**

- Specify any requirements regarding security and privacy surrounding
  - Use of the product
  - Protection of the data used or created by the product
- Define any user identity authentication requirements
- Define any security or privacy certifications that must be satisfied

**Software quality attributes**

- Specify any additional quality characteristics for the product
- Write these with specific, quantitative, verifiable language when possible
- At the very least, clarify relative preferences for various attributes (prioritize easy-of-use over ease-of-learning)

### Other requirements

- List any other requirements not covered elsewhere in the SRS
- Add any new sections that are pertinent to the project

### Data flow diagram

- Attach the data flow diagram
- Should be drawn to at least 2-3 levels

### Functional requirements

- Describe specific features of the software project

### Sequence diagram

- Attach sequence diagram
- Draw interactions among the classes

### Class diagram

- Attach the class diagram
- Identify all classes with relationships, attributes and services
