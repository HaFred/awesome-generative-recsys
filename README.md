# Awesome Generative Recommendation System (RecSys)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

## Papers April 28

1. **Learning to Rotate: Temporal and Semantic Rotary Encoding for Sequential Modeling (SIREN-RoPE)**
   * Affiliation: LinkedIn Inc., Mountain View, CA
   * Link: [arxiv.org/abs/2604.24717](https://arxiv.org/abs/2604.24717)
   * Venue: arXiv preprint, April 27, 2026
   * TL;DR: SIREN-RoPE introduces learnable rotation manifold via dual-branch SIREN to encode temporal/semantic signals for sequential modeling in generative recommenders
   * Key techniques:
     - Rotary Position Embedding (RoPE) extended to learnable rotation manifold
     - Dual-branch Sinusoidal Representation Network (SIREN) for heterogeneous signal encoding
     - Temporal patterns, continuous timestamps, categorical metadata as rotation signals
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Novel perspective: treating rotation space as learnable (not fixed) for attention mechanisms; creative analogy to complex numbers
     - **Fairness: 5/10** — Not explicitly addressed; rotation encoding is neutral but could amplify biases if training data is biased
     - **Robustness: 7/10** — Negligible computational overhead; SIREN provides stable gradient flow for learning rotation weights
     - **Impact: 8/10** — From LinkedIn production team; evaluated on large-scale social network news feed dataset; applicable to any RoPE-based generative recommender
     - **Opensource?: 7/10** — Code available at https://github.com/hailingc/siren_rope; demo code provided but full training/eval pipeline completeness TBD

2. **Modeling Behavioral Intensity and Transitions for Generative Recommendation (BITRec)**
   * Affiliation: Ant Group; Fudan University
   * Link: [arxiv.org/abs/2604.24472](https://arxiv.org/abs/2604.24472)
   * Venue: arXiv preprint, April 27, 2026
   * TL;DR: BITRec explicitly models behavioral intensity differences and transition patterns via hierarchical behavior aggregation and transition relation encoding for generative multi-behavior recommendation
   * Key techniques:
     - Hierarchical Behavior Aggregation (HBA): separated exploration and commitment pathways
     - Transition Relation Encoding (TRE): explicit learnable relation matrices for behavior transitions
     - Generative sequence modeling for multi-behavior recommendation
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Explicit intensity + transition modeling in generative recommendation is novel; HBA/TRE are sensible designs
     - **Fairness: 5/10** — Not explicitly addressed; multi-behavior modeling could help or hurt fairness depending on behavior definitions
     - **Robustness: 7/10** — Structured behavior modeling (HBA+TRE) is more robust than implicit attention; validated on 4 large-scale datasets
     - **Impact: 8/10** — From Ant Group (industrial relevance); 15-23% improvements on RetailRocket, Taobao, Tmall, Insurance Dataset
     - **Opensource?: 0/10** — No public code found

3. **FreeScale: Distributed Training for Sequence Recommendation Models with Minimal Scaling Cost**
   * Affiliation: — *(Chenhao Feng, Haoli Zhang, Shakhzod Ali-Zade, Yanli Zhao, Liang Luo, Jennifer Cao, Lisen Deng, Siqiao Chen, Chenyu Zhao, Tristan Rice, Daniel Johnson, Min Si, Tiantu Xu, Yi Zhang, Siqi Yan, Chuanhao Zhuge, Min Ni, Bi Xue, Qunshu Zhang, Shen Li — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24073](https://arxiv.org/abs/2604.24073)
   * Venue: MLSys 2026 (9th Conference on Machine Learning and Systems)
   * TL;DR: FreeScale reduces compute bubble by 90.3% for distributed training of sequence recommendation models via load balancing and communication overlap
   * Key techniques:
     - Load balancing via careful input sample balancing to mitigate straggler effect
     - Prioritized embedding communication overlapping with computation
     - SM-Free technique to resolve GPU resource contention during communication-computation overlap
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 6/10** — Distributed training optimizations are incremental but well-engineered; SM-Free technique is a useful contribution
     - **Fairness: 4/10** — Not relevant to fairness; pure systems optimization work
     - **Robustness: 8/10** — Empirically validated on 256 H100 GPUs; significant compute bubble reduction (90.3%) improves training stability
     - **Impact: 8/10** — MLSys 2026; critical for industrial-scale sequence recommendation model training; 256 GPU scaling
     - **Opensource?: 0/10** — No public code found

4. **SAGE: Sparse Adaptive Guidance for Dependency-Aware Tabular Data Generation**
   * Affiliation: — *(Shuo Yang, Zheyu Zhang, Bardh Prenkaj, Gjergji Kasneci — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24368](https://arxiv.org/abs/2604.24368)
   * Venue: ACL 2026
   * TL;DR: SAGE uses LLM with sparse, adaptive dependency guidance for high-fidelity tabular data generation; relevant to generative recommendation data synthesis
   * Key techniques:
     - Feature discretization into value-aware pseudo-features
     - Mutual information-based sparse dependency graph construction
     - Adaptive guidance via explicit context selection or implicit logic correction
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Sparse + adaptive dependency guidance for tabular generation is novel; addresses key limitations of dense modeling and static dependencies
     - **Fairness: 6/10** — Synthetic data generation could help privacy but may also amplify biases present in training data; not explicitly addressed
     - **Robustness: 7/10** — Sparse graph reduces spurious correlations; 10% F1 improvement and reduced policy violations
     - **Impact: 7/10** — ACL 2026; tabular data generation is useful for recommendation (user/item feature synthesis); strong empirical results
     - **Opensource?: 0/10** — No public code found (paper says code will be released, but not available yet)

5. **Disagreement as Signals: Dual-view Calibration for Sequential Recommendation Denoising (DC4SR)**
   * Affiliation: — *(Sijia Li, Min Gao, Zongwei Wang, Zhiyi Liu, Xin Xia, Yi Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24048](https://arxiv.org/abs/2604.24048)
   * Venue: arXiv preprint, April 27, 2026
   * TL;DR: DC4SR uses disagreement between LLM semantic priors and model-learned posteriors as signals for joint optimization and denoising in sequential recommendation
   * Key techniques:
     - Dual-view calibration: LLM-based semantic prior + model-learned posterior
     - Disagreement-based denoising signal identification
     - Joint optimization of semantic understanding and model representation
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Using LLM-model disagreement as denoising signal is a creative idea; dual-view calibration is well-motivated
     - **Fairness: 5/10** — Not explicitly addressed; LLM semantic priors may carry biases
     - **Robustness: 7/10** — Denoising via disagreement signals improves robustness to noisy interactions; novel approach
     - **Impact: 7/10** — Sequential recommendation denoising is an important problem; LLM integration adds value
     - **Opensource?: 0/10** — No public code found

---

## Papers April 27

1. **ReCast: Recasting Learning Signals for Reinforcement Learning in Generative Recommendation**
   * Affiliation: — *(Peiyan Zhang, Hanmo Liu, Chengxuan Tong, Yuxia Wu, Wei Guo, Yong Liu — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22169](https://arxiv.org/abs/2604.22169)
   * TL;DR: "Fix-contrast" learning signal framework for sparse-hit generative recommendation
   * Key techniques:
     - Min-learnability recovery for all-zero groups
     - Boundary-focused contrastive updates (hardest negatives + strongest positives)
     - Partial decoupling of rollout width and actor update width
   * Venue: arXiv preprint, April 24, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Identifies and fixes a real problem in group-based RL for sparse-hit rec
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — Min-learnability recovery stabilizes training on hard groups
     - **Impact: 7/10** — Practical fix for a common failure mode in RL-based generative rec
     - **Opensource?: 0/10** — No public code found

2. **Objective Shaping with Hard Negatives: Windowed Partial AUC Optimization for RL-based LLM Recommenders**
   * Affiliation: — *(Wentao Shi, Qifan Wang, Chen Chen, Fei Liu, Dongfang Liu, Xu Liu, Wanli Ma, Junfeng Pan, Linhong Zhu, Fuli Feng — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22504](https://arxiv.org/abs/2604.22504)
   * TL;DR: Windowed partial AUC (WPAUC) optimization for better Top-K alignment in RL-based LLM recommenders
   * Key techniques:
     - Theoretical analysis: GRPO ≈ AUC maximization (misfit for Top-K)
     - Beam-search negatives → partial AUC shaping
     - Threshold-Adjusted Window (TAWin) for explicit Top-K control
   * Venue: arXiv preprint, April 24, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Novel theoretical connection between GRPO and AUC; WPAUC is a creative solution
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — WPAUC shaping is more stable than raw GRPO for Top-K
     - **Impact: 8/10** — Strong theoretical backing; from Multi-Scenarios team (likely industry)
     - **Opensource?: 0/10** — No public code found

3. **GraphRAG-IRL: Personalized Recommendation with Graph-Grounded Inverse Reinforcement Learning and LLM Re-ranking**
   * Affiliation: — *(Siqi Liang, Xiawei Wang, Yudi Zhang, Jiaying Zhou — institutions TBD)*
   * Link: [arxiv.org/abs/2604.19128](https://arxiv.org/abs/2604.19128)
   * TL;DR: Hybrid recommendation framework combining GraphRAG, Inverse RL, and persona-guided LLM re-ranking
   * Key techniques:
     - Heterogeneous knowledge graph (items, categories, concepts)
     - Maximum-entropy IRL for calibrated pre-ranking
     - Persona-conditioned LLM fusion on short candidate lists
   * Venue: arXiv preprint, April 21, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Creative combination of GraphRAG + IRL + LLM re-ranking
     - **Fairness: 6/10** — Persona-guided re-ranking could help or hurt fairness depending on persona design
     - **Robustness: 6/10** — Hybrid approach; graph + IRL + LLM each add complexity
     - **Impact: 6/10** — Niche but interesting; persona-guided LLM fusion is a growing area
     - **Opensource?: 0/10** — No public code found

4. **Modular Representation Compression (MARC): Adapting LLMs for Efficient and Effective Recommendations**
   * Affiliation: — *(Yunjia Xi, Menghui Zhu, Jianghao Lin, Bo Chen, Ruiming Tang, Yong Yu, Weinan Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.18146](https://arxiv.org/abs/2604.18146)
   * TL;DR: Modular representation compression to resolve mid-layer representation advantage (MRA) in LLM-based recommendation
   * Key techniques:
     - Module tuning (explicit compression + task adaptation modules)
     - Module task decoupling (information constraints + divergent architectures)
     - Middle-layer representation extraction for compression
   * Venue: SIGIR 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Identifies MRA phenomenon; modular compression is a clever fix
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — Explicit compression modules are more stable than end-to-end fine-tuning
     - **Impact: 8/10** — SIGIR 2026; addresses a key efficiency-effectiveness trade-off in LLM4Rec
     - **Opensource?: 0/10** — No public code found

5. **Multi-LLM Token Filtering and Routing for Sequential Recommendation (MLTFR)**
   * Affiliation: — *(Wuhan Chen, Min Gao, Xin Xia, Zongwei Wang, Wentao Li, Shane Culpepper — institutions TBD)*
   * Link: [arxiv.org/abs/2604.18200](https://arxiv.org/abs/2604.18200)
   * TL;DR: Multi-LLM token embedding filtering and routing for corpus-free sequential recommendation
   * Key techniques:
     - User-guided token filtering (task-relevant embedding selection)
     - Mixture-of-Experts (MoE) architecture for multi-LLM integration
     - Fisher-weighted semantic consensus expert (prevent dominant experts)
   * Venue: arXiv preprint, April 20, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Multi-LLM integration via MoE is interesting; corpus-free is a plus
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 6/10** — MoE routing can be unstable; Fisher-weighted consensus helps
     - **Impact: 7/10** — Multi-LLM trend is growing; corpus-free is practical for industry
     - **Opensource?: 0/10** — No public code found

6. **ResRank: Unifying Retrieval and Listwise Reranking via End-to-End Joint Training with Residual Passage Compression**
   * Affiliation: — *(Xiaojie Ke, Shuai Zhang, Liansheng Sun, Yongjin Wang, Hengjun Jiang, Xiangkun Liu, Cunxin Gu, Jian Xu, Guanjun Jiang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22180](https://arxiv.org/abs/2604.22180)
   * TL;DR: Unified retrieval-reranking with residual passage compression for efficient LLM-based listwise reranking
   * Key techniques:
     - Encoder-LLM for passage compression (one embedding per passage)
     - Residual connection (encoder embedding + reranker hidden states)
     - One-step cosine-similarity scoring (zero generated tokens)
   * Venue: arXiv preprint, April 24, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Residual compression for unified retrieval-reranking is novel
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — One-step scoring is efficient and stable
     - **Impact: 8/10** — Unified retrieval-reranking is a hot topic; efficient listwise reranking has high industrial value
     - **Opensource?: 0/10** — No public code found

7. **Rethinking Semantic Collaborative Integration: Why Alignment Is Not Enough**
   * Affiliation: — *(Maolin Wang, Dongze Wu, Jianing Zhou, Hongyu Chen, Beining Bao, Yu Jiang, Chenbin Zhang, Chang Wang, Jian Liu, Lei Sha — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22195](https://arxiv.org/abs/2604.22195)
   * TL;DR: Beyond alignment — complementary fusion of semantic and collaborative representations for recommendation
   * Key techniques:
     - "Shared + private" latent structure assumption
     - Complementarity-aware diagnostics (overlap, unique hit contribution, fusion upper bound)
     - Controlled alignment probes (low-capacity mapping cannot recover full geometry)
   * Venue: SIGIR 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Rigorous analysis of why alignment is insufficient; complementarity-aware fusion is novel
     - **Fairness: 6/10** — Deeper fusion could amplify biases; not explicitly addressed
     - **Robustness: 7/10** — Diagnostics help understand fusion quality; more robust than blind alignment
     - **Impact: 8/10** — SIGIR 2026; fundamental contribution to LLM4Rec representation learning
     - **Opensource?: 0/10** — No public code found

8. **Deep Interest Mining with Cross-Modal Alignment for SemanticID Generation in Generative Recommendation**
   * Affiliation: — *(Yagchen Zeng — institution TBD)*
   * Link: [arxiv.org/abs/2604.20861](https://arxiv.org/abs/2604.20861)
   * TL;DR: Cross-modal alignment and deep interest mining for high-quality Semantic ID generation in generative recommendation
   * Key techniques:
     - Vision-Language Model (VLM) for cross-modal alignment
     - Deep Contextual Interest Mining (DCIM)
     - Cross-Modal Semantic Alignment (CMSA)
     - Quality-Aware Reward Mechanism (QARM)
   * Venue: arXiv preprint, March 3, 2026
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Cross-modal alignment for Semantic ID is novel; Deep Interest Mining is a solid addition
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 6/10** — VLM alignment can be noisy; QARM helps but adds complexity
     - **Impact: 7/10** — Semantic ID quality is a key bottleneck; cross-modal approach is promising
     - **Opensource?: 0/10** — No public code found

---

## Papers April 26

1. **ReRec: Reasoning-Augmented LLM-based Recommendation Assistant via Reinforcement Fine-Tuning**
   * Affiliation: — *(Jiani Huang, Shijie Wang, Liangbo Ning, Wenqi Fan, Qing Li — affiliation not listed on arxiv)*
   * Link: [arxiv.org/abs/2604.07851](https://arxiv.org/abs/2604.07851)
   * Venue: ACL 2026
   * TL;DR: RL + Reasoning for LLM-based recommendation assistant
   * Key techniques:
     - Dual-graph augmented reward shaping (NDCG@K + query alignment + preference alignment)
     - Reasoning-aware advantage estimation (penalize wrong reasoning steps)
     - Online curriculum scheduler (dynamic query difficulty assessment)
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — New "reason-then-recommend" + RL fine-tuning paradigm for recommendation assistants
     - **Fairness: 5/10** — Not explicitly addressed; may inherit LLM biases
     - **Robustness: 7/10** — Curriculum learning improves training stability; reasoning decomposition adds resilience
     - **Impact: 8/10** — ACL 2026, addresses a growing real-world need (complex query recommendation)
     - **Opensource?: 0/10** — No public code repository found

2. **Generative Reasoning Re-ranker (GR2)**
   * Affiliation: Meta *(Mingfu Liang et al.)*
   * Link: [arxiv.org/abs/2602.07774](https://arxiv.org/abs/2602.07774)
   * TL;DR: Generative LLM re-ranking via reasoning + DAPO (Decoupled Clip and Dynamic Sampling Policy Optimization)
   * Key techniques:
     - Three-stage training: mid-training on semantic IDs → SFT on LLM-generated reasoning traces → DAPO RL
     - Decoupled clipping (separate upper/lower clip bounds)
     - Dynamic sampling (filter zero-advantage groups)
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — First to apply DAPO-style RL to generative re-ranking; reasoning-augmented re-ranking is novel
     - **Fairness: 5/10** — Not discussed; RL optimization may inadvertently introduce ranking bias
     - **Robustness: 7/10** — Dynamic sampling improves training stability; reasoning traces add interpretability
     - **Impact: 9/10** — Outperforms OneRec-Think; from Meta; high industrial relevance
     - **Opensource?: 0/10** — No public code available (Meta paper)

3. **Verifiable Reasoning for LLM-based Generative Recommendation (VRec)**
   * Affiliation: — *(Xinyu Lin, Hanchao Yu, Yinglong Xia, Jiang Zhang, Aashu Singh, Fei Liu, Wenjie Wang, Fuli Feng, Tat-Seng Chua, Qifan Wang — institutions TBD)*
   * Link: [arxiv.org/abs/2603.07725](https://arxiv.org/abs/2603.07725)
   * TL;DR: "Reason-verify-recommend" paradigm with multi-dimensional verification to mitigate reasoning degradation
   * Key techniques:
     - Hybrid verifier (rule-based + model-based) for multi-dimensional assessment
     - Proxy prediction targets to improve verifier reliability
     - Reasoning chain decomposition with step-level verification
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 9/10** — "Reason-verify-recommend" is a genuinely new paradigm; step-level verification for recommendation is novel
     - **Fairness: 6/10** — Verification may propagate existing biases; not explicitly mitigated
     - **Robustness: 8/10** — Verification mechanism catches reasoning errors before recommendation; strong resilience
     - **Impact: 8/10** — Addresses key LLM reasoning failure modes; from NUS/Meta team
     - **Opensource?: 2/10** — Repo exists (github.com/Linxyhaha/Verifiable-Rec) but empty (1 ⭐, no code uploaded)

4. **Unleashing the Native Recommendation Potential: LLM-Based Generative Recommendation via Structured Term Identifiers (GRLM)**
   * Affiliation: — *(Zhiyang Zhang, Junda She, Kuo Cai, Bo Chen, Shiyao Wang, Xinchen Luo, Qiang Luo, Ruiming Tang, Han Li, Kun Gai, Guorui Zhou — likely industry labs)*
   * Link: [arxiv.org/abs/2601.06798](https://arxiv.org/abs/2601.06798)
   * TL;DR: Uses structured Term Identifiers (TIDs) — semantic-rich standardized text keywords — as item IDs for generative recommendation
   * Key techniques:
     - Context-aware term generation (convert item metadata to canonical TIDs)
     - Hybrid instruction fine-tuning (co-optimizes term internalization and sequential recommendation)
     - Elastic identifier grounding (robust item mapping despite ID variations)
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — TID is a middle ground between text and SID; idea is solid but incremental over existing Semantic ID work
     - **Fairness: 6/10** — Term standardization could introduce systematic bias from term vocabulary design
     - **Robustness: 7/10** — Elastic grounding handles ID variation; TIDs are more robust than pure SIDs
     - **Impact: 7/10** — Addresses a real industrial bottleneck (SID semantic gap); from Kuaishou/industry team
     - **Opensource?: 8/10** — Official repo (github.com/ZY0025/GRLM), 36 ⭐, well-documented, complete implementation with training/eval scripts

5. **R3-VAE: Reference Vector-Guided Rating Residual Quantization VAE for Generative Recommendation**
   * Affiliation: — *(Qiang Wan, Ze Yang, Dawei Yang, Ying Fan, Xin Yan, Siyang Liu)*
   * Link: [arxiv.org/abs/2604.11440](https://arxiv.org/abs/2604.11440)
   * TL;DR: VAE-based generative recommendation with residual quantization guided by reference vectors
   * Key techniques:
     - Reference vector guidance (anchors quantization centroids with collaborative filtering signals)
     - Rating residual quantization (explicitly models rating information in the latent space)
     - VAE generative framework for recommendation
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 6/10** — Residual quantization + reference guidance is a moderate extension of existing VAE rec work
     - **Fairness: 5/10** — Not addressed; standard VAE collaborative filtering may have popularity bias
     - **Robustness: 6/10** — VAEs are generally stable; residual quantization adds some robustness to rating noise
     - **Impact: 5/10** — More niche; VAE-based generative rec is less prominent than LLM/RL approaches currently
     - **Opensource?: 7/10** — Repo (github.com/wwqq/R3-VAE), 14 ⭐, clean code structure, matches paper well, has training scripts

---

## By Keyword

### RL / Reinforcement Learning
- ReRec: Reasoning-Augmented LLM-based Recommendation Assistant
- Generative Reasoning Re-ranker (GR2)
- ReCast
- Objective Shaping with Hard Negatives

### Reasoning
- ReRec
- VRec (Verifiable Reasoning)
- GR2
- GraphRAG-IRL

### Generative Recommendation / VAE
- R3-VAE
- ReCast
- Deep Interest Mining (SemanticID)
- BITRec (Modeling Behavioral Intensity and Transitions)

### LLM-based Recommendation
- ReRec
- VRec
- GRLM (Structured Term IDs)
- MARC (Modular Representation Compression)
- MLTFR (Multi-LLM Token Filtering)
- Rethinking Semantic Collaborative Integration
- DC4SR (Disagreement as Signals)

### Re-ranking
- GR2
- ResRank
- GraphRAG-IRL (LLM re-ranking)

### Semantic / Structured IDs
- GRLM
- Deep Interest Mining (SemanticID)

### Retrieval / Representation
- ResRank (retrieval + reranking)
- MARC (LLM representation compression)

### Graph-based Recommendation
- GraphRAG-IRL

### Distributed Training / Systems
- FreeScale (Distributed Training for Sequence Recommendation)

### Sequential Modeling / RoPE
- SIREN-RoPE (Learning to Rotate)

### Data Generation / Synthetic Data
- SAGE (Tabular Data Generation)

### Multi-behavior Recommendation
- BITRec

### Denoising
- DC4SR (Disagreement as Signals)

---

## By Affiliation

| Affiliation | Papers |
|---|---|
| **Meta** | Generative Reasoning Re-ranker (GR2) |
| **LinkedIn** | SIREN-RoPE (Learning to Rotate) |
| **Ant Group** | BITRec (Modeling Behavioral Intensity and Transitions) |
| **ACL 2026** | ReRec, SAGE |
| **SIGIR 2026** | MARC, Rethinking Semantic Collaborative Integration |
| **MLSys 2026** | FreeScale |
| *(TBD)* | VRec, GRLM, R3-VAE, ReCast, Objective Shaping, GraphRAG-IRL, MLTFR, ResRank, Deep Interest Mining, DC4SR |
