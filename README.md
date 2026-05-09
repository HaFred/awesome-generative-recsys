# Awesome Generative Recommendation System (RecSys)

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

## Quick Indexing
- [By Opensource](#by-opensource)
- [By Keyword](#by-keyword)
- [By Affiliation](#by-affiliation)

---
## Papers May 09:

> **Note:** No new generative recommendation papers were found in the last 24 hours (May 8-9, 2026). Following the fallback procedure, 5 papers from the last 3 months (October 2025 - May 2026) are included to meet the minimum 5 papers requirement.

1. **TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation**
   * Affiliation: Southeast University; Tsinghua University; Shenzhen University; Fudan University; Zhejiang University; Swinburne University of Technology
   * Link: [arxiv.org/abs/2605.05249](https://arxiv.org/abs/2605.05249)
   * Venue: arXiv preprint, May 5, 2026
   * TL;DR: TriAlignGR is a unified multitask-multimodal framework that resolves SID Content Degradation and SID Semantic Opacity through cross-modal semantic alignment, multimodal deep interest mining, and triangular multitask learning
   * Key techniques:
     - Cross-Modal Semantic Alignment (CMSA): integrates visual content into SID construction
     - Multimodal Deep Interest Mining (MDIM): leverages LLM Chain-of-Thought reasoning to extract latent user intents
     - Triangular Multitask (TMT): jointly trains on eight complementary generation tasks under a single autoregressive loss
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Multimodal SID is novel; triangular multitask is a creative solution to SID Semantic Opacity
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Multimodal integration should improve robustness; validated on experiments
     - **Impact: 8/10** — From multiple universities; multimodal generative recommendation is a growing area

2. **One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving**
   * Affiliation: — *(Wenjun Yu, Shuguang Han, Amelie Chi Zhou — institutions TBD)*
   * Link: [arxiv.org/abs/2605.04450](https://arxiv.org/abs/2605.04450)
   * Venue: arXiv preprint, May 6, 2026
   * TL;DR: HELM jointly manages HBM allocation and request routing for generative recommender inference, reducing P99 latency by 24-38% over static policies
   * Key techniques:
     - Adaptive Memory Allocation: three-layer PPO-based controller for dynamic EMB-KV allocation
     - EMB-KV-Aware Scheduling: routes requests by jointly considering KV residency, embedding locality, and node load
     - Online reallocation without H2D refill traffic on the critical path
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (systems paper)
     - **Novelty: 7/10** — Novel adaptive HBM partitioning for generative recommender inference; addresses key latency bottleneck
     - **Fairness: 4/10** — Not relevant to fairness; pure systems optimization work
     - **Robustness: 9/10** — 24-38% P99 latency reduction; 93.5-99.6% SLO satisfaction; validated on 32-node A100 cluster
     - **Impact: 8/10** — Addresses key serving bottleneck for industrial GR deployment; significant engineering contribution

3. **PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation**
   * Affiliation: — *(Dengzhao Fang, Jingtong Gao, Yu Li, Xiangyu Zhao, Yi Chang — institutions TBD)*
   * Link: [arxiv.org/abs/2601.16556](https://arxiv.org/abs/2601.16556)
   * Venue: arXiv preprint, January 23, 2026
   * TL;DR: PRISM addresses impure semantic tokenization and lossy generation in generative sequential recommendation via purified representation and integrated semantic modeling
   * Key techniques:
     - Purified Semantic Quantizer: constructs robust codebook via adaptive collaborative denoising and hierarchical semantic anchoring
     - Integrated Semantic Recommender: incorporates dynamic semantic integration and semantic structure alignment
     - Two-stage approach: purified tokenization + integrated generation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 5.5/10** — GitHub: https://github.com/DengzhaoFang/PRISM; code structure is clear but documentation is brief; 0 stars/forks; limited community engagement
     - **Novelty: 8/10** — Purified quantization + integrated semantic modeling is a novel approach to GSR
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Outperforms SOTAs on 4 real-world datasets; substantial performance gains in high-sparsity scenarios
     - **Impact: 8/10** — Addresses key GSR limitations; from CityU/Jilin University

4. **Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)**
   * Affiliation: — *(Zhefan Wang, Guokai Yan, Jinbei Yu, Siyu Gu, Jingyan Chen, Peng Jiang, Zhiqiang Guo, Min Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2511.03155](https://arxiv.org/abs/2511.03155)
   * Venue: arXiv preprint, November 5, 2025
   * TL;DR: GAMER is a novel generative framework for multi-behavior sequential recommendation with cross-level interaction layer and sequential augmentation strategy
   * Key techniques:
     - Cross-Level Interaction Layer: captures hierarchical dependencies among behaviors
     - Sequential Augmentation Strategy: enhances robustness in training
     - ShortVideoAD Dataset: large-scale multi-behavior dataset from short-video platform
     - Decoder-only backbone for generative recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7.5/10** — GitHub: https://github.com/wzf2000/GAMER; well-structured code with good documentation; 210 commits; 30 stars; no tests or CI/CD
     - **Novelty: 7/10** — Hierarchical behavior modeling for generative rec is novel; cross-level interaction is creative
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Sequential augmentation enhances robustness; validated on multiple datasets
     - **Impact: 7/10** — Releases ShortVideoAD dataset; novel approach to multi-behavior generative recommendation

5. **On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)**
   * Affiliation: — *(Wenyu Mao, Jiancan Wu, Guoqing Hu, Zhengyi Yang, Wei Ji, Xiang Wang — institutions TBD)*
   * Link: [arxiv.org/abs/2510.17245](https://arxiv.org/abs/2510.17245)
   * Venue: NeurIPS 2025
   * TL;DR: TA-Rec achieves one-step generation for diffusion-based recommenders via temporal consistency regularization and adaptive preference alignment, mitigating the efficiency-effectiveness trade-off
   * Key techniques:
     - Temporal Consistency Regularization (TCR): enforces consistency between denoising results across adjacent steps
     - Adaptive Preference Alignment (APA): aligns denoising process with user preference adaptively
     - Two-stage objective: pretraining (efficiency) + fine-tuning (effectiveness)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 6.5/10** — GitHub: https://github.com/maowenyu-11/TA-Rec; complete implementation but limited documentation; 9 commits; 9 stars
     - **Novelty: 8/10** — One-step generation for diffusion rec is novel; addresses key trade-off in diffusion-based recommenders
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — TCR + APA for stable training; mitigates discretization errors
     - **Impact: 7/10** — NeurIPS 2025; addresses efficiency-effectiveness trade-off in diffusion rec

---


## Papers May 08:

> **Note:** 3 generative recommendation papers identified (submitted May 7, 2026). All papers are newly added to the repository.

1. **Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)**
   * Affiliation: — *(Yupeng Hou, Haven Kim, Clark Mingxuan Ju, Eduardo Escoto, Neil Shah, Julian McAuley — institutions TBD)*
   * Link: [arxiv.org/abs/2605.06331](https://arxiv.org/abs/2605.06331)
   * Venue: arXiv preprint, May 7, 2026
   * TL;DR: Identifies expressiveness limits in autoregressive semantic ID generation and proposes Latte, which injects latent tokens before each SID to reshape the decoding space
   * Key techniques:
     - Theoretical analysis of tree-induced structural correlation in autoregressive SID generation
     - Latte: injects latent tokens before each semantic ID to create multiple latent-token-conditioned trees
     - Reshapes decoding space from single tree to multiple latent-conditioned trees
     - Addresses fundamental expressiveness limitation in generative recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 10/10** — GitHub: https://github.com/hyp1231/Latte; complete implementation available
     - **Novelty: 8/10** — First to identify and address expressiveness limits of autoregressive SID generation; theoretical contribution is significant
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — 3.45% average relative improvement on NDCG@10; validated on multiple datasets
     - **Impact: 8/10** — From Yupeng Hou, Neil Shah, Julian McAuley; significant theoretical contribution to generative recommendation

2. **Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA)**
   * Affiliation: Tencent (16 authors)
   * Link: [arxiv.org/abs/2605.05803](https://arxiv.org/abs/2605.05803)
   * Venue: arXiv preprint, May 7, 2026
   * TL;DR: UniVA aligns commercial value with generative recommendation for industrial advertising, using commercial SID tokenizer and value-guided beam search
   * Key techniques:
     - Commercial SID tokenizer: injects value-related attributes into SID construction
     - Generation-as-Ranking SID Decoder: supervised learning + eCPM-aware reinforcement learning
     - Value-guided personalized beam search with personalized trie tree constraints
     - Unified value alignment for generative recommendation in advertising
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial deployment at Tencent WeChat Channels)
     - **Novelty: 9/10** — First to address value alignment in generative recommendation for advertising; novel commercial SID tokenizer
     - **Fairness: 6/10** — Value optimization may indirectly affect fairness; not explicitly addressed
     - **Robustness: 9/10** — Deployed on Tencent WeChat Channels advertising platform; 37.04% Hit Rate@100 improvement; 1.5% GMV lift in online A/B tests
     - **Impact: 9/10** — From Tencent; significant industrial impact for generative recommendation in advertising

3. **Bridging Passive and Active: Enhancing Conversation Starter Recommendation via Active Expression Modeling (PA-Bridge)**
   * Affiliation: — *(Yiqing Wu, Haoming Li, Guanyu Jiang, Jiahao Liang, Yongchun Zhu, Jingwu Chen, Feng Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2605.05855](https://arxiv.org/abs/2605.05855)
   * Venue: SIGIR 2026
   * TL;DR: PA-Bridge bridges passive recommendation and active user expressions using adversarial distribution alignment and semantic discretization for conversation starter recommendation
   * Key techniques:
     - Adversarial distribution aligner: bridges gap between passive recommendations and active expressions
     - Semantic discretizer: enables popularity debiasing algorithms
     - Harnesses user "free will" through active expressions (manually typed queries)
     - Breaks harmful echo chamber effect in conversational search
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel application of LLMs to conversation starter recommendation; adversarial alignment is interesting
     - **Fairness: 6/10** — Semantic discretizer enables popularity debiasing; addresses echo chamber effect
     - **Robustness: 7/10** — Online A/B tests show +0.54% Feature Penetration Rate and improved User Active Days
     - **Impact: 6/10** — SIGIR 2026; relevant to LLM-driven conversational recommendation but peripheral to core generative recommendation

---


## Papers May 07:

> **Note:** 6 new generative recommendation papers found in the last 24 hours (May 6-7, 2026). All papers are newly published and not previously included.

1. **CapsID: Soft-Routed Variable-Length Semantic IDs for Generative Recommendation**
   * Affiliation: — *(Wenzhuo Cheng, Menghang Gong, Qixin Guo, Hang Zheng, Zhaobin Yang, Jianguo Lou, Zhengwei Zheng — institutions TBD)*
   * Link: [arxiv.org/abs/2605.05096](https://arxiv.org/abs/2605.05096)
   * Venue: arXiv preprint, May 7, 2026
   * TL;DR: CapsID replaces hard residual quantization with capsule routing for soft SID assignment, enabling variable-length Semantic IDs with confidence-driven termination
   * Key techniques:
     - Capsule routing: probabilistic routing to multiple semantic capsules (not hard nearest-neighbor)
     - Residual updated by routed reconstruction (not single winning code)
     - SEMANTICBPE: composes adjacent SID tokens into reusable subwords by co-occurrence + embedding compatibility
     - Confidence-driven SID length (terminates when active capsule confidence is high)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Soft routing for SID is a novel alternative to hard RQ; addresses codeword collapse and boundary semantics
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — 9.6% Recall@10 improvement over ReSID; 51% inference latency of COBRA-style system; gains largest on tail items
     - **Impact: 8/10** — Addresses key SID tokenizer bottleneck; validated on 35M-item industrial catalog

2. **RecGPT-Mobile: On-Device Large Language Models for User Intent Understanding in Taobao Feed Recommendation**
   * Affiliation: Alibaba Group (Taobao)
   * Link: [arxiv.org/abs/2605.04726](https://arxiv.org/abs/2605.04726)
   * Venue: arXiv preprint, May 7, 2026
   * TL;DR: Deploys LLM directly on mobile devices for real-time user intent understanding and recommendation adjustment in Taobao feed
   * Key techniques:
     - On-device LLM deployment for mobile e-commerce
     - Lightweight LLM-based intent understanding agent
     - Real-time recommendation adjustment based on evolving user interests
     - Next-query prediction with reduced inference cost
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial deployment at Taobao)
     - **Novelty: 8/10** — First on-device LLM deployment for recommendation; novel approach to reducing cloud inference cost
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — On-device deployment enables real-time adjustment; validated with offline analyses and online experiments
     - **Impact: 9/10** — From Alibaba/Taobao; significant practical impact for mobile e-commerce recommendation

3. **Rethinking Convolutional Networks for Attribute-Aware Sequential Recommendation (ConvRec)**
   * Affiliation: — *(Shereen Elsayed, Ngoc Son Le, Ahmed Rashed, Lars Schmidt-Thieme — institutions TBD)*
   * Link: [arxiv.org/abs/2605.04723](https://arxiv.org/abs/2605.04723)
   * Venue: IJCAI-ECAI 2026
   * TL;DR: ConvRec uses convolutional layers with linear complexity to replace attention for efficient sequential recommendation with long user histories
   * Key techniques:
     - Convolutional layers in hierarchical, down-scaled fashion
     - Linear computational and memory complexity (vs. quadratic for attention)
     - Gradual neighborhood aggregation for diverse sequential pattern capture
     - Compact yet expressive sequence representation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8/10** — GitHub: https://github.com/ismll-research/ConvRec; complete implementation with datasets; well-documented
     - **Novelty: 7/10** — Convolution for sequential recommendation is not entirely new, but efficient linear-complexity design is valuable
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Linear complexity enables processing longer user histories; validated on 4 real-world datasets
     - **Impact: 7/10** — IJCAI-ECAI 2026; provides efficient alternative to attention-based sequential recommendation

4. **Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE)**
   * Affiliation: — *(Ruijun Chen, Chongming Gao, Jiawei Chen, Weiqin Yang, Xiangnan He — institutions TBD, likely USTC)*
   * Link: [arxiv.org/abs/2605.04559](https://arxiv.org/abs/2605.04559)
   * Venue: SIGIR 2026
   * TL;DR: BLADE introduces a Bayesian framework that continuously updates the target distribution by fusing historical priors with dynamic evidence, breaking the static BoN performance upper bound
   * Key techniques:
     - Bayesian List-wise Alignment (BLADE)
     - Dynamic target distribution update (fuses historical priors + current rollouts)
     - Self-evolving target adapts to model's growing capabilities
     - Addresses indiscriminate supervision and gradient decay in BoN Alignment
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — GitHub: https://github.com/RegionCh/BLADE; complete implementation; well-documented; SIGIR 2026
     - **Novelty: 9/10** — Bayesian framework for list-wise alignment is novel; breaks static BoN upper bound
     - **Fairness: 6/10** — Explicitly optimizes fairness metrics (Fairness in list-wise metrics)
     - **Robustness: 8/10** — Self-evolving target ensures sustained training signal; validated on 3 real-world datasets
     - **Impact: 9/10** — SIGIR 2026; from Xiangnan He's team (likely USTC); addresses key limitation of BoN Alignment

5. **Interests Burn-down Diffusion Process for Personalized Collaborative Filtering (StageCF)**
   * Affiliation: — *(Yifang Qin, Zhaobin Li, Arisa Watanabe, Wei Ju, Zhiping Xiao, Ming Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2605.05165](https://arxiv.org/abs/2605.05165)
   * Venue: arXiv preprint, May 7, 2026
   * TL;DR: Proposes "interests burn-down process" as a diffusion scheme tailored for collaborative filtering, with StageCF method demonstrating superior performance over generative and diffusion baselines
   * Key techniques:
     - Interests burn-down process (forward process modeling interest decay)
     - Reverse burn-up process (generates personalized recommendations)
     - StageCF method illustrating the burn-down diffusion process
     - Tailored diffusion scheme for interaction systems (not Gaussian noise)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel diffusion process tailored for CF; addresses incongruity between Gaussian noise and user interaction behavior
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 6/10** — Diffusion process is more aligned with CF tasks; validated on experiments against baselines
     - **Impact: 6/10** — Novel application of diffusion to CF; empirical results demonstrate effectiveness

6. **Revisiting General Map Search via Generative Point-of-Interest Retrieval (GenPOI)**
   * Affiliation: Tencent Map
   * Link: [arxiv.org/abs/2605.03397](https://arxiv.org/abs/2605.03397)
   * Venue: arXiv preprint, May 6, 2026
   * TL;DR: GenPOI uses LLM for generative POI retrieval with geo-semantic tokenization and proximity-aware constrained generation, handling underspecified queries in map search
   * Key techniques:
     - GenPOI (Generative POI retrieval framework)
     - Geo-Semantic POI Tokenization: encodes semantic and geographic context
     - Proximity-aware constrained generation: restricts decoding space for geospatial relevance
     - Heterogeneous context synergy for complex search intent inference
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial dataset from Tencent Map)
     - **Novelty: 7/10** — Novel generative paradigm for POI retrieval; addresses underspecified query challenge in map search
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Proximity-aware constrained generation ensures geospatial validity; validated on 10M+ POI scale
     - **Impact: 7/10** — From Tencent Map; novel application of generative recommendation to POI retrieval

---


## Papers May 06:

> **Note:** Only 1 new generative recommendation paper was found in the last 24 hours (May 5-6, 2026). Following the fallback procedure, 5 additional papers from the last 3 months (April-May 2026) are included to meet the minimum 5 papers requirement.

1. **On the Equivalence Between Auto-Regressive Next Token Prediction and Full-Item-Vocabulary Maximum Likelihood Estimation in Generative Recommendation--A Short Note**
   * Affiliation: — *(Yusheng Huang, Shuang Yang, Zhaojie Liu, Han Li — institutions TBD)*
   * Link: [arxiv.org/abs/2604.15739](https://arxiv.org/abs/2604.15739)
   * Venue: arXiv preprint, April 17, 2026
   * TL;DR: First formal proof that auto-regressive next-token prediction is mathematically equivalent to full-item-vocabulary MLE in generative recommendation
   * Key techniques:
     - Formal mathematical proof of AR-NTP and FV-MLE equivalence
     - Proof holds for both cascaded and parallel tokenizations
     - Theoretical foundation for industrial GR systems
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (theoretical paper)
     - **Novelty: 7/10** — First formal theoretical foundation for the dominant industrial GR paradigm
     - **Fairness: 4/10** — Not relevant to fairness; theoretical contribution
     - **Robustness: 6/10** — Theoretical proof; no empirical robustness evaluation
     - **Impact: 7/10** — Provides principled guidance for future GR system optimization

2. **SAGER: Self-Evolving User Policy Skills for Recommendation Agent**
   * Affiliation: — *(Zhen Tao, Riwei Lai, Chenyun Yu, Weixin Chen, Li Chen, Beibei Kong, Leicheng, Chengxiang Zhuo, Zang Li, Qingqiang Sun — institutions TBD)*
   * Link: [arxiv.org/abs/2604.14972](https://arxiv.org/abs/2604.14972)
   * Venue: arXiv preprint, April 16, 2026 (v2 revised April 21, 2026)
   * TL;DR: SAGER equips each user with a dedicated policy skill that evolves continuously through interaction, enabling personalized reasoning for recommendation agents
   * Key techniques:
     - Two-representation skill architecture (evolution substrate + inference-time injection)
     - Incremental contrastive chain-of-thought engine for reasoning flaw diagnosis
     - Skill-augmented listwise reasoning for fine-grained decision boundaries
     - Self-evolving recommendation agent framework
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — First recommendation agent with self-evolving policy skills; novel paradigm
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — State-of-the-art performance; gains orthogonal to memory accumulation
     - **Impact: 8/10** — Novel approach to personalizing reasoning process in recommendation agents

3. **Enhancing Local Life Service Recommendation with Agentic Reasoning in Large Language Model**
   * Affiliation: — *(Shiteng Cao, Xiaochong Lan, Yuwei Du, Jie Feng, Yinxing Liu, Xinlei Shi, Yong Li — institutions TBD)*
   * Link: [arxiv.org/abs/2604.14051](https://arxiv.org/abs/2604.14051)
   * Venue: arXiv preprint, April 15, 2026
   * TL;DR: Novel LLM-based framework that jointly performs living need prediction and service recommendation, with behavioral clustering and curriculum learning + RL
   * Key techniques:
     - Joint modeling of need prediction and service recommendation
     - Behavioral clustering for noise filtering in raw consumption data
     - Curriculum learning strategy combined with reinforcement learning
     - Sequential learning from need generation to category mapping to service selection
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel joint modeling of need prediction and service recommendation for local life scenarios
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Validated on local life service data; generalizes to long-tail scenarios
     - **Impact: 7/10** — From Tsinghua (Yong Li); novel LLM-based local life service recommendation

4. **Mitigating Collaborative Semantic ID Staleness in Generative Retrieval**
   * Affiliation: — *(Vladimir Baikalov, Iskander Bagautdinov, Sergey Muravyov — institutions TBD)*
   * Link: [arxiv.org/abs/2604.13273](https://arxiv.org/abs/2604.13273)
   * Venue: SIGIR 2026
   * TL;DR: Lightweight SID alignment update that mitigates SID staleness under temporal drift, enabling warm-start fine-tuning without full rebuild
   * Key techniques:
     - SID staleness analysis under strict chronological evaluation
     - Lightweight, model-agnostic SID alignment update
     - Aligning refreshed SIDs to existing SID vocabulary for compatibility
     - Warm-start fine-tuning without full rebuild-and-retrain pipeline
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — First to explicitly study SID staleness under temporal drift; novel alignment update
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — 8-9x retriever-training compute reduction; validated on 3 public benchmarks
     - **Impact: 9/10** — SIGIR 2026; addresses key practical problem in generative retrieval

5. **DUET: Joint Exploration of User Item Profiles in Recommendation System**
   * Affiliation: — *(Yue Chen, Yifei Sun, Lu Wang, Fangkai Yang, Pu Zhao, et al., 20 authors total — institutions TBD)*
   * Link: [arxiv.org/abs/2604.13801](https://arxiv.org/abs/2604.13801)
   * Venue: arXiv preprint, April 15, 2026
   * TL;DR: Duet jointly generates user and item profiles conditioned on both history and evidence, with RL-based optimization using downstream recommendation performance as feedback
   * Key techniques:
     - Interaction-aware profile generator (joint user-item profile generation)
     - Three-stage procedure: cue extraction → prompt expansion → profile generation
     - RL-based generation policy optimization with downstream performance feedback
     - Template-free profile exploration and semantic alignment
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel joint user-item profile generation; addresses semantic inconsistency
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Outperforms strong baselines on 3 real-world datasets
     - **Impact: 8/10** — From Microsoft Research (hinted by author names); novel approach to profile-based recommendation

6. **DynamicPO: Dynamic Preference Optimization for Recommendation**
   * Affiliation: — *(Xingyu Hu, Kai Zhang, Jiancan Wu, Shuli Wang, Chi Wang, Wenshuai Chen, Yinhua Zhu, Haitao Wang, Xingxing Wang, Xiang Wang — institutions TBD)*
   * Link: [arxiv.org/abs/2605.00327](https://arxiv.org/abs/2605.00327)
   * Venue: DASFAA 2026
   * TL;DR: DynamicPO prevents preference optimization collapse in LLM-based recommendation via dynamic boundary negative selection and dual-margin beta adjustment
   * Key techniques:
     - Dynamic Boundary Negative Selection (prioritizes informative negatives near decision boundary)
     - Dual-Margin Dynamic beta Adjustment (calibrates optimization strength per sample)
     - Theoretical analysis of preference optimization collapse
     - Lightweight and plug-and-play framework
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — GitHub: https://github.com/xingyuHuxingyu/DynamicPO; complete codebase; well-documented
     - **Novelty: 8/10** — Novel solution to preference optimization collapse; dynamic negative selection
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Prevents optimization collapse; negligible computational overhead; validated on 3 datasets
     - **Impact: 8/10** — DASFAA 2026; from Xiang Wang's team (USTC); practical optimization for LLM-based recommendation

---

## Papers May 05:

> **Note:** Only 1 new generative recommendation paper was found in the last 24 hours (May 4-5, 2026). Following the fallback procedure, 4 additional papers from the last 3 months (February-May 2026) are included to meet the minimum 5 papers requirement.

1. **Bridging Behavior and Semantics for Time-aware Cross-Domain Sequential Recommendation (BST-CDSR)**
   * Affiliation: — *(Zhida Qin, Zemu Liu, Haoyan Fu, Chong Zhang, Tianyu Huang, Yidong Li, Gangyi Ding — institutions TBD)*
   * Link: [arxiv.org/abs/2605.02369](https://arxiv.org/abs/2605.02369)
   * Venue: arXiv preprint, May 4, 2026
   * TL;DR: BST-CDSR bridges behavioral and semantic preferences using LLMs with temporal counterfactual enhancement for cross-domain sequential recommendation
   * Key techniques:
     - Behavioral preference evolution module with neural ODE for continuous-time preference modeling
     - Temporal counterfactual-enhanced semantic generator using LLMs
     - Time-aware semantic preference capture with discretized temporal interval tokens
     - Time-preference guided domain transfer module for adaptive transfer weight control
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel integration of LLMs with temporal semantics for cross-domain recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Validated on real-world datasets; handles domain transfer robustly
     - **Impact: 7/10** — Novel approach to cross-domain sequential recommendation with LLM integration

2. **Semantic Trimming and Auxiliary Multi-step Prediction for Generative Recommendation (STAMP)**
   * Affiliation: — *(Tianyu Zhan, Kairui Fu, Chengfei Lv, Zheqi Lv, Shengyu Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.05329](https://arxiv.org/abs/2604.05329)
   * Venue: arXiv preprint, April 7, 2026
   * TL;DR: STAMP addresses the Semantic Dilution Effect in generative recommendation via semantic adaptive pruning and multi-step auxiliary prediction
   * Key techniques:
     - Semantic Adaptive Pruning (SAP) for dynamic redundancy filtering
     - Multi-step Auxiliary Prediction (MAP) with multi-token objective
     - Dual-end optimization strategy for training efficiency and representation capability
     - Semantic dilution effect analysis and mitigation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel identification and solution to the Semantic Dilution Effect in generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — 1.23-1.38× speedup and 17.2%-54.7% VRAM reduction; validated on public and industrial datasets
     - **Impact: 8/10** — Significant efficiency improvements for generative recommendation; practical industrial relevance

3. **Multi-Business Prediction for Generative Recommendation at Meituan (MBGR)**
   * Affiliation: Meituan (Changhao Li, Junwei Yin, Zhilin Zeng, et al., 9 authors total)
   * Link: [arxiv.org/abs/2604.02684](https://arxiv.org/abs/2604.02684)
   * Venue: arXiv preprint, April 3, 2026
   * TL;DR: MBGR is the first generative recommendation framework tailored for multi-business scenarios, addressing seesaw phenomenon and representation confusion
   * Key techniques:
     - Business-aware Semantic ID (BID) module for domain-aware tokenization
     - Multi-Business Prediction (MBP) structure for business-specific prediction
     - Label Dynamic Routing (LDR) module for dense label transformation
     - Unified Semantic ID space for multi-business scenarios
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial deployment at Meituan)
     - **Novelty: 8/10** — First framework for multi-business generative recommendation; novel BID and MBP designs
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed on Meituan's food delivery platform; validated with offline and online experiments
     - **Impact: 9/10** — From Meituan production team; addresses key multi-business challenge in generative recommendation

4. **One Model, Two Markets: Bid-Aware Generative Recommendation (GEM-Rec)**
   * Affiliation: — *(Yanchen Jiang, Zhe Feng, Christopher P. Mah, Aranyak Mehta, Di Wang — institutions TBD)*
   * Link: [arxiv.org/abs/2603.22231](https://arxiv.org/abs/2603.22231)
   * Venue: arXiv preprint, March 31, 2026
   * TL;DR: GEM-Rec integrates commercial relevance and monetization objectives into generative recommendation via control tokens and bid-aware decoding
   * Key techniques:
     - Control tokens to decouple ad placement decision from item recommendation
     - Bid-Aware Decoding mechanism for real-time pricing injection
     - Unified generative sequence for semantic retrieval and monetization
     - Allocation monotonicity guarantee for bidding consistency
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 9/10** — Novel integration of commercial objectives (ads, bidding) into generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed; bidding mechanism may introduce fairness concerns
     - **Robustness: 7/10** — Theoretical guarantee of allocation monotonicity; novel approach to commercial generative recommendation
     - **Impact: 8/10** — Novel paradigm for commercial generative recommendation; bridges semantic retrieval and monetization

5. **IntRR: A Framework for Integrating SID Redistribution and Length Reduction**
   * Affiliation: — *(Zesheng Wang, Longfei Xu, Weidong Deng, Huimin Yan, Kaikui Liu, Xiangxiang Chu — institutions TBD)*
   * Link: [arxiv.org/abs/2602.20704](https://arxiv.org/abs/2602.20704)
   * Venue: arXiv preprint, February 28, 2026
   * TL;DR: IntRR addresses objective misalignment and sequence length inflation in generative recommendation via SID redistribution and structural length reduction
   * Key techniques:
     - Objective-aligned SID Redistribution using item-specific Unique IDs (UIDs) as collaborative anchors
     - Structural Length Reduction via recursive SID hierarchy handling
     - Fixed cost of one token per item for efficient generation
     - Dynamic semantic weight redistribution across codebook layers
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel approach to SID optimization and sequence length reduction in generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Fixed token cost per item; substantial improvements over generative baselines
     - **Impact: 8/10** — Addresses key efficiency challenge in generative recommendation; strong empirical results

6. **DeepInterestGR: Mining Deep Multi-Interest Using Multi-Modal LLMs for Generative Recommendation**
   * Affiliation: — *(Yangchen Zeng — institution TBD)*
   * Link: [arxiv.org/abs/2602.18907](https://arxiv.org/abs/2602.18907)
   * Venue: arXiv preprint, February 21, 2026
   * TL;DR: DeepInterestGR captures deep multi-interest representations from multi-modal LLMs via Chain-of-Thought prompting and reinforcement learning
   * Key techniques:
     - Multi-LLM Interest Mining (MLIM) with Chain-of-Thought prompting
     - Reward-Labeled Deep Interest (RLDI) using lightweight binary classifier
     - Interest-Enhanced Item Discretization (IEID) via RQ-VAE
     - Two-stage training: supervised fine-tuning + GRPO with Interest-Aware Reward
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel deep interest mining from multi-modal LLMs for generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Validated on three Amazon Review benchmarks; GRPO optimization for stable training
     - **Impact: 8/10** — Addresses Shallow Interest problem in generative recommendation; novel integration of multi-modal LLMs

---

## Papers May 04:

> **Note:** No new generative recommendation papers were found in the last 24 hours (May 3-4, 2026). Following the fallback procedure, papers from the last 3 months (April 2026) are included to meet the minimum 5 papers requirement.

1. **ProMax: Exploring the Potential of LLM-derived Profiles with Distribution Shaping for Recommender Systems**
   * Affiliation: Anhui University; University of Electronic Science and Technology of China (UESTC); The University of Queensland
   * Link: [arxiv.org/abs/2604.26231](https://arxiv.org/abs/2604.26231)
   * Venue: SIGIR 2026
   * TL;DR: ProMax uses LLM-derived user/item profiles with distribution shaping to enhance recommendation, outperforming existing LLM-based approaches
   * Key techniques:
     - Dense retrieval to uncover collaborative relationships between profiles
     - Dual distribution-reshaping process
     - Profile distribution as guiding signal
     - Distribution shaping for recommendation enhancement
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel application of LLM-derived profiles with distribution shaping for recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Validated on 3 public datasets; improves base model performance
     - **Impact: 8/10** — SIGIR 2026; from Anhui University/UESTC/UQ; novel profile-based approach

2. **Beyond Static Collision Handling: Adaptive Semantic ID Learning for Multimodal Recommendation at Industrial Scale (AdaSID)**
   * Affiliation: University of Electronic Science and Technology of China (UESTC); Kuaishou Technology
   * Link: [arxiv.org/abs/2604.23522](https://arxiv.org/abs/2604.23522)
   * Venue: arXiv preprint, April 26, 2026
   * TL;DR: AdaSID adapts Semantic ID learning by relaxing collision penalties for semantically compatible items, validated on Kuaishou e-commerce platform
   * Key techniques:
     - Adaptive Semantic ID Learning (AdaSID) framework
     - Two-stage adaptive collision handling
     - Stage 1: Relax penalties for semantically compatible items
     - Stage 2: Adaptive regularization based on collision load and training progress
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial collaboration with Kuaishou)
     - **Novelty: 8/10** — Novel adaptive approach to Semantic ID collision handling; addresses key scalability issue
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed on Kuaishou e-commerce; GMV +0.98%; significant online A/B test gains
     - **Impact: 9/10** — From UESTC/Kuaishou; industrial-scale validation; addresses real-world multimodal recommendation challenge

3. **MTServe: Efficient Serving for Generative Recommendation Models with Hierarchical Caches**
   * Affiliation: Wuhan University; Meituan; NVIDIA
   * Link: [arxiv.org/abs/2604.22881](https://arxiv.org/abs/2604.22881)
   * Venue: arXiv preprint, April 24, 2026
   * TL;DR: MTServe is a hierarchical cache management system for generative recommendation that virtualizes GPU memory using host RAM, achieving 3.1x speedup with >98.5% hit rate
   * Key techniques:
     - Hierarchical cache management system
     - Host RAM as scalable backup storage for GPU memory virtualization
     - Hybrid storage layout
     - Asynchronous data transfer pipeline
     - Locality-driven replacement policy
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel hierarchical caching system for generative recommendation serving; addresses key inference bottleneck
     - **Fairness: 4/10** — Not relevant to fairness; systems optimization work
     - **Robustness: 9/10** — 3.1x speedup on public and production datasets; >98.5% hit rate; robust architecture
     - **Impact: 8/10** — From Wuhan University/Meituan/NVIDIA; significant engineering contribution for industrial GR deployment

4. **UniRec: Bridging the Expressive Gap between Generative and Discriminative Recommendation via Chain-of-Attribute**
   * Affiliation: Shopee
   * Link: [arxiv.org/abs/2604.12234](https://arxiv.org/abs/2604.12234)
   * Venue: arXiv preprint, April 2026 (v4 revised April 30, 2026)
   * TL;DR: UniRec bridges the expressive gap between generative and discriminative recommendation via Chain-of-Attribute (CoA), achieving +22.6% HR@50 improvement and deployed on Shopee
   * Key techniques:
     - Chain-of-Attribute (CoA) mechanism
     - Attribute token prefixing before SID decoding
     - Capacity-constrained SID with exposure-weighted capacity penalty
     - Conditional Decoding Context (CDC)
     - Joint RFT and DPO framework
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial deployment at Shopee)
     - **Novelty: 9/10** — Novel approach to bridging generative and discriminative recommendation; CoA is a creative solution to the expressive gap
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed on Shopee; PVCTR +5.37%, orders +4.76%, GMV +5.60%; rigorous online A/B testing
     - **Impact: 9/10** — From Shopee; significant industrial deployment; bridges key gap in GR research

5. **CRAB: Codebook Rebalancing for Bias Mitigation in Generative Recommendation**
   * Affiliation: Walmart Global Tech; Stony Brook University
   * Link: [arxiv.org/abs/2604.05113](https://arxiv.org/abs/2604.05113)
   * Venue: arXiv preprint, April 6, 2026
   * TL;DR: CRAB is a post-hoc debiasing strategy for generative recommendation that alleviates popularity bias by rebalancing the codebook based on semantic token frequencies
   * Key techniques:
     - Post-hoc debiasing strategy for GeneRec
     - Codebook rebalancing by splitting over-popular tokens
     - Preservation of hierarchical semantic structure
     - Tree-structured regularizer for semantic consistency
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel post-hoc debiasing for generative recommendation; addresses popularity bias amplification
     - **Fairness: 9/10** — Core contribution is bias mitigation in generative recommendation; explicitly addresses popularity bias
     - **Robustness: 7/10** — Validated on real-world datasets; improves recommendation performance while alleviating bias
     - **Impact: 8/10** — From Walmart Global Tech/Stony Brook; addresses key fairness issue in generative recommendation

---

## Papers May 03:

> **Note:** Only 2 new generative recommendation papers were found in the last 24 hours (May 2-3, 2026). Following the fallback procedure, papers from March-April 2026 are also included to meet the minimum 5 papers requirement.

1. **Position-Aware Drafting for Inference Acceleration in LLM-Based Generative List-Wise Recommendation (PAD-Rec)**
   * Affiliation: — *(Jiaju Chen, Chongming Gao, Chenxiao Fan, Haoyan Liu, Qingpeng Cai, Peng Jiang, Xiangnan He — institutions TBD)*
   * Link: [arxiv.org/abs/2604.27747](https://arxiv.org/abs/2604.27747)
   * Venue: arXiv preprint, April 30, 2026
   * TL;DR: PAD-Rec introduces item position embeddings and step position embeddings to improve speculative decoding for LLM-based generative list-wise recommendation
   * Key techniques:
     - Position-Aware Drafting (PAD-Rec)
     - Item position embeddings (encode within-item slot)
     - Step position embeddings (encode draft step)
     - Learnable gates for signal harmonization
     - Speculative decoding acceleration
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel application of speculative decoding to generative recommendation with position-aware drafting
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Up to 3.1x wall-clock speedup with ~5% average gain; negligible accuracy loss
     - **Impact: 8/10** — From Xiangnan He's team (likely USTC); addresses key inference efficiency bottleneck

2. **One Pass, Any Order: Position-Invariant Listwise Reranking for LLM-Based Recommendation (InvariRank)**
   * Affiliation: RMIT University, Melbourne, Australia
   * Link: [arxiv.org/abs/2604.27599](https://arxiv.org/abs/2604.27599)
   * Venue: SIGIR 2026
   * TL;DR: InvariRank enables permutation-invariant listwise reranking with LLMs via structured attention mask and shared positional framing
   * Key techniques:
     - InvariRank (permutation-invariant listwise reranking)
     - Structured attention mask (blocks cross-candidate attention)
     - Shared positional framing under RoPE
     - Listwise learning-to-rank objective
     - Single forward pass scoring
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — GitHub: https://github.com/ejbito/InvariRank; complete implementation; well-documented
     - **Novelty: 8/10** — Novel permutation-invariant LLM reranking; addresses order sensitivity
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Stable rankings across candidate permutations; validated on benchmarks
     - **Impact: 9/10** — SIGIR 2026; from RMIT; novel architectural solution

3. **How Well Does Generative Recommendation Generalize?**
   * Affiliation: — *(Yijie Ding, Zitian Guo, Jiachen Li, et al. — institutions TBD, likely UCSD/University of Illinois)*
   * Link: [arxiv.org/abs/2603.19809](https://arxiv.org/abs/2603.19809)
   * Venue: arXiv preprint, March 20, 2026
   * TL;DR: Systematic analysis showing GR models generalize better on unseen item transitions, while item ID-based models excel at memorization
   * Key techniques:
     - Memorization vs. generalization categorization
     - Token-level analysis of generalization
     - Memorization-aware indicator for adaptive combination
     - Complementary fusion of GR and item ID-based models
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 9/10** — First systematic analysis of generalization in generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Rigorous experimental analysis; token-level insights
     - **Impact: 9/10** — From Julian McAuley's team (UCSD); fundamental contribution

4. **GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation**
   * Affiliation: JD.com (JD App team)
   * Link: [arxiv.org/abs/2604.14878](https://arxiv.org/abs/2604.14878)
   * Venue: SIGIR 2026 (Camera-Ready)
   * TL;DR: GenRec is a production generative recommendation framework deployed on JD App, addressing pagination inconsistency, long sequence encoding, and preference alignment
   * Key techniques:
     - GenRec (generative recommendation framework)
     - Page-wise NTP (Next-Token Prediction) task
     - Asymmetric linear Token Merger (compresses multi-token Semantic IDs)
     - GRPO-SR (Group Relative Policy Optimization with NLL regularization)
     - Hybrid Rewards (dense reward model + relevance gate)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (industrial deployment)
     - **Novelty: 8/10** — Novel page-wise NTP and token merger for industrial-scale generative recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed on JD App; 9.5% click improvement, 8.7% transaction improvement
     - **Impact: 9/10** — SIGIR 2026; from JD.com; significant industrial deployment

5. **Tencent Advertising Algorithm Challenge 2025: All-Modality Generative Recommendation**
   * Affiliation: Tencent (Tencent Ads team)
   * Link: [arxiv.org/abs/2604.04976](https://arxiv.org/abs/2604.04976)
   * Venue: arXiv preprint, April 5, 2026 (competition paper)
   * TL;DR: TencentGR datasets (1M/10M users) with all-modality data for industrial generative recommendation research
   * Key techniques:
     - TencentGR-1M dataset (1M users, 100 interactions each)
     - TencentGR-10M dataset (10M users, click/conversion labels)
     - Baseline generative recommendation model
     - Weighted evaluation for high-value conversion events
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — Datasets: https://huggingface.co/datasets/TAAC2025; Baseline: https://github.com/TencentAdvertisingAlgorithmCompetition/baseline_2025
     - **Novelty: 7/10** — First large-scale all-modality dataset for generative recommendation in advertising
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Real de-identified Tencent Ads logs; realistic industrial data
     - **Impact: 8/10** — From Tencent; enables research on all-modality generative recommendation

---

## Papers April 30:

1. **CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation**
   * Affiliation: University of Electronic Science and Technology of China; Southwestern University of Finance and Economics
   * Link: [arxiv.org/abs/2604.26427](https://arxiv.org/abs/2604.26427)
   * Venue: arXiv preprint, April 29, 2026
   * TL;DR: CARD introduces visual semantic units to unify multi-modal signals for SID construction and proposes non-uniform quantization (NU-RQ-VAE) to address codeword imbalance in generative recommendation
   * Key techniques:
     - Visual Semantic Unit: unifies text, visual, and collaborative signals
     - Non-Uniform Quantization (NU-RQ-VAE): learnable invertible non-uniform transformation
     - Plug-and-play non-uniform transformation module
     - End-to-end generative recommendation framework
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 6/10** — GitHub: https://github.com/HAI-UESTC/CARD; code structure is clear but documentation is brief; no requirements.txt; depends on user to prepare data and tune parameters
     - **Novelty: 8/10** — Novel visual semantic unit for unified multi-modal SID; non-uniform quantization for imbalanced semantic distribution is creative
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — NU-RQ-VAE is plug-and-play and robust across different quantization schemes
     - **Impact: 8/10** — From UESTC; addresses key SID quality and codeword imbalance problems in generative recommendation

2. **Factorized Latent Reasoning for LLM-based Recommendation (FLR)**
   * Affiliation: Independent Researcher; Macquarie University; University of New South Wales; Meituan LongCat Interaction Team
   * Link: [arxiv.org/abs/2604.26760](https://arxiv.org/abs/2604.26760)
   * Venue: arXiv preprint, April 29, 2026
   * TL;DR: FLR decomposes latent reasoning into multiple disentangled preference factors via a lightweight multi-factor attention module, combined with GRPO for stable alignment in latent space
   * Key techniques:
     - Factorized Latent Reasoning (FLR): multi-factor latent representation
     - Multi-factor Attention Module: each factor attends to different aspects of user history
     - Orthogonality, attention diversity, and sparsity regularization
     - Dynamic aggregation of factor contributions
     - GRPO (Group-relative Policy Optimization) for latent space alignment
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8.5/10** — GitHub: https://github.com/ToAdventure/FLR; 58 commits, complete training/evaluation pipeline, well-documented README, but no tests or CI/CD
     - **Novelty: 8/10** — Factorized latent reasoning is a novel approach to LLM-based recommendation; addresses single latent vector limitation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Regularization objectives promote factor diversity; GRPO provides stable alignment
     - **Impact: 8/10** — From Meituan/UNSW; novel latent reasoning paradigm for LLM-based recommendation

3. **Generative Recommendation for Large-Scale Advertising (GR4AD)**
   * Affiliation: Kuaishou Technology (快手科技), Beijing, China
   * Link: [arxiv.org/abs/2602.22732](https://arxiv.org/abs/2602.22732)
   * Venue: arXiv preprint, February 26, 2026 (v3 revised April 2026)
   * TL;DR: Production-oriented generative recommender co-designed across architecture (UA-SID, LazyAR), learning (VSL, RSPO), and serving (dynamic beam search) for large-scale advertising
   * Key techniques:
     - UA-S-ID (Unified Advertisement Semantic ID): captures complex business information
     - LazyAR: lazy autoregressive decoder for short-text, multi-candidate generation
     - VSL (Value-Aware Supervised Learning)
     - RSPO (Ranking-Guided Softmax Preference Optimization): listwise RL algorithm
     - Dynamic beam search service: adaptive beam width adjustment
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (industrial deployment)
     - **Novelty: 9/10** — Comprehensive co-design of architecture, learning, and serving for generative advertising; LazyAR and RSPO are novel
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed at Kuaishou (400M+ users); A/B test shows 4.2% ad revenue lift; handles real-time serving under fixed budget
     - **Impact: 10/10** — From Kuaishou; full industrial deployment; significant business impact (4.2% revenue lift)

4. **Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE)**
   * Affiliation: National University of Singapore; University of Science and Technology of China (USTC); Renmin University of China; Meta AI
   * Link: [arxiv.org/abs/2602.03692](https://arxiv.org/abs/2602.03692)
   * Venue: WWW 2026
   * TL;DR: CARE addresses bias amplification in generative recommendation via cascaded reasoning: progressive history encoding + query-anchored inference to introduce heterogeneous information and allocate more computation per token
   * Key techniques:
     - Cascaded Reasoning framework (CARE)
     - Progressive History Encoding: gradually introduces finer-grained history information
     - Query-Anchored Inference: parallel inference steps for deeper history understanding
     - De-biasing via heterogeneous information integration
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 9/10** — GitHub: https://github.com/Linxyhaha/CARE; excellent documentation, complete training/evaluation pipeline, clear structure; only minor drawback is lack of requirements.txt
     - **Novelty: 9/10** — Novel perspective: bias amplification in GR; cascaded reasoning is a creative solution
     - **Fairness: 7/10** — Explicitly addresses bias amplification, a key fairness issue in generative recommendation
     - **Robustness: 8/10** — Cascaded reasoning improves diversity and reduces bias; validated on 3 GR backbones and 4 datasets
     - **Impact: 9/10** — WWW 2026; from NUS/USTC/Meta; addresses key limitation of existing GR models

5. **Adaptive Autoguidance for Item-Side Fairness in Diffusion Recommender Systems (A2G-DiffRec)**
   * Affiliation: Johannes Kepler University Linz, Austria (Institute of Computational Perception)
   * Link: [arxiv.org/abs/2602.14706](https://arxiv.org/abs/2602.14706)
   * Venue: arXiv preprint, February 16, 2026 (v2 revised April 2026)
   * TL;DR: A2G-DiffRec incorporates adaptive autoguidance (main model guided by weaker version of itself) and fairness-aware regularization to balance accuracy and item-side fairness in diffusion recommenders
   * Key techniques:
     - Adaptive Autoguidance: learnable guidance weight (not fixed)
     - Fairness-Aware Regularization: promotes balanced exposure across items with different popularity
     - Diffusion Recommender framework
     - Weak model guidance for stable training
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8/10** — GitHub: https://github.com/zihanlizi/A2G-DiffRec; MIT License; complete codebase with requirements.txt; uses older PyTorch (1.12.0) which may cause compatibility issues
     - **Novelty: 7/10** — Adaptive autoguidance for diffusion rec is novel; fairness-aware regularization is a valuable addition
     - **Fairness: 9/10** — Core contribution is item-side fairness; explicitly addresses popularity bias in diffusion recommenders
     - **Robustness: 7/10** — Adaptive guidance is more robust than fixed-weight guidance; validated on 3 public datasets
     - **Impact: 7/10** — From JKU Linz; novel fairness-aware diffusion rec; good empirical results

---
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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Novel unified framework addressing the gap between generative retrieval and ranking
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 7/10** — Unified framework improves training stability
     - **Impact: 7/10** — From NJUST/Kuaishou, provides unified generative recommendation solution

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel global action space for reranking, addresses semantic inconsistency
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 8/10** — Robust to cold-start scenarios, decouples scoring from input order
     - **Impact: 8/10** — From Kuaishou/CityU/UC San Diego, two-stage optimization

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code (industrial deployment)
     - **Novelty: 8/10** — Novel action-aware generative sequence modeling for short video recommendation
     - **Fairness: 5/10** — Not explicitly addressed
     - **Robustness: 9/10** — Deployed at scale (400M+ users), significant online A/B test gains (+0.34% watch time, +8.1% interaction rate)
     - **Impact: 9/10** — SIGIR 2026, industrial deployment at Kuaishou

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — Code available at https://github.com/hailingc/siren_rope; demo code provided but full training/eval pipeline completeness TBD
     - **Novelty: 8/10** — Novel perspective: treating rotation space as learnable (not fixed) for attention mechanisms; creative analogy to complex numbers
     - **Fairness: 5/10** — Not explicitly addressed; rotation encoding is neutral but could amplify biases if training data is biased
     - **Robustness: 7/10** — Negligible computational overhead; SIREN provides stable gradient flow for learning rotation weights
     - **Impact: 8/10** — From LinkedIn production team; evaluated on large-scale social network news feed dataset; applicable to any RoPE-based generative recommender

2. **Modeling Behavioral Intensity and Transitions for Generative Recommendation (BITRec)**
   * Affiliation: Ant Group; Fudan University
   * Link: [arxiv.org/abs/2604.24472](https://arxiv.org/abs/2604.24472)
   * Venue: arXiv preprint, April 27, 2026
   * TL;DR: BITRec explicitly models behavioral intensity differences and transition patterns via hierarchical behavior aggregation and transition relation encoding for generative multi-behavior recommendation
   * Key techniques:
     - Hierarchical Behavior Aggregation (HBA): separated exploration and commitment pathways
     - Transition Relation Encoding (TRE): explicit learnable relation matrices for behavior transitions
     - Generative sequence modeling for multi-behavior recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Explicit intensity + transition modeling in generative recommendation is novel; HBA/TRE are sensible designs
     - **Fairness: 5/10** — Not explicitly addressed; multi-behavior modeling could help or hurt fairness depending on behavior definitions
     - **Robustness: 7/10** — Structured behavior modeling (HBA+TRE) is more robust than implicit attention; validated on 4 large-scale datasets
     - **Impact: 8/10** — From Ant Group (industrial relevance); 15-23% improvements on RetailRocket, Taobao, Tmall, Insurance Dataset

3. **FreeScale: Distributed Training for Sequence Recommendation Models with Minimal Scaling Cost**
   * Affiliation: — *(Chenhao Feng, Haoli Zhang, Shakhzod Ali-Zade, Yanli Zhao, Liang Luo, Jennifer Cao, Lisen Deng, Siqiao Chen, Chenyu Zhao, Tristan Rice, Daniel Johnson, Min Si, Tiantu Xu, Yi Zhang, Siqi Yan, Chuanhao Zhuge, Min Ni, Bi Xue, Qunshu Zhang, Shen Li — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24073](https://arxiv.org/abs/2604.24073)
   * Venue: MLSys 2026 (9th Conference on Machine Learning and Systems)
   * TL;DR: FreeScale reduces compute bubble by 90.3% for distributed training of sequence recommendation models via load balancing and communication overlap
   * Key techniques:
     - Load balancing via careful input sample balancing to mitigate straggler effect
     - Prioritized embedding communication overlapping with computation
     - SM-Free technique to resolve GPU resource contention during communication-computation overlap
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 6/10** — Distributed training optimizations are incremental but well-engineered; SM-Free technique is a useful contribution
     - **Fairness: 4/10** — Not relevant to fairness; pure systems optimization work
     - **Robustness: 8/10** — Empirically validated on 256 H100 GPUs; significant compute bubble reduction (90.3%) improves training stability
     - **Impact: 8/10** — MLSys 2026; critical for industrial-scale sequence recommendation model training; 256 GPU scaling

4. **SAGE: Sparse Adaptive Guidance for Dependency-Aware Tabular Data Generation**
   * Affiliation: — *(Shuo Yang, Zheyu Zhang, Bardh Prenkaj, Gjergji Kasneci — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24368](https://arxiv.org/abs/2604.24368)
   * Venue: ACL 2026
   * TL;DR: SAGE uses LLM with sparse, adaptive dependency guidance for high-fidelity tabular data generation; relevant to generative recommendation data synthesis
   * Key techniques:
     - Feature discretization into value-aware pseudo-features
     - Mutual information-based sparse dependency graph construction
     - Adaptive guidance via explicit context selection or implicit logic correction
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found (paper says code will be released, but not available yet)
     - **Novelty: 7/10** — Sparse + adaptive dependency guidance for tabular generation is novel; addresses key limitations of dense modeling and static dependencies
     - **Fairness: 6/10** — Synthetic data generation could help privacy but may also amplify biases present in training data; not explicitly addressed
     - **Robustness: 7/10** — Sparse graph reduces spurious correlations; 10% F1 improvement and reduced policy violations
     - **Impact: 7/10** — ACL 2026; tabular data generation is useful for recommendation (user/item feature synthesis); strong empirical results

5. **Disagreement as Signals: Dual-view Calibration for Sequential Recommendation Denoising (DC4SR)**
   * Affiliation: — *(Sijia Li, Min Gao, Zongwei Wang, Zhiyi Liu, Xin Xia, Yi Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.24048](https://arxiv.org/abs/2604.24048)
   * Venue: arXiv preprint, April 27, 2026
   * TL;DR: DC4SR uses disagreement between LLM semantic priors and model-learned posteriors as signals for joint optimization and denoising in sequential recommendation
   * Key techniques:
     - Dual-view calibration: LLM-based semantic prior + model-learned posterior
     - Disagreement-based denoising signal identification
     - Joint optimization of semantic understanding and model representation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Using LLM-model disagreement as denoising signal is a creative idea; dual-view calibration is well-motivated
     - **Fairness: 5/10** — Not explicitly addressed; LLM semantic priors may carry biases
     - **Robustness: 7/10** — Denoising via disagreement signals improves robustness to noisy interactions; novel approach
     - **Impact: 7/10** — Sequential recommendation denoising is an important problem; LLM integration adds value

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Identifies and fixes a real problem in group-based RL for sparse-hit rec
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — Min-learnability recovery stabilizes training on hard groups
     - **Impact: 7/10** — Practical fix for a common failure mode in RL-based generative rec

2. **Objective Shaping with Hard Negatives: Windowed Partial AUC Optimization for RL-based LLM Recommenders**
   * Affiliation: — *(Wentao Shi, Qifan Wang, Chen Chen, Fei Liu, Dongfang Liu, Xu Liu, Wanli Ma, Junfeng Pan, Linhong Zhu, Fuli Feng — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22504](https://arxiv.org/abs/2604.22504)
   * TL;DR: Windowed partial AUC (WPAUC) optimization for better Top-K alignment in RL-based LLM recommenders
   * Key techniques:
     - Theoretical analysis: GRPO ≈ AUC maximization (misfit for Top-K)
     - Beam-search negatives → partial AUC shaping
     - Threshold-Adjusted Window (TAWin) for explicit Top-K control
   * Venue: arXiv preprint, April 24, 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Novel theoretical connection between GRPO and AUC; WPAUC is a creative solution
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — WPAUC shaping is more stable than raw GRPO for Top-K
     - **Impact: 8/10** — Strong theoretical backing; from Multi-Scenarios team (likely industry)

3. **GraphRAG-IRL: Personalized Recommendation with Graph-Grounded Inverse Reinforcement Learning and LLM Re-ranking**
   * Affiliation: — *(Siqi Liang, Xiawei Wang, Yudi Zhang, Jiaying Zhou — institutions TBD)*
   * Link: [arxiv.org/abs/2604.19128](https://arxiv.org/abs/2604.19128)
   * TL;DR: Hybrid recommendation framework combining GraphRAG, Inverse RL, and persona-guided LLM re-ranking
   * Key techniques:
     - Heterogeneous knowledge graph (items, categories, concepts)
     - Maximum-entropy IRL for calibrated pre-ranking
     - Persona-conditioned LLM fusion on short candidate lists
   * Venue: arXiv preprint, April 21, 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Creative combination of GraphRAG + IRL + LLM re-ranking
     - **Fairness: 6/10** — Persona-guided re-ranking could help or hurt fairness depending on persona design
     - **Robustness: 6/10** — Hybrid approach; graph + IRL + LLM each add complexity
     - **Impact: 6/10** — Niche but interesting; persona-guided LLM fusion is a growing area

4. **Modular Representation Compression (MARC): Adapting LLMs for Efficient and Effective Recommendations**
   * Affiliation: — *(Yunjia Xi, Menghui Zhu, Jianghao Lin, Bo Chen, Ruiming Tang, Yong Yu, Weinan Zhang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.18146](https://arxiv.org/abs/2604.18146)
   * TL;DR: Modular representation compression to resolve mid-layer representation advantage (MRA) in LLM-based recommendation
   * Key techniques:
     - Module tuning (explicit compression + task adaptation modules)
     - Module task decoupling (information constraints + divergent architectures)
     - Middle-layer representation extraction for compression
   * Venue: SIGIR 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Identifies MRA phenomenon; modular compression is a clever fix
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — Explicit compression modules are more stable than end-to-end fine-tuning
     - **Impact: 8/10** — SIGIR 2026; addresses a key efficiency-effectiveness trade-off in LLM4Rec

5. **Multi-LLM Token Filtering and Routing for Sequential Recommendation (MLTFR)**
   * Affiliation: — *(Wuhan Chen, Min Gao, Xin Xia, Zongwei Wang, Wentao Li, Shane Culpepper — institutions TBD)*
   * Link: [arxiv.org/abs/2604.18200](https://arxiv.org/abs/2604.18200)
   * TL;DR: Multi-LLM token embedding filtering and routing for corpus-free sequential recommendation
   * Key techniques:
     - User-guided token filtering (task-relevant embedding selection)
     - Mixture-of-Experts (MoE) architecture for multi-LLM integration
     - Fisher-weighted semantic consensus expert (prevent dominant experts)
   * Venue: arXiv preprint, April 20, 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Multi-LLM integration via MoE is interesting; corpus-free is a plus
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 6/10** — MoE routing can be unstable; Fisher-weighted consensus helps
     - **Impact: 7/10** — Multi-LLM trend is growing; corpus-free is practical for industry

6. **ResRank: Unifying Retrieval and Listwise Reranking via End-to-End Joint Training with Residual Passage Compression**
   * Affiliation: — *(Xiaojie Ke, Shuai Zhang, Liansheng Sun, Yongjin Wang, Hengjun Jiang, Xiangkun Liu, Cunxin Gu, Jian Xu, Guanjun Jiang — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22180](https://arxiv.org/abs/2604.22180)
   * TL;DR: Unified retrieval-reranking with residual passage compression for efficient LLM-based listwise reranking
   * Key techniques:
     - Encoder-LLM for passage compression (one embedding per passage)
     - Residual connection (encoder embedding + reranker hidden states)
     - One-step cosine-similarity scoring (zero generated tokens)
   * Venue: arXiv preprint, April 24, 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Residual compression for unified retrieval-reranking is novel
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 7/10** — One-step scoring is efficient and stable
     - **Impact: 8/10** — Unified retrieval-reranking is a hot topic; efficient listwise reranking has high industrial value

7. **Rethinking Semantic Collaborative Integration: Why Alignment Is Not Enough**
   * Affiliation: — *(Maolin Wang, Dongze Wu, Jianing Zhou, Hongyu Chen, Beining Bao, Yu Jiang, Chenbin Zhang, Chang Wang, Jian Liu, Lei Sha — institutions TBD)*
   * Link: [arxiv.org/abs/2604.22195](https://arxiv.org/abs/2604.22195)
   * TL;DR: Beyond alignment — complementary fusion of semantic and collaborative representations for recommendation
   * Key techniques:
     - "Shared + private" latent structure assumption
     - Complementarity-aware diagnostics (overlap, unique hit contribution, fusion upper bound)
     - Controlled alignment probes (low-capacity mapping cannot recover full geometry)
   * Venue: SIGIR 2026
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 8/10** — Rigorous analysis of why alignment is insufficient; complementarity-aware fusion is novel
     - **Fairness: 6/10** — Deeper fusion could amplify biases; not explicitly addressed
     - **Robustness: 7/10** — Diagnostics help understand fusion quality; more robust than blind alignment
     - **Impact: 8/10** — SIGIR 2026; fundamental contribution to LLM4Rec representation learning

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code found
     - **Novelty: 7/10** — Cross-modal alignment for Semantic ID is novel; Deep Interest Mining is a solid addition
     - **Fairness: 5/10** — Not addressed
     - **Robustness: 6/10** — VLM alignment can be noisy; QARM helps but adds complexity
     - **Impact: 7/10** — Semantic ID quality is a key bottleneck; cross-modal approach is promising

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
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code repository found
     - **Novelty: 8/10** — New "reason-then-recommend" + RL fine-tuning paradigm for recommendation assistants
     - **Fairness: 5/10** — Not explicitly addressed; may inherit LLM biases
     - **Robustness: 7/10** — Curriculum learning improves training stability; reasoning decomposition adds resilience
     - **Impact: 8/10** — ACL 2026, addresses a growing real-world need (complex query recommendation)

2. **Generative Reasoning Re-ranker (GR2)**
   * Affiliation: Meta *(Mingfu Liang et al.)*
   * Link: [arxiv.org/abs/2602.07774](https://arxiv.org/abs/2602.07774)
   * TL;DR: Generative LLM re-ranking via reasoning + DAPO (Decoupled Clip and Dynamic Sampling Policy Optimization)
   * Key techniques:
     - Three-stage training: mid-training on semantic IDs → SFT on LLM-generated reasoning traces → DAPO RL
     - Decoupled clipping (separate upper/lower clip bounds)
     - Dynamic sampling (filter zero-advantage groups)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (Meta paper)
     - **Novelty: 8/10** — First to apply DAPO-style RL to generative re-ranking; reasoning-augmented re-ranking is novel
     - **Fairness: 5/10** — Not discussed; RL optimization may inadvertently introduce ranking bias
     - **Robustness: 7/10** — Dynamic sampling improves training stability; reasoning traces add interpretability
     - **Impact: 9/10** — Outperforms OneRec-Think; from Meta; high industrial relevance

3. **Verifiable Reasoning for LLM-based Generative Recommendation (VRec)**
   * Affiliation: — *(Xinyu Lin, Hanchao Yu, Yinglong Xia, Jiang Zhang, Aashu Singh, Fei Liu, Wenjie Wang, Fuli Feng, Tat-Seng Chua, Qifan Wang — institutions TBD)*
   * Link: [arxiv.org/abs/2603.07725](https://arxiv.org/abs/2603.07725)
   * TL;DR: "Reason-verify-recommend" paradigm with multi-dimensional verification to mitigate reasoning degradation
   * Key techniques:
     - Hybrid verifier (rule-based + model-based) for multi-dimensional assessment
     - Proxy prediction targets to improve verifier reliability
     - Reasoning chain decomposition with step-level verification
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 2/10** — Repo exists (github.com/Linxyhaha/Verifiable-Rec) but empty (1 ⭐, no code uploaded)
     - **Novelty: 9/10** — "Reason-verify-recommend" is a genuinely new paradigm; step-level verification for recommendation is novel
     - **Fairness: 6/10** — Verification may propagate existing biases; not explicitly mitigated
     - **Robustness: 8/10** — Verification mechanism catches reasoning errors before recommendation; strong resilience
     - **Impact: 8/10** — Addresses key LLM reasoning failure modes; from NUS/Meta team

4. **Unleashing the Native Recommendation Potential: LLM-Based Generative Recommendation via Structured Term Identifiers (GRLM)**
   * Affiliation: — *(Zhiyang Zhang, Junda She, Kuo Cai, Bo Chen, Shiyao Wang, Xinchen Luo, Qiang Luo, Ruiming Tang, Han Li, Kun Gai, Guorui Zhou — likely industry labs)*
   * Link: [arxiv.org/abs/2601.06798](https://arxiv.org/abs/2601.06798)
   * TL;DR: Uses structured Term Identifiers (TIDs) — semantic-rich standardized text keywords — as item IDs for generative recommendation
   * Key techniques:
     - Context-aware term generation (convert item metadata to canonical TIDs)
     - Hybrid instruction fine-tuning (co-optimizes term internalization and sequential recommendation)
     - Elastic identifier grounding (robust item mapping despite ID variations)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 8/10** — Official repo (github.com/ZY0025/GRLM), 36 ⭐, well-documented, complete implementation with training/eval scripts
     - **Novelty: 7/10** — TID is a middle ground between text and SID; idea is solid but incremental over existing Semantic ID work
     - **Fairness: 6/10** — Term standardization could introduce systematic bias from term vocabulary design
     - **Robustness: 7/10** — Elastic grounding handles ID variation; TIDs are more robust than pure SIDs
     - **Impact: 7/10** — Addresses a real industrial bottleneck (SID semantic gap); from Kuaishou/industry team

5. **R3-VAE: Reference Vector-Guided Rating Residual Quantization VAE for Generative Recommendation**
   * Affiliation: — *(Qiang Wan, Ze Yang, Dawei Yang, Ying Fan, Xin Yan, Siyang Liu)*
   * Link: [arxiv.org/abs/2604.11440](https://arxiv.org/abs/2604.11440)
   * TL;DR: VAE-based generative recommendation with residual quantization guided by reference vectors
   * Key techniques:
     - Reference vector guidance (anchors quantization centroids with collaborative filtering signals)
     - Rating residual quantization (explicitly models rating information in the latent space)
     - VAE generative framework for recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — Repo (github.com/wwqq/R3-VAE), 14 ⭐, clean code structure, matches paper well, has training scripts
     - **Novelty: 6/10** — Residual quantization + reference guidance is a moderate extension of existing VAE rec work
     - **Fairness: 5/10** — Not addressed; standard VAE collaborative filtering may have popularity bias
     - **Robustness: 6/10** — VAEs are generally stable; residual quantization adds some robustness to rating noise
     - **Impact: 5/10** — More niche; VAE-based generative rec is less prominent than LLM/RL approaches currently

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

## By Opensource

Papers whose daily entry lists **Opensource?** strictly above **0/10**. Sorted by score (highest first), then by title.

**Count:** 25 papers as of May 09.

| Score | Paper |
| --- | --- |
| 10/10 | Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte) |
| 10/10 | MiniOneRec: An Open-Source Framework for Scaling Generative Recommendation |
| 9/10 | Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE) |
| 9/10 | One Pass, Any Order: Position-Invariant Listwise Reranking for LLM-Based Recommendation (InvariRank) |
| 9/10 | OpenOneRec Technical Report |
| 9/10 | Rank-GRPO: Training LLM-based Conversational Recommender Systems with Reinforcement Learning (ConvRec-R1) |
| 9/10 | [STATIC] Vectorizing the Trie: Efficient Constrained Decoding for LLM-based Generative Retrieval on Accelerators |
| 9/10 | Tencent Advertising Algorithm Challenge 2025: All-Modality Generative Recommendation |
| 9/10 | DynamicPO: Dynamic Preference Optimization for Recommendation (DASFAA 2026) |
| 8.5/10 | Factorized Latent Reasoning for LLM-based Recommendation (FLR) |
| 8/10 | Adaptive Autoguidance for Item-Side Fairness in Diffusion Recommender Systems (A2G-DiffRec) |
| 8/10 | MuonRec: Shifting the Optimizer Paradigm Beyond Adam in Scalable Generative Recommendation |
| 8/10 | OneRec-Think: In-Text Reasoning for Generative Recommendation |
| 8/10 | UniGRec: Unified Generative Recommendation with Soft Identifiers for End-to-End Optimization |
| 8/10 | Unleashing the Native Recommendation Potential: LLM-Based Generative Recommendation via Structured Term Identifiers (GRLM) |
| 7.5/10 | Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER) |
| 7/10 | Learning to Rotate: Temporal and Semantic Rotary Encoding for Sequential Modeling (SIREN-RoPE) |
| 7/10 | R3-VAE: Reference Vector-Guided Rating Residual Quantization VAE for Generative Recommendation |
| 7/10 | Rec-R1: Bridging Generative Large Language Models and User-Centric Recommendation Systems via Reinforcement Learning |
| 6.5/10 | On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec) |
| 6/10 | CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation |
| 5.5/10 | PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation |
| 2/10 | Verifiable Reasoning for LLM-based Generative Recommendation (VRec) |
| 9/10 | Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE) |
| 8/10 | Rethinking Convolutional Networks for Attribute-Aware Sequential Recommendation (ConvRec) |

---

## By Keyword

### RL / Reinforcement Learning
- Bridging Passive and Active: Enhancing Conversation Starter Recommendation via Active Expression Modeling (PA-Bridge)
- ReRec: Reasoning-Augmented LLM-based Recommendation Assistant
- Generative Reasoning Re-ranker (GR2)
- ReCast
- Objective Shaping with Hard Negatives
- Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA)
- OpenOneRec
- OneMall
- OneRec-Think
- OneRec-V2
- MiniOneRec
- Rec-R1
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner)
- Rank-GRPO
- Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization (GRAD)
- Factorized Latent Reasoning for LLM-based Recommendation (FLR)
- Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE)
- SAGER: Self-Evolving User Policy Skills for Recommendation Agent
- DynamicPO: Dynamic Preference Optimization for Recommendation
- ProMax: Exploring the Potential of LLM-derived Profiles
- Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE)

### Generative Retrieval / Ranking
- Harmonizing Generative Retrieval and Ranking in Chain-of-Recommendation (RecoChain)
- Mitigating Collaborative Semantic ID Staleness in Generative Retrieval
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- CapsID: Soft-Routed Variable-Length Semantic IDs
- Revisiting General Map Search via Generative Point-of-Interest Retrieval (GenPOI)

### Reasoning
- Bridging Passive and Active: Enhancing Conversation Starter Recommendation via Active Expression Modeling (PA-Bridge)
- ReRec
- VRec (Verifiable Reasoning)
- GR2
- GraphRAG-IRL
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- Reasoning over Semantic IDs Enhances Generative Recommendation
- Factorized Latent Reasoning for LLM-based Recommendation (FLR)
- Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE)
- Bridging Behavior and Semantics for Time-aware Cross-Domain Sequential Recommendation (BST-CDSR)
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- SAGER: Self-Evolving User Policy Skills for Recommendation Agent
- DeepInterestGR: Mining Deep Multi-Interest Using Multi-Modal LLMs
- Rethinking Convolutional Networks for Attribute-Aware Sequential Recommendation (ConvRec)

### Generative Recommendation / VAE
- Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA)
- R3-VAE
- ReCast
- Deep Interest Mining (SemanticID)
- BITRec (Modeling Behavioral Intensity and Transitions)
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- A2Gen (Action-Aware Generative Sequence Modeling)
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- Generative Recommendation for Large-Scale Advertising (GR4AD)
- How Well Does Generative Recommendation Generalize?
- GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation
- Tencent Advertising Algorithm Challenge 2025: All-Modality Generative Recommendation
- Beyond Static Collision Handling: Adaptive Semantic ID Learning (AdaSID)
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- MTServe: Efficient Serving for Generative Recommendation Models
- UniRec: Bridging the Expressive Gap via Chain-of-Attribute
- CRAB: Codebook Rebalancing for Bias Mitigation in Generative Recommendation
- Semantic Trimming and Auxiliary Multi-step Prediction for Generative Recommendation (STAMP)
- One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving
- Multi-Business Prediction for Generative Recommendation at Meituan (MBGR)
- One Model, Two Markets: Bid-Aware Generative Recommendation (GEM-Rec)

### LLM-based Recommendation
- ReRec
- VRec
- GRLM (Structured Term IDs)
- MARC (Modular Representation Compression)
- MLTFR (Multi-LLM Token Filtering)
- Rethinking Semantic Collaborative Integration
- DC4SR (Disagreement as Signals)
- A2Gen (Action-Aware Generative Sequence Modeling)
- Factorized Latent Reasoning for LLM-based Recommendation (FLR)
- Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE)
- ProMax: Exploring the Potential of LLM-derived Profiles
- Bridging Behavior and Semantics for Time-aware Cross-Domain Sequential Recommendation (BST-CDSR)
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- Enhancing Local Life Service Recommendation with Agentic Reasoning in Large Language Model
- DUET: Joint Exploration of User Item Profiles in Recommendation System
- DeepInterestGR: Mining Deep Multi-Interest Using Multi-Modal LLMs
- RecGPT-Mobile: On-Device Large Language Models
- Beyond Static Best-of-N: Bayesian List-wise Alignment (BLADE)

### Re-ranking
- GR2
- ResRank
- GraphRAG-IRL (LLM re-ranking)
- GloRank (From Local Indices to Global Identifiers)
- One Pass, Any Order: Position-Invariant Listwise Reranking for LLM-Based Recommendation (InvariRank)

### Semantic / Structured IDs
- GRLM
- Deep Interest Mining (SemanticID)
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- Reasoning over Semantic IDs Enhances Generative Recommendation
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- Beyond Static Collision Handling: Adaptive Semantic ID Learning (AdaSID)
- TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation
- PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation
- Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)
- UniRec: Bridging the Expressive Gap via Chain-of-Attribute
- Mitigating Collaborative Semantic ID Staleness in Generative Retrieval
- IntRR: A Framework for Integrating SID Redistribution and Length Reduction
- One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving

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
- Position-Aware Drafting for Inference Acceleration in LLM-Based Generative List-Wise Recommendation (PAD-Rec)
- MTServe: Efficient Serving for Generative Recommendation Models
- Semantic Trimming and Auxiliary Multi-step Prediction for Generative Recommendation (STAMP)
- One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving

### Model / Architecture
- OpenOneRec
- OneMall
- MiniOneRec
- UniGRec
- Generative Recommendation for Large-Scale Advertising (GR4AD)
- GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation
- UniRec: Bridging the Expressive Gap via Chain-of-Attribute
- Multi-Business Prediction for Generative Recommendation at Meituan (MBGR)
- One Model, Two Markets: Bid-Aware Generative Recommendation (GEM-Rec)
- IntRR: A Framework for Integrating SID Redistribution and Length Reduction
- One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving
- DeepInterestGR: Mining Deep Multi-Interest Using Multi-Modal LLMs

### MoE
- OneMall
- Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization

### Optimizer
- MuonRec

### Diffusion
- Adaptive Autoguidance for Item-Side Fairness in Diffusion Recommender Systems (A2G-DiffRec)
- Interests Burn-down Diffusion Process for Personalized Collaborative Filtering (StageCF)
- On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)

### Fairness
- Adaptive Autoguidance for Item-Side Fairness in Diffusion Recommender Systems (A2G-DiffRec)
- CRAB: Codebook Rebalancing for Bias Mitigation in Generative Recommendation

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
| **Kuaishou** | OpenOneRec · OneMall · OneRec-Think · OneRec-V2 · A2Gen · GloRank · GR4AD · AdaSID |
| **USTC** | MiniOneRec · UniGRec |
| **UIUC Illinois** | Rec-R1 |
| **Huawei Cloud** | RelayGR |
| **NUS** | Reasoning over Semantic IDs · CARE |
| **Shanghai JTU** | MuonRec |
| **Youtube** | [STATIC] Vectorizing the Trie |
| **Meituan** · MBGR | Generative Large-Scale Pre-trained Models for Automated Ad Bidding · FLR · MTServe |
| **Netflix** | Rank-GRPO |
| **University of Electronic Science and Technology of China** | CARD · ProMax · AdaSID |
| **Macquarie University / UNSW** | FLR (Factorized Latent Reasoning) |
| **Johannes Kepler University Linz** | A2G-DiffRec |
| **RMIT University** | One Pass, Any Order: Position-Invariant Listwise Reranking for LLM-Based Recommendation (InvariRank) |
| **JD.com** | GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation |
| **Tencent** | Tencent Advertising Algorithm Challenge 2025: All-Modality Generative Recommendation · Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA) |
| **ACL 2026** | ReRec, SAGE |
| **SIGIR 2026** | MARC, Rethinking Semantic Collaborative Integration, A2Gen, CARE, PAD-Rec, InvariRank, GenRec |
| **MLSys 2026** | FreeScale |
| **Anhui University** | ProMax |
| **The University of Queensland** | ProMax |
| **Wuhan University** | MTServe |
| **NVIDIA** | MTServe |
| **Shopee** | UniRec |
| **Walmart Global Tech** | CRAB |
| **Stony Brook University** | CRAB |
| **Alibaba** | RecGPT-Mobile: On-Device Large Language Models |
| **Tencent Map** | Revisiting General Map Search via Generative Point-of-Interest Retrieval (GenPOI) |
| **(TBD)** | Bridging Behavior and Semantics for Time-aware Cross-Domain Sequential Recommendation (BST-CDSR) · Semantic Trimming and Auxiliary Multi-step Prediction for Generative Recommendation (STAMP) · One Model, Two Markets: Bid-Aware Generative Recommendation (GEM-Rec) · IntRR: A Framework for Integrating SID Redistribution and Length Reduction · DeepInterestGR: Mining Deep Multi-Interest Using Multi-Modal LLMs · On the Equivalence Between Auto-Regressive Next Token Prediction and Full-Item-Vocabulary Maximum Likelihood Estimation in Generative Recommendation—A Short Note · SAGER: Self-Evolving User Policy Skills for Recommendation Agent · Enhancing Local Life Service Recommendation with Agentic Reasoning in Large Language Model · Mitigating Collaborative Semantic ID Staleness in Generative Retrieval · DUET: Joint Exploration of User Item Profiles in Recommendation System · DynamicPO: Dynamic Preference Optimization for Recommendation · VRec · GRLM · R3-VAE · ReCast · Objective Shaping · GraphRAG-IRL · MLTFR · ResRank · Deep Interest Mining · DC4SR · FLR · GR4AD · A2G-DiffRec · How Well Does Generative Recommendation Generalize? | · CapsID: Soft-Routed Variable-Length Semantic IDs · Interests Burn-down Diffusion Process (StageCF) · Rethinking Convolutional Networks for Attribute-Aware Sequential Recommendation (ConvRec) · Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE) · Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte) · Bridging Passive and Active: Enhancing Conversation Starter Recommendation via Active Expression Modeling (PA-Bridge)

 · TriAlignGR: Triangular Multitask Alignment with Multimodal Deep Interest Mining for Generative Recommendation · One Pool, Two Caches: Adaptive HBM Partitioning for Accelerating Generative Recommender Serving · PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation · Generative Sequential Recommendation via Hierarchical Behavior Modeling (GAMER) · On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec)---
