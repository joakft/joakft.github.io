\# Study Guide — AI Product Development (Tier Prod)

This is the \*\*product frontier\*\*.    
At this level, technical skills and research alone aren’t enough.    
The question is: \*Can you turn AI into real, reliable, user-facing products that scale?\*  

Each section contrasts \*\*fakers vs doers vs true AI product builders\*\*.    
Use it to polarize between buzzword product managers, technical builders, and genuine AI product leaders.

\---

\## 1. Product Thinking & Use-Case Fit

\### Faker Line  
\*“AI makes the app smarter and more personalized.”\*

\### Strong Practitioner  
\- Identifies clear use-cases: fraud prevention, personalization, summarization.    
\- Links ML capability to user pain points.  

\### True Product Builder  
\- Frames feature in \*\*user journey + business KPI terms\*\*.    
\- Can answer: \*“Which metric (retention, churn, fraud $ saved) will this move, by how much, and why is AI needed instead of rules?”\*    
\- Knows when \*\*not\*\* to use AI (complexity > benefit).  

\---

\## 2. End-to-End System Design

\### Faker Line  
\*“We’ll just plug the model into the app.”\*

\### Strong Practitioner  
\- Talks about APIs, data pipelines, inference services.  

\### True Product Builder  
\- Designs \*\*infra blueprint\*\*: ingestion, feature store, model registry, inference server, caching, monitoring, fallback rules.    
\- Thinks in \*\*latency budgets\*\* (100ms for fraud API, 500ms for chatbot response).    
\- Explains trade-offs between REST vs gRPC, sync vs async APIs.  

\---

\## 3. MLOps & Lifecycle

\### Faker Line  
\*“We retrain when performance drops.”\*

\### Strong Practitioner  
\- Mentions CI/CD, retraining pipelines, A/B tests.  

\### True Product Builder  
\- Explains \*\*safe deployment playbook\*\*:    
 - Canary releases, shadow mode, automated rollback.    
 - Monitoring \*\*drift + latency + cost per request\*\*.    
 - Continuous retraining with governance gates.    
\- Connects lifecycle to \*\*compliance requirements\*\* (e.g., audit logs, version lineage).  

\---

\## 4. Retrieval-Augmented Generation (RAG) & LLMOps

\### Faker Line  
\*“We add RAG to make chatbots smarter.”\*

\### Strong Practitioner  
\- Mentions vector DBs, embeddings, retrievers.  

\### True Product Builder  
\- Designs full RAG pipeline:    
 - Document ingestion → chunking → embedding → vector DB → retriever → re-ranker → LLM.    
\- Evaluates RAG with \*\*grounding accuracy, hallucination rate, and user satisfaction metrics\*\*.    
\- Adds \*\*guardrails against prompt injection\*\* and PII leakage.  

\---

\## 5. Scaling & Cost Management

\### Faker Line  
\*“We’ll scale in the cloud.”\*

\### Strong Practitioner  
\- Talks about autoscaling, GPUs vs CPUs.  

\### True Product Builder  
\- Knows \*\*infra economics\*\*:    
 - When to use quantization/distillation.    
 - When to cache vs recompute.    
 - Cost per 1k requests and ROI per feature.    
\- Explains migration path: start with vendor API → move to OSS hosted models when traffic justifies.  

\---

\## 6. Security & Compliance

\### Faker Line  
\*“We need to follow GDPR.”\*

\### Strong Practitioner  
\- Mentions anonymization, secure logging.  

\### True Product Builder  
\- Designs \*\*PII-aware data pipelines\*\*: masking, encryption at rest/in transit.    
\- Knows \*\*audit & explainability requirements\*\* for finance/defense.    
\- Implements rate limiting, abuse detection, SOC2-compliant monitoring.  

\---

\## 7. Monitoring & Observability

\### Faker Line  
\*“We track accuracy and latency.”\*

\### Strong Practitioner  
\- Mentions dashboards for model drift and uptime.  

\### True Product Builder  
\- Tracks \*\*multi-layer observability\*\*:    
 - Input/output drift.    
 - Infra metrics (QPS, latency, cost).    
 - Business metrics (fraud savings, churn, analyst tickets).    
\- Has a \*\*playbook for silent failures\*\* (shadow models, anomaly alerts).  

\---

\## 8. Off-the-Shelf vs Custom

\### Faker Line  
\*“We should use GPT-4 for everything.”\*

\### Strong Practitioner  
\- Knows trade-offs between APIs vs fine-tuning.  

\### True Product Builder  
\- Decides based on:    
 - \*\*Sensitivity\*\* (keep in-house if PII/regulatory).    
 - \*\*Scale\*\* (APIs for early stages, OSS for cost efficiency at scale).    
 - \*\*Customization\*\* (fine-tuning for domain, API for generic tasks).    
\- Plans \*\*vendor exit strategies\*\* to avoid lock-in.  

\---

\## 9. Product Metrics & Iteration

\### Faker Line  
\*“We want the model to be accurate.”\*

\### Strong Practitioner  
\- Mentions A/B tests, user feedback loops.  

\### True Product Builder  
\- Measures \*\*end-to-end outcomes\*\*:    
 - Retention uplift.    
 - Fraud loss reduced.    
 - Customer support ticket drop.    
\- Iterates not just on model, but \*\*feature adoption\*\* (onboarding, UX, education).  

\---

\## 10. Cross-Functional Execution

\### Faker Line  
\*“We need to work with PMs and designers.”\*

\### Strong Practitioner  
\- Talks about cross-team collaboration.  

\### True Product Builder  
\- Aligns across \*\*PM, legal, infra, ops, GTM\*\*.    
\- Frames AI limitations in \*\*stakeholder language\*\* (e.g., “80% recall = 20% of fraud may slip, need fallback process”).    
\- Balances \*\*tech debt vs roadmap\*\* under deadlines, with trade-off transparency.  

\---

\# Final Note  
This is the \*\*AI Product Builder tier\*\*.    
\- \*\*Fakers\*\* stay at “AI is cool, it personalizes.”    
\- \*\*Practitioners\*\* know pipelines and tools.    
\- \*\*True builders\*\*:    
 - Design APIs and infra end-to-end.    
 - Tie models to \*\*business KPIs\*\*.    
 - Manage compliance, cost, and scale.    
 - Ship products that \*\*real users adopt\*\*.  

That’s the \*\*polarization frontier\*\*: AI as \*\*product, not prototype\*\*.