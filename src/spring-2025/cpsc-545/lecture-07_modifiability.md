# Lecture 7: modifiability

## What is modifiability?

- Change happens
  - Most of the cost of a typical software system occurs after it has been initially released
  - Changes include adding new features, changing existing ones, or retiring older ones
  - Changes occur to fix defects, tighten security, or improve performance
  - Changes enhance the user's experience
  - Changes embrace new technologies, platforms, protocols, and standards
  - Changes make systems work together, even if they were never designed to
- Modifiability is about change and the cost and risk of making changes
- To plan for modifiability, an architect must consider
  - What can change?
  - What is the likelihood of change?
  - When is the change made and who makes it?
  - What is the cost of the change?
    - Cost of introducing mechanisms to make the system modifiable
    - Cost of making the modification using those mechanisms

## Modifiability general scenario

- **Source of stimulus**: specifies who makes the change: a developer, a system admin, or an end user
- **Stimulus**: specifies the change to be made: addition, modification, or deletion of a function or adjustments to qualities of a system
- **Artifact**: specifies what is to be changed, such as specific components or modules, or the system's platform, UI, environment and interoperating systems
- **Environment**: specifies when the change can be made: at design time, compile time, build time, initiation time, or runtime
- **Response**: make the change, test it, and deploy it
- **Response measure**: Time and/or cost to make the change are the most common. Others include extent of changes, such of number of new defects introduced or effect on other quality attributes

## Tactics for modifiability

- These tactics control modifiability by
  - Controlling the complexity of making changes
  - Reducing the time and cost to make changes
- A few things to understand about modifiability
  - Low coupling is good
  - High cohesion is good
  - Smaller sized modules are good
    - Splitting modules reduces the cost to make modifications to the module being split
  - Deferred binding time of modifications is preferred
    - Late binding is preferable
    - Consider cost of preparing the architecture for late binding

![Modifiability tactics](./figures/modifiability-tactics.md)

## Design checklist for modifiability

### Allocation of responsibilities

- Determine which changes or category of changes are likely to occur through consideration of changes in technical, legal, social, business, and customer forces. For each potential change or category of changes
  - Determine the responsibilities that would need to be added, modified, or deleted to make the change
  - Determine what responsibilities are impacted by the change
  - Determine an allocation of responsibilities to modules that places, as much as possible, responsibilities that will be changed (or impacted by the change) together in the same module, and place responsibilities that will be changed at different times in separate modules

### Coordination model

- Determine which functionality or quality attribute can be changed at runtime and how this affects coordination
  - For example, will the information being communicated change at runtime?
  - Or will the communication protocol change at runtime?
  - If so, ensure that such changes affect a small number set of modules
- Determine which devices, protocols, and communication paths used for coordination are likely to change. Ensure that the impact of changes will be limited to a small set of modules
- For those elements for which modifiability is a concern, use a coordination model that reduces coupling such as publish-subscribe, defer bindings such as enterprise service bus, or restricts dependencies such as broadcast

### Data model

- Determine which changes (or categories of changes) to the date abstractions, their operations, or their properties and likely to occur
  - Consider if the changes will involve their creation, initialization, persistence, manipulation, translation, or destruction
- For each change or category of change, determine if the changes will be made by an end user, a system admin, or a developer. For changes made by an end user or system admin, ensure that the necessary attributes are visible to that user and that the user has the correct privileges to modify the data, its operations, or its properties
- For each potential change or category of change
  - Determine which data abstractions would need to be added, modified, or deleted to make the change
  - Determine whether there would be any changes to the creation, initialization, persistence, manipulation, translation, or destruction or these data abstractions
  - Determine which other data abstractions are impacted by the change. For these additional data abstractions, determine whether the impact would be on the operations, their properties, their creation, initialization, persistence, manipulation, translation, or destruction
  - Ensure an allocation of data abstractions that minimizes the number and severity of modifications to the abstractions by the potential change
- Design your data model so that items allocated to each element of the data model are likely to change together

### Mapping among architectural elements

- Determine if it is desirable to change the way in which functionality is mapped to computational elements at runtime, compile time, design time, or build time
- Determine the extent of modifications necessary to accommodate the addition, deletion, or modification of a function or a quality attribute. This might involve a determination of the following, for example:
  - Execution dependencies
  - Assignment of data to databases
  - Assignment of runtime elements to processes, threads, or processors
- Ensure that such changes are performed with mechanisms that utilize deferred binding of mapping decisions

### Resource management

- Determine how the addition, deletion, or modification of a responsibility or quality attribute will affect resource usage. This involves, for example:
  - Determining what changes might introduce new resources or remove old ones or affect existing resource usage
  - Determining what resource limits will change and how
- Ensure that the resources after the modification are sufficient to meet the system requirements
- Encapsulate all resource managers and ensure that the policies implemented by those resource managers are themselves encapsulated and bindings are deferred to the extend possible

### Binding time

- For each change or category of change
  - Determine the latest time at which the change will need to be made
  - Choose a defer binding mechanism that delivers the appropriate capability at the time chosen
  - Determine the cost of introducing the mechanism and the cost of making changes using the chosen mechanism
  - Do not introduce so many binding choices that change is impeded because the dependencies among the choices are complex and unknown

### Choice of technology

- Determine what modifications are made easier or harder by your technology choices
  - Will you technology choices help to make, test, and deploy modifications?
  - How easy is it to modify your choice of technologies (in case some of these technologies change or become obsolete)?
- Choose your technologies to support the most likely modifications
  - For example, an enterprise service bus makes it easier to change how elements are connected but may introduce vendor lock-in
