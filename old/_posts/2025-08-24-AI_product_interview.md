\# Tier P — AI/ML Product Builder Interview Guide (with Reasoning)

This guide pairs each question with the \*\*logic to answer\*\* — not just the answer itself.    
It explains what a strong candidate should highlight and why it matters for real-world product delivery.

\---

\## Section 1. Product Thinking & Use-Case Design

1\. \*\*How would you design an AI-powered feature for a mobile banking app?\*\*    
  - Logic: Start with the \*\*user journey\*\*, find friction points, then map AI to value-add.    
  - Good answers focus on fraud prevention, smart personalization, or reducing user effort.  

2\. \*\*How do you translate model metrics into business KPIs (retention, fraud savings, churn)?\*\*    
  - Logic: Show you can bridge \*\*model-world metrics\*\* (accuracy, precision, latency) to \*\*business-world metrics\*\* (dollars saved, fewer analyst tickets, smoother UX).  

3\. \*\*What’s the difference between shipping a PoC vs a production-ready feature?\*\*    
  - Logic: Highlight infra maturity: PoC = notebook, no monitoring. Prod = CI/CD, API contracts, rollback, monitoring.  

4\. \*\*When do you fine-tune a model vs use an off-the-shelf API?\*\*    
  - Logic: Emphasize \*\*ROI trade-offs\*\*. Fine-tune when data is domain-specific or privacy-sensitive; use APIs for generic, non-sensitive tasks.  

5\. \*\*How do you decide whether a feature should be AI-powered at all?\*\*    
  - Logic: Show product judgment — AI should only be used when it creates measurable value beyond heuristics/rules.  

\---

\## Section 2. System Design & APIs

6\. \*\*Design a fraud detection API with \<100ms SLA. What infra do you need?\*\*    
  - Logic: End-to-end design: stream ingestion (Kafka), low-latency model server (ONNX/Triton), Redis caching, API gateway, monitoring.  

7\. \*\*What’s the difference between synchronous vs asynchronous ML APIs?\*\*    
  - Logic: Sync = real-time decision (fraud scoring). Async = batch/offline jobs (reports).  

8\. \*\*How do you design an API so it can be rolled back if a new model fails?\*\*    
  - Logic: Versioned endpoints + feature flags; model registry for rollback.  

9\. \*\*What caching strategies help reduce cost in LLM APIs?\*\*    
  - Logic: Emphasize embedding caches, output caches, and request deduplication.  

10\. \*\*What is the difference between REST vs gRPC for ML serving?\*\*    
  - Logic: REST = simple and widely supported; gRPC = lower latency, better for high-throughput microservices.  

\---

\## Section 3. Data Engineering & Feature Stores

11\. \*\*What’s the difference between an online vs offline feature store?\*\*    
  - Logic: Offline = training/historical analysis; Online = real-time inference.  

12\. \*\*How would you design real-time features for fraud detection?\*\*    
  - Logic: Streaming aggregates (e.g., transaction velocity, last N min) → available in low-latency serving.  

13\. \*\*How do you ensure data lineage and reproducibility in ML pipelines?\*\*    
  - Logic: Use feature registries, versioned datasets, and metadata tracking.  

14\. \*\*What strategies help handle schema drift in production data?\*\*    
  - Logic: Schema validation (Great Expectations), rejection of bad payloads, alerts.  

15\. \*\*How do you ensure features used in training = features used in inference?\*\*    
  - Logic: Use a \*\*shared feature store\*\*; same codepaths for training/serving.  

\---

\## Section 4. MLOps & Lifecycle Management

16\. \*\*How do you structure CI/CD pipelines for ML models?\*\*    
  - Logic: Automated unit tests, linting, containerization, smoke tests, staged rollout.  

17\. \*\*What’s the difference between a canary release and an A/B test?\*\*    
  - Logic: Canary = gradual rollout for stability. A/B = random cohorts to test product impact.  

18\. \*\*How do you set up continuous monitoring for drift and model performance?\*\*    
  - Logic: Monitor \*\*inputs, outputs, latency, error rates\*\*, not just accuracy.  

19\. \*\*How would you trigger automatic retraining safely?\*\*    
  - Logic: Based on drift thresholds or schedules, but gated by evaluation before deploy.  

20\. \*\*What’s the role of model registries in MLOps?\*\*    
  - Logic: Source of truth: track versions, metadata, lineage, and approvals.  

\---

\## Section 5. Retrieval-Augmented Generation (RAG) & LLMOps

21\. \*\*How would you design a RAG pipeline for enterprise documents?\*\*    
  - Logic: Ingest → chunk → embed → vector DB → retriever → re-ranker → LLM.  

22\. \*\*What are the trade-offs between BM25, dense embeddings, and hybrid retrieval?\*\*    
  - Logic: BM25 = cheap keyword, Dense = semantic recall, Hybrid = balance.  

23\. \*\*How do you evaluate the quality of RAG outputs?\*\*    
  - Logic: Grounding accuracy, hallucination rate, answer relevance; use human eval when needed.  

24\. \*\*How do you prevent prompt injection in RAG systems?\*\*    
  - Logic: Input sanitization, guardrails, retrieval filters, allowlists.  

25\. \*\*What vector DBs have you used, and what are the trade-offs?\*\*    
  - Logic: FAISS = local + fast; Pinecone/Weaviate = managed, scalable but costly.  

\---

\## Section 6. Scaling & Cost Management

26\. \*\*How do you reduce cost when an API call to GPT-4 costs $0.05 and you have 10M calls/day?\*\*    
  - Logic: Caching, batching, smaller models, hybrid retrieval before API call.  

27\. \*\*How do you design autoscaling for an ML service?\*\*    
  - Logic: Horizontal pod autoscaling (K8s HPA), tied to QPS and latency metrics.  

28\. \*\*When would you use CPU inference vs GPU inference?\*\*    
  - Logic: CPU = simple/low volume. GPU = deep nets, large LLMs, high QPS.  

29\. \*\*What are quantization and distillation, and when would you use them?\*\*    
  - Logic: Quantization = lower precision → faster/cheaper inference. Distillation = smaller model for scale.  

30\. \*\*How do you monitor cost per prediction in production?\*\*    
  - Logic: Instrument cost logging per endpoint; track $/1k requests.  

\---

\## Section 7. Security & Compliance

31\. \*\*How do you log ML inferences while meeting GDPR/CCPA compliance?\*\*    
  - Logic: Hash IDs, anonymize, log metadata only.  

32\. \*\*What’s the difference between PII masking vs anonymization?\*\*    
  - Logic: Masking = reversible; Anonymization = irreversible.  

33\. \*\*How do you secure model endpoints against abuse or scraping?\*\*    
  - Logic: API keys, auth layers, rate limits, WAF.  

34\. \*\*What controls do you add for API rate limiting in production?\*\*    
  - Logic: Per user/IP/token quotas.  

35\. \*\*How do you ensure SOC2 compliance for ML pipelines?\*\*    
  - Logic: Access control, audit logs, monitoring, approval workflows.  

\---

\## Section 8. Monitoring & Observability

36\. \*\*What’s the difference between data drift monitoring and concept drift monitoring?\*\*    
  - Logic: Data drift = input feature distribution changes. Concept drift = label relationship changes.  

37\. \*\*What metrics would you track to detect RAG hallucinations?\*\*    
  - Logic: Grounding accuracy, factual consistency, user complaint rates.  

38\. \*\*How would you design a dashboard for model health?\*\*    
  - Logic: Show system + model + business metrics: latency, drift, precision, fraud savings.  

39\. \*\*How do you monitor latency spikes in inference?\*\*    
  - Logic: Tracing (OpenTelemetry), log inference per stage, alert on outliers.  

40\. \*\*How do you debug a silent model failure (no errors, but bad predictions)?\*\*    
  - Logic: Shadow deployment comparison, anomaly detection, backtesting on held-out data.  

\---

\## Section 9. Off-the-Shelf vs Custom

41\. \*\*When do you prefer calling OpenAI API vs training/fine-tuning your own model?\*\*    
  - Logic: API = speed, low dev cost. Custom = control, compliance, scale.  

42\. \*\*How do you decide between open-source LLMs vs closed-source APIs?\*\*    
  - Logic: OSS = privacy + customization. Closed = reliability + support.  

43\. \*\*How do you evaluate a vendor’s latency and uptime SLAs?\*\*    
  - Logic: Test with synthetic load, compare against SLA terms, require contractual penalties.  

44\. \*\*What trade-offs exist between off-the-shelf fraud rules engines vs custom ML?\*\*    
  - Logic: Rules = transparent/fast. ML = adaptive/scalable. Often use both.  

45\. \*\*How would you migrate a product from vendor API → in-house model?\*\*    
  - Logic: Run in parallel (shadow mode), benchmark cost/performance, switch gradually.  

\---

\## Section 10. Cross-Functional Execution

46\. \*\*How do you work with PMs and designers when building an AI feature?\*\*    
  - Logic: Start from PRD, align on UX, then design API integration.  

47\. \*\*How do you align with legal/compliance teams for AI product launches?\*\*    
  - Logic: Bring them in early, define consent/audit requirements, bake into pipeline.  

48\. \*\*How do you prioritize tech debt vs new features in an ML roadmap?\*\*    
  - Logic: Fix blocking debt first, balance with PM roadmap, communicate trade-offs.  

49\. \*\*How do you communicate model limitations to non-technical stakeholders?\*\*    
  - Logic: Use analogies (e.g., model = junior analyst), stress uncertainty + fallback.  

50\. \*\*Describe a time you had to ship under tight deadlines. What compromises did you make?\*\*    
  - Logic: Ship with smaller model + caching instead of full retrain → meet SLA with acceptable trade-off.  

\---

\# Final Note  
These questions test whether someone can think in \*\*APIs, infra, compliance, monitoring, and product metrics\*\*.    
The logic shows \*why the right answers matter\* → it’s not just correctness, but \*\*execution judgment\*\*.    
That’s how you polarize \*\*true product builders\*\* from researchers/strategists.