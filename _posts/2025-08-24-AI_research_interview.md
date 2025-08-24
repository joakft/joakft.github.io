\# Tier 4 — AI/ML Research Interview Guide (with Reasoning)

These 50 questions test whether a candidate can \*\*derive, prove, critique, and propose novel contributions\*\*.    
They polarize between \*\*industry mastery (Tiers 1–3)\*\* and \*\*true research mastery (Tier 4)\*\*.  

\---

\## Section 1. Mathematical Foundations

1\. \*\*Derive the gradient of the logistic regression log-likelihood.\*\*    
  - Logic: Candidate must derive ∂L/∂w = Σ (yᵢ – σ(w·xᵢ))xᵢ. Shows comfort with calculus + probability.  

2\. \*\*What conditions make linear regression solvable in closed form?\*\*    
  - Logic: Must mention XᵀX invertibility (full rank). Demonstrates linear algebra rigor.  

3\. \*\*State the bias–variance decomposition formally.\*\*    
  - Logic: E\[(ŷ – y)²\] = (Bias\[ŷ\])² + Var\[ŷ\] + irreducible error. Candidate knows formal decomposition, not just intuition.  

4\. \*\*Define convex vs non-convex optimization.\*\*    
  - Logic: Convex = any local min = global min; non-convex = multiple minima/saddles. Candidate should connect to ML optimization challenges.  

5\. \*\*Explain why eigenvalues matter in PCA.\*\*    
  - Logic: They quantify variance explained per component. Candidate links spectral properties to dimensionality reduction.  

6\. \*\*Derive the update rule for SGD.\*\*    
  - Logic: θₜ₊₁ = θₜ – η∇L(θₜ;xᵢ,yᵢ). Must show link to stochastic approximation.  

7\. \*\*What is the curse of dimensionality?\*\*    
  - Logic: Exponential volume growth → sparsity, distances lose meaning. Candidate should cite at least two consequences.  

8\. \*\*Explain L1 vs L2 regularization.\*\*    
  - Logic: L1 → sparsity (Manhattan geometry). L2 → shrinkage (Euclidean). Must connect to geometry of optimization.  

9\. \*\*What is the representer theorem in kernels?\*\*    
  - Logic: Solution in RKHS lies in span of training data kernels. Must connect to SVMs/GPs.  

10\. \*\*Define Lipschitz continuity in DL robustness.\*\*    
  - Logic: |f(x) – f(y)| ≤ K‖x–y‖. Important for bounding adversarial sensitivity.  

\---

\## Section 2. Probability & Statistics

11\. \*\*State Bayes’ theorem and apply it to Naïve Bayes.\*\*    
  - Logic: Candidate must recall formula, explain conditional independence simplification.  

12\. \*\*Define KL divergence and role in VI.\*\*    
  - Logic: Dₖₗ(P‖Q) definition + minimizing divergence in variational inference.  

13\. \*\*LLN vs CLT.\*\*    
  - Logic: LLN → convergence to mean. CLT → sampling distribution tends to Gaussian.  

14\. \*\*Explain PAC-learning and sample complexity.\*\*    
  - Logic: Candidate must know ε–δ guarantees, polynomial dependence on 1/ε,1/δ,dim(H).  

15\. \*\*Concentration inequalities (Hoeffding, Chernoff).\*\*    
  - Logic: Must state form and why useful (bounds deviations).  

16\. \*\*How does importance sampling reduce variance?\*\*    
  - Logic: By reweighting with q(x), reduces mismatch variance.  

17\. \*\*What is a martingale? ML use-case?\*\*    
  - Logic: Martingale property definition; bandits, sequential analysis as examples.  

18\. \*\*What is stationarity and why does it matter?\*\*    
  - Logic: Distribution stability over time. Candidate must tie to time series, RL stability.  

19\. \*\*Define concept drift formally.\*\*    
  - Logic: P(y|x) changes, not just P(x). Candidate should differentiate from covariate shift.  

20\. \*\*MLE vs Bayesian inference.\*\*    
  - Logic: MLE = maximize likelihood. Bayesian = posterior ∝ prior × likelihood.  

\---

\## Section 3. Optimization & Learning Theory

21\. \*\*What is vanishing/exploding gradient mathematically?\*\*    
  - Logic: Product of Jacobians, eigenvalues \<1 → vanish, >1 → explode.  

22\. \*\*Why does ReLU help?\*\*    
  - Logic: Derivative is 0 or 1 → mitigates vanishing vs sigmoid/tanh.  

23\. \*\*Derive backprop for 2-layer NN.\*\*    
  - Logic: Must write δ² = (ŷ–y)σ’, δ¹ = δ²·W²σ’, then weight updates.  

24\. \*\*What is convex duality? Where used?\*\*    
  - Logic: Transform primal ↔ dual problems. Mention SVMs.  

25\. \*\*Define generalization bounds.\*\*    
  - Logic: With prob ≥1–δ, error ≤ empirical + O(√(VCdim/n)).  

26\. \*\*Explain Rademacher complexity.\*\*    
  - Logic: Measures richness of hypothesis class by correlation with random labels.  

27\. \*\*State the no-free-lunch theorem.\*\*    
  - Logic: Averaged across all distributions, all algorithms are equal. Shows need for inductive bias.  

28\. \*\*What is stochastic approximation? Relation to SGD?\*\*    
  - Logic: Iterative noisy root-finding → SGD is a case.  

29\. \*\*Define Bellman optimality in RL.\*\*    
  - Logic: V\*(s)=maxₐ\[R(s,a)+γΣP(s’|s,a)V\*(s’)\].  

30\. \*\*Why is policy gradient high variance, how reduced?\*\*    
  - Logic: Stochastic rewards → high variance. Mitigated with baselines/advantage functions.  

\---

\## Section 4. Advanced Architectures

31\. \*\*Math behind attention in Transformers.\*\*    
  - Logic: Softmax(QKᵀ/√d)V. Candidate must connect Q,K,V.  

32\. \*\*What are positional encodings?\*\*    
  - Logic: Add sinusoidal/learned vectors to encode sequence order.  

33\. \*\*Compare RNNs, LSTMs, GRUs mathematically.\*\*    
  - Logic: RNN simple recurrence; LSTM adds gates; GRU simplified gating.  

34\. \*\*Define graph convolution in GNNs.\*\*    
  - Logic: hᵥ^(k+1)=σ(WΣ hᵤ^(k)). Must connect to message passing.  

35\. \*\*What is Laplacian eigenmaps?\*\*    
  - Logic: Graph embedding via eigenvectors of Laplacian.  

36\. \*\*Why are normalizing flows invertible?\*\*    
  - Logic: Built with invertible transforms, Jacobian det tractable.  

37\. \*\*Define ELBO in VAEs.\*\*    
  - Logic: log p(x) ≥ Eq\[log p(x|z)\] – KL\[q(z)‖p(z)\].  

38\. \*\*Explain GAN mode collapse mathematically.\*\*    
  - Logic: Generator maps many z → same x. Minimax optimization pathology.  

39\. \*\*Autoregressive vs masked LM.\*\*    
  - Logic: AR = next token; MLM = predict masked tokens.  

40\. \*\*What is diffusion modeling?\*\*    
  - Logic: Forward noising process, learn reverse denoising → approximate data likelihood.  

\---

\## Section 5. Robustness, Adversaries & Open Problems

41\. \*\*Define adversarial perturbations.\*\*    
  - Logic: δ-bounded changes cause misclassification. Formal ∀‖δ‖≤ε, f(x+δ)≠f(x).  

42\. \*\*What is certified robustness?\*\*    
  - Logic: Provable guarantees, e.g., randomized smoothing.  

43\. \*\*What are limits of adversarial training?\*\*    
  - Logic: Overfits to known attacks, poor generalization.  

44\. \*\*Distributional shift vs adversarial drift.\*\*    
  - Logic: Shift = natural change. Drift = adaptive adversary.  

45\. \*\*Define OOD detection mathematically.\*\*    
  - Logic: Low likelihood under training p(x); thresholding.  

46\. \*\*Why is fairness ill-posed?\*\*    
  - Logic: Competing definitions (parity vs odds) are mutually incompatible.  

47\. \*\*State one open problem that excites you.\*\*    
  - Logic: Candidate must cite current frontier (robustness, alignment, continual learning).  

48\. \*\*Limits of PAC-learning in adversarial domains?\*\*    
  - Logic: Assumes i.i.d. and fixed distributions → unrealistic in adversarial/fraud.  

49\. \*\*How to define emergent behavior mathematically?\*\*    
  - Logic: Appears when scaling laws surpass thresholds; not captured by small-model asymptotics.  

50\. \*\*What are unsolved frontiers in AI?\*\*    
  - Logic: Generalizable RL, robust multi-modal reasoning, continual/adaptive learning, alignment.  

\---

\# Final Note  
Tier 4 candidates must:    
\- \*\*Derive math\*\*, not just recite.    
\- \*\*Connect proofs to ML systems.\*\*    
\- \*\*Critique literature and name open problems.\*\*    
\- \*\*Show novelty in thinking.\*\*  

That’s how you polarize \*\*true researchers\*\* from even the strongest industry leaders.