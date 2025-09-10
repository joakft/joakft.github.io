# Study Guide — AI/ML Research Depth (Tier 4)

This is the **research frontier**.  
At this level, enterprise strategy and buzzwords aren’t enough — only **theory, math fluency, and novelty** distinguish candidates.  
Each section shows how to polarize between an **industry strategist** and a **true researcher**.

---

## 1\. Mathematical Foundations

### Industry Master Line

_“We use linear regression, logistic regression, and gradient descent.”_

### Research Knowledge

*   Derives **gradients, Hessians, convexity conditions** from first principles.
*   Understands bias–variance decomposition mathematically.
*   Applies linear algebra: eigenvalues in PCA, spectral decompositions, representer theorem in kernels.
*   Talks about **Lipschitz continuity** and its role in robustness proofs.
*   Can prove or at least outline convergence guarantees.

---

## 2\. Probability & Statistics

### Industry Master Line

_“We use Bayes’ theorem, KL divergence, and monitor drift.”_

### Research Knowledge

*   States Bayes’ theorem and applies it rigorously in inference.
*   Uses **KL divergence, ELBO, variational inference** in proofs.
*   Knows LLN, CLT, and concentration inequalities (Hoeffding, Chernoff).
*   Frames PAC-learning formally (ε-δ guarantees, sample complexity).
*   Applies martingale theory, stochastic processes, stationarity.
*   Defines **concept drift in probabilistic terms** (P(y|x) changing over time).

---

## 3\. Optimization & Learning Theory

### Industry Master Line

_“We use SGD to optimize models and avoid overfitting.”_

### Research Knowledge

*   Derives **SGD update rules** and explains stochastic approximation.
*   Knows convex vs non-convex optimization, duality, and saddle point behavior.
*   Discusses **generalization bounds** (VC dimension, Rademacher complexity).
*   States **no-free-lunch theorem** and implications for inductive bias.
*   Frames RL with **Bellman equations** and policy gradient variance analysis.

---

## 4\. Advanced Architectures

### Industry Master Line

_“Transformers dominate NLP, GNNs are used for graphs, VAEs and GANs for generative models.”_

### Research Knowledge

*   Writes out the **attention formula** and positional encodings.
*   Compares RNNs, LSTMs, and GRUs mathematically.
*   Defines **graph convolutions** (message passing, spectral methods).
*   Explains normalizing flows and invertibility constraints.
*   Derives the **ELBO** for VAEs.
*   Discusses mode collapse in GANs mathematically.
*   Understands diffusion models as **likelihood approximation via stochastic processes**.

---

## 5\. Robustness, Adversaries & Open Problems

### Industry Master Line

_“We must make models robust against adversarial attacks.”_

### Research Knowledge

*   Defines adversarial perturbations formally: ∀‖δ‖≤ε.
*   Explains **certified robustness** (randomized smoothing, provable bounds).
*   Critiques limits of adversarial training (poor generalization).
*   Differentiates **distributional shift vs adversarial drift**.
*   Defines OOD detection mathematically (likelihood-based, uncertainty).
*   Recognizes **fairness is ill-posed without normative choices** (incompatible definitions).
*   Points to **open problems**: robustness guarantees, continual learning under adversaries, emergent behaviors.

---

## 6\. Literature & Research Positioning

### Industry Master Line

_“We track SOTA models, fine-tuning benchmarks, and Gartner hype cycles.”_

### Research Knowledge

*   Reads NeurIPS/ICML/ICLR papers and **compares assumptions**.
*   Critiques methods: what’s novel vs incremental.
*   Knows open questions in ML theory: sample complexity, robustness, alignment.
*   Frames research in terms of **contribution types**: new theory, new model class, new optimization, new proof technique.
*   Positions own work in relation to prior art.

---

## 7\. Novelty Creation

### Industry Master Line

_“We adapt models with transfer learning and prompt engineering.”_

### Research Knowledge

*   Proposes **new architectures, loss functions, or optimization frameworks**.
*   Formulates **new mathematical abstractions** (e.g., fraud as stochastic control, adversarial drift as game theory).
*   Produces **proof-of-concept algorithms** with theoretical guarantees.
*   Contributes papers, code, or theory → peer-reviewed or cited.

---

# Final Note

This is the **Tier 4 research mastery zone**.  
Industry leaders (Tier 3) can strategize, but **only researchers** can:

*   Derive from first principles.
*   Prove guarantees.
*   Critique literature.
*   Propose new methods.
*   Identify open problems.

That’s the true mark of an **AI/ML Researcher**.