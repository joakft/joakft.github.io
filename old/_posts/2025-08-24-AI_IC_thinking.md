\# Study Guide — DS/ML/AI \*Beyond the Obvious\* (Expanded)

This is the \*\*polarizing zone\*\*.    
Here, buzzwords aren’t enough — real expertise shows.    
Each topic contrasts the \*faker’s line\* with what a legitimate candidate actually understands.    
Use this as a studying map to separate shallow prep from true mastery.

\---

\## 1. Problem Formulation & Abstraction

\### Faker Line  
\*“We translate business problems into ML tasks like classification or regression.”\*

\### Real Knowledge  
\- Recognizes when the ML framing itself is \*\*wrong or too narrow\*\*.    
\- Understands trade-offs:    
 - \*\*Detection vs prevention\*\* (do we stop fraud after it happens, or before it clears?).    
 - \*\*Latency vs accuracy\*\* (milliseconds vs batch processing).    
 - \*\*False positives vs false negatives\*\* (blocking customers vs missing fraud).    
\- Fraud: binary classifiers are naïve — true systems use \*\*sequential decision-making + adaptive thresholds\*\*.    
\- Defense: noisy radar/sonar cannot just be treated as "time series"; requires \*\*domain-preserving abstractions\*\*.    
\- Core skill: knows \*\*when not to model the problem as “just another classifier.”\*\*

\---

\## 2. Data Beyond CSVs

\### Faker Line  
\*“We clean data, handle nulls, normalize, and balance classes.”\*

\### Real Knowledge  
\- Real-world data = \*\*messy, multi-modal, structured + unstructured\*\*.    
\- Modalities in fraud/defense:    
 - \*\*Graphs\*\* (transaction networks, identity graphs).    
 - \*\*Sequences\*\* (streams of transactions, login attempts).    
 - \*\*Signals\*\* (radar, sonar, RF spectra, biometrics).    
 - \*\*Geospatial tiles\*\* (imagery + metadata layers).    
\- Understands systemic risks:    
 - \*\*Label leakage\*\* (e.g., fraud flag leaking into features).    
 - \*\*Feedback loops\*\* (model outputs altering future training data).    
 - \*\*Survivor bias\*\* (only seeing fraud caught, not fraud that slipped).    
\- Speaks about \*\*data fusion\*\*: e.g., combining vision with radar, or structured customer profiles with behavioral logs.

\---

\## 3. Signal vs Noise

\### Faker Line  
\*“We remove noise and outliers during preprocessing.”\*

\### Real Knowledge  
\- Distinguishes \*\*true anomalies vs data artifacts\*\*.    
\- Fraud: adversaries deliberately inject “cover noise” to mask signals.    
\- Defense: separating \*\*weak but real signals\*\* from clutter, jamming, or atmospheric interference.    
\- Tools:    
 - \*\*Fourier/wavelet transforms\*\* for frequency-space filtering.    
 - \*\*Spectrograms\*\* for non-stationary signals.    
 - \*\*Robust statistics\*\* for heavy-tailed data.    
\- Adversarial awareness: camouflage/spoofing vs natural variance — requires \*\*domain knowledge\*\* beyond generic preprocessing.

\---

\## 4. Real-Time Constraints

\### Faker Line  
\*“We deploy models with Docker and monitor drift.”\*

\### Real Knowledge  
\- Speaks concretely about \*\*latency budgets\*\*:    
 - Fraud: \<100 ms decision at checkout.    
 - Defense: near-instant detection for radar locks.    
\- Explains \*\*speed vs accuracy vs explainability trade-offs\*\* in production.    
\- Knows about \*\*feature store architectures\*\* (online vs offline) for real-time access.    
\- Streaming infra: Kafka, Flink, or equivalent low-latency pipelines.    
\- Fail-safe design: \*\*graceful degradation\*\* — rules fallback, thresholds, escalation when model is uncertain.  

\---

\## 5. Decision Systems vs Models

\### Faker Line  
\*“We use supervised learning or anomaly detection for fraud.”\*

\### Real Knowledge  
\- Recognizes \*\*model ≠ system\*\*.    
 - Upstream: rules, retrieval, candidate selection.    
 - Core: ML models (multiple, specialized).    
 - Downstream: orchestration, cost optimization, human review loops.    
\- Can explain \*\*adaptive control\*\*:    
 - Threshold controllers (PID-like).    
 - RL agents tuning decision parameters.    
\- Understands \*\*adversarial adaptation\*\*: fraud/defense is a \*\*moving target\*\*, not a static distribution.

\---

\## 6. Evaluation in Context

\### Faker Line  
\*“We use accuracy, precision, recall, F1.”\*

\### Real Knowledge  
\- Evaluation depends on \*\*domain economics & ops constraints\*\*.    
\- Fraud:    
 - Base-rate fallacy (fraud \<\<1%).    
 - Precision–Recall curves more relevant than ROC.    
 - \*\*Cost-sensitive metrics\*\* (dollar losses saved, customer friction).    
\- Defense signals:    
 - \*\*Detection probability\*\* vs \*\*false alarm rate\*\*.    
 - ROC under varying SNR levels.    
\- Identity:    
 - Calibration metrics (are predicted probabilities trustworthy?).    
 - Fairness across sensitive groups.    
\- Crucial: links metrics back to \*\*operational workload\*\* (e.g., too many alerts overload human analysts).

\---

\## 7. Adversarial & Robustness

\### Faker Line  
\*“Models can suffer from adversarial attacks.”\*

\### Real Knowledge  
\- Fraud:    
 - Synthetic identities, velocity attacks, probing black-box models.    
\- Defense:    
 - Camouflage, spoofing radar/IR, jamming, adversarial perturbations.    
\- Robustness techniques:    
 - Adversarial training, randomized defenses, gating anomalies, robust loss functions.    
 - \*\*Red-teaming\*\* pipelines to probe weaknesses.    
\- Trade-off awareness: \*\*robustness vs adaptability\*\* — over-robust models may miss new behaviors.  

\---

\## 8. Scaling & Lifecycle

\### Faker Line  
\*“We do MLOps with CI/CD and retrain models when drift happens.”\*

\### Real Knowledge  
\- Differentiates types of drift:    
 - \*\*Population drift\*\* (natural change).    
 - \*\*Adversarial drift\*\* (active fraudster/attacker adaptation).    
 - \*\*Sensor/environmental drift\*\* (defense contexts).    
\- Lifecycle strategies:    
 - Active learning pipelines.    
 - Continual/online learning vs batch retraining.    
 - Simulation engines (“wind tunnels” for fraud, synthetic signal environments for defense).    
\- Governance: system-level monitoring, not just model accuracy — track \*\*decision outcomes, costs, and side-effects\*\*.  

\---

\## 9. Research vs Commodity

\### Faker Line  
\*“Transformers changed everything, we fine-tune embeddings.”\*

\### Real Knowledge  
\- Can separate \*\*commodity tooling vs frontier research\*\*:    
 - Logistic regression & gradient boosting still optimal for explainability and tabular fraud.    
 - GNNs, temporal CNNs, or LSTMs still crucial for sequences and transaction graphs.    
\- Knows open challenges:    
 - Label scarcity, class imbalance, adversarial learning environments.    
 - Evaluation under shifting incentives (fraudsters, adversaries).    
\- Speaks about \*\*regulatory fit\*\*: simple interpretable models often outperform deep nets in banks/defense because of audit requirements.  

\---

\## 10. Domain-Specific Deep Dives

\### Fraud / Banking  
\- Techniques: graph embeddings, velocity checks, entity resolution.    
\- Concepts: synthetic identities, collusion rings, mule accounts.  

\### Identity  
\- Continuous authentication: device fingerprinting, keystroke dynamics, mouse movement.    
\- Biometric spoofing defenses.  

\### Geospatial  
\- Multi-resolution CNNs, temporal change detection, SAR/IR imagery.    
\- Challenges: tiling strategies, cloud cover, seasonal confounders.  

\### Signal Processing (Defense)  
\- Matched filters, adaptive beamforming, clutter suppression.    
\- Multi-sensor fusion (radar + EO/IR + RF).  

\### Computer Vision  
\- Robustness to occlusion, adversarial camouflage.    
\- Few-shot adaptation for rare events.    
\- Multi-modal fusion (vision + text + metadata).  

\*\*Faker\*\*: repeats buzzwords.    
\*\*Real\*\*: grounds answers in \*\*math, physics, operations, and adversarial realities\*\*.  

\---

\## Final Note  
This is the \*\*beyond-trivial territory\*\*.    
Buzzwords collapse here — only \*\*operational trade-offs, domain knowledge, and real modeling experience\*\* can save you.    
If you can articulate these with depth and context, you’re in the Staff tier.    
If not, you’re exposed.