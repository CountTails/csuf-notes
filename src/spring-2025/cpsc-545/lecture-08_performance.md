# Lecture 8: performance

## What is performance?

- Performance is about time and a software system's ability to meet timing requirements
  - When an event occurs, the system must respond to them in time
  - Characterizing events that can occur (and when they can occur) and the system's time-based response is the essence of discussing performance
- Performance has been the driving factor in system architecture for much of software engineering history
  - Frequently compromises the achievement of all other qualities
  - All systems have performance requirements, even if not explicitly stated
  - Often linked to scalability (increasing a system's capacity for work while still performing well)

## Performance general scenario

- Begins with an event arriving at the system
  - Responding correctly requires resource (including time) to be consumed
  - Simultaneously, the system may be servicing other events
- Arrival pattern of events can be characterized as:
  - Periodic: events that arrive at predictably regular time intervals
  - Stochastic: events arrive according to some probabilistic distribution
  - Sporadic: events arrive according to a pattern that is neither periodic nor stochastic
- System response to the stimulus can be measured by the following:
  - Latency: time between arrival of the stimulus and the system's response to it
  - Deadlines in processing: allowed time to respond
  - Throughput: number of transaction in a unit of time
  - Jitter: Allowable variation in latency
  - Miss rate: number of events *not* processed because system was too busy to respond

| Portion of Scenario | Possible Values |
| ------------------- | --------------- |
| Source | Internal or external to the system |
| Stimulus | Arrival of a periodic, stochastic, or sporadic event |
| Artifact | System or one or more components in the system |
| Environment | Operational mode: normal, emergency, peak load, overload |
| Response | Proess events, change level of service |
| Response measures | Latency, deadline, throughput, jitter, or miss rate |

## Tactics for performance

- Goal of these tactics is to generate a response to an event within some time-based constraint
  - Event can be a single or stream and is the trigger to perform computation
  - Tactics control the time within which a response is generated
- Base contributors to the response time:
  - Processing time: resources consumed during computation, including time
    - Resources behave differently as utilization approaches capacity
  - Blocked time: computation blocked due to contention of needed resource
    - Contention for resources
    - Availability of resources
    - Dependency on other computation

### Control resource demand

- Done by reducing the number of events processed
  - Manage sampling rate
  - Limit event response
  - Prioritize events
  - Reduce overhead
  - Bound execution times
  - Increase resource efficiency

### Manage resource

- If demand for resources is not controllable, management of them can be
  - Increase resources
  - Introduce concurrency
  - Maintain multiple copies of computations
  - Maintain multiple copies of data
  - Bound queue sizes
  - Schedule resources

### Scheduling policies

- A scheduling policy conceptually has two parts: priority assignment and dispatching
  - A high-priority stream can be dispatch only if the resource to which it is assigned is available
- Some common scheduling policies include
  - First-in/first-out
  - Fixed-priority scheduling
    - Semantic importance
    - Deadline monotonic
    - Rate monotonic
  - Dynamic priority scheduling
    - Round-robin
    - Earliest-deadline-first
    - Least-slack-first
  - Static scheduling

## A design checklist for performance

### Allocation of responsibilities

- Determine the system's responsibilities that will involve heavy loading, have time-critical response requirements, are heavily used, or impact portions of the system where heavy loads or time-critical events occur
- For those responsibilities, identify the processing requirements of each responsibility, and determine whether they cause bottlenecks
- Also, identify additional responsibilities to recognize and process requests appropriately, including
  - Responsibilities that result from a thread of control crossing process or processor boundaries
  - Responsibilities to manage the threads of control
    - Allocation and deallocation of threads
    - Maintaining thread pools
  - Responsibilities for scheduling shared resources or managing performance-related artifacts such as queues, buffers, and caches
- For the responsibilities and resources you identified, ensure that the required performance response can be met (perhaps by building a performance model to help in the evaluation)

### Coordination model

- Determine the elements of the system that must coordinate with each other (directly or indirectly) and choose communication and coordination mechanisms that do the following:
  - Support any introduced concurrency, event prioritization, or scheduling strategy
  - Ensure that the required performance response can be delivered
  - Can capture periodic, stochastic, or sporadic event arrivals, as needed
  - Have the appropriate properties of the communication mechanisms

### Data model

- Determine those portions of the data model that will be heavily loaded, have time-critical response requirements, are heavily used, or impact portions of the system where heavy loads or time-critical events occur
- For those data abstractions, determine the following:
  - Whether maintaining multiple copies of key data would benefit performance
  - Whether partitioning data would benefit performance
  - Whether reducing the processing requirements for the creation, initialization, persistence, manipulation, translation, or destruction of the enumerated data abstractions is possible
  - Whether adding resources to reduce bottlenecks for the creation, initialization, persistence, manipulation, translation, or destruction of the enumerated data abstractions is feasible

### Mapping among architectural elements

- Where heavy network loading will occur, determine whether co-locating some components will reduce loading and improve overall efficiency
- Ensure that components with heavy computation requirements are assigned to processors with the most processing capacity
- Determine where introducing concurrency (that is, allocating a piece of functionality to two or more copies of a component running simultaneously) is feasible and has a significant positive effect on performance
- Determine whether the choice of threads of control and their associated responsibilities introduce bottlenecks

### Resource management

- Determine which resources in your system are critical for performance
- For these resources, ensure that they will be monitored and managed under normal and overloaded system operation
  - System elements that need to be aware of, manage, time and other performance-critical resources
  - Process/thread models
  - Prioritization of resources and access to resources
  - Scheduling and locking strategies
  - Deploying additional resources on demand to meet increased loads

### Binding time

- For each element that will be bound after compile time, determine the following
  - Time necessary to complete the binding
  - Additional overhead introduced by using the late binding mechanism
- Ensure that these values do not pose unacceptable performance penalties on the system

### Choice of technology

- Will your choice of technology let you set and meet hard, real-time deadlines?
- Do you know its characteristics under load and its limits?
- Does your choice of technology give you the ability to set the following:
  - Scheduling policy
  - Priorities
  - Policies for reduced demand
  - Allocation of portions of the technology to processors
  - Other performance-related parameters
- Does your choice of technology introduce excessive overhead for heavily used operations?
