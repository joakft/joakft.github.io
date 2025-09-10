\# Study Guide — The “Obvious” AI/ML Interview Topics (Expanded)

This is the \*\*basic buzzword territory\*\*.    
It’s the stuff \*every candidate\* will parrot — and you must too.    
Yes, it’s shallow, yes, it’s dumb, but interviewers expect you to know it cold.    
Here’s a detailed rundown with ready-to-repeat explanations, examples, and buzz lines.

\---

\## 1. High-Level AI/ML Trends & Vocabulary

\### Supervised Learning  
\- \*\*Definition\*\*: Learning from labeled data (input → output).    
\- \*\*Examples\*\*: Fraud detection (fraud/not fraud), credit scoring (loan default yes/no), medical diagnosis.    
\- \*\*Key buzzwords\*\*: classification, regression, training labels, ground truth.    
\- \*\*Buzz line\*\*: \*“Supervised learning uses labeled data to train models for prediction or classification.”\*

\### Unsupervised Learning  
\- \*\*Definition\*\*: Learning patterns without labels.    
\- \*\*Examples\*\*: Customer segmentation, market basket analysis, anomaly detection.    
\- \*\*Key buzzwords\*\*: clustering, dimensionality reduction, embeddings.    
\- \*\*Buzz line\*\*: \*“Unsupervised learning finds hidden structure in unlabeled data.”\*

\### Reinforcement Learning (RL)  
\- \*\*Definition\*\*: Agents learn by trial and error, optimizing a reward.    
\- \*\*Examples\*\*: Game-playing AI (AlphaGo), robotic navigation, ad bidding.    
\- \*\*Key buzzwords\*\*: agent, environment, reward, policy, exploration vs exploitation.    
\- \*\*Buzz line\*\*: \*“Reinforcement learning is about agents learning by trial and error with rewards.”\*

\### Deep Learning  
\- \*\*Definition\*\*: Neural networks with multiple layers that learn hierarchical features.    
\- \*\*Architectures\*\*:    
 - \*\*CNNs\*\*: image recognition, object detection.    
 - \*\*RNNs/LSTMs\*\*: sequential data, time series, NLP.    
 - \*\*Transformers\*\*: attention-based, dominating NLP and vision.    
\- \*\*Buzz line\*\*: \*“Deep learning is about multi-layer neural networks — CNNs for vision, RNNs for sequences, and Transformers for language.”\*

\### Overfitting & Generalization  
\- \*\*Overfitting\*\*: Model memorizes training data, fails on new data.    
\- \*\*Generalization\*\*: Capturing true patterns that work on unseen cases.    
\- \*\*Bias/Variance trade-off\*\*:    
 - High bias = underfitting (too simple).    
 - High variance = overfitting (too complex).    
\- \*\*Buzz line\*\*: \*“Overfitting means the model learns noise; generalization means it learns real patterns.”\*

\### LLM Talking Points  
\- \*\*Embeddings\*\*: Represent text as dense vectors in semantic space.    
\- \*\*Attention\*\*: Mechanism that lets models “focus” on relevant tokens.    
\- \*\*Fine-tuning vs Prompt Engineering\*\*:    
 - Fine-tuning: retraining on new labeled data.    
 - Prompt-engineering: shaping inputs without retraining.    
\- \*\*Buzz line\*\*: \*“LLMs use embeddings to represent text, attention to capture context, and can be adapted with fine-tuning or prompt engineering.”\*

\### Standard Libraries  
\- \*\*PyTorch\*\*: flexible, research-friendly.    
\- \*\*TensorFlow\*\*: production-grade, scalable.    
\- \*\*Scikit-learn\*\*: classical ML toolbox (regression, clustering, preprocessing).    
\- \*\*Buzz line\*\*: \*“We typically use PyTorch or TensorFlow for deep learning and Scikit-learn for classical ML.”\*

\---

\## 2. Use-Case Framing

\### Fraud Detection  
\- Goal: catch unusual/malicious transactions.    
\- Techniques: supervised for known fraud, anomaly detection for new fraud.    
\- \*\*Buzz line\*\*: \*“We combine supervised learning for known fraud with unsupervised anomaly detection for new fraud.”\*

\### Anomaly Detection  
\- Goal: detect outliers.    
\- Examples: abnormal login location, network intrusion, machine failure.    
\- \*\*Buzz line\*\*: \*“Anomaly detection flags activity that deviates from normal patterns.”\*

\### Customer Segmentation  
\- Goal: group customers with similar behavior.    
\- Example: k-means clustering, RFM analysis.    
\- \*\*Buzz line\*\*: \*“Customer segmentation uses clustering methods to find similar groups.”\*

\### Credit Scoring  
\- Goal: predict loan default risk.    
\- Methods: logistic regression, decision trees, simple explainable models.    
\- \*\*Buzz line\*\*: \*“Credit scoring applies supervised learning to assess risk of default.”\*

\### Defense Applications  
\- Goal: monitor signals, automate detection, reduce analyst load.    
\- Examples: anomaly detection in radar/sonar, object tracking in imagery.    
\- \*\*Buzz line\*\*: \*“Defense uses AI for real-time monitoring, anomaly detection, and intelligence automation.”\*

\---

\## 3. Data Science Lifecycle

\### Buzzword Pipeline  
\- \*\*Data cleaning\*\*: fill missing values, remove outliers.    
\- \*\*Feature engineering\*\*: categorical encoding, feature scaling, domain-driven features.    
\- \*\*Model training\*\*: fit algorithms (e.g., logistic regression, random forests).    
\- \*\*Validation\*\*: train/test split, cross-validation.    
\- \*\*Deployment\*\*: expose model via API or batch system.    
\- \*\*Buzz line\*\*: \*“Data → features → model → validation → deployment — the ML lifecycle.”\*

\### CRISP-DM  
\- Phases: business understanding → data understanding → data prep → modeling → evaluation → deployment.    
\- Still the most quoted “process map.”    
\- \*\*Buzz line\*\*: \*“We follow CRISP-DM from business understanding to deployment.”\*

\### Model Monitoring & Drift  
\- \*\*Data drift\*\*: input distribution changes.    
\- \*\*Concept drift\*\*: input–output relationship changes.    
\- \*\*Buzz line\*\*: \*“We monitor for data and concept drift to ensure stability over time.”\*

\---

\## 4. AI Risks & Governance

\### Fairness  
\- Prevent discrimination across demographics.    
\- \*\*Buzz line\*\*: \*“We need fairness metrics to prevent bias in decisions.”\*

\### Explainability  
\- Make model reasoning interpretable.    
\- Tools: SHAP, LIME, saliency maps.    
\- \*\*Buzz line\*\*: \*“Explainability builds trust in AI decisions.”\*

\### Adversarial Attacks  
\- Small perturbations cause model errors.    
\- Example: altered pixels fooling an image classifier.    
\- \*\*Buzz line\*\*: \*“Adversarial attacks show how fragile models can be.”\*

\### Compliance & Regulation  
\- Requirements: GDPR, Basel, ECB, DoD/NATO AI ethics.    
\- Needs: auditability, explainability, record-keeping.    
\- \*\*Buzz line\*\*: \*“Banks and defense need strict compliance for AI use.”\*

\---

\## 5. Cloud / MLOps Buzzwords

\### Docker  
\- Package app + dependencies in containers.    
\- \*\*Buzz line\*\*: \*“Docker ensures consistent environments for ML models.”\*

\### Kubernetes  
\- Orchestration to deploy and scale containers.    
\- \*\*Buzz line\*\*: \*“Kubernetes lets us scale AI deployments reliably.”\*

\### CI/CD  
\- Automate testing, integration, and deployment.    
\- \*\*Buzz line\*\*: \*“CI/CD pipelines automate the ML lifecycle.”\*

\### Cloud Services  
\- \*\*AWS SageMaker\*\*: train, tune, deploy models.    
\- \*\*GCP Vertex AI\*\*: pipelines, model registry, endpoints.    
\- \*\*Buzz line\*\*: \*“We use SageMaker or Vertex AI to run models at enterprise scale.”\*

\### MLOps Challenges  
\- Monitoring drift, managing feature stores, versioning, reproducibility.    
\- \*\*Buzz line\*\*: \*“MLOps ensures monitoring, reproducibility, and scale.”\*

\---

\## Final Note  
This is the \*\*obvious buzzword territory\*\*.    
You repeat these lines, and you check the box.    
Everyone knows them, so you must too.    
It won’t win you the role, but failing here will lose it immediately.