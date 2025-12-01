# Lecture 9: establish stable process behavior charts

## Defects and problems are opportunities

- A process out of control is not a terrible event
- It should not be hidden, it should be celebrated
- Gives the process owner an opportunity to improve the process

### How much data is enough?

- In terms of calculating control limits for the purpose of detecting assignable cause
  - 3-4 samples
  - May get indications of assignable cause even when the control charts are not stable
  - Info gained early is more important in analyzing assignable causes during early phase of control chart construction
- Reasons of determining control limits of a stable process
  - To determine process capability
  - To compare to standards or process requirements
  - To predict the process behavior

### Calculating control limits for a stable process

- For X-Bar and R charts: 25-30 data samples is the minimum desired
- For XmR charts: 40-35 data samples is the minimum desired

> When limited amount of data are available, calculate and plot the limits, seek out the assignable causes that the data suggest, and then update the control limits as more data become available

### Revising control chart limits

- Remove the data points falling outside the computed limits
  - May lead to recalculate the limits
- When using additional data
  - More recently collected data may recalculate the limits for an ongoing chart
- When the process has shifted
  - Recalculate limits using newly collected data and any previous data that remains applicable
- When a deliberate change is made to the process
  - Previously collected data may no longer be applicable

> Updating control limits without evidence of significant change will quickly lead to false alarms (or worse, no distinction between signal and noise)

## Sustaining statistical control

- Never stop control charting your process, especially one that has had history of going out of control
- Only way to ensure the process does not fall back into its old ways once it is stabilized and predictable
- Keep in mind
  - A process can exhibit a lack of control without exceeding control limits
  - Other unnatural or anomalous patterns of points could also point to process symptoms useful for the diagnoses to make process better

### Rational sampling

- Concerned with what, where, how, and why of measurements that are plotted and used to compute control limits
- Data collection context is always the largest factor in determining the best ways to analyze the data
- If outflows of parallel operations are combined without retaining such information, one will not be able to identify which of the operations gave rise seen in a sampled item. Thus, hard to identify which operation is the assignable cause
- Before combining outflows of a parallel process, one needs to confirm all of the parallel outputs are consistent and homogeneous with one another
- Unrepresentative subset should be removed from the computation of control limits
- Sampling frequency and its relation to the rates with which performance can change are another rational sampling consideration

### Rational subgrouping

- Deals with organizing the data so that the control chart answers the right questions
- Subgroups should be selected so that the variations within any given subgroup all come from the same system of chance causes
  - They contain measured values from small regions of time and space
- Control charts on average ask the question: "Do the subgroup averages vary more than they should based on observed variation within subgroups?"
- Control charts on ranges ask the question: "Is the variation within subgroups consistent from subgroup to subgroup?"

## Insufficient granularity

1) Inadequate measurement instruments
2) Imprecise reading of the instruments
3) Rounding
4) Taking measurements at intervals that are too short to permit detectable variation to occur

### Aggregation and Decomposition of Process Performance Data

> When analyzing process performing data, you must be constantly concerned that you have identified all sources of variation in the process

Reasons to overlook sources of variation (overly aggregated data)

- Inadequately formulated operational definitions of product and process measures
- Inadequately description and recording of context information
- Lack of traceability from data back to the context from whence it originated
- Working with data whose elements are combinations (mixtures) of values form non-homogeneous sources

### Consequences of overly aggregated data

- Difficulty in identifying instabilities in process performance
- Difficulty in tracking instabilities to assignable causes
- Using results from unstable processes to draw inferences or make predictions about capability or performance
