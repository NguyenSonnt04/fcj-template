---
title: "Event 1"
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

# Event 1 Report – AI, AWS Cloud, and Multi-Agent Systems

### Event Objectives

- Explain how providing the right context enables AI to produce more accurate and useful results.
- Introduce AI tools for data exploration, workflow creation, and natural-language visualization.
- Present Amazon CloudFront's role in application cost optimization, security, reliability, and performance.
- Share practical experience turning an idea into a product during a time-limited hackathon.
- Clarify LLM non-determinism and mitigation strategies for real-world deployments.
- Introduce enterprise multi-agent architecture through a startup credit-scoring use case.
- Provide career guidance and opportunities for questions and discussion with the speakers.

### Speakers

- **Tinh Truong** – *Context Is Everything: Making AI Actually Work for You*
- **Anh Pham** – *Friendly AI Assistant with Amazon Quick*
- **Thinh Nguyen** – *From Edge To Origin: CloudFront as Your Foundation*
- **Team VIB** – *36 hrs with LotusHacks – Building UTMorpho from Idea to Reality*
- **Duc Dao** – *Non-Determinism of “Deterministic” LLM Settings*
- **Vy Lam** – *Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring*

### Event Agenda

#### 9:00 – 9:30 AM | Context Is Everything: Making AI Actually Work for You

**Speaker: Tinh Truong**

- Explained why AI systems often fail without sufficient context and clarified what context means in practice.
- Discussed the evolution from individual prompts to memory through the **Second AI Brain** concept.
- Shared practical thinking and techniques for providing better context and improving AI results.
- Offered career insights and ways for students to start building with AI.
- Concluded with questions and answers.

#### 9:30 – 9:45 AM | Friendly AI Assistant with Amazon Quick

**Speaker: Anh Pham**

- Introduced **Quick Chat Agent** for exploring data and analyzing insights.
- Presented **Quick Flows** for creating intelligent workflows with natural language and no code.
- Introduced **Quick Spaces**, collaborative spaces that turn individual insights into shared team knowledge.
- Demonstrated how **Quick Sight** can create dashboards and reports from raw data using natural language.

#### 9:45 – 10:25 AM | From Edge To Origin: CloudFront as Your Foundation

**Speaker: Thinh Nguyen**

- Presented Amazon CloudFront as a foundation for different workload types.
- Explained approaches to CloudFront cost optimization.
- Covered security capabilities for protecting applications and origins.
- Demonstrated how CloudFront improves system reliability and availability.
- Shared techniques for improving performance and the user experience.

#### 10:25 – 10:55 AM | 36 hrs with LotusHacks – Building UTMorpho from Idea to Reality

**Speaker: Team VIB**

- Shared why the team joined LotusHacks and how its brainstorming journey began.
- Explained how the team defined the problem and shaped UTMorpho.
- Described building a product under pressure during a 36-hour development sprint.
- Reviewed challenges, failures, and major turning points.
- Presented a product overview and demonstration of UTMorpho.
- Summarized key lessons and the team's next steps.

#### 10:55 – 11:00 AM | Break

Attendees took a short break before the final two sessions on LLM behavior and multi-agent systems.

#### 11:00 – 11:30 AM | Non-Determinism of “Deterministic” LLM Settings

**Speaker: Duc Dao**

- Explained how LLMs select the next token during inference.
- Examined the common assumption that `temperature = 0` guarantees deterministic output.
- Clarified how inference optimizations can still produce different results.
- Discussed practical consequences for testing, evaluation, and production LLM applications.
- Proposed mitigation strategies for more stable and controllable systems.

#### 11:30 AM – 12:00 PM | Enterprise-Grade Multi-Agent System: The Case of Startup Credit Scoring

**Speaker: Vy Lam**

- Analyzed the structural mismatch between traditional banking systems and startup data.
- Explained when a single agent should and should not be used.
- Introduced the multi-agent paradigm and responsibility separation among specialized agents.
- Presented a **Virtual Credit Committee** blueprint for startup credit scoring.
- Covered guardrails, compliance requirements, and risk controls for enterprise systems.
- Discussed operational ROI, an implementation roadmap, and future development.
- Concluded with questions and answers.

### Event Attendance Evidence

The following photograph was taken while I attended Event 1.

![Startup data session presented during Event 1](/fcj-template/images/4-EventParticipated/4.1-Event1/event1-startup-data-session.png)

*Figure 1: A session explaining the key data dimensions used to evaluate startups.*

### Knowledge and Experience Gained

#### Context-Aware AI Applications

- Understood that context quality directly influences the accuracy and usefulness of AI responses.
- Learned how AI development is moving beyond prompt engineering toward memory, knowledge, and context management.
- Recognized the need to design input data, conversation history, and supporting knowledge intentionally.

#### AI-Assisted Data Work

- Learned how conversational assistants support data exploration and insight analysis.
- Understood the ability to create workflows, collaborative spaces, dashboards, and reports through natural language.
- Recognized how these tools can reduce technical barriers for non-programmers.

#### Amazon CloudFront

- Learned that CloudFront is not only a CDN but also a foundation for security, performance, and reliability.
- Understood key considerations for optimizing cost and protecting origins.
- Gained a broader view of workload design from edge to origin.

#### Product Development Under Pressure

- Learned how to move from brainstorming and problem definition to product delivery and demonstration within a limited time.
- Recognized the importance of scope, feature prioritization, and teamwork during a hackathon.
- Understood that failures and direction changes are valuable parts of product development.

#### Reliable LLM System Design

- Learned that `temperature = 0` does not guarantee identical output every time.
- Recognized the risk of building tests or business processes on the assumption of complete LLM determinism.
- Understood the importance of evaluation criteria, guardrails, logging, and variance handling.

#### Enterprise Multi-Agent Architecture

- Learned to distinguish suitable use cases for single-agent and multi-agent solutions.
- Understood how specialized agents can be organized to emulate a decision-making committee.
- Recognized the importance of guardrails, compliance, explainability, and ROI in financial AI systems.

### Application to Work

- Improve project AI prompts and flows by providing structured context instead of relying on short instructions alone.
- Apply CloudFront when content delivery requires high performance, origin protection, and an improved user experience.
- Test LLM systems using acceptance criteria rather than exact response matching.
- Select multi-agent architecture only when a problem genuinely needs specialized roles, coordination, and decision controls.
- Apply the hackathon mindset by defining the core problem, limiting MVP scope, and prioritizing demonstrable value.

### Conclusion

Event 1 provided perspectives ranging from AI, data, and AWS infrastructure to practical product development. It helped me better understand context-aware AI, CloudFront as a platform layer, LLM non-determinism, and the appropriate use of multi-agent architecture. Team VIB's session also offered practical lessons in teamwork, time management, and turning an idea into a working product under significant time pressure.
