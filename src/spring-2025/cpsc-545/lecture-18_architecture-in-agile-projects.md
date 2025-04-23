# Lecture 18: architecture in agile projects

## Introduction

- **Software Architecture** bridges multiple contexts: technical, project life cycle, business, and professional roles.
- Transition from theoretical quality attributes to practical application in Agile projects.

## Methods Overview
- Core methodologies:
  - **PALM**: Captures business goals.
  - **Views and Beyond**: Architectural documentation through stakeholder-oriented views.
  - **ATAM**: Evaluates architectures against quality attributes.
  - **CBAM**: Guides architectural evolution based on stakeholder value.
- **Stakeholder engagement models** vary by:
  - Location (co-located/distributed)
  - Synchronicity (synchronous/asynchronous)
  - Preferred: Co-located, synchronous due to enhanced focus and collaboration.
  - Flexibility and adjustments are critical due to situational uniqueness.

## Agile Projects and Architecture Integration

- Agile emerged to address responsiveness, stakeholder value, early progress, and reduced documentation burdens.
- Key Agile dilemma: balancing upfront architectural design with iterative agility.
- "Agile versus Architecture" is misleading; optimal focus is blending them effectively.

### Agile Manifesto (Key values):

- **Individuals/interactions** > processes/tools
- **Working software** > comprehensive documentation
- **Customer collaboration** > contract negotiation
- **Responding to change** > strict planning

### Agile Principles (Highlighted principles):

- Customer satisfaction through rapid, iterative software delivery.
- Adaptation to changing requirements.
- Sustainable pace of development.
- Technical excellence and simplicity prioritized.
- Best architectures emerge from self-organizing teams.
- Regular reflection and improvement.

## How Much Architecture?

- Historical perspective contrasting Waterfall (plan-driven, predictable) with Agile (flexible, creative).
- User stories exemplify Agile: immediate, feature-focused, but challenging for cross-cutting architectural concerns.

### Just Enough Architecture

- Balance between **up-front planning** (predictability, coordination) and **agility** (creativity, flexibility).
- Optimal amount and timing of architectural work depends on project scale and complexity.
- **"Sweet spot" analysis (Boehm and Turner)** indicates:
  - Minimal upfront architecture for small projects.
  - Moderate planning (approx. 20%) for medium complexity.
  - Significant upfront planning (up to 40%) for highly complex projects.

## Agility in Architectural Methods

- Agile-compatible architecture methods focus on risk reduction, cost-benefit analysis, and stakeholder relevance.
- Most potential Agile friction found in **documentation** and **evaluation**.

### Documentation (Views and Beyond)

- Emphasizes only essential documentation.
- Follows Agile's YAGNI ("You Ain’t Gonna Need It") principle.

### Evaluation (ATAM approach)

- Concentrates on high-risk, high-value scenarios only.
- Lightweight evaluations possible, ensuring Agile compatibility.

## Case Study: Agile Architecting in Web-Conferencing

- Challenges: balancing real-time performance, security, modifiability, usability.
- Constraints: Rapid market demands, unpredictable requirements.
- **Two-mode architecture design**:
  - Top-down for core architecture and quality attributes.
  - Bottom-up for practical, immediate implementation and constraints.

### Key Agile Architecting Practices

- **Continuous experimentation (spikes)** vital for handling uncertainty.
- Agile architecture adapted through incremental improvements informed by empirical evaluation.
- Demonstrated alignment with Agile principles: frequent delivery, welcoming change, technical excellence, sustainable development.

## Guidelines for Agile Architects

### Barry Boehm’s Incremental Commitment Model balances agility and commitment

- Commitment and accountability of success-critical stakeholder
- Meet an acceptability threshold through success-based negotiation and trade-offs
- Incremental and evolutionary growth
- Iterative system development
- Interleaved system definition and development, early core capabilities followed by continual adaptation to change
- Risk management with anchor point milestones

### Grady Booch’s Agile Architecture Recommendations:

- Effective architectures inherently Agile (resilient, loosely coupled).
- Incremental growth, modifiability, clear architecture reflected in code/documentation.

### Ward Cunningham’s Technical Debt Concept:

- Quick, short-term solutions may lead to future "technical debt."
- Regular refactoring critical to manage and reduce technical debt.

### Practical Advice for Agile Architects:

1. **Large, stable projects**: Significant upfront architecture.
2. **Large, unstable projects**: Rapid initial architecture ("walking skeleton"), frequent updates, lightweight analysis.
3. **Small, uncertain projects**: Basic architecture patterns upfront; minimal early investment in detailed documentation or heavy analysis.
