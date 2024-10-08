# Lecture 11: writing excellent requirements

## Characteristics of excellent requirements

- **Complete**: nothing is missing; no TBDs
- **Consistent**: does not conflict with other requirements
- **Correct**: accurately states a customer or external need
- **Feasible**: can be implemented within known constraints
- **Modifiable**: can be easily changed, with history, when necessary
- **Necessary**: documents something customers really need
- **Prioritized**: ranked as to importance of inclusion in product
- **Traceable**: can be linked to system requirements, and to designs, code, and tests
- **Unambiguous**: has only one possible meaning
- **Verifiable**: correct implementation can be determined by testing, inspection, analysis, or demonstration

## Guidelines for writing requirements

### Writing clear requirements

- Evaluate from the developer's perspective
- Document in a hierarchical, structure form
- Keep sentences and paragraphs short and simple
  - Avoid long narrative paragraphs
  - Use proper grammar, spelling, and punctuation
  - Use vocabulary of the business domain
- Document both expected behaviors and exception conditions

### Writing quality requirements

- Write requirements at fine granularity
  - Decompose requirements until each is discretely testable
  - Avoid bullet list and long narrative paragraphs
  - "and" and "or" suggest multiple requirements are combined
  - Label each requirement
  - Organize similar requirements into tables
- Be precise and specific, not vague and ambiguous
  - use **shall** or **must** not "should", "might", or "may"
  - Avoid ambiguous words

### Structure for functional requirements

**From system's perspective**

| Part | Format |
| -------------- | --------------- |
| Conditions | When {some conditions are true}... |
| Result | ...the system shall {do something}... |
| Qualifier | ... {response time or quality statement} |

> When the Patron indicates that he does not wish to order any more food items, the system shall display the food items ordered, the individual food item prices, and the payment amount within 1 second.

**From user's perspective**

| Part | Format |
| -------------- | --------------- |
| User type | The {user class name}... |
| Result type | ...shall be able to {verb} |
| Object | ...to something... |
| Qualifier | ... {response time or quality statement} |

> The Patron shall be able to reorder any meal he had ordered within the previous six months, provided that all food items in that order are available on the menu for the meal date

### Details in requirements

- Less details are required when there is
  - Extensive customer involvement
  - Considerable domain expertise amongst developers
  - Precedents are available
  - Packaged solutions available for use
- More details are required when
  - Outsourcing development
  - Team is geographically dispersed
  - Testing will be based on requirements
  - Accurate estimates are needed
  - Requirements traceability is needed

### Some weak words to avoid

- **Extremes**: minimize, maximize, optimize
- **UI descriptions**: user-friendly, rapid, easy, simple, intuitive, efficient, flexible, robust
- **Transitions**: seamless, transparent, graceful
- **Tech hype**: improved, state-of-the-art, superior
- **Good enough**: sufficient, adequate, at least
- **Unclear action**: reasonable, where appropriate, to the extent possible, if necessary
- **Non-numeric amounts**: few, several, some, many
- **Extraneous information**: etc., including, and/or

### Requirements ambiguity

**Ambiguity of reference**

- Statements that can refer to more than one thing
- Often caused by misused pronouns
- Can be created by definite articles where uniqueness is not guaranteed

**Scope of action**

- TBD

**Omissions**

- Causes without effects
- Effects without causes
- Complete omissions
- Missing causes of effects
- Implicit or assumed cases

| Requirement with omission | Requirement without omission |
| ------------------------- | ---------------------------- |
| The system shall display the user's defined bookmarks in a collapsible hierarchical tree structure | The system shall display the user's defined bookmarks in a collapsible **and expandable** hierarchical tree structure |

**Ambiguous logic**

- Nested ands, ors, nots
- Compound operators
- Missing "else"
- Implicit logical connectors

**Negation**

- Unnecessary negation
- Scope of negation
- Double or triple negation

| Requirement with negation | Requirement without negation |
| ------------------------- | ---------------------------- |
| All users with three or more account should not be migrated | The system shall migrate only users having fewer than three accounts |
| The security module will not allow access by user who do not have a valid userid and password | The security module shall only allow access by users who have a valid userid and password |

**Ambiguous statements**

- Synonyms
  - Use terms consistently
  - Define terms in a glossary
- Ambiguous precedents
  - Pronouns: make the antecedent crystal clear
  - Adverbs
    - Provide a *reasonably* predictable end-user experience
    - Offer *significantly* better download times
    - Optimize upload and download to perform *quickly*
    - Downloading should complete in *approximately* 15 minutes
    - Exposing information *appropriately*...
    - *Generally* incurs a per-unit cost ...
    - To enable remedial action to be initiated in a *timely* manner...
    - ...as *expediently* as possible ...
    - *Occasionally* (not very *frequently*) there will be an error condition
- Ambiguous timing
- Language pitfalls
  - i.e and e.g.
    - i.e. = "that is"
    - e.g. = "for example"
    - Better to use English
  - Avoid the A/B construct
    - "Prior to operator intervention, a snapshot of this data should be recorded in an **audit/history** table"
      - Is A and B the same thing?
      - Does A and B have to both occur?
      - Or does only one of A or B have to occur?
      - Are A and B opposite actions?
      - Is this a division problem?
    - Too many interpretation, the reader will need to decide (possibly incorrectly)

**Poor organization**

- Mixed causes and effects
- Random sequence
- Fragmented requirements

**Boundary ambiguity**

| Requirement with boundary ambiguity | Requirement without boundary ambiguity |
| ----------------------------------- | -------------------------------------- |
| If the amount of the cash refund is less than $50, the system shall open the cash register drawer. If the amount of the cash refund is more then $50, and the user is not a supervisor, the system shall display a message: "Call a supervisor for this transaction." | If the amount of the cash refund is less than **or equal to** $50, the system shall open the cash register drawer. If the amount of the cash refund is more then $50, and the user is not a supervisor, the system shall display a message: "Call a supervisor for this transaction." |

## Rewriting requirements

### Example 1

> The background task manager should provide status messages at regular intervals not less than every 60 seconds

- What status message should be displayed?
- What does "provide" mean?
- Desired timing interval is phrased *very* ambiguously

> 1. The Background Task Manager (BTM) shall display status messages in a designated area of the user interface 

> 1.1 The BTM shall update the messages every 60 plus or minus 10 seconds after background task processing begins and shall remain visible continuously

> 1.2 Whenever communication with the background task processing is possible, the BTM shall display the percent completed of the background task
  
> 1.3 The BTM shall display a "done" message when the background task is completed

> 1.4 The BTM shall display an error message if the background task has stalled

### Example 2

> The XML editor shall switch between displaying and hiding non-printing characters instantaneously

- What are non-printing characters?
- Instantaneously is unfeasible
- What causes the switch?
- What is the scope of the switch?

> The user shall be able to toggle between displaying and hiding all XML tags in the document being edited with the activation of a specific triggering condition. The display shall change in 0.1 seconds or less.

### Example 3

> The XML parser shall produce a markup error report which allows quick resolution of errors when used by XML novices

- What is included in the error report?
- How is XML novice distinguished?
- Does quick resolution refer to a system or manual process?

> After the XML parser has completely parsed a file, it shall produce an error report that contains the line number and text of any XML errors found in the parsed file and a description of each error found. If no errors are found, the parser shall not produce an error report.
