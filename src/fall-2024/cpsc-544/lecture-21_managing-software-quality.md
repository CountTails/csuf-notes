# Lecture 21: managing software quality

- One of the best ways to evaluate a software organization is to look at the quality of its products
  - Product quality is a key measure of the software process
  - Product quality provides a clear record of
    - Development progress
    - A basis for setting objectives
    - A framework for current action
- 4 basic quality principles
  1) Unless you establish aggressive quality goals, nothing will change
  2) If these goals are not numerical, the quality program will remain just talk
  3) Without quality plans, only you are committed to quality
  4) Quality plans are just paper unless you track and review them

## The quality management paradigm

- Software quality management is like cost management
- Set goals -> make plans -> track performance -> adjust the plan
- This cycle is foundational for industrial engineering and it applies equally to software

**Quality examples**

- Rigorously following a quality plan
  - Reduces failure density rates by a lot
  - Gives an enormous productivity boost
- Quality and productivity improvements are the result of finding and fixing all the errors early in a program

**Quality motivation**

- Purpose of quality program is to motivate action
- To result in better products, measurements must represent goodness in customer terms
- When considered as a motivational program, quality measurements take on a special meaning

**Measuring quality**

- A different approach is needed to motivate an aggressive quality effort
- People can only respond to a few motivational drives at a time
  - Measurement and tracking for the quality program must be tightly focused
  - Establish a small number of specific, numerical quality measures

**Classes of quality measures**

- Development: defects found, change activity
- Product: defects found, software structure, information structure controlled tests
- Acceptance: problems, effort to install effort to use
- Usage: problems, availability, effort to install, effort to use, user opinions
- Repair: defects, resources expended

## Measurement criteria

- Consider the objectives of the measurement program to decide what measures to use
  - To manage software development, choose objective, timely, available, and controllable measures
  - To decide on product acceptance, choose measures that represent user needs and that are available *before* decision time
- Defect measures can be valuable, but controlled tests generally give better results

**Defect measures**

- Defect counts only moderately represent the customer's view of product quality
- Generally true that program with a lot of bugs have poor customer satisfaction
- Once a base level of quality is achieved, defect measures no longer predict customer satisfaction
- Factors such as usability, performance, and functionality become more important
- Determining what truly represents quality in the customer's eyes is *not* a simple task

**Change activities**

- Can be a useful measure of development quality
- High change activity late in a development program indicates overall quality problems
- This measure it generally not directly controllable by developers; it is a consequence of defect rates or requirements stability

**Error seeding**

- A potentially interesting way to evaluate program quality
- The idea is to inject a known number of dummy defects into the program and track how many of them are found by various tests or inspections
- Evidence suggests the seeding idea is promising, but it must still be viewed as an experimental technique

**Controlled tests**

- Product is subjected to a simulated work environment
- Evaluation of its operational suitability is made

**Problem measures**

- Problem activity data provides a potentially useful measure of program quality
- After program installation and cut-over, records can be kept of user-reported problems
- Remainder generally concern user errors, hardware problems, duplicate defects, suggested improvements, and unknown causes
- For large systems, the number of problems due to software defects is around 3-5% of the total records

**Installation and operational effort**

- Effort required to install and operate the system is a good indicator of customer satisfaction
- Such measures are not available until after completion and customer delivery
- Factors that make installation and operation expensive can be examined early in program development (and resolved before customer delivery)

**Customer satisfaction surveys**

- Used to understand the customer's view of an organization's products
- Includes a question to provide a suggestion on where product or services could be improved
- Properly conducted surveys yield and informed view of product quality
- Measure is unavailable until well after development completion

**Reliability and availability**

- Customer's most concerned about a system's ability to perform the intended function whenever needed
- Such measures are particularly important for system and communication programs that are fundamental to overall system operation

$$
  \text{Availability} = \left( 1 - \frac{\text{MTTR}}{\text{MTTR} + \text{MTBF}} \right) * 100
$$

- `MTTR`: the mean time required to repair and restore the system to full operation
- `MTBF`: The mean time between failures

**Selecting quality measures**

- Selecting appropriate quality measures depends on
  - The intended use
  - The kinds of data available
- Defect data is mostly attainable before system shipment
- When no quantitative measures are available for functionality, performance and human Factors
  - Include selected customer representatives in specification reviews
  - Conduct laboratory usability tests
  - Do benchmark testing of customer programs
  - Conductor customer surveys
- Early testing in either a simulated or real operational environment prior to final delivery is always worthwhile

## Establishing a software quality program

Software quality principles can be expanded into the following steps

1) Senior management establishes aggressive and explicit numerical quality goals
2) The quality measures used are objective, requiring a minimum of human judgment
3) These measures are precisely defined and documented so computer programs can be written to gather and process them
4) A quality plan is produced at the beginning of each project
5) These plans are reviewed for compliance with management quality goals
6) Quality performance is tracked and publicized
7) Since no single measures can adequately represent a complex product, the quality measures are treated as indicators of overall performance

**Development plan quality measures**

- To motivate superior development or maintenance performance, defects are the most practical quality measure
- This is also because little other data is available during development
- If defects are not measured, it is hard for software developers to take any other measures very seriously

**Portraying software quality during acceptance test and use**

- For tracking customer-found defects
  - Use a set of cumulative defect curves, starting with system test
  - Curves are normalized per 1000 lines of code and plotted
- When normalized by program size, such historical data can provide a helpful reference in producing new quality estimates

## Estimating software quality

- Important to note that every project is different
- Estimates should be based on historical experience
- Good estimating requires an intuitive understanding of the special characteristics of the product involved

**Making a software quality estimate**

An estimate of program quality is made as follows

1) Recent programs completed by the organization are reviewed to identify the ones most similar to the proposal product
2) Available quality data on these programs is examined to establish a basis for the quality estimate
3) The significant product and process differences are then determined and their potential effects estimated
4) Based on these historical data and the planned process changes, a projection is made of anticipated quality for the new product development process
5) This projection is then compared with goals and needed process improvements are devised to meet the goals
6) The project quality profile is then examined to determine the areas for potential improvement, and a desired quality profile is produced
7) A development plan is produced that specifies the process to bu used to achieve this quality profile

**Software quality models**

- Accurate quality estimate require a quality model
- Not needed to be an explicit mathematical model, but should identify the basic assumptions behind the estimates
- Most mathematical software models are not helpful for estimation purposes because they make some *highly restrictive assumptions* about the software process
  - Failures are independent
  - Number of failures is constant
  - Each failure is repaired before testing continues
  - All failures are observed
  - Testing is of uniform intensity and representative of the operational environment
  - Failure rate at any time is proportional to the current number of remaining defects in the program
  - Time between failures are independent
  - Different types of errors are of equal importance
  - Each error exhibits the same failure rate
  - No errors will be introduced during the testing and repair process
  - Failure rate will decline during debugging and operation

**Intuitive quality models**

- Unique, non-uniform characteristics of quality models that make the software engineering process tractable
  - Program module quality will vary, with a relatively few modules containing the bulk of the errors
  - The remaining modules will likely contain a few randomly distributed defects that must be individually found and removed
  - The distribution of defects will also be highly skewed, with a relatively few types covering a large proportion of the defects
  - Since programming changes are highly error prone, all changes should be viewed as potential sources of defect injection
- The Pareto principle (80/20 rule): a majority of problems (80%) are from a few key causes (20%)
  - Over 1/3 of defects were in the three highest categories

**The quality estimate**

- In comparing components and modules of the new product with similar elements of prior products
  - Each program's unique design and implementation characteristics must be considered
  - Consequently, the quality profile for each program will also probably be different

## Removal efficiency

- An indicator and the development process
- Indicates the cumulative percent of the previously injected errors that have been removed by the end of each project phase
- Since defect removal costs double with each project phase, attention should focus on early removal

## Quality goals

- Must be established by senior management
- Senior managers are the only ones who can set such standards and they are the ones who best appreciate the full benefits of an aggressive quality program
- To establish a quality goal
  1) Every new product or product release must have better quality than its predecessor
  2) The corporate quality organization, with the assistance of the software groups, will establish the quality measures to be used
  3) Each product manager is responsible for producing a documented quality plan to meet these goals
  4) Product quality performance will be judged by
    - The degree to which quality plans show improvement
    - The effectiveness of the action plans to address areas of deficient performance
    - Product management's willingness to establish more aggressive goals when performance exceeds plan
  5) The quality organization will periodically report to senior management on product and organizational performance against these goals

## Quality plans

- Documents the quality actions management intends to implement
- Includes the derivation of the quality measures, identification of the planned process changes, and the anticipated quality improvements

## Tracking and controlling software quality

- The critical elements of a software quality management system are
  - A responsible authority is named to own the quality data and the tracking and reporting system
  - Quality performance is tracked and reported to this authority, during both development and maintenance
  - Resources are established for validating the reported data and retaining it in the process database
- Actual product and organizational performance data is periodically reviewed against the plan
  - Results are initially reviewed with responsible line management and any discrepancies resolved
  - Performance against targets is determined, and, if worse than panned, line management prepares an action plan for review with higher management
  - If actual performance is substantially better than planned, product management established more aggressive targets
- Quality performance is published, and a highlight report is provided to senior management
- Overall performance is periodically reviewed with senior management
