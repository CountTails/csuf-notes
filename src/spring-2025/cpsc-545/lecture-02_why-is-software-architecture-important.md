# Lecture 2: why is software architecture important?

## Inhibit or enable a system's quality attributes

- A system's architecture determines if it will exhibit its quality attributes
  - For high performance, pay attention to
    - Management time-based behaviors of elements
    - Use of shared resources
    - Frequency and volume of inter-element communication
  - For modifiability, pay attention to
    - Assigning responsibilities to elements
    - Do it in such a way that changes affect a small number of those elements
  - To make a system highly secure
    - Manage and protect inter-element communication
    - Control which elements are allowed to access which information
    - Perhaps introduce specialized elements (like an authorization mechanism)
  - To have the ability to deliver incremental subsets
    - Manage inter-component usage
  - To make elements reusable
    - Restrict inter-element coupling
    - Removal does not include too many attachments in current environment to to be useful
- Architecture alone cannot guarantee functionality or quality for a system
  - Poor downstream design/implementation can undermine architectural design
  - Decisions at all stages affect system quality
  - Quality is not completely a function of an architectural design
- Good architecture is necessary, but not sufficient, to ensure quality
  - Quality attributes must be considered throughout design, implementation, and deployment to achieve them
  - No quality attribute is entirely dependent on its design, implementation, or deployment
  - Satisfactory results come from getting architecture and implementation correct

## Reasoning about and managing change

- Roughly 80% of a typical software system's cost occurs after initial deployment
- Virtually all software system's change over their lifetime to accommodate
  - New features
  - New environments
  - Bug fixes
- Every architecture partitions possible changes into 3 categories
  - Local change: accomplished by modifying a single element
  - Nonlocal change: requires multiple element modifications, but leaves architectural approach in tact
  - Architectural change: affects the fundamental ways elements interact with each other
- Reasoning about the architecture and analyzing it can give insight to make decisions about anticipated changes

## Predicting system qualities

- We can make quality predictions by evaluating a system's architecture
- The earlier you find your problem, the cheaper, easier, and less disruptive it will be to fix

## Enhancing communication among stakeholder

- Represents a common abstraction of the system
  - Most, if not all, stakeholders can use it as a basis for mutual understanding
  - Assists with negotiating, forming consensus, communication among stakeholders
  - Sufficiently abstract that most non-technical people can understand it
  - Can be refined into rich technical specifications for implementation
- Each stakeholder is concerned with different characteristics of the system
  - Users want a fast, reliable, and available system
  - Manager worries if architecture will allow for teams to work together effectively
  - Architect is worried about strategies to achieve all these goals

## Carrying early design decisions

- A manifestation of early design decisions about a system
  - Carries enormous weight with regard to remaining development
  - Earliest point these decisions can be scrutinized
- Constrains the decisions that follow
  - Changing early decisions can cause a ripple effect in terms of additional decisions that must now be changed
  - Refactor or redesigning architecture is sometimes necessary, but is not a task taken on lightly
- Some early decisions embodied by software architecture include
  - Will the system run on one processor or distributed across multiple processors?
  - Will the software be layered? If so, how many layers and what will each one do?
  - Will components communicate synchronously or asynchronously? Will they interact by transferring control, data, or both?
  - Will the system depend on specific OS or HW?
  - Will the information that flows through the system be encrypted or not?
  - What operating system will we use?
  - What communication protocol will we choose?

## Defining constraints on an implementation

- An implementation exhibits an architecture if it conforms to design decisions prescribed by it
  - Implemented as the set of prescribed elements
  - Elements interact with each other in the prescribed fashion
  - Each element fulfills its responsibility to other elements as dictated by the architecture
  - Each of these prescriptions is a constraint on the implementer
- Element builder must be fluent in the specifications for their individual elements
  - May not be aware of technical trade-offs
  - Architecture simply constrains them to meet the trade-offs

## Influencing the organizational structure

- On top of prescribing the structure of the system
  - Architecture can engrave structure into the development project
  - Sometimes, this extends to the entire organization
- There is a method to divide work in a large project
  - Done by assigning different groups to different portions
  - Called the work-breakdown structure of a system
- Architecture is the broadest decomposition of a system and a useful basis for the work-breakdown structure
  - Dictates units of planning, scheduling, and budgets
  - Defines inter-team communication channels
  - Specifies integration and test plans and procedures
- Once agreed upon, significant modifications become very costly
  - Should carry out extensive analysis before settling on an architecture
  - Because so much depends on it

## Enable evolutionary prototyping

- Once defined, architecture can be analyzed and prototyped as a skeletal system
- Skeletal systems build some infrastructure before system functionality is implemented
- Reduces potential risk in the project

## Improving cost and schedule estimates

- Cost and estimate are important tools for project managers
  - Allows them to acquire necessary resources
  - Monitor progress on the project
  - Know if and when a project is in trouble
- Architects help project managers create cost and schedule estimates early in the project life cycle
- Best cost estimates emerge from
  - Top-down estimates (created by architects and project managers)
  - Bottom-up estimates (created by developers)
- More up-front knowledge means more accurate cost and schedule estimates

## Supplying a transferable and reusable model

- The earlier reuse is considered, the greater benefit it can provide
- Code reuse is nice, but reuse of architecture is amazing when faced with systems with similar requirements
- Reusing architectural decisions transfers all the early decisions consequences
- A product line (or family) is a set of software systems built using the same set of reusable assets
  - Product line architects choose an architecture that serves all envisioned members of the product line
  - The architecture defines what is fixed for all members and what is variable between members
  - Represent a powerful approach to multi-system development with much better
    - Time to market
    - Cost and productivity
    - Product quality

## Allowing incorporation of independently developed components

- Architecture based development focuses on composing or assembling elements
  - Likely built separately or even independently from each other
  - Composition is possible because architecture defines the elements that can be incorporated into a system
- The architecture constrains possible replacements or additions according to
  - How they interact with the environment
  - How they receive and relinquish control
  - How they access data
  - What protocols they use for communication and resource sharing
- Interchangeable parts give way to interchangeability
- For software, payoff can be
  - Decreased time to market
  - Increased reliability
  - Lower cost
  - Flexibility

## Restricting the vocabulary of design alternatives

- As useful architectural patterns emerge
  - Elements can be combined in more or less infinite ways
  - Voluntarily restricting ourselves to a relatively small number of choices of elements and interactions minimizes design complexity
- Patterns restrict the vocabulary of design alternatives
  - Enhances reuse and allows for more regular and simpler designs
  - Designs are more easily understood and communicated
  - Analysis is more capable and selection is quicker

## Providing a basis for training

- Can serve as a first introduction to the system for new project members
  - Supports and encourages communication among various stakeholders
  - Provides a common reference point
