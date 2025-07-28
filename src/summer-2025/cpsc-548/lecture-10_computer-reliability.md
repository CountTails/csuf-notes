# Lecture 10: computer reliability

## Data and software errors

### Data errors

**Some errors caused by poor data in databases**

- Disfranchised voters for 2000 general election in Florida
  - Incorrectly identified as felons which might have affected election outcome
- False arrests
  - Sheila Jackson Stossier arrested and spedt  5 days in detention
  - Roberto Hernandez arrested twice and spent 12 days in jail
  - Terry Dean Rogan arrested after someone stole his identity

**Questions about the accuracy of NCIC records**

- DOJ announces FBI is not responsible for accuracy of NCIC information
- Exempts NCIC from some provisions of Privacy Act of 1974
  - Maintaining accurate data is hard because the data are entered by different agents in different law enforcement and agencies
  - Agents should be able to use discretion
- Privacy advocates criticize that cases of privacy violation will increase
  - Number of records is increasing
  - More erroneous records -> more false arrests
  - Accuracy of NCIC records more important than ever

### Software errors

**Errors leading to system malfunctions**

- Qwest sends incorrect bills to cell phone customers
- Faulty USDA beef price reports
- US postal service returns mail addressed to Patent and Trademark Office
- BMW on-board computer failure
- Computer system failure in Los Angeles County + USC Medical Center laboratory
- About 450 California prison inmates mistakenly released
- Japan's air traffic control system and other airline system failures
- Chicago Board of Trade and London International Financial Futures and Options Exchange system failure

**Incorrectly posted products**

- Amazon.com in Britain offered iPad for 7 pounds instead of 275 pounds
- Site shut down and refused to deliver unless customers paid true price based on their price and availability policy
- Ethical analysis
  - Utilitarian perspective: may increase the overall cost for buyers
  - Kantian perspective: people's good faith

## Notable software system failures

- Patriot Missile
- Ariane 5
- Robot missions to Mars
- At&t long-distance network
- Denver international airport
- Tokyo stock exchange
- Direct recoding electronic voting machines
- Tesla version 7.0 and Uber test-vehicle with Autopilot (fatal accidents)

### Therac-25

- Cause: race condition error occurred in concurrent tasks
- Postmortem and many lessons learned
  - AECL focused on fixing individual bugs
  - System not designed to be fail-safe
  - No devices to report overdoses
  - Difficult to debug programs with concurrent tasks
  - Design must be as simple as possible
  - Documentation crucial
  - Code reuse does not always lead to higher quality
  - AECL did not communicate fully with customers

### Postscript

- Another radiation overdose case (about 3 decades later)
- Computer errors related to radiation machines continue killed patients
- Investigated by the *New York Times*

### Uses of simulations

- Modeling past events and understanding world around us
  - Simulation of weapon
  - Simulation of automobile accident
  - Oil exploration
  - Can predict the future
- Simulations replace physical experiments
  - Experiment too expensive or time-consuming
  - Experiment unethical
  - Experiment impossible
- What if computer simulation is wrong?
  - Verification: does program correctly implement model?
  - Validation: does the model accurately represent the real system?
    - Predict the present from old data
    - Test credibility with experts and decision makers

### Moral responsibility of software failures

- Conditions for moral responsibility
  - Casual condition: actions (or inactions) caused the harm
  - Mental condition: actions (or inactions) intended or willed or moral agent is careless, reckless, or negligent
- Analysis of some software failure cases
  - Therac-25 team morally responsible (constructed the device that caused the harm negligently)
- Software quality is not only customers' requirements but can be moral responsibility for software engineers

## Software engineering for software quality

- Standish group tracks IT projects
- Situation in 1994
  - 1/3 projects cancelled before completion
  - 1/2 projects had time and/or cost overruns
  - 1/6 projects completed on time and on budget
- Situation in 2009
  - 1/4 projects cancelled
  - 5/12 projects had time and/or cost overruns
  - 1/3 projects completed on time and on budget
- Successes of IT projects is increasing over time

## Software warranties and vendor liability

**Shrink wrap warranties**

- Some say you accept software "as is" or 90-day replacement or money-back guarantee
- Non accept liability for harm caused by use of software

**Are software warranties enforceable?**

- Mass marketed software and software included in sale of hardware likely to be considered a good by a court of law (Magnuson-Moss Warranty Act)
- Uniform commercial code applies to goods, despite what warranties may say

**Key court cases**

- Step-save data system v. Wyse technology and the software link (provisions of UCC held)
- ProCD v. Zeidenberg (shrinkwrap licenses are enforceable)
- Mortenson v. Timberline software (in favor of Timerline and licensing agreement that limited consequential damages)

**Moral responsibility of software manufacturers**

- If software vendors are responsible for harmful consequences of defects
  - Companies would test software more and therefore software would be more reliable (really?)
  - They would have to purchase liability insurance (software would cost more)
  - Startups would be affected more than big companies
  - Less innovation in software industry
- Making vendors responsible for harmful consequences of defects may be a bad idea
- Software quality is not only customers' requirements but can be moral responsibility for software engineers
