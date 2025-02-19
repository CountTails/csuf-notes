# Lecture 12: other quality attributes

## Other important quality attributes

> This section introduces additional quality attributes beyond those covered in depth earlier in the presentation. These attributes frequently arise in software architecture but are often overlooked in standard discussions.

### Variability

- Definition: a special form of modifiability that allows a system and its supporting artifacts (e.g., requirements, test plans, configurations) to support the creation of different variants.
- Relevance:
  - Critical for software product lines, where a core asset must be adaptable across different products.
  - Ensures ease of building and maintaining product variants over time.
- Key considerations:
  - Variability depends on the binding time of variations (compile-time, load-time, runtime).
  - Reducing effort for achieving variability is a design goal.

### Portability

- Definition: the ease with which software built for one platform can be adapted to another.
- Strategies to Enhance Portability:
  - Minimize platform dependencies in code.
  - Isolate dependencies into well-defined modules.
  - Use platform-agnostic execution environments like virtual machines (e.g., JVM).
- Scenarios: a portability scenario may involve measuring the effort required to adapt software to a new platform.

### Development distributability

- Definition: the ability to design software to facilitate distributed development across teams.
- Challenges in distributed development:
  - Coordinating team activities across different locations and time zones.
  - Managing dependencies between modules developed by different teams.
- Architectural strategies:
  - Minimize coordination needs between teams by clearly defining module interfaces.
  - Ensure data model compatibility across different development units.
- Scenarios: evaluating how communication structures and data models align with team distribution.

### Scalability (Elasticity)

- Definition: the ability of a system to handle increased workload efficiently.
- Types of scalability:
  - Horizontal scalability (scaling out): Adding more units (e.g., servers in a cluster).
  - Vertical scalability (scaling up): Adding more resources (e.g., more memory or CPU to a server).
- Cloud-specific considerations:
  - Elasticity is a cloud-centric form of scalability that allows systems to dynamically allocate or remove resources.
  - Large-scale cloud providers manage thousands of physical machines to enable elasticity.
- Key challenges: ensuring that additional resources lead to measurable improvements in performance.

### Deployability

- Definition: the ease with which software can be distributed and installed on target systems.
- Key questions in deployment:
  - How does the software arrive at the host system? (push vs pull updates)
  - Can it be integrated without downtime?
  - How is it updated in mobile environments with limited bandwidth?
- Deployment considerations:
  - Different update strategies (e.g., full redeployment vs incremental updates).
  - Deployment scenarios consider efficiency, risk, and integration impact.

### Mobility

- Definition: the challenges related to running software on mobile platforms and handling device movement.
- Key concerns:
  - Hardware constraints (e.g., screen size, input methods, battery life).
  - Bandwidth limitations affecting data synchronization.
  - Reconnection issues after periods of disconnection.
- Scenarios: designing for software that must support multiple device types and operating conditions.

### Monitorability

- Definition: the ability for operations teams to observe system performance and detect potential failures.
- Key metrics to monitor:
  - Queue lengths
  - Average transaction times
  - Component health status.
- Architectural considerations:
  - Implementing logging and real-time monitoring tools.
  - Ensuring visibility of critical system operations to prevent failures.

### Safety

- Definition: the ability of a system to avoid states that could cause harm to users or the environment.
- Notable Example: in 2009, a remote software command at the Shushenskaya hydroelectric plant accidentally activated an unused turbine, leading to catastrophic failure and loss of life.
- Safety vs reliability: a system can be reliable but unsafe (e.g., software following a faulty specification that leads to hazards).
- Engineering for safety:
  - Failure mode analysis and hazard detection.
  - Architectural tactics that focus on preventing, detecting, and recovering from failures.

## Other Categories of Quality Attributes

> Beyond traditional product attributes, software architecture must consider:

### Conceptual Integrity of the Architecture

- Ensures consistency in design, reducing errors due to confusion.
- Encourages using one standard approach for key design choices (e.g., messaging, error handling).

### Quality in Use (ISO/IEC 25010)

- Includes factors that affect user experience and business value:
  - Effectiveness: does the system meet user needs?
  - Efficiency: how much effort and time does development require?
  - Freedom from risk: does the system minimize economic, safety, or environmental risks?

### Marketability

- Public perception of an architecture can be as important as its technical merits.
- Example: Many companies feel pressure to adopt cloud-based architectures for marketability, even if it's not the best technical choice.

## Software Quality Attributes and System Quality Attributes

- Software must interact with system-level concerns like:
  - Size and weight
  - Energy consumption
  - Power efficiency.
- Example: green computing is now a major architectural concern.
  - Data centers consume 2% of all US electricity.
  - Companies are exploring offshore data servers and alternative energy sources.

## Dealing with "X-Ability": Bringing a New Quality Attribute into the Fold

When an architect encounters a new quality attribute that lacks established best practices, they should:

1) Capture scenarios: interview stakeholders to define specific needs and challenges.
2) Assemble design approaches: study existing patterns and industry examples.
3) Model the quality attribute: identify key parameters that affect the attribute.
4) Assemble a set of tactics: define architectural decisions that improve the quality attribute.
5) Construct a design checklist: develop review questions to evaluate architectural choices.

