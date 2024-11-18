# Lecture 23: requirements management tools

## What they do

- Store requirements in a database (statement + attributes)
- Automatically control versions
- Allow to add traceability information
- Make some use of traceability information
  - At least marking suspected links
  - Maybe also reporting on requirements that were not traced to anything else

## The benefits of using tools

- Generate (or update) textual documents from the database
- Provide some possibilities for importing requirements from text
- Generate some other reports (e.g. about statuses of requirements)
- Put database online so different team members can access it easily, with no need of creating copies of data
- Provide means for discussion about requirements
- Automatically send notifications
- Enforce access control (e.g. changes are only by designated people)
- Both customers and developers may stop to consider requirements as "paper work" and start to see them as a project asset

## The limitations of using tools

- Tools are for requirements management, not for requirements development
  - Cannot help with elicitation, validations, and negotiating requirements
  - Not recommended to capture requirements directly into a tool
  - Better when requirements are base-lined
- Do not expect tools to compensate for a lack of discipline, process or expertise
- Expensive (several thousands of USD)

## Types of tools

**Database centric**

- Store all requirements, attributes and traceability information in a database
- Can import requirements from various source documents, but they reside in the database

**Document centric**

- Treat a document created using a word processing program as the primary container for the requirements
- Attributes and traceability information are stored in an additional database

**Major requirements management tools**

| Feature | DOORS | Caliber-RM | RequisitePro |
| --------------- | --------------- | --------------- | --------------- |
| Parses a source document to load requirements into database | Yes | Yes | Yes |
| Imports requirements from Word tables into database | Yes | Yes | No |
| Incoporates non-textual objects such as Excel worksheets and images into database | Yes | Yes | No |
| Synchronizes textual SRS with database contents | No | No | Yes |
| Defines different attributes for different types of requirements and set attribute values for indivudal requirements | Yes | Yes | Yes |
| Defines requirement baselines | Yes | No | No |
| Notifies affected project participants by e-mail about requirements changes | Yes | Yes | No |
| Defines traceability relationships or links between individual requirements and between requirements and other system elements | Yes | Yes | Yes |
| Tailors usability options | Yes | Yes | Yes |
| Includes learning aids, such as a tutorial and/or sample projects | Yes | Yes | Yes |
| Integrates with other tools, such as testing, design, and project management | Yes | Yes | Yes |
| Defines users and groups and their access privileges | Yes | Yes | Yes |
| Enables threaded discussions on requirements | No | Yes | Yes |
| Includes web interface for database query, discusion, and perhaps updating requirement attributes | Yes | Yes | Yes |
| Includes built in change proposal system | Yes | No | No |
| Includes hardcopy user manuals | Yes | Yes | Yes |

## Implementation of tools

**Selection of tools**

- Select a tool based on platform, pricing, access mode, and type
- Possible steps of choosing a tool are given in the book

**Changing the culture**

- Changing the company culture and process to accept the tool is much harder
- One approach is to use the tools once the SRS is more or less clear and stabilized
- More approaches discussed in the book
