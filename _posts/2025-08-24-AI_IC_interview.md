\# Tier 2 — DS/ML/AI Beyond the Obvious (with Reasoning)

These 50 questions separate \*\*Tier 1 buzzword parrots\*\* from \*\*Tier 2 staff-level practitioners\*\*.    
Each question is paired with the \*\*reasoning path\*\* that shows true applied mastery.  

\---

\## Section 1. Problem Formulation & Abstraction

1\. \*\*Why is fraud detection not just a “binary classification” problem?\*\*    
  - Logic: Fraud adapts over time. Need \*\*sequential models, thresholds, cost-sensitive optimization\*\*, not static classifiers.  

2\. \*\*How do you handle FP vs FN trade-offs in fraud/defense?\*\*    
  - Logic: Depends on domain cost. FPs = customer friction/ops overload. FNs = direct losses. Must show business framing.  

3\. \*\*Give an example where classification/regression framing is inadequate.\*\*    
  - Logic: Chargeback prediction or AML monitoring → require \*\*sequential/graph framing\*\*.  

4\. \*\*How would you redesign a model for sub-second latency?\*\*    
  - Logic: Simplify features/models, precompute embeddings, approximate inference.  

5\. \*\*Why is problem formulation harder than model selection?\*\*    
  - Logic: Wrong framing → wasted effort regardless of algorithm. Must show ability to reframe problems.  

\---

\## Section 2. Data Beyond CSVs

6\. \*\*Challenges of modeling graph data in fraud?\*\*    
  - Logic: Scalability, evolving structures, partial labels. Relationships (device ↔ account) critical.  

7\. \*\*How to represent sequential behavior in transactions?\*\*    
  - Logic: Encode as \*\*time series\*\* (RNNs, temporal CNNs, Transformers). Order and velocity matter.  

8\. \*\*Processing radar/sonar signals vs text?\*\*    
  - Logic: Continuous, noisy → need \*\*signal transforms (FFT, wavelets), filtering\*\*.  

9\. \*\*What problems arise from label leakage?\*\*    
  - Logic: Features accidentally encode target (e.g., fraud flag in history). Leads to inflated offline accuracy, failure in prod.  

10\. \*\*What is a feedback loop in ML? Why dangerous?\*\*    
  - Logic: Model decisions alter future training data. Example: blocking fraud changes observed distribution.  

\---

\## Section 3. Signal vs Noise

11\. \*\*How do you distinguish true anomaly vs sensor artifact?\*\*    
  - Logic: Cross-validate across independent sensors; domain checks (GPS jump vs real travel).  

12\. \*\*Why is outlier removal risky in adversarial fraud?\*\*    
  - Logic: Fraud is often the outlier. Removing anomalies may discard real fraud.  

13\. \*\*Detecting weak signals in cluttered radar?\*\*    
  - Logic: Use \*\*matched filters, SNR boosting, ensembles across sensors\*\*.  

14\. \*\*Role of spectral transforms (FFT, wavelets)?\*\*    
  - Logic: Convert to frequency domain for denoising and feature extraction.  

15\. \*\*Example of adversaries injecting noise?\*\*    
  - Logic: Fraudsters may add \*\*dummy transactions\*\* to mask fraud bursts.  

\---

\## Section 4. Real-Time Constraints

16\. \*\*What does “\<100ms latency” mean in fraud systems?\*\*    
  - Logic: End-to-end SLA from swipe → decision. Must optimize \*\*inference + retrieval + orchestration\*\*.  

17\. \*\*How do you balance accuracy vs speed vs explainability?\*\*    
  - Logic: Often deploy \*\*simple/fast model online, heavy model offline\*\*.  

18\. \*\*Offline vs online feature stores?\*\*    
  - Logic: Offline = training/historical. Online = low-latency inference.  

19\. \*\*Why are batch models insufficient for streaming fraud?\*\*    
  - Logic: Fraud is dynamic. Need \*\*incremental/online learning\*\* to adapt in near-real time.  

20\. \*\*How would you design a fail-safe fallback system?\*\*    
  - Logic: Hard rules, conservative thresholds, escalation to manual review.  

\---

\## Section 5. Decision Systems vs Models

21\. \*\*Why is “model ≠ system” in production?\*\*    
  - Logic: Real systems = \*\*models + rules + pipelines + orchestration\*\*.  

22\. \*\*What surrounds a fraud model in production?\*\*    
  - Logic: Upstream (feature retrieval), downstream (queues, portfolio optimization, analysts).  

23\. \*\*What is a PID controller in fraud scoring?\*\*    
  - Logic: Dynamic threshold adjustment to smooth FP/FN trade-offs.  

24\. \*\*How could RL auto-tune thresholds?\*\*    
  - Logic: Reward = fraud caught – cost of false alarms. RL optimizes balance dynamically.  

25\. \*\*Why is adversarial adaptation game-theoretic?\*\*    
  - Logic: Fraudsters adapt strategically. Must frame as \*\*multi-agent game\*\*, not static drift.  

\---

\## Section 6. Evaluation in Context

26\. \*\*Why is accuracy useless in fraud detection?\*\*    
  - Logic: Fraud base-rate \<1%. Trivial “all good” model = >99% accuracy.  

27\. \*\*When PR curve > ROC?\*\*    
  - Logic: Class imbalance → PR better captures precision/recall.  

28\. \*\*How to account for $ costs in evaluation?\*\*    
  - Logic: Use \*\*expected monetary loss/savings\*\*. Business-driven metrics.  

29\. \*\*Why do FPs sometimes matter more than FNs?\*\*    
  - Logic: In AML, FPs overload analysts. In card fraud, FNs = direct money loss. Depends on domain.  

30\. \*\*What metrics for radar/sonar?\*\*    
  - Logic: \*\*Probability of detection, false alarm rate, ROC vs SNR.\*\*  

\---

\## Section 7. Adversarial & Robustness

31\. \*\*What is synthetic ID fraud?\*\*    
  - Logic: Mix of real + fake info passes checks → then used for fraud.  

32\. \*\*How would fraudsters probe a black-box model?\*\*    
  - Logic: Send small/innocuous queries to map boundary behavior.  

33\. \*\*What is adversarial camouflage in CV?\*\*    
  - Logic: Textures/perturbations hide objects from detection.  

34\. \*\*Robustness methods vs perturbations?\*\*    
  - Logic: Adversarial training, randomized preprocessing, input sanitization.  

35\. \*\*Why robustness vs adaptability trade-off?\*\*    
  - Logic: Robust models resist known attacks but may miss novel fraud patterns.  

\---

\## Section 8. Scaling & Lifecycle

36\. \*\*Data drift vs concept drift?\*\*    
  - Logic: Drift in inputs vs drift in target mapping. Both must be monitored differently.  

37\. \*\*Why is adversarial drift special?\*\*    
  - Logic: Driven by \*\*adaptive attacker\*\* → faster and more targeted than natural drift.  

38\. \*\*How would you design active learning for fraud?\*\*    
  - Logic: Query uncertain/high-risk cases for human labeling to improve coverage.  

39\. \*\*What is a “wind tunnel” for fraud models?\*\*    
  - Logic: Simulation environment to stress-test defenses under hypothetical attacks.  

40\. \*\*When to retrain online vs batch?\*\*    
  - Logic: Online = rapid adaptation but unstable. Batch = stable but laggy. Depends on ops context.  

\---

\## Section 9. Research vs Commodity

41\. \*\*Why logistic regression/GBMs dominate in banking?\*\*    
  - Logic: Transparent, auditable, strong tabular performance. Regulator-friendly.  

42\. \*\*When use GNN vs random forest?\*\*    
  - Logic: When relationships/graph structure matter (device ↔ merchant links).  

43\. \*\*Why regulators prefer interpretable models?\*\*    
  - Logic: Auditability + explainability mandated in finance/defense.  

44\. \*\*Risk of adopting latest Transformer blindly?\*\*    
  - Logic: Costly, opaque, regulatory risk. Must balance hype vs compliance.  

45\. \*\*How to judge a research paper’s production relevance?\*\*    
  - Logic: Dataset similarity, reproducibility, operational constraints.  

\---

\## Section 10. Domain-Specific Deep Dives

46\. \*\*What features matter in graph-based fraud?\*\*    
  - Logic: Degree, centrality, motifs, connected components.  

47\. \*\*How to defend against account takeover?\*\*    
  - Logic: Device fingerprinting, behavioral biometrics, velocity checks.  

48\. \*\*What are SAR images, why hard?\*\*    
  - Logic: Radar imaging → speckle noise, non-intuitive intensity values.  

49\. \*\*How to fuse radar + imagery + metadata?\*\*    
  - Logic: Early fusion vs late fusion; align by time/geolocation.  

50\. \*\*Why few-shot adaptation matters in defense CV?\*\*    
  - Logic: Rare events, limited labeled data. Need meta-learning, transfer, synthetic augmentation.  

\---

\# Final Note  
Tier 2 candidates must:    
\- Show \*\*applied judgment\*\*, not just buzzwords.    
\- Emphasize \*\*trade-offs, domain realities, adversarial adaptation\*\*.    
\- Collapse fakers by asking for \*\*examples and operational consequences\*\*.  

That’s the bar for “Beyond the Obvious.”