# Lecture 10: software quality assurance

## Quality management

**What is quality management**

- Quality is a characteristic or attribute of something
  - It is measurable
  - It can be compared to known standards
- Software quality encompasses design and conformance
  - Quality of design: focuses on requirements, specification, and design of a system
  - Quality of conformance: focuses primarily around implementation
- User satisfaction is gained with 
  - A compliant product
  - Good quality
  - Delivered within budget and schedule
- Quality control (AKA variation control)
  - Involves a series of inspections, reviews, and tests
  - Ensures each work product meets the requirements placed upon it
- Quality assurance
  - A set of auditing and reporting functions
  - Assesses effectiveness and completeness of quality control activities
  - Aims to provide management with data to be informed about product quality
- Quality management is an umbrella activity applied throughout the software process
  - Requires a SQA process
  - Specific QA and QC tasks
  - Effective software engineering practices
  - Control of all software work products and changes made to them
  - Procedure to ensure compliance with software development standards
  - Measuring and reporting mechanisms

**Software quality assurance**

- Critical challenge: a way for ordinary people to review the work of experts
- The best designer go to product development instead of SQA
- SQA has methods that permit non-developers to review the work of developers
- The role involves:
  - Monitoring methods and standards used by software experts
  - Verifying the methods were applied properly
- SQA expertise includes:
  - Statistical methods
  - Quality control principles
  - The software process
  - An ability to deal with people in contentious situations
- SQA people can fill the role *without* being software design experts
- "What is not tracked is not done"
  - Tracking is the role of SQA
  - SQA is a management tools that must be used properly to be effective
  - Before establishing SQA, an organization must determine how important quality is to them
  - SQA assures management that the officially established process is being followed
- SQA ensures 
  - Appropriate software methodology is in place
  - Projects use standards and procedures in their work
  - Independent reviews and audits are conducted
  - Documentation supports maintenance and enhancement
  - Mechanisms are in place to control changes
  - Testing is emphasized in all high-risk product areas
  - Each software tasks is satisfactorily completed before moving on
  - Deviations from standards and procedures are exposed as soon as possible
  - Projects are auditable be external professionals
  - Quality control work is itself performed against establish standards
  - The SQA plan and software development plan are compatible

**Benefits**

- Software is enormously impactful and will only be more so in the future
- Ensuring that critical systems work starts with ensuring they are built right

**Needs**

- Independent checks are needed because people are humans
- With software, who and how checks are done matters more than if they are needed

**Goals**

- Broadly speaking: 
  1) Improve software quality by monitoring the software and development process that builds it
  2) Ensure full compliance with established standards and procedures
  3) Bring any inadequacies in product, process, or standards to the attention of management so they may be fixed
- SQA does not produce quality products or make quality plans
- SQA does audit quality actions and alerts management to deviations
- Effective SQA
  - Works closely with development
  - Understands plans
  - Can verify execution and monitor performance
- SQA can be ineffective if
  - Development people view SQA as the enemy
  - SQA does not have an attitude of cooperation and support

## The role of SQA

- People who are responsible for software projects can be responsible for quality

**Responsibilities**

- SQA is effective when
  - They report through an independent management chain
  - They are properly staffed with competent professionals
  - They see their role as supporting development and maintenance personnel in improving product quality
- SQA can remove major inhibitors to producing quality software when they are effective
- SQA is responsible for
  - Reviewing all development and quality plans for completeness
  - Participating as inspection moderators in design and code inspections
  - Ensuring all test plans adhere to standards
  - Reviewing a significant sample of all test results to determine adherence to plans
  - Participating in project quarterly and phase reviews 
  - Registering non-concurrence if standards and procedures have not been reasonably met

**Functions**

- Quality assurance practices
- Software project planning evaluation
- Requirements evaluation
- Evaluation of the design process
- Evaluation of coding practices
- Evaluating the software integration and test process
- In-process evaluation of management and project control process
- Tailoring of quality assurance procedures

**Reporting**

- SQA must **not** be under the software development manager
- SQA should report to a higher level so
  - They have some chance to influence priorities
  - They may be able to obtain resources and time to fix key problems
- Reporting level decision must be made for each organization

## Launching an SQA program

- Establishing need
  - Secure top management agreement on goals
  - Senior managers must resolve SQA issues to allow them to be effective
- Launching the program
  1) Initiate the program
  2) Identify SQA issues
  3) Write the SQA plan
  4) Establish standards
  5) Establish the SQA function
  6) Conduct training and promote the SQA program
  7) Implement the SQA plan
  8) Evaluate the SQA plan
- Sampling
  - Generally not practical to review every development action of product item
  - Plan should specify a statistically sound sampling approach
- Sampling methods
  - Ensure all required design and code inspections are performed and participate in a select set
  - Review inspection reports and analyze them outside established control limits
  - Ensure all required tests are performed and test reports are produced
  - Examine a selected set of test reports for accuracy and completeness
  - Review all module test results and further study data on those modules with test histories that are outside established control limits

## The SQA plan

- Every development and maintenance project has one that specifies
  - Goals
  - Tasks to be performed
  - Standards against which development work is to be measured
  - Procedures and organizational structure
- The section on standards, practices, and conventions should have
  - Documentation standards
  - Logic structure standards
  - Coding standards
  - Commentary standards
- The section on reviews and audits should
  - Describe technical audits to be conducted
  - Describe managerial audits to be conducted

## SQA considerations

- Common reasons for failure
  - SQA is not staffed with people of sufficient knowledge or experience
  - SQA management is not capable of negotiating with development
  - Senior management often stands with development over SQA
  - SQA operates without suitably documented or approved development standards
  - Development groups rarely produce verifiable quality plans

## SQA people

- Getting good people into SQA is one of the most difficult problems software managers face
- Can try promoting development managers from SQA
- Requires potential managers to spend 6-12 months in SQA before being promoted to their home department
- Good people isn't enough on its own to make SQA effective, they must also have full management backing

## Independent verification and validation

- DoD contracts commonly have an independent verification and validation (IV&V) organization involved
  - Also monitors development or maintenance performance
  - The role is *different* from SQA
- SQA is a tool for development management
  - Monitors its own organization
  - Ensures established standards and procedures are followed
- IV&V does the same, but *for the customer*
  - Ensures customer needs are reflected in the work
  - Does not duplicate work of ineffective SQA and does not try to replace it
  - Ensures the right skills and attitude are in place
  - Looks beyond standards and procedures to see if first class software work is being done and risks and feasibility issues are being addressed
