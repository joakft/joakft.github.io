# Study Guide — The “Obvious” AI/ML Interview Topics

This is the **basic buzzword territory**.  
It’s the stuff *every candidate* will parrot — and you must too.  
Yes, it’s shallow, yes, it’s dumb, but interviewers expect you to know it cold.  
Here’s a detailed rundown with ready-to-repeat explanations.

---

## 1. High-Level AI/ML Trends & Vocabulary

### Supervised Learning
- **Definition**: Learning from labeled data (inputs + known outputs).  
- **Examples**: Fraud detection (fraud/not fraud), credit scoring (approve/deny loan).  
- **Buzz line**: *“Supervised learning uses labeled data to train models for prediction or classification.”*

### Unsupervised Learning
- **Definition**: Learning patterns or structure from data with no labels.  
- **Examples**: Customer segmentation, anomaly detection.  
- **Buzz line**: *“Unsupervised learning finds hidden structures in unlabeled data.”*

### Reinforcement Learning
- **Definition**: Agents learn to take actions in an environment to maximize cumulative reward.  
- **Examples**: Game-playing AI, robotic navigation.  
- **Buzz line**: *“Reinforcement learning is about agents learning by trial and error with rewards.”*

### Deep Learning
- **Definition**: Neural networks with multiple layers that learn hierarchical representations.  
- **Architectures**:  
  - **CNNs** (Convolutional Neural Networks): process images by detecting local features.  
  - **RNNs** (Recurrent Neural Networks): handle sequential/time-series data.  
  - **Transformers**: use self-attention, dominate NLP and vision.  
- **Buzz line**: *“Deep learning is about multi-layer neural networks — CNNs for vision, RNNs for sequences, and Transformers for language.”*

### Overfitting & Generalization
- **Overfitting**: Model memorizes training data, performs poorly on new data.  
- **Generalization**: Model captures underlying patterns, works well on unseen data.  
- **Bias/Variance trade-off**:  
  - High bias → underfitting (too simple).  
  - High variance → overfitting (too complex).  
- **Buzz line**: *“Overfitting means the model learns noise, generalization is learning true patterns.”*

### LLM Talking Points
- **Embeddings**: Represent words/sentences/documents as dense vectors in a semantic space.  
- **Attention**: Mechanism allowing models to “focus” on relevant parts of the input.  
- **Fine-tuning vs Prompt Engineering**:  
  - Fine-tuning: retraining a model with task-specific data.  
  - Prompt-engineering: crafting inputs to steer outputs without retraining.  
- **Buzz line**: *“LLMs use embeddings to represent text, attention to capture context, and can be adapted with fine-tuning or prompt engineering.”*

### Standard Libraries
- **PyTorch**: flexible deep learning framework, popular in research.  
- **TensorFlow**: industry-grade deep learning framework.  
- **Scikit-learn**: classical ML algorithms (regression, clustering, preprocessing).  
- **Buzz line**: *“We typically use PyTorch or TensorFlow for deep learning and Scikit-learn for classical ML.”*

---

## 2. Use-Case Framing

### Fraud Detection
- Detect unusual or malicious transactions.  
- Buzzword combo: *“We combine supervised learning for known fraud with unsupervised anomaly detection for new fraud.”*

### Anomaly Detection
- Identifying outliers that don’t fit normal patterns.  
- Example: abnormal login locations, sudden spikes in network traffic.  
- **Buzz line**: *“Anomaly detection is used when unusual activity signals risk.”*

### Customer Segmentation
- Grouping customers with similar behavior (spending patterns, demographics).  
- Example: k-means clustering.  
- **Buzz line**: *“Customer segmentation uses clustering methods to find similar groups.”*

### Credit Scoring
- Predicting default risk for loans.  
- Often simple models (logistic regression) for transparency.  
- **Buzz line**: *“Credit scoring applies supervised models to assess default risk.”*

### Defense Applications
- Monitoring sensor streams, pattern detection in signals, surveillance automation.  
- **Buzz line**: *“Defense uses AI for real-time monitoring, anomaly detection, and automation of intelligence analysis.”*

---

## 3. Data Science Lifecycle

### Buzzword Pipeline
- **Data cleaning**: handle missing values, outliers.  
- **Feature engineering**: create new features, encode categorical variables.  
- **Model training**: fit algorithms to data.  
- **Validation**: evaluate on hold-out sets, cross-validation.  
- **Deployment**: push model into production.  

### CRISP-DM
- Cross-Industry Standard Process for Data Mining.  
- Phases: business understanding → data understanding → data preparation → modeling → evaluation → deployment.  
- **Buzz line**: *“We follow CRISP-DM from business understanding to deployment.”*

### Model Monitoring & Drift
- **Data drift**: input distribution changes over time.  
- **Concept drift**: relationship between inputs and target changes.  
- **Buzz line**: *“We monitor models for drift to ensure stability over time.”*

---

## 4. AI Risks & Governance

### Fairness
- Ensuring models don’t discriminate against groups (e.g., race, gender).  
- **Buzz line**: *“We need fairness metrics to prevent bias in decision-making.”*

### Explainability
- Making models transparent (why did the model make this decision?).  
- Tools: SHAP, LIME, attention visualization.  
- **Buzz line**: *“Explainability builds trust in model decisions.”*

### Adversarial Attacks
- Small input perturbations fooling models.  
- Example: changing pixels in an image.  
- **Buzz line**: *“Adversarial attacks show how fragile models can be.”*

### Compliance & Regulation
- GDPR, Basel, ECB, DoD, NATO rules.  
- Requirement: auditability and explainability.  
- **Buzz line**: *“Banks and defense require compliance with strict AI regulations.”*

---

## 5. Cloud / MLOps Buzzwords

### Docker
- Package apps with dependencies into containers.  
- **Buzz line**: *“Docker ensures consistent environments for ML models.”*

### Kubernetes
- Orchestration tool for deploying and scaling containers.  
- **Buzz line**: *“Kubernetes lets us scale model deployments.”*

### CI/CD
- Continuous Integration: automated tests, builds.  
- Continuous Deployment: automatic release of models.  
- **Buzz line**: *“CI/CD pipelines automate the ML lifecycle.”*

### Cloud Services
- **AWS SageMaker**: training, tuning, deployment.  
- **GCP Vertex AI**: model pipelines, registry, endpoints.  
- **Buzz line**: *“On the cloud, we use SageMaker or Vertex AI to train and deploy models at scale.”*

### MLOps Challenges
- Model drift monitoring.  
- Feature store versioning.  
- Data lineage and reproducibility.  
- **Buzz line**: *“MLOps ensures reproducibility, monitoring, and scalability of ML systems.”*

---

## Final Note
This is the **obvious buzzword territory**.  
You repeat these lines, and you check the box.  
Everyone knows them, so you must too.
