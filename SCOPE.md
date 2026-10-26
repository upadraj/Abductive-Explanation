# Survey Scope

**Working title:** Formal Abductive Explanations for Deep Neural Networks: Solvers, Bound Propagation, and Abstraction–Refinement

**Target size:** ~100 papers (currently 57 collected, 18 read)

---

## 1. Topics

### Core (must be covered in depth)

| Topic | What counts | Anchor papers |
|---|---|---|
| Abductive / sufficient-reason explanations | Minimal feature subsets that provably fix the prediction; prime implicants; cardinality- vs subset-minimal | Ignatiev 2019, Shih 2018, Darwiche 2020 |
| Contrastive explanations and duality | Minimal feature changes that flip the prediction; MHS duality with abductive explanations | Ignatiev 2019 (NeurIPS) |
| Exact solver-based explainers | SMT (Reluplex, Marabou, Z3) and MILP (Tjeng) used as the oracle for explanation queries | Bassan & Katz 2023, VeriX 2023 |
| Bound-propagation-based explainers | CROWN / auto_LiRPA / β-CROWN used as an incomplete but fast oracle | Zhang 2018, Xu 2020, Wang 2021 |
| Abstraction–refinement for explanations | Network reduction, neuron merging, bisimulation, and CEGAR-style refinement to scale explanation queries | Fast and Slow 2025, FAME 2026, Ladner 2025, Prabhakar 2022 |
| Distance-restricted and robust explanations | Explanations valid within an ε-ball rather than the full input domain | Izza 2024, La Malfa 2021 |

### Adjacent (one section each, shallower)

| Topic | Why it is in scope | Anchor papers |
|---|---|---|
| Preimage approximation / global explanations | Explaining a whole output region rather than an instance; shares the same bound-propagation machinery | PREMAP 2025, INVPROP 2023, Zhang 2024 |
| Hyperproperties of networks | Robustness, fairness, and information flow as multi-execution properties; self-composition as a technique | Barthe 2004, Clarkson 2010, Kabaha 2024, Urban 2020 |
| Explanations for learned controllers | Abductive explanations in reactive / RL settings; policy-level explanation | Bassan 2023 (FMCAD), Amir 2021, Corsi 2021 |
| Heuristic XAI as baselines | LIME, SHAP, Anchors — needed to state what formal methods guarantee that these do not | Ribeiro 2016, Lundberg 2017, Ribeiro 2018 |

### Out of scope

- Attribution methods without guarantees (Grad-CAM, Integrated Gradients, saliency maps)
- Mechanistic interpretability of LLMs (circuits, probing, sparse autoencoders)
- Formal explanations of non-neural models (decision trees, random forests, Bayesian classifiers) except where the technique transfers to NNs
- Pure verification / robustness certification with no explanation angle, beyond the solver and bound-propagation foundations above

---

## 2. Venues

### Tier 1 — main focus

| Venue | Why |
|---|---|
| NeurIPS, ICML, ICLR | Bound propagation (CROWN family), VeriX, Fast and Slow, FAME, INVPROP |
| AAAI, IJCAI, KR | Logic-based XAI (Marques-Silva, Ignatiev, Izza), abductive/contrastive theory |
| CAV, TACAS, FMCAD, VMCAI, SAT | Solvers (Reluplex, Marabou), abstraction, network reduction, SMT/SAT encodings |

### Tier 2 — adjacent, applied, journals

| Venue | Why |
|---|---|
| OOPSLA, POPL, PLDI | Hyperproperties, abstract interpretation, global robustness |
| ATVA, HSCC, NFM | Specification, hybrid systems with NN controllers |
| UAI, AAMAS, ICAPS | RL and policy verification/explanation |
| ECAI, AIES, ASE, KDD | Occasional foundational papers (Darwiche 2020, Lakkaraju) |
| JMLR, TMLR | PREMAP, Ladner; longer-form method papers |
| Artificial Intelligence, JAIR, ACM Computing Surveys | Logic-based XAI theory; competing/adjacent surveys |
| Formal Methods in System Design, J. Automated Reasoning | Verification-community journal versions |

### Workshops

- SAIV (AI Verification, co-located with CAV)
- FoMLAS (Formal Methods for ML-Enabled Autonomous Systems)
- XAI workshops at IJCAI / NeurIPS / ICML

### arXiv

- cs.LG, cs.AI, cs.LO
- Forward/backward citation sweep from: VeriX, Fast and Slow, FAME, PREMAP, Marques-Silva 2022 (AAAI) and 2024 (arXiv)

---

## 3. Year range

| Window | Years | Purpose | Target count |
|---|---|---|---|
| Foundations | 2004–2018 | Hyperproperties (Barthe 2004, Clarkson 2010), Z3 2008, Reluplex 2017, SHAP/LIME, first prime-implicant explanations (Shih 2018), CROWN 2018 | 10–15 |
| Core | 2019–2026 | Abductive explanations formalized for ML (Ignatiev 2019), Marabou 2019, and everything on making formal explanations of NNs tractable | 80–90 |
| Cutoff | through ICLR 2026 + arXiv up to submission date | State the cutoff date explicitly in the paper | — |

2019 starts the core window because that year gives the field its definitions (Ignatiev et al., AAAI 2019), its duality result (Ignatiev et al., NeurIPS 2019), and its main solver (Marabou, CAV 2019).
