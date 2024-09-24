# Lecture 11: software standards

## Software standards

- A standard is a rule or basis for comparison
- Used to asses size, content, value, or quality of an object or activity
- Software uses two kinds of standards
  1) To describe the nature of the object to be produced
  2) To define the way the work is to be performed
- Procedures are similar to standards
  - There may be a standard for software reviews and audits, and a procedure for conducting them
  - The standard specifies the review materials and resulting reports
  - The procedure describes *how* the work is actually to be done
- Standards can be established in many ways

## Definitions

**Authoritative direction**

- Policy: a governing principle stated by the highest authority in the organization
- Regulation: a rule, law, or instruction typically established by some legislative or regulatory body
- Specification: a precise and verifiable description of the characteristics of a product produced by technical experts

**Characterization directives**

- Guideline: a suggest practice, method, or procedure
- Procedure: a defined way to do something
- Standard: A rule or basis for comparison that is used to assess size, content, or value, typically established by common practice or by a designated standards body

**Accomplish directives**

- Convention: a general agreement on practices, methods or procedures
- Method: a regular, orderly procedure or process for performing a task
- Practice: a usual procedure or practice, typically a matter of habit or tacit agreement
- Process: a defined way to perform some activity

## Reasons for software standards

- Needed when many people, products, and tools must co-exist
- Standards help to
  - Establish common support environments
  - Perform integration
  - Conducting system test
- Having a common way of doing tasks makes it 
  - Easier to move between projects
  - Reduces the need for training
  - Permits a uniform method for reviewing work and its status
- Promotes the consistent use of better tools and methods
  - Common coding conventions make it practical for programmers to review each others' work
  - Facilitates design and code inspections
  - Improves the maintainability of the finished project

## Benefits of standards

- Little quantitative support for the use of standards
  - Experienced software managers can cite at least one standard the was key to project success
  - Standards will not make the difference between success and failure, but they clearly help
- Views on key software problems ranked enforcement of standards and procedures as the number one effective solution

## Establishing software standards

- Before establishing
  - Formulate an overall plan
  - Consider available standards and the priority needs of the organization
  - Note project statuses and available staff skills
  - Consider the means for enforcing standards
- Choose standards that
  - Can be implemented in a reasonable time
  - Will provide the most immediate benefit to the organization
- Start by examining current standards and procedure needs
  - Management and planning standards and procedures
    - Configuration management
    - Estimating and costing
    - Software quality assurance
    - Status reporting
  - Development process standards and methods
    - Requirement
    - Design
    - Documentation
    - Coding
    - Integration and test
    - Reviews, walkthroughs, and inspections
  - Tools and process standards
    - Product naming
    - Size and cost measures
    - Defect counting and recording
    - Code entry and editing tools
    - Documentation systems
    - Languages
    - Library system

### Standards development process

1) Establish and standards strategy that defines priorities and recognizes prior work
2) Distribute, review, and maintain this property
3) Select individuals or small working groups to develop the top-priority standards
4) Define areas of applicability, specify the introduction strategy, and propose an enforcement plan
5) Draft standards should be widely distributed and reviewed
6) Revise standards to incorporate review comments and re-review in changes are extensive
7) Implement standards initially in a test environment
8) Review and revise standards based on test experience
9) Implement and enforce standards across defined areas of applicability
10) Evaluate the effectiveness of the standards in actual practice

### Maintaining standards

- Standards must be kept current
  - Modify and adjust them based on experience using and enforcing them
  - Unmaintained standards become *less pertinent* to working conditions and enforcing becomes less practical
  - Ultimately becomes a bureaucratic procedure that takes time without adding value
- Responsibilities of standards maintenance include
  - Stay aware of standards implementation problems
  - Be a source of guidance and advise on using the standard
  - Maintain the standards baseline and control changes
  - Periodically review the standards to ensure their effectiveness and pertinence

### Enforcing standards

- A part of the SQA role
  - Done with a mix of reviews and test
  - Exhaustive reviews are done if monitoring can be done with automated processes
  - Statistical sampling is sufficient unless major problems are encountered
- Exhaustive reviews are advisable for
  - Product plans
  - Delivery commitments
  - Test plans
  - Acceptable tests
  - Configuration management
  - Change control procedures
  - Maintenance plans
  - Requirements walkthroughs
- Exhaustive reviews should be selected carefully since they dictate SQA resources
- Statistical reviews are used for all other standards and procedures

## Standards versus guidelines

- A standard is appropriate when *no further judgement* is needed
- Standardization makes sense when items are arbitrary, must be done uniformly, and their is one clear best alternative
  - May be many possible solutions, with no obvious choice, but must be done the same way be everyone
  - Some standards are essential to business maintenance or technical control
  - Choices may seem arbitrary, but are needed because supporting several different approaches is confusing and expensive
- Standardization is inappropriate when
  - Solutions involve technical judgement
  - No convincing evidence that there is *always* a right way to do something
- In questionable cases, use guidelines or have a standard that has practical escape conventions

