# Lecture 15: software inspections

- A powerful way to improve the quality and productivity of the SW process
- An inspection is a **peer review** of a programmers work
  - Help find problems
  - Improve quality of programs
  - Recognize and fix problems early
  - Motivate better work
- Errors start from an early misconception that is repeated through the software lifecycle
  - Brief inspections by competent co-workers can invariably reveal mistakes
  - When work is critically examined by peers, programmers are encouraged to work more carefully
- Inspections is *not* a replacement for software testing
- *All* software organizations should use inspections on all major aspects of work

## Types of reviews

### Reviews

**Management and technical reviews**

- Generally conducted for management to provide them information for management action

| Objective | Management review | Technical review |
| --------------- | --------------- | --------------- |
| Ensure progress | X |  |
| Recommend corrective action | X |  |
| Ensure proper allocation of resources | X |  |
| Evaluate conformance to specifications and plan |  | X |
| Ensure change integrity | | X |

**Inspections and walkthroughs**

- Are peer evaluations aimed at improving work quality
- Inspections examine work technically
  - Provide producer with independent assessment
  - Identify which product areas may need improvement
- Walkthroughs are a less formal meeting conducted in an educational format
- Inspections have a formal format with
  - Specified attendees
  - Data reported on results

| Objective | Software inspection | Walkthrough |
| --------------- | --------------- | --------------- |
| Detect and identify defects | X |  |
| Verify resolution | X |  |
| Detect defects |  | X |
| Examine alternatives |  | X |
| Forum for learning |  | X |

### Work products for inspection

- No limit to what can be inspected, but a question of cost
- If cost of inspection is not warranted, walkthroughs are generally adequate

## Inspection objectives

**Goals**

1) To find errors at the earliest possible point in the development cycle
2) To ensure that the appropriate parties technically agree on the work
3) To verify that the work meets predefined criteria
4) To formally complete a technical task
5) To provide data on the product and the inspection process

**Benefits**

- Ensure that associated workers are technically aware of the product
- Help to build an effective technical team
- Help to utilize the best talents in the organization
- Provide people with a sense of achievement and participation
- Help the participants develop their skills are reviewers

## Basic inspection principles

- The inspection is a formal, structured process
  - A system of checklists
  - Defined roles for participants
- Reviewers are prepared in advance with questions and concerns before inspection starts
- Inspection focuses on *identifying* problem, not solving them
- Inspections are conducted by technical people for technical people
- Inspection data is used
  - To monitor inspection effectiveness
  - Track and manage product quality

## The conduct of inspections

- Should be conducted at every point of the development/maintenance process yielding intermediate products
- Must be planned well in advance
- Must be an explicit part of the project plan

### A basic set of inspections

| Phase | Inspections | Walkthroughs | Technical reviews |
| --------------- | --------------- | --------------- | --------------- |
| Requirements |  | Detailed requirements | Initial requirements |
| Plans | | | Development plan |
| Development | Detailed design/code | Sytem design/high-level design | |
| Publications | | Draft/final publication | |
| Test | | Test implementation | | 

### Inspection participants

- Limit attendance to 5-6 reviewers
- Only technical peers should attend

**Moderator**

- Not the manager of the work of being reviewed (neither are they any of the participants)
  - Inclusion of managers distorts participants' objectivity
  - participants may feel *they* are being reviewed rather than the product
- 

**Producers**

- Person(s) responsible for the work being inspected

**Reviewer**

- Person(s) responsible for inspecting the work

**Recorder**

- Scribe of the inspection meeting

### Preparing for the inspection

1) Producers and their managers decide that the product is ready for inspection
2) Participants are identified, inspection entry criteria are prepared, and supporting materials are produced
3) Moderator opens up meeting with a brief statement of subject being inspected
4) Moderator provides copies of the inspection package to the participants
5) Reviewers individually prepare for the inspection
6) Reviewers record their time and errors identified on the error log form
7) Reviewers submit the log to inspection moderator at or before the inspection meeting

> Experience shows that about three-quarters of the errors found are found during preparation

### The inspection

1) Moderator first checks if all participants are prepared
2) Producers review each major error to
  - Clarify why it is not an error
  - Understand what the reviewers meant
  - Accept it
3) Pertinent data on each error is recorded
4) After all major errors are covered, product is briefly reviewed for other areas of concern or confusion
5) Based on inspection results, moderator decides if re-inspection is needed

### Post inspection

**Re-inspection criteria**

- Inspection rates unusual
  - Inspection time per LOC too short
  - Inspection time per LOC too long
  - Too many errors per programmer hour
  - Too few errors per programmer hour
- Error data out of line
  - Too many minor errors, and too few major errors (preoccupied with details)
  - Too many major errors
  - Unusual error distribution
  - Too low a percent of errors found during preparation
- Other
  - Any module with more than N errors (N is set in the project plan)
  - Any module with persistently high error rates
  - The reviewers suggest a re-inspection
  - The moderator suggests a re-inspection
  - The testers suggest a re-inspection
  - The module contain un-inspected changes

**Actions**

1) Producers fix the identified problems
2) Moderator ensures inspection results are inserted into process DB
3) Management is informed inspection has been successfully completed

## Inspection training

- Moderator training is essential
  - Need a complete grounding in principles and methods of inspection
  - Provides the skills and self-confidence needed to lead a potentially contentious activity
- Participants training is also desirable
  - A competent moderator can be a good substitute if inspections are well-run

## Reports and tracking

- Essential to track inspection completions to ensure they are done as required
- Can learn about effectiveness from a brief study of data gathered

**The inspection report**

- Project
- System name
- Moderator
- Meeting type (overview, re-inspection, requirements, design, code)
- Number of inspections, inspection duration
- Total number of reviewers, inspection prep time
- Total lines inspected, pages of diagrams
- Disposition (accepted, conditional, reinspect)
- Reviewers
- Producers
- Recorder

**The inspection summary**

- Project and system name
- Moderator
- Meeting type (overview, re-inspection, requirements, design, code)
- Majors errors, minor errors (categorized)
- Distribution of errors (who gets a copy)

## Other considerations

- Inspection require intense concentration from participants and can be very tiring
  - Inspection session should generally not exceed 2 hours
  - Inspections involving the same people should not be scheduled back-to-back
- One inspection per day is advisable for any one individual
- Focus on the quality of work rather than the number of errors being found
  - Errors are a fact of life that must be expected
  - Improve methods and tools to reduce or eliminate more prevalent error causes
- Some types of errors are not effectively discovered with inspections
  - Lots of minor errors -> discontinue inspection and have producers check their work

## Initiating an inspection program

**Actions**

1) Select a location and a key project for the initial effort
2) Introduce the concept of inspections to managers and key professionals
3) Form a working team with members determined to
  - Meet training requirements
  - Develop needed forms and procedures
  - Establish an introduction plan
4) If trained moderator is not available, conduct a 2-3 day moderator training class
5) Hold a developer workshop to introduce methods and obtain the support of professionals who will use them
6) Conduct inspections for a couple months
7) Hold a management seminar to emphasize the need to continue inspections
8) Periodically assess the inspection program

**Costs**

- Depends on time of effort spent preparing for and conducting inspections
- Rates differ based on type of product and the skill and experience of people doing them

**Benefits**

- No documented cases of poor outcomes
  - Partly due to people's reluctance to write about project failure
- Inspections that were ineffective generally had errors in the way they were conducted
  - Preparation not adequate
  - Too many people involved
  - Wrong people attended
  - Too much material covered at once
  - Management inattention and schedule pressure
- Inspection can be highly effective and should be used widely
  - An important way to find errors
  - More effective than testing for some types of errors and can find them earlier than testing can

## Future directions

- Inspections are highly cost-effective with quality programs produced today
- Inspections are labor-intensive
  - Each requires the concentrated involvement of a number of talented software professionals
  - Inspections will be needed as long as software remains a human-intensive process
