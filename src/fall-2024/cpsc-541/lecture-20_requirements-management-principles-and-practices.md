# Lecture 20: requirements management principles and practices

## Importance of management

- All project stakeholders must have access to the *same* requirements agreement
- Requirements management involves the following activities
  1) Change control
  2) Version control
  3) Status tracking
  4) Requirements tracing

**Change control**

- Proposing changes
- Analyzing impact
- Making decisions
- Updating requirements documents
- Updating plans
- Measuring requirements volatility

**Version control**

- Defining a version identification scheme
- Identifying requirements document versions
- Identifying individual requirement versions

**Requirements status tracking**

- Defining possible requirements statuses
- Recording the status of each requirement
- Reporting the status distribution of all requirements

**Requirements tracing**

- Defining links to other requirements
- Defining links to other system elements

## Management topics

- Tools, techniques, conventions
- Baselining method
- Requirements status conditions and tracking
- Change proposal, processing, and approval (or rejection)
- Impact analysis
- Effect on plans and commitments

## Version control

- Unique identification of every version is essential
- Version changes whenever a requirement changes
- Revision history is very helpful when "Who?", "When?", and "What?" are included
- Use structured identifier, not a date
  - `{major}.{minor}, draft #`
- Use tools
  -  Word processor's change-tracking features
  - File version control, with check-out/check-in
  - Specialized commercial tools

## Requirements attributes

- Store additional information about each requirement
- Some suggestions
  - Status
  - Date created and version number
  - Author and person responsible for the requirement
  - Origin or rationale behind the requirement
  - Allocated subsystem, product release, and build
  - Priority
  - Risk
  - Criticality
  - Validation method

## Tracking requirements status

- *Proposed*: requirement was requested by a legitimate source
- *Approved*: requirement was analyzed, impact evaluated, and allocated to a baseline
- *Implemented*: code was designed, written, and tested
- *Verified*: requirement was shown to be implemented correctly in the product
- *Deleted*: planned requirement was deleted from the baseline
- *Rejected*: requirement was requested, not approved

## Measuring efforts

- Proposing new and changed requirements
- Evaluating proposed changes
- Updating requirements repository
- Change control board activities
- Communicating changes
- Tracking status
- Tracing (linking)
