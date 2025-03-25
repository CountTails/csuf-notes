# Lecture 15: designing an architecture

- Building blocks for designing a software architecture are:
  - Architecturally significant requirements (ASRs)
  - Quality attribute requirements
  - Choosing, generating, tailoring, and analyzing design decisions for achieving those requirements
- The missing parts: a way to pull the pieces together

## Design strategy

> There are 3 ideas that are key to architecture design methods

### Decomposition

- Architecture determines the quality attributes of a system
- Quality attributes are properties of the system as a whole
- To design a system to achieve quality attribute requirements, we begin with the system as a whole
- As design is decomposed, quality attribute requirements can also be decomposed and assigned to the elements of the decomposition
- As the designer, keep in mind:
  - The constraints give to you
  - Arrange the decomposition so that it will accommodate those constraints
  - Goal is to generate a design that accommodates the constraints and achieves the quality and business goals for the system

### Designing to architecturally significant requirements

- [Lecture 14](./lecture-14_architecture-and-requirements.md) discussed ASRs and gave a technique to collect and structure them
  - These are requirements that drive the architectural design (hence they are significant)
  - Driving the design means these requirements have a profound effect on the architecture
  - You must generate a design that satisfies theses requirements 

**What about non-ASR requirements?**

- The choice of ASRs implies a prioritization of the requirements
- Once you have produced a design that satisfies the ASRs, you are in good shape
- In reality, there are other requirements that are not ASRs you would like to be able to satisfy
  - Still meet the other requirements
  - Meet the other requirements with a slight adjustment of the existing design
  - Cannot meet the other requirements
- If you can meet the other requirements, nothing more to be done
- If you cannot meet them
  - You are close to meeting the requirement, see if the requirement can be relaxed
  - You can reprioritize the requirements and revisit the design
  - Report that you cannot meet the requirement

**Design one ASR at a time or all at once?**

- The answer to this question is a matter of experience
  - Novice architects will likely focus on one ASR at a time
  - Experience and education will give an intuition for designing for multiple ASRs

### Generate and test

- One way of viewing design is a process of generate and test
  - This approach views a particular design as a hypothesise: "this design satisfies the requirements"
  - Testing is the process of determining if the hypothesis is correct
  - It it is not, then another design hypothesis must be generated
- To be effective, the generation of the next hypothesis builds on the results of the tests
  - The things wrong with the current design hypothesis are fixed in the next design hypothesis and the things already correct are kept so
  - If no coupling between the testing and generation of the next design hypothesis exist, the process becomes a "guess and check" method

> The generate and test strategy leads to the following ideas

### Creating the initial hypothesis

> Design solutions are created using "collateral"" that available to the project, which can include

**Existing systems**

- Likely that a system already exists that is similar to the one you are constructing
- Most powerful form of collateral because
  - Business context and requirements for existing system are likely similar to your new systm
  - Many problems that occur have already been solved in the existing design
- The existing design serves as the initial design hypothesis
- The test part of the process will reveal the parts that don't work under the current set of requirements

**Frameworks**

- A partial design that provides services that are common in particular domains
- Frameworks exist in many domains from web applications to middleware systems
- Design of the framework provides the initial design hypothesis
- The design framework constrains you initial hypothesis

**Patterns and tactics**

- A pattern is a known solution to a common problem in a given context
- Cataloged architectural patterns (augmented with tactics) should be considered as candidates for the design hypothesis

**Domain decomposition**

- Another option for the initial design hypothesis comes from performing domain decomposition
- Decomposition will divide the responsibilities to make certain modification easier, but does not speak to many other quality attribute requirements

**Design checklists**

- Can guide an architect to making quality attribute targeted design choices
- Point of using a checklist is to ensure completeness

### Choosing the tests

> Provided by three sources to be applied to the hypothesis

1) The analysis techniques
2) The design checklists for quality attributes
3) The architecturally significant requirements

### Generating the next hypothesis

- After applying the tests
  - You might be done
  - You might still have some concerns
- This is the problems that tactics are intended to solve
  - To improve a design with respect to a particular quality attribute
  - Use the set of tactics to help you improve your design so that you can satisfy these outstanding quality attribute requirements

### Terminating the process

- You are done with the generate-and-test process when
  - You have a design that satisfies the ASRs
  - You exhaust your budget for producing the design
- If you do not product such a design within budget
  - Proceed to implementation with the best hypothesis and realize that some ASRs may not met, need to be relaxed or eliminated (common)
  - Argue for more budget for design and analysis, revisit major early design decisions and resume generate-and-test from that point
  - If all else fails, suggest that the project be terminated

## The attribute driven design method

- Attribute-Driven Design (ADD) is a packaging of the strategies previously discussed
- ADD is an iterative method that, at each iteration, helps the architect to the following
  - Choose part of the system to design
  - Marshal all the architecturally significant requirements for that part
  - Create and test a design for that part

### Inputs to ADD

- Before beginning a design process, the requirements (functional, quality , and constraints) should be known
  - Not realistic to wait for all requirements to be known or else project will never be finished
  - ADD can begin when a set of architecturally significant requirements is known
- In addition to ASRs, input to ADD should include a context description which gives you 2 vital pieces of information as a designer
  - 1) What are the boundaries of the system being designed?
  - 2) What are the external systems, devices, users, and environmental conditions with which the system being designed must interact?

### Outputs of ADD

- Not an architecture complete in every detail, but the main design approaches have been selected and vetted
  - Produces a "workable" architecture early and quickly
  - Can be given to other project teams so they can begin their work while the architect continues to elaborate and refine
- A set of sketches of architectural views
  - Views together will identify a collection of architectural elements and their relationships or interactions
  - When completed, a full-fledged architecture is roughly documented as a set of views
  - Collection can be polished or merged with other views to the extent required by your project

## The steps of ADD

### Step 1: choose an element of the system to design

- For green field designs, the element to begin with is simply the entire system
  - First trip through ADD yields a broad, shallow design that will produce a set of newly identified architectural elements and their interactions
  - These elements will almost certainly require more design decisions to flesh out what they do and how they satisfy ARSs allocated to them
  - During the next iteration of ADD, these elements become candidate for this step
- First iteration of ADD creates a collection of elements that together constitute the entire system
  - Second iteration will take one of these elements and desigit it, resulting in still finer-grained elements
  - Third iteration will take another elements as so forth
- Two main refinement strategies to pursue with ADD
  - Breadth-first: refine all second-level elements before any third-level elements and so forth
  - Depth-first: one downward chain is completed before beginning a second downward chain
- The order you work through is influenced by the business and technical context within which the project is operating
  - Personnel availability: design part of the system to the point where ti can be handed off for implementation or defer to later
  - Risk mitigation: design risky parts of the system to enough depth so that problems can be identified and solved early
  - Deferral of some functionality of quality attribute concern: requires some backtracking to revisit earlier decisions and refine or modity them to accommodate new requirements

### Step 2: identify the ASRs for the chosen element

- If the chosen element for design in step 1 is the whole system, then autility tree can be a good source for the ASRs
- Otherwise, construct a utility tree specifically focused on the chosen element, using the quality attribute requirements that apply to the element

### Step 3: generate a design solution for the chosen element

- Step starts with a chosen element for design and a list of ASRs that apply to it
- For each ASR, develop a solution by choosing a candidate design approach
  - This is the application of the generate-and-test strategy
- Initial candidate design will likely be inspired by a pattern, possibly augmented by one or more tactics
- Refine this candidate design by considering the design checklists for the quality attributes
  - For ASRs that correspond to quality attributes, invoke those checklists to help you instantiate or refine the major design approach
- Step is performed for each ASR in tune, but sources of design candidates may help find design candidates that address several ASRs at once
- Design decisions made in this step now become constraints on all future steps of the method

### Step 4: Inventory remaining requirements and select the input for the next iteration

- Possible that the design solution won't satisfy all ASRs
  - This test step is applied to your design for the element you chose to elaborate in step 1
  - Possible outcome of the test is to backtrack (important requirement was not satisfied and cannot be satisfied by further elaborating this design)
  - Design needs to be reconsidered
- ASRs you have not yet satisfied could be related to the following
  - Quality attribute requirement allocated to the parent element
    - Consider applying (more) tactics to improve the design with respect ot the quality attribute
  - Functional responsibility of the parent element
    - Add responsibilities to either to existing modules or to newly created modules
  - One or more constraints on the parent elements
    - Modify the design or try to relax the constraint
- Most real-world system have requirement that outstrip available time and resources
  - You will find yourself unable to meet some quality attribute requirements, functional requirements, and constraints
  - This step is about taking stock and seeing what requirement are left that still have not been satisfied
- For each one, there are 4 possibilities
  - 1) Quality attribute requirement, functional requirement, or constraint has been satisfied
  - 2) Quality attribute requirement, functional requirement, or constraint is delegated to one of the children
  - 3) Quality attribute requirement, functional requirement, or constraint is distributed among the children
  - 4) Quality attribute requirement, functional requirement, or constraint cannot be satisfied with the current design
- Report to the project manager that a constraint cannot be satisfied without deopardizing other requirements and be prepared to justify such an assertion

### Step 5: Repeat steps 1-4 until all the ASRs have been satisfied

- After the prior steps, each element has assigned to it
  - A set of responsibilities
  - A set of quality attribute requirements
  - A set of constraints
- Repeat steps 1-4 until done
  - If it is clear that all of the requirements are satisfied, then this unequivocally ends the ADD process
- In projects with a high degree of trust between architect and implementation teams, ADD can be terminatd when only a sketch of the architecture is available
  - You trust the implementation team to be able to flesh out the architecture design in a manner consistent with the overall design approaches
  - If you have less trust in the implementation team, then additional levels of design may be necessary
- If there is a contractual arrangement between your organization and the implementation organization
  - The specification of the portion of the system that the implementers are providing must be legally enforceable
  - This means that ADD must continue until that level of specificity has been achieved
- Finally, another condition for terminating ADD is when the project's design budget has been exhausted
- Choosing when to terminate ADD and when to start releasing the architecture are not the same decision
  - Start releasing early architectural views based on the needs of the project
  - Unpalatable alternative is to make everyone wait until the architecture design is finished
- Release the documentation with a caveat as to how likely it is to change
  - Even early broad-and-shallow architectural descriptions can be enormously helful to implementers and other project staff
