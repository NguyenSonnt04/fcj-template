---
title: "Events Participated"
weight: 4
chapter: false
pre: " <b> 4. </b> "
---

Throughout my internship at the enterprise, alongside my core technical work on **TrustBite**, I was encouraged to participate in major industry seminars and deep-dive sessions focusing on Cloud Computing (AWS Cloud) and Artificial Intelligence (AI/LLM).

Below is a synthesized overview of the two key technology events I attended, along with the knowledge and engineering principles I gained to apply directly to my project:

---

### 1. [Event 1 — AI, AWS Cloud, and Multi-Agent Systems](4.1-Event1/)

*   **Time:** 9:00 AM – 12:00 PM
*   **Role:** Attendee
*   **Main Topics & Summary:**
    This seminar focused on optimized context engineering techniques for LLMs (Context Engineering), natural language data exploration via **Amazon Quick** tools (Quick Chat Agent, Quick Flows, Quick Spaces, Quick Sight), and configuring highly secure, high-performance content distribution using **Amazon CloudFront**.
    Additionally, the sessions explored the non-determinism of LLMs (even under **temperature = 0** configurations) and enterprise-grade **Multi-Agent** architectures through a startup credit scoring case study (**Virtual Credit Committee**).
*   **Key Takeaways:**
    *   Understood the critical role of **Context Engineering** in shaping accurate LLM outputs.
    *   Mastered CloudFront edge-to-origin routing concepts to optimize content distribution costs and shield origin servers.
    *   Learned rapid prototyping and MVP prioritization under tight constraints from the LotusHacks 36-hour hackathon experience.
    *   Learned multi-agent task segregation and building robust verification frameworks for non-deterministic LLM behaviors.

---

### 2. [Event 2 — AI-Powered Cloud Operations and Enterprise Productivity](4.2-Event2/)

*   **Time:** 9:00 AM – 11:30 AM
*   **Role:** Attendee
*   **Main Topics & Summary:**
    This event deep-dived into AI solutions designed to boost enterprise productivity and automate cloud operations. Core topics included the **Deep Response Engine** (automated cloud incident detection and resolution to minimize system downtime), building low-latency real-time voice agents using the **Amazon Nova Sonic** speech-to-speech foundation model, and deploying **AWS DevOps Agent** in multi-cloud or hybrid environments.
    Crucially, speakers demonstrated secure private VPC integrations for Amazon Quick utilizing the **Model Context Protocol (MCP)** to securely retrieve internal enterprise data.
*   **Key Takeaways:**
    *   Learned autonomous cloud operations design patterns aimed at decreasing MTTD and MTTR metrics.
    *   Understood low-latency real-time audio processing (Speech-to-Speech) pipelines for AI Voice Agents.
    *   Mastered the fundamentals of the **Model Context Protocol (MCP)** to securely bridge internal enterprise data with Large Language Models.

---

### 3. Conclusion & Real-World Application
Participating in these events provided me with valuable systems architecture perspectives. I applied these principles directly to my work on the **TrustBite** project:
1.  **Structured Prompting & Contexts:** Utilized context engineering practices to structure prompt and context inputs for S3 OCR and anti-fraud processing workers.
2.  **Flexible LLM Verification:** Realizing LLM non-determinism helped me establish review verification logic based on fuzzy risk scores (using Levenshtein distance) instead of strict string comparisons.
3.  **Prototyping Focus:** Adopted the hackathon mindset to focus on building and delivering the core S3 upload, Textract OCR, and anti-fraud verification engine on time.
