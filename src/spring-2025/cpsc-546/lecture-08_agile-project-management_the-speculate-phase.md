# Lecture 8: agile project management (the speculate phase)

## Speculation

> To form a theory or conjecture about a subject without firm evidence

- Speculation establishes target and direction, but at the same time indicates that, we expect much to change over the life of a project
- Planning is an important activity, but speculating is a more appropriate term as uncertainty increases

### Speculating on product and project

- Two crucial components of an iterative planning and development approach
  - 1) Short iterative time boxes: teams have to figure out faster ways of accomplishing every aspect of development
  - 2) Features: the first goal is to make the process visible and understandable to the customer team
- Product teams speculate about the features in a project and try to make the engineering teams understand those features and requirements
- Product teams attach value points to the features and make priority decisions
- Engineering teams translate the feature from customer view to a technical view to design and build the product
- Product managers control *which* features are included
- Development engineers control *how* features are designed and implemented

### Product backlog

- Simply put, a product backlog expands the product vision into a product feature list
- Product backlog serves as a platform from which the product team determines the significance and priorities of each feature
- The feature list consists of creating story cards that contain basic descriptive and estimating information
- The stories should identify
  - People involved who will used the feature
  - Functions performed by these people
  - Breaking down of feature into implementable stories

### Feature stories

- A feature or story is defined as a piece of product that delivers some useful and valuable functionality to a customer
- Stories are basically small portions of an entire epic feature
- Stories deliver useful functionality, but may not deliver a complete function

## Decomposition of features

**A large and complex story**

- As a frequent flyer I want to book flights customized to my preferences, so I save time

**Decomposed into multiple stories**

1) As a frequent flyer I want to book a trip using miles so that I can save money
2) As a frequent flyer I want to easily book a trip I take often so that I can save time
3) As a premium frequent flyer I want to request an upgrade so I can be more comfortable

### Increase granularity of features

- User stories are derived from XP and are now widely used for all agile processes
- Cards provide a template to write stories and add notes
- Conversations require face-to-face communication to help with specification
- Confirmation takes the form of acceptance tests

### User story

**Definition**

> A UserStory is a story, told by the user, specifying how the system is supposed to work, written on a card, and of a complexity permitting estimation of how long it will take to implement. The User Story promises a s much subsequent conversation as necessary to fill in the details of what is wanted. The cards themselves are used as tokens in the planning process after assessment of business value and \[possibly\] risk. The customer prioritizes the stories and schedules them for implementation.

**Templates**

```plaintext
- As a <role> I would like to be able to <action> to achieve <business value>.
- As a <user role> I can <story> so that <benefit>.
- As a <person name> can <story> so that <benefit>.
- As a <user> I want to <goal> so that <value to attain>.
```

> The "so that" line is generally considered optional, but used as a default

### Story cards

- Purpose of story cards is to provide a simple medium for
  - Gathering information about stories
  - Recording high-level requirements
  - Developing work estimates
  - Defining acceptance tests
- It is an agreement between the customer and team members to discuss detail requirements during an iteration

## Product owner's view

### Feature details evolve over the development phases

- In the envision phase: a preliminary feature or product breakdown structure are identified
- In the speculate phase: Expands the list and create one or more "story" cards that contain basic descriptive and estimating information for identified features
- During the explore phase: Stories are built and tested, the requirements are adjusted and determined in detail

### The focus of stories

- Traditional project plans focus on technical details; stories are customer oriented

**For release planning**

- Used to allocate work to iterations in a release plan
- Want to involve the product team in the process, and they don't need to relate to technical tasks

**For detailed iteration planning**

- Stories are broken down into technical task which the development team uses
- Technical tasks are small and implement only what is needed for a story

### Types of work breakdown structures

- Feature breakdown structure (FBS): offers a significant increase of interaction between the team and customers but may be more difficult to administer
- Phased based WBS: captures requirements, build, design, and test but does not match how engineers perform work

## Release planning

- Presents a roadmap of how the team intends to achieve the product vision within the project objectives and constraints
- Agile life cycles are a significant change from traditional task-driven plans
- Story driven aspect changes the primary focus of planning and executing from tasks to product features
- Any product has a set of features that customers can use for some purpose. The more quickly we link customers to the feature they requested and get feedback on them, the more likely the product development effort will succeed
- Primary task in release planning is assigning stories to iterations, on the basis of value and risk
- A story may deliver high value but not be risky, or it may employ risky new technologies that is invisible to the end customer
- Normally the first priority in assigning stories to iterations is delivering customer value as defined by the product team
- The second priority is to schedule stories that reduce risk early in the project
- Sometimes a technical risk takes top priority
- Release planning should be a collaborative team effort

### Kano analysis

- Mandatory/baseline: must be present in order for users to be satisfied
- Linear: the more of it, the better
- Exciter/delighter: features a user doesn't know he/she wants until seeing it

### Surveying users

- To assess whether a feature is baseline, linear, or exciting we
  - Sometimes guess
  - Survey a small set of users (20 - 30)
- We ask two questions
  - A functional question: how do you feel if a feature is present?
  - A dysfunctional question: how do you feel if a feature is absent
- Include *all* of the baseline features, some of the linear features, but leave room for exciters

### Iteration 0

- Nothing useful delivered to customer here
- Strictly for the team
- Helps team balance anticipation with adaptation

### Iteration 1-N

- Team creates a plan that assigns stories to iterations
- Following activities are involved in a plan
  - Determine how identified risks will influence iteration planning
  - Identify the schedule target
  - Develop a theme for each iteration
  - Assigning story cards to each iteration in some combination of story card layout, complete release planning
  - Adjusting the completed plan as necessary using a trade-off matrix as a guide
- Stories are assigned to iterations for the duration of the project to understand the overall plan and estimate
  - Completion dates
  - Staffing
  - Costs
- Development and product teams do release planning which includes
  - Determining how identified risks will influence iteration planning
  - Assigning story cards to each iteration, balancing value, risks, resources, and dependencies as needed

### First feasible deployment

- The first iteration in which the product could potentially be deployed
  - Companies might be able to deploy an early version to key customers
  - Limited features
  - Might generate revenue and feedback
  - Many benefits but can have potential costs
- Most common with web-based systems (competition needs to be considered)

## Estimating

- You can't estimate the unknown
  - Guessing rather than estimating is sometimes the best we can do
  - Agile organizations learn to live with uncertainty rather then trying to demand certainty
- Agile projects are planned by capabilities and stories
  - Estimation is done on a story-by-story basis
  - Story based planning provides better estimation by those who worked on identifying them and assigning them to iterations
- Estimation can be costly
  - Detailed estimating of items too early in the project life cycle wastes time because items may be dropped anyway
  - Estimating items over and over again while they are in the backlog  can also be wasteful
- Sizing attempts to answer strategic questions about the teams' ability to deliver a quality product within the project's constraints
- Many agile team estimate story points
  - Define a unit of work size rather then effort
  - A relative measure
  - Teams assign story points relative to work complexity, the amount of work, and risk or uncertainty
- These three activities need to be completed prior to beginning story development
  - Articulating a product vision
  - Defining the product's objectives and constraints
  - Creating an iterative, story-based release plan
