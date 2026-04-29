# Awesome Generative Recommendation System (RecSys)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

## Papers April 29

> **Note:** Only 3 new generative recommendation papers were found in the last 24 hours (less than the minimum 5 required).

1. **Harmonizing Generative Retrieval and Ranking in Chain-of-Recommendation (RecoChain)**
   * Affiliation: Nanjing, China (Yu Liu, Jiangxia Cao)
   * Link: [arxiv.org/abs/2604.25787](https://arxiv.org/abs/2604.25787)
   * Venue: arXiv preprint, April 28, 2026
   * TL;DR: RecoChain unifies generative retrieval and ranking in a single Transformer backbone for sequential recommendation
   * Key techniques:
     - Chain-of-Recommendation paradigm
     - Unified generative retrieval and ranking
     - Hierarchical semantic ID prediction
     - SIM-based ranking process
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 7/10** — Novel unified framework addressing the gap between generative retrieval and ranking
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Unified framework improves training stability
     - **Impact: 7/10** — From NJUST/Kuaishou, provides unified generative recommendation solution
     - **Opensource?: 0/10** — No public code found

2. **From Local Indices to Global Identifiers: Generative Reranking for Recommender Systems via Global Action Space (GloRank)**
   * Affiliation: City University of Hong Kong; Kuaishou; UC San Diego; etc.
   * Link: [arxiv.org/abs/2604.25291](https://arxiv.org/abs/2604.25291)
   * Venue: arXiv preprint, April 28, 2026
   * TL;DR: GloRank shifts reranking from selecting local indices to generating global identifiers via generative framework
   * Key techniques:
     - Global Action Space Ranker (GloRank)
     - Generative reranking paradigm
     - Supervised pre-training + RL post-training
     - Cold-start robust design
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Novel global action space for reranking, addresses semantic inconsistency
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Robust to cold-start scenarios, decouples scoring from input order
     - **Impact: 8/10** — From Kuaishou/CityU/UC San Diego, two-stage optimization
     - **Opensource?: 0/10** — No public code found

3. **Action-Aware Generative Sequence Modeling for Short Video Recommendation (A2Gen)**
   * Affiliation: Kuaishou Inc., Beihang University
   * Link: [arxiv.org/abs/2604.25834](https://arxiv.org/abs/2604.25834)
   * Venue: SIGIR 2026
   * TL;DR: A2Gen refines user actions along temporal dimension for short video recommendation, deployed at Kuaishou serving 400M+ users daily
   * Key techniques:
     - Action-Aware Generative Sequence Network (A2Gen)
     - Context-aware Attention Module (CAM)
     - Hierarchical Sequence Encoder (HSE)
     - Action-seq Autoregressive Generator (AAG)
   * Scores (Novelty / Fairness / Robustness / Impact / Opensource?):
     - **Novelty: 8/10** — Novel action-aware generative sequence modeling for short video recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed at scale (400M+ users), significant online A/B test gains (+0.34% watch time, +8.1% interaction rate)
     - **Impact: 9/10** — SIGIR 2026, industrial deployment at Kuaishou
     - **Opensource?: 0/10** — No public code (industrial deployment)

---

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

## Papers Before April

1. **OpenOneRec Technical Report**
   * Affiliation: Kuaishou (Guorui Zhou, Honghui Bao, Jiaming Huang, et al., 47 authors total)
   * Link: [arxiv.org/abs/2512.24762](https://arxiv.org/abs/2512.24762)
   * Venue: arXiv preprint, December 2025 (v2 revised February 2026)
   * TL;DR: Open-source end-to-end generative recommendation framework with RecIF-Bench benchmark and OneRec-Foundation model family (1.7B/8B parameters)
   * Key techniques:
     - RecIF-Bench: comprehensive benchmark covering 8 tasks from basic prediction to complex reasoning
     - Large-scale open dataset: 960K interactions, 160K users
     - Full training pipeline: data processing, collaborative pre-training, post-training
     - Model scaling with catastrophic forgetting mitigation
     - OneRec-Foundation models (1.7B/8B) achieving SOTA on RecIF-Bench
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — GitHub: https://github.com/Kuaishou-OneRec/OpenOneRec; complete training pipeline with data processing, pre-training, and post-training code; well-documented; active maintenance
     - **Novelty: 8/10** — First open-source framework bridging recommendation systems and LLMs; RecIF-Bench fills evaluation gap
     - **Fairness: 5/10** — Not explicitly addressed; open data/pretrained models could help fairness research
     - **Robustness: 8/10** — Comprehensive evaluation on 8 diverse tasks; demonstrated scaling behavior
     - **Impact: 9/10** — From Kuaishou production team; 26.8% avg Recall@10 improvement on Amazon transfer learning; high open-source value for community

2. **OneMall: One Architecture, More Scenarios — End-to-End Generative Recommender Family at Kuaishou E-Commerce**
   * Affiliation: Kuaishou (Kun Zhang, Jingming Zhang, Wei Cheng, et al., 32 authors total)
   * Link: [arxiv.org/abs/2601.21770](https://arxiv.org/abs/2601.21770)
   * Venue: arXiv preprint, January 2026 (v2 revised February 2026)
   * TL;DR: End-to-end generative recommendation framework for Kuaishou e-commerce, unifying product cards, short videos, and live streaming via Transformer architecture + RL pipeline
   * Key techniques:
     - E-commerce Semantic Tokenizer: captures real-world semantics and cross-scenario business relationships
     - Transformer-based architecture: Query-Former (long-sequence compression), Cross-Attention (multi-behavior fusion), Sparse MoE (scalable autoregressive generation)
     - Reinforcement Learning Pipeline: connects retrieval and ranking models with end-to-end policy optimization
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Systematically unifies multiple e-commerce scenarios into one generative framework; novel semantic tokenizer design
     - **Fairness: 5/10** — Not explicitly addressed; unified model may propagate biases across scenarios
     - **Robustness: 8/10** — Deployed on 400M+ DAU; consistent improvements across all e-commerce scenarios (GMV +13.01%, order volume +15.32%/+2.78%)
     - **Impact: 9/10** — Deployed at Kuaishou scale; significant business metrics improvements; high industrial relevance

3. **OneRec-Think: In-Text Reasoning for Generative Recommendation**
   * Affiliation: Kuaishou (Zhanyu Liu, Shiyao Wang, Xingmei Wang, et al., 26 authors total)
   * Link: [arxiv.org/abs/2510.11639](https://arxiv.org/abs/2510.11639)
   * Venue: arXiv preprint, October 2025 (v2 revised November 2025)
   * TL;DR: Unified framework integrating conversation, reasoning, and personalized recommendation with explicit text-based reasoning capabilities for generative recommendation
   * Key techniques:
     - Item-Textual Alignment: cross-modal alignment for semantic grounding
     - Reasoning Scaffolding: mechanism to activate LLM reasoning in recommendation context
     - Recommendation-specific Reward Function: considers multi-validity nature of user preferences
     - "Think-Ahead" architecture: enables effective industrial deployment
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8/10** — GitHub: https://github.com/wangshy31/OneRec-Think; 255⭐; complete implementation (basemodel/data/train/test); Apache-2.0 license; from paper author Shiyao Wang
     - **Novelty: 9/10** — First to introduce explicit text-based reasoning into generative recommendation; "Think-Ahead" architecture is novel
     - **Fairness: 5/10** — Not explicitly addressed; reasoning may inherit LLM biases
     - **Robustness: 8/10** — Explicit reasoning improves interpretability; validated on Kuaishou with +0.159% App Stay Time
     - **Impact: 9/10** — From Kuaishou; SOTA on public benchmarks; successful industrial deployment

4. **OneRec-V2 Technical Report**
   * Affiliation: Kuaishou (Guorui Zhou, Hengrui Hu, Hongtao Cheng, et al., 75 authors total)
   * Link: [arxiv.org/abs/2508.20900](https://arxiv.org/abs/2508.20900)
   * Venue: arXiv preprint, August 2025 (v4 revised October 2025)
   * TL;DR: Lazy decoder-only architecture reducing 94% computation with real-user-interaction-based preference alignment for scalable generative recommendation
   * Key techniques:
     - Lazy Decoder-Only Architecture: eliminates encoder bottleneck, reduces 94% computation, 90% training resources
     - Duration-Aware Reward Shaping: aligns with real-world user feedback
     - Adaptive Ratio Clipping: improves RL training stability
     - Model scaling to 8B parameters
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (Meta paper style, industry team)
     - **Novelty: 8/10** — Lazy decoder-only architecture is novel for generative recommendation; addresses key scalability challenges
     - **Fairness: 5/10** — Not discussed; real-user-interaction-based alignment may have bias concerns
     - **Robustness: 8/10** — Extensive A/B testing on Kuaishou; +0.467%/+0.741% App Stay Time
     - **Impact: 9/10** — From Kuaishou; significant engineering contribution; deployed at scale

5. **MiniOneRec: An Open-Source Framework for Scaling Generative Recommendation**
   * Affiliation: USTC (Xiaoyu Kong, Leheng Sheng, Junfei Tan, Yuxin Chen, Jiancan Wu, An Zhang, Xiang Wang, Xiangnan He)
   * Link: [arxiv.org/abs/2510.24431](https://arxiv.org/abs/2510.24431)
   * Venue: arXiv preprint, October 2025
   * TL;DR: First fully open-source generative recommendation framework with end-to-end workflow (SID construction, SFT, RL) validating scaling laws on public benchmarks
   * Key techniques:
     - Semantic ID (SID) construction via Residual Quantized VAE
     - Autoregressive Transformer for generative recommendation
     - Supervised Fine-Tuning on public datasets (Amazon Review)
     - Recommendation-oriented RL with constrained decoding and hybrid rewards
     - Full-process SID alignment
     - Scaling experiments (0.5B to 7B parameters)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 10/10** — GitHub: https://github.com/AkaliKong/MiniOneRec; first complete open-source framework; full end-to-end workflow; well-documented; active maintenance; 1.5K+ stars
     - **Novelty: 7/10** — First fully open-source implementation; validates scaling laws for generative recommendation on public benchmarks
     - **Fairness: 5/10** — Not explicitly addressed; open framework enables fairness research
     - **Robustness: 7/10** — Validated scaling behavior; hybrid rewards improve ranking accuracy and candidate diversity
     - **Impact: 8/10** — From USTC (Xiangnan He's team); high open-source value; enables reproducible research

6. **UniGRec: Unified Generative Recommendation with Soft Identifiers for End-to-End Optimization**
   * Affiliation: USTC (Jialei Li, Yang Zhang, Yimeng Bai, Shuai Zhu, Ziqi Xue, Xiaoyan Zhao, Dingxian Wang, Frank Yang, Andrew Rabinovich, Xiangnan He)
   * Link: [arxiv.org/abs/2601.17438](https://arxiv.org/abs/2601.17438)
   * Venue: arXiv preprint, January 2026
   * TL;DR: Unifies tokenizer and recommender via differentiable soft identifiers with end-to-end joint training, addressing training-inference mismatch and codeword collapse
   * Key techniques:
     - Differentiable Soft Identifiers: enables end-to-end joint training of tokenizer and recommender
     - Annealed Inference Alignment: smoothly bridges soft training and hard inference
     - Codeword Uniformity Regularization: prevents identifier collapse and encourages codebook diversity
     - Dual Collaborative Distillation: distills collaborative priors from lightweight teacher model
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8/10** — GitHub: https://github.com/Jialei-03/UniGRec; code matches paper; good documentation; complete implementation
     - **Novelty: 8/10** — Soft identifiers for end-to-end unification is novel; effectively addresses training-inference mismatch
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Codeword uniformity regularization prevents collapse; dual distillation improves stability
     - **Impact: 7/10** — From USTC (Xiangnan He's team); novel technical approach; strong empirical results

7. **Rec-R1: Bridging Generative Large Language Models and User-Centric Recommendation Systems via Reinforcement Learning**
   * Affiliation: UIUC Illinois (Jiacheng Lin, Tian Wang, Kun Qian)
   * Link: [arxiv.org/abs/2503.24289](https://arxiv.org/abs/2503.24289)
   * Venue: arXiv preprint, March 2025 (v4 revised January 2026)
   * TL;DR: General RL framework bridging LLMs and recommendation systems via closed-loop optimization using feedback from fixed black-box recommendation models
   * Key techniques:
     - Reinforcement Learning framework with closed-loop optimization
     - Black-box recommendation model feedback (no synthetic data needed)
     - Task-agnostic framework supporting different recommendation tasks
     - Preserves LLM general capabilities (avoids catastrophic forgetting)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — GitHub: https://github.com/linjc16/Rec-R1; code available but may need updates for latest paper version
     - **Novelty: 8/10** — Novel approach using black-box rec model feedback for RL; avoids expensive data distillation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Preserves LLM general capabilities; outperforms prompting and SFT baselines
     - **Impact: 8/10** — From UIUC; novel RL framework for LLM-recsys bridging; strong empirical results

8. **RelayGR: Scaling Long-Sequence Generative Recommendation via Cross-Stage Relay-Race Inference**
   * Affiliation: Huawei Cloud (Jiarui Wang, Huichao Chai, Yuanhang Zhang, et al., 41 authors total)
   * Link: [arxiv.org/abs/2601.01712](https://arxiv.org/abs/2601.01712)
   * Venue: arXiv preprint, January 2026
   * TL;DR: Production system for GR with HBM-based relay-race inference, enabling longer sequences within strict latency SLO via prefix KV cache reuse
   * Key techniques:
     - Sequence-aware trigger: selective prefix caching based on risk assessment
     - Affinity-aware router: co-locates pre-inference and ranking on same instance
     - Memory-aware expander: uses server local DRAM for cross-request reuse
     - HBM-based relay-race inference with prefix KV cache reuse
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (Huawei Cloud production system)
     - **Novelty: 8/10** — Creative system design for long-sequence GR in production; relay-race inference is novel
     - **Fairness: 4/10** — Not relevant to fairness; pure systems optimization
     - **Robustness: 9/10** — Deployed on Huawei Ascend NPUs; 1.5x sequence length increase, 3.6x SLO-compliant throughput improvement
     - **Impact: 8/10** — Huawei Cloud production system; significant engineering contribution for industrial GR deployment

9. **Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner)**
   * Affiliation: NUS (Yingzhi He, Yan Sun, Junfei Tan, Yuxin Chen, Xiaoyu Kong, Chunxu Shen, Xiang Wang, An Zhang, Tat-Seng Chua)
   * Link: [arxiv.org/abs/2603.23183](https://arxiv.org/abs/2603.23183)
   * Venue: arXiv preprint, March 2026
   * TL;DR: Two-stage framework (SIDReasoner) that elicits reasoning over SIDs by strengthening SID-language alignment and outcome-driven RL optimization
   * Key techniques:
     - Stage 1: Multi-task training with teacher-model-synthesized SID-centric corpus for SID-language alignment
     - Stage 2: Outcome-driven RL optimization for effective reasoning without explicit reasoning annotations
     - Transferable LLM reasoning capabilities for SID-based recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 9/10** — First to address reasoning over SIDs; two-stage framework is novel and well-designed
     - **Fairness: 5/10** — Not explicitly addressed; SID-language alignment may have bias concerns
     - **Robustness: 8/10** — Outcome-driven RL avoids reliance on reasoning annotations; strong empirical results on 3 datasets
     - **Impact: 8/10** — From NUS (Tat-Seng Chua's team); addresses key challenge in SID-based generative recommendation

10. **MuonRec: Shifting the Optimizer Paradigm Beyond Adam in Scalable Generative Recommendation**
    * Affiliation: Shanghai JTU / Kuaishou (Rong Shan, Aofan Yu, Bo Chen, Kuo Cai, Qiang Luo, Ruiming Tang, Han Li, Weiwen Liu, Weinan Zhang, Jianghao Lin)
    * Link: [arxiv.org/abs/2603.00416](https://arxiv.org/abs/2603.00416)
    * Venue: arXiv preprint, February 2026
    * TL;DR: First framework bringing Muon optimizer to RecSys training, reducing 32.4% training steps while improving NDCG@10 by 12.6% on average
    * Key techniques:
      - Muon optimizer: orthogonal momentum updates via Newton-Schulz iteration
      - Open-source training solution for recommendation models
      - Evaluation on both traditional sequential recommenders and modern generative recommenders
    * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
      - **Opensource?: 8/10** — Code available (link in paper); matches paper description; good reproducibility
      - **Novelty: 8/10** — First to apply Muon optimizer to recommendation systems; significant training efficiency improvement
      - **Fairness: 4/10** — Not relevant to fairness; optimizer design
      - **Robustness: 8/10** — Consistent improvement over Adam/AdamW baselines; 32.4% training step reduction
      - **Impact: 8/10** — From Shanghai JTU/Kuaishou; practical optimization contribution with significant efficiency gains

11. **[STATIC] Vectorizing the Trie: Efficient Constrained Decoding for LLM-based Generative Retrieval on Accelerators**
    * Affiliation: Youtube / Google Research (Zhengyang Su, Isay Katsman, Yueqi Wang, Ruining He, et al., 13 authors total)
    * Link: [arxiv.org/abs/2602.22647](https://arxiv.org/abs/2602.22647)
    * Venue: arXiv preprint, February 2026
    * TL;DR: STATIC converts irregular Trie traversal to fully vectorized sparse matrix operations via CSR matrix representation, achieving 948x speedup over CPU Trie
    * Key techniques:
      - STATIC (Sparse Transition Matrix-Accelerated Trie Index for Constrained Decoding)
      - Flattens prefix tree (Trie) into static Compressed Sparse Row (CSR) matrix
      - Fully vectorized sparse matrix operations native to TPUs/GPUs
      - Branch-free decoding on hardware accelerators
    * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
      - **Opensource?: 9/10** — GitHub: https://github.com/youtube/static-constraint-decoding; 212⭐; complete implementation (JAX + PyTorch); well-documented; from Youtube/Google Research
      - **Novelty: 9/10** — Highly novel approach to constrained decoding; vectorization of Trie is clever and effective
      - **Fairness: 4/10** — Not relevant to fairness; systems optimization
      - **Robustness: 9/10** — Deployed on large-scale industrial video recommendation platform; 948x speedup over CPU Trie; 0.25% inference time overhead
      - **Impact: 9/10** — From Youtube/Google Research; first production-scale constrained generative retrieval deployment; significant engineering contribution

12. **Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization (GRAD)**
    * Affiliation: Meituan (Yu Lei, Jiayang Zhao, Yilei Zhao, Zhaoqi Zhang, Linyou Cai, Qianlong Xie, Xingxing Wang)
    * Link: [arxiv.org/abs/2508.02002](https://arxiv.org/abs/2508.02002)
    * Venue: KDD 2026
    * TL;DR: GRAD is a scalable foundation model for automated bidding with Action-MoE and causal Transformer value estimator, deployed at Meituan with GMV +2.18% and ROI +10.68%
    * Key techniques:
      - GRAD (Generative Reward-driven Ad-bidding with Mixture-of-Experts)
      - Action-Mixture-of-Experts module for diverse bidding action exploration
      - Causal Transformer-based value estimator for constraint-aware optimization
      - Conditional generative model for bidding trajectory generation
    * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
      - **Opensource?: 0/10** — No public code found
      - **Novelty: 8/10** — Novel application of generative models to ad bidding; Action-MoE is creative design
      - **Fairness: 5/10** — Not explicitly addressed; ad bidding optimization may have fairness implications
      - **Robustness: 8/10** — Deployed at Meituan; GMV +2.18%, ROI +10.68%; handles CPM and ROI constraints
      - **Impact: 8/10** — KDD 2026; from Meituan; significant business impact; novel approach to ad bidding

13. **Rank-GRPO: Training LLM-based Conversational Recommender Systems with Reinforcement Learning (ConvRec-R1)**
    * Affiliation: Netflix (Yaochen Zhu, Harald Steck, Dawen Liang, et al.)
    * Link: [arxiv.org/abs/2510.20150](https://arxiv.org/abs/2510.20150)
    * Venue: ICLR 2026
    * TL;DR: ConvRec-R1 is a two-stage framework with Rank-GRPO, a principled extension of GRPO for rank-style outputs, achieving faster convergence and higher Recall/NDCG
    * Key techniques:
      - ConvRec-R1: two-stage end-to-end training framework
      - Remap-Reflect-Adjust pipeline for high-quality behavior cloning dataset construction
      - Rank-GRPO: treats each ranking as a unit, redefines rewards, introduces rank-level importance ratios
      - Two-stage training: behavior cloning warm-up + Rank-GRPO fine-tuning
    * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
      - **Opensource?: 9/10** — GitHub: https://github.com/yaochenzhu/Rank-GRPO; complete training/alignment/evaluation pipeline; well-documented; from Netflix
      - **Novelty: 9/10** — Rank-GRPO is a principled and novel extension of GRPO for ranking tasks; clever design
      - **Fairness: 5/10** — Not explicitly addressed
      - **Robustness: 8/10** — Faster convergence than GRPO baselines; rank-level importance ratios stabilize policy updates
      - **Impact: 9/10** — ICLR 2026; from Netflix; novel RL algorithm for conversational recommendation

---

## By Keyword

### RL / Reinforcement Learning
- ReRec: Reasoning-Augmented LLM-based Recommendation Assistant
- Generative Reasoning Re-ranker (GR2)
- ReCast
- Objective Shaping with Hard Negatives
- OpenOneRec
- OneMall
- OneRec-Think
- OneRec-V2
- MiniOneRec
- Rec-R1
- Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner)
- Rank-GRPO
- Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization (GRAD)

### Generative Retrieval / Ranking
- Harmonizing Generative Retrieval and Ranking in Chain-of-Recommendation (RecoChain)

### Reasoning
- ReRec
- VRec (Verifiable Reasoning)
- GR2
- GraphRAG-IRL
- Reasoning over Semantic IDs Enhances Generative Recommendation

### Generative Recommendation / VAE
- R3-VAE
- ReCast
- Deep Interest Mining (SemanticID)
- BITRec (Modeling Behavioral Intensity and Transitions)
- A2Gen (Action-Aware Generative Sequence Modeling)

### LLM-based Recommendation
- ReRec
- VRec
- GRLM (Structured Term IDs)
- MARC (Modular Representation Compression)
- MLTFR (Multi-LLM Token Filtering)
- Rethinking Semantic Collaborative Integration
- DC4SR (Disagreement as Signals)
- A2Gen (Action-Aware Generative Sequence Modeling)

### Re-ranking
- GR2
- ResRank
- GraphRAG-IRL (LLM re-ranking)
- GloRank (From Local Indices to Global Identifiers)

### Semantic / Structured IDs
- GRLM
- Deep Interest Mining (SemanticID)
- Reasoning over Semantic IDs Enhances Generative Recommendation

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

### Inference
- OpenOneRec
- RelayGR
- [STATIC] Vectorizing the Trie

### Model / Architecture
- OpenOneRec
- OneMall
- MiniOneRec
- UniGRec

### MoE
- OneMall
- Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization

### Optimizer
- MuonRec

---

## By Affiliation

| Affiliation | Papers |
|---|---|
| **Meta** | Generative Reasoning Re-ranker (GR2) |
| **LinkedIn** | SIREN-RoPE (Learning to Rotate) |
| **Ant Group** | BITRec (Modeling Behavioral Intensity and Transitions) |
| **NJUST / Nanjing** | Harmonizing Generative Retrieval (RecoChain) |
| **City University of Hong Kong** | GloRank (From Local Indices to Global Identifiers) |
| **Beihang University** | A2Gen (Action-Aware Generative Sequence Modeling) |
| **Kuaishou** | OpenOneRec · OneMall · OneRec-Think · OneRec-V2 · A2Gen · GloRank |
| **USTC** | MiniOneRec · UniGRec |
| **UIUC Illinois** | Rec-R1 |
| **Huawei Cloud** | RelayGR |
| **NUS** | Reasoning over Semantic IDs |
| **Shanghai JTU** | MuonRec |
| **Youtube** | [STATIC] Vectorizing the Trie |
| **Meituan** | Generative Large-Scale Pre-trained Models for Automated Ad Bidding |
| **Netflix** | Rank-GRPO |
| **ACL 2026** | ReRec, SAGE |
| **SIGIR 2026** | MARC, Rethinking Semantic Collaborative Integration, A2Gen |
| **MLSys 2026** | FreeScale |
| *(TBD)* | VRec, GRLM, R3-VAE, ReCast, Objective Shaping, GraphRAG-IRL, MLTFR, ResRank, Deep Interest Mining, DC4SR |
