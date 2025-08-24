\# Tier 1 Interview — Q&A (The “Obvious” AI/ML Topics)

These are baseline questions.    
A good candidate should answer them smoothly, with clarity and relevant examples.  

\---

\## Section 1. High-Level AI/ML Trends & Vocabulary

1\. \*\*What is supervised learning? Give two examples.\*\*    
  - Training on labeled data (inputs + outputs). Examples: credit scoring (approve/deny), spam detection (spam/ham).  

2\. \*\*What is unsupervised learning? Give two examples.\*\*    
  - Finding structure in unlabeled data. Examples: customer segmentation, market basket analysis.  

3\. \*\*What is reinforcement learning? How is it different from supervised learning?\*\*    
  - Agent learns via trial and error, guided by rewards. Unlike supervised learning, there are no fixed labels — only feedback over time.  

4\. \*\*Define deep learning in one sentence.\*\*    
  - Training neural networks with multiple layers to learn hierarchical representations from raw data.  

5\. \*\*What are CNNs used for?\*\*    
  - Primarily image data — object detection, recognition, medical imaging.  

6\. \*\*What are RNNs or LSTMs used for?\*\*    
  - Sequential/time-series data — language modeling, speech recognition, financial forecasting.  

7\. \*\*What are Transformers, and what key innovation do they use?\*\*    
  - Architecture for sequence modeling based on self-attention, which captures long-range dependencies better than RNNs.  

8\. \*\*What is overfitting? How do you recognize it?\*\*    
  - When a model memorizes training data but fails on unseen data. Recognized by high train accuracy but poor validation/test accuracy.  

9\. \*\*What is generalization in ML?\*\*    
  - The ability of a model to perform well on unseen data drawn from the same distribution.  

10\. \*\*Explain the bias–variance trade-off in simple terms.\*\*    
  - High bias → too simple, underfits. High variance → too complex, overfits. Goal: find balance for best generalization.  

\---

\## Section 2. Core ML Concepts

11\. \*\*What is cross-validation and why do we use it?\*\*    
  - Splitting data into multiple folds, training on some and validating on others, to get a robust estimate of performance.  

12\. \*\*What is the difference between classification and regression?\*\*    
  - Classification predicts categories (fraud/not fraud). Regression predicts continuous values (house price).  

13\. \*\*What is the purpose of a loss function? Name one for classification.\*\*    
  - Measures error between predictions and true values. Example: cross-entropy loss.  

14\. \*\*What is gradient descent, in simple terms?\*\*    
  - Iteratively adjusting parameters in the direction that reduces loss the most.  

15\. \*\*What is a feature in ML?\*\*    
  - Input variable used for prediction. Example: transaction amount in fraud detection.  

16\. \*\*What is feature engineering? Give one example.\*\*    
  - Creating better features from raw data. Example: velocity of transactions per minute for fraud.  

17\. \*\*What is normalization vs standardization?\*\*    
  - Normalization: scale data to \[0,1\]. Standardization: mean=0, std=1.  

18\. \*\*What is regularization, and why do we need it?\*\*    
  - Techniques like L1/L2 to prevent overfitting by penalizing overly complex models.  

19\. \*\*What does it mean for a dataset to be imbalanced?\*\*    
  - One class dominates (e.g., fraud \<1%). Leads to misleading accuracy if untreated.  

20\. \*\*What is the difference between training, validation, and test sets?\*\*    
  - Train = learn parameters. Validation = tune hyperparameters. Test = evaluate final performance.  

\---

\## Section 3. LLM Talking Points

21\. \*\*What are embeddings in LMs?\*\*    
  - Dense vector representations capturing semantic meaning of words/sentences.  

22\. \*\*What is attention, and why important?\*\*    
  - Mechanism to weight relevant parts of input. Enables handling long-range dependencies.  

23\. \*\*Fine-tuning vs prompt-engineering?\*\*    
  - Fine-tuning: retrain with task-specific data. Prompt-engineering: craft inputs to steer pre-trained models.  

24\. \*\*What is transfer learning, and how applied in NLP/vision?\*\*    
  - Reusing knowledge from a pre-trained model on a new task. Example: ImageNet-trained CNN fine-tuned for medical images.  

25\. \*\*Why are Transformers state-of-the-art in NLP?\*\*    
  - They parallelize training, capture long dependencies, and scale effectively.  

\---

\## Section 4. Use-Case Framing

26\. \*\*How is ML used in fraud detection?\*\*    
  - Supervised models for known fraud patterns; anomaly detection for novel ones.  

27\. \*\*What is anomaly detection? Give one example.\*\*    
  - Identifying outliers that deviate from normal. Example: sudden foreign login attempt.  

28\. \*\*What is customer segmentation?\*\*    
  - Grouping users by similar behavior. Example: clustering customers by spend patterns.  

29\. \*\*Why is logistic regression still used in credit scoring?\*\*    
  - Simple, interpretable, regulator-approved, good for tabular data.  

30\. \*\*How can ML support defense/national security?\*\*    
  - Analyzing sensor streams, detecting anomalies, automating surveillance.  

\---

\## Section 5. Data Science Lifecycle

31\. \*\*List main steps of ML pipeline.\*\*    
  - Data cleaning → feature engineering → model training → validation → deployment → monitoring.  

32\. \*\*What does CRISP-DM stand for?\*\*    
  - Cross-Industry Standard Process for Data Mining. Steps: business understanding → data understanding → prep → modeling → evaluation → deployment.  

33\. \*\*What is data drift?\*\*    
  - Change in input distribution over time.  

34\. \*\*What is concept drift?\*\*    
  - Change in relationship between inputs and outputs (e.g., fraud tactics evolve).  

35\. \*\*Why is model monitoring important?\*\*    
  - Detect drift, maintain reliability, comply with regulations.  

36\. \*\*What is data cleaning? Example?\*\*    
  - Handling errors/missing values. Example: imputing nulls, dropping corrupted rows.  

37\. \*\*What is model deployment? How done?\*\*    
  - Putting trained models into production (via APIs, batch jobs, or embedded systems).  

38\. \*\*What is cross-industry standard practice in DS lifecycle?\*\*    
  - CRISP-DM or similar frameworks for structured workflow.  

\---

\## Section 6. AI Risks & Governance

39\. \*\*What is AI fairness, and why does it matter?\*\*    
  - Ensuring no discrimination across demographics. Important in finance (loan fairness).  

40\. \*\*What is model explainability? Name one tool.\*\*    
  - Ability to interpret model decisions. Example: SHAP or LIME.  

41\. \*\*What is an adversarial attack in ML? Example?\*\*    
  - Small perturbations fooling models. Example: modified pixels mislead image classifier.  

42\. \*\*Why do banks care about explainability?\*\*    
  - Regulatory requirement, trust, customer transparency.  

43\. \*\*What regulations affect AI in finance?\*\*    
  - GDPR, Basel, ECB guidance on model risk.  

44\. \*\*Why is compliance important in defense/finance ML?\*\*    
  - Models affect critical decisions; must be auditable, fair, and legally compliant.  

\---

\## Section 7. Cloud / MLOps Buzzwords

45\. \*\*What is Docker and why useful?\*\*    
  - Containers ensure consistent environments across dev, test, prod.  

46\. \*\*What is Kubernetes, in simple words?\*\*    
  - Orchestrator to deploy/scale/manage containers automatically.  

47\. \*\*What is CI/CD, and why does it matter for ML?\*\*    
  - Continuous integration & deployment pipelines automate testing, reduce errors, accelerate delivery.  

48\. \*\*What is AWS SageMaker used for?\*\*    
  - Managed service for training, tuning, deploying ML models on AWS.  

49\. \*\*What is GCP Vertex AI used for?\*\*    
  - Google’s managed ML platform: pipelines, model registry, endpoints.  

50\. \*\*What does MLOps mean, and why needed?\*\*    
  - “DevOps for ML.” Practices/tools to monitor, reproduce, and scale ML reliably.  

\---

\# Final Note  
Tier 1 candidates should answer with \*\*clarity and confidence\*\*.    
\- Smooth definitions.    
\- Practical examples.    
\- Regulatory/infra awareness sprinkled in.  

Failing here is a red flag; passing here clears the way for deeper Tiers (2–4).