# Lecture 1: Software process maturity

## Software maturity framework

> A **software process** is a set of tools, methods, and practices used to produce a software product.

### What is a software process?

- A truly effective software process is:
  - **Predictable**: future performance can be predicted based on past performance.
  - **Consistent**: *cost estimates* and *schedule commitments* are met.
  - **Successful**: resulting software products meet users' *functional and quality* requirements.
- Software process management aims to:
  - Produce software products according to plan.
  - Improve the organization's *capability* to produce better products.

### Statistical process control

- A process under statistical control will
  - Make future performance predictable within established statistical limits
  - Produce *roughly* the same result if the work is repeated in *roughly* the same way.
- A process not under statistical control 
  - Prevents the organization from making sustained progress
  - Yields inconsistent or inadequate results
  - To improve a process, it must be **measured**
- Measuring with the intent to improve can be tricky
  - Measurements must *properly represent* the process being controlled
  - Must be sufficiently well defined are verified to provide a reliable basis for action
  - The mere act of measuring human processes changes them
  - Essential to limit measurements to those with a predefined use

## Software process improvement

The improvement of software development organizations follows 6 steps:

1) Understand the **current status** of the development process
2) Develop a **vision** of the desired process
3) Establish a **list of required process improvement actions** in order of priority
4) Produce a **plan** to accomplish the required actions
5) Commit the resources to **execute the plan**
6) Start over at step 1

### Process maturity levels

- **Initial**: unmanaged, ad-hoc, and chaotic
- **Repeatable**: basic management control
- **Defined**: process is defined
- **Managed**: process is measurable
- **Optimizing**: process in under continuous improvement

These levels are chosen because they

- Represent *actual* historical phases of evolutionary improvement is real software organizations
- Provide a measure of improvement that is *reasonable to achieve* from the prior levels
- Suggest interim improvement goals and progress measures
- Highlight a set of *immediate improvement priorities* once status in the framework is known

### The initial process

#### Identifying an initial process

- The software process is characterized as **ad-hoc** and **chaotic**
- Organization typically operates without
  - Formal procedures
  - Cost estimates
  - Project plans
- Tools are neither well integrated nor used consistently
- Change control is lax; little management exposure or understanding of problems and issues
- Organizations that do operate with formal procedures may not follow them
  - No management mechanism in place to ensure compliance
  - A crisis may cause abandonment of any procedures in place

#### Improving the initial process

Organizations at this level can improve performance by:

- Establishing basic project management controls
  - Ensure effective control of commitments
  - Understand a job's magnitude to anticipate required resources
- Instituting management oversight
  - Review of approve major development plans prior to commitment
  - Regular review process compliance
  - Lack of review may lead to uneven and inadequate process implementation
- Dedicating resources to quality assurance
  - Group charged with **assuring management software work is done the way it is supposed to be done**
  - Requires an independent reporting line to senior management and sufficient resources to monitor performance
  - Should be about 3-6% of the size of the software development organization
- Implementing basic change control
  - Fundamental to business and financial control and technical stability
  - Requirements must be **established and maintained** throughout the development cycle (with reasonable stability)
  - Uncontrolled changes make orderly design, implementation, and testing impossible

### The repeatable process

#### Identifying a repeatable process

- Process provides control over the way the organization *establishes* plans and commitments
- Organizations at this level face major risks when presented with new challenges
  - New tools and methods **will** affect the process
  - Developing a new product is **unknown territory**
  - Major organization changes can be **highly disruptive**

#### How to improve the repeatable process

- Establish a process group (Engineering Process Group or Software Engineering Process Group)
  - A technical resource that focuses exclusively on *improving* the software process
  - Early organization may not dedicate full-time staff to the group as everyone is dedicated to product work
  - Until full-time assignment is possible, little orderly progress can be made on improving the software process
- Establish a software development process architecture (or a development life cycle)
  - Describes the **technical and management activities** required for proper execution
  - Process architecture decomposes the development process into tasks, each of which have:
    1) A defined set of prerequisites
    2) A functional description
    3) Verification procedures
    4) Task completion specifications
  - Decomposition continues until each defined task can be performed by an individual or single management unit
- Introduce a family of software engineering methods and technologies
  - Design and code inspections
  - Formal design methods
  - Library control systems
  - Comprehensive testing methods
  - Prototyping
  - Adoption of modern implementation languages

### The defined process

#### Identifying a defined process

- Organization has laid out a **foundation for major and continued** progress
- A software team undergoing a crisis will **continue to use** the defined process
- The process is now able to be **examined** and actions taken to **improve** it

#### How to improve the defined process

- Establish a minimum set of process measurements
- Establish a process database and the resources to maintain it
- Provide resources to gather and maintain process data (and encourage its use)
- Assess the relative quality of each product and inform management where quality target are not being met

### The managed process

#### Identifying a managed process

- Organizations should expect to make **substantial quality improvements** at this level
- Greatest problem is the *cost of gathering* data for making further improvements
- Now an **enormous** number of *potentially valuable* measurements of the software process

#### How to improve the managed process

- Support automatic gathering of process data
- Use process data both to **analyze** and modify the process to **prevent** problems and **improve** proficiency

### The optimizing process

> In varying degree, this occurs on all levels of process maturity

- This step presents a **paradigm shift**
  - From largely focusing on products 
  - To gathering and analyzing data that directly relates to **product improvement**
- Data is available to *tune* the process itself
- Management can see the major *quality and productivity benefits* the process optimization offers
- Organizations at this level have the means to **identify** weakest elements in a process and **fix them**

#### People in the optimizing process

- Any software process in *dependent on the quality of people* implementing it
- Helps **managers** understand where help is needed and how to provided it
- Lets **professionals** communicate is concise, quantitative terms
- Provides a **framework** for understanding work performance and how to improve it

#### The need for the optimizing process

- Error rates indicate that *the greater volume of code* will mean an **increased risk of errors**
- The *complexity of our systems* will make systems progressively **more difficult to test**
- Process improvement is not only a management issue, but also a *economic* issue as well (more testing is always possible given enough time and money)
- Only the **optimizing process** makes data available to show the costs and benefits of process improvement
- Provides a **foundation for significant advances** in software quality and productivity
