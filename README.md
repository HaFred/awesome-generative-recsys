# Awesome Generative Recommendation System (RecSys)

```
 ██████╗                ██████╗                ███████╗                
██╔════╝  ███╗  ███╗    ██╔══██╗ ███╗   ███╗   ██╔════╝██╗ ██╗ ██████╗ 
██║      ██╔═██╗████╗   ██████╔╝██╔═██╗██╔═██╗ ███████╗╚██╗██║ ██╔═══╝ 
██║  ███╗██████║██╔██╗  ██╔══██╗██████║██║ ╚═╝ ╚════██║ ╚███╔╝ ██████╗ 
██║   ██║██║    ██║╚██╗ ██║  ██║██║    ██║ ██╗      ██║  ██╔╝      ██║
╚██████╔╝╚████╗ ██║ ╚██╗██║  ██║╚████╗ ╚███╔═╝ ███████║  ██║   ██████║
 ╚═════╝  ╚═══╝ ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═══╝  ╚══╝   ╚══════╝  ╚═╝   ╚═════╝
```
---

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

RecSys is starting to adopt LLM for feature extraction, retrieval, and ranking/re-ranking! Although you can get some hands-on materials in either the [classics](#papers-classic-must-read) or some surveys, but since you're already interested in applying generative AI to industrial tasks, you probably wanna stay on the bleeding edge, right? That's exactly what this repo is for — automatically updated daily by agents with the latest generative RecSys papers fresh off arXiv, making sure that you never miss a beat.

> [!IMPORTANT]
> For those who are not familiar with GenRec, or not even the recommendation system, please checkout the kickstart posts [here](docs/kickstart.md).
> These posts are in Chinese, for English simply do your browser's internal translation or turn to __Ask Gemini__ :shipit:

## Quick Indexing
- [By Date](#by-date)
- [By Opensource](#by-opensource)
- [By Keyword](#by-keyword)
- [By Affiliation](#by-affiliation)
- [Papers Classic Must Read](#papers-classic-must-read)
- [Verl-GR: An Awesome RL Toolkit for GenRecSys](#verl-gr-an-awesome-rl-toolkit-for-genrecsys)

```mermaid
mindmap
  root((Awesome Generative RecSys))
    Decision Layer: LLM in Recommendation Chain
      Reasoning & RL
        Rank-GRPO -- Netflix
        DynamicPO -- USTC
        BLADE -- USTC
        SPRINT -- UTS
        CARE -- NUS / USTC
        Mult-DPO -- UVA / Netflix / Cornell
        CA-PG -- Meta / Cornell
        ProRL -- Fudan U
      Ranking & Reranking
        InvariRank -- RMIT
        LLM-as-Judge -- CityU HK
    Representation Layer: Model Training & Optimization
      Frameworks & Benchmarks
        MiniOneRec -- USTC
        OpenOneRec -- Kuaishou
        RecRM-Bench -- Shenzhen U
        SIDScope -- Huawei
        RPCBench -- Jilin University
        tau-Rec-Books -- Princeton University
      Efficient Decoding
        STATIC -- Google
      Optimization & Scaling
        MuonRec -- SJTU / Kuaishou
        Tencent Advertising -- Tencent
        LION -- NUS / Meta
        KL-MOPD -- Zhejiang U / Alibaba
    Feature Layer: Item Representation & Tokenization
      Semantic ID & Tokenization
        Latte -- UCSD
        FORGE SID -- Zhejiang U / Alibaba
        DACT -- Fudan U
        CHAP -- USTC
        OptST -- Shenzhen Tech U
        MV-Thinker -- City University of Hong Kong / Tencent
        Semantic-ID-Tutorial -- Huawei Ireland / UCD
      Feature Quality & Safety
        SafeGEO -- U Toronto / UCSD
        MemGen-GR -- CMU / UCSD / Meta
```

<div align="center">
  <i> Open-source Generative RecSys Map </i>
</div>

---
## `Verl-GR`: An Awesome RL Toolkit for GenRecSys
If you are interested in RFT your own GenRecSys, come check out our `verl`-based implementation called `verl-gr` here:
* [https://github.com/HaFred/verl-GR/tree/main/verl_gr/recipes/openonerec](https://github.com/HaFred/verl-GR/tree/main/verl_gr/recipes/openonerec)
* [https://github.com/HaFred/verl-GR/tree/main/verl_gr/recipes/rankgrpo](https://github.com/HaFred/verl-GR/tree/main/verl_gr/recipes/rankgrpo)

We manage to achieve 22% and 32% boosting for the end-to-end training efficiencies, compared with their respective vanilla implementations.

## By Date

We only keep the last 10 days summary below, for the past records before these, please see [the archive](docs/archive_by_month).

---

### Papers November 09

*Monday, November 9, 2026. The live arXiv 24-hour window (the Monday announcement; arXiv does not announce on weekends, so the freshest submissions are dated Nov 5-6) surfaced 4 strictly on-topic generative-recommendation / LLM-recommendation preprints: PHiT / 2611.09006, SID-LLM / 2611.08804, SteerGR / 2611.08790 and the memory-aware multi-agent conversational recommender / 2611.08718 — **below the 5-paper floor, so the fallback chain was applied**. (1) Missing dates in the current 10-day README window were checked: `date_list = [2026-11-05]` (there is no `### Papers November 05` section; that gap is now covered by the SID-LLM / SteerGR / ICTi entries below, and the pre-existing Oct 28 gap falls outside the 10-day window). (2) Papers published from the last paper summary date (November 08) through today were searched — the weekend produced no new submissions. (3) Still short of 5, the recent-backlog / last-3-month keyword pool was searched, adding 3 more strictly on-topic gen-rec preprints from Nov 1-3 and Oct 30 (Semantic-ID-Tutorial / 2611.04140, SA-OPSD / 2611.01568, ACT / 2611.00323). All 7 entries below were verified absent from README, both docs indexes and the monthly archive (981-ID dedup set). 1 is open-source (IDs That Mean Something / Huawei Ireland Research Center + University College Dublin, 7/10). By Opensource count 242 -> 243. Mindmap 30-leaf cap held (+Semantic-ID-Tutorial under Semantic ID & Tokenization; dropped LMStaR, a tied-lowest 7/10 leaf; all 3 layers retained).*

1. **Rethinking Latent Reasoning for Generative Recommendation: Beyond Teacher-Generated CoT and Recurrent Hidden-State Feedback**
   * Affiliation: Beihang University, School of Artificial Intelligence, Beijing, China — *(Yiwen Chen)* — with Baidu Inc., Beijing, China
   * Link: [arxiv.org/abs/2611.09006](https://arxiv.org/abs/2611.09006)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 6 Nov 2026)
   * TL;DR: Diagnoses which chain-of-thought steps actually help next-SID prediction, then replaces teacher-generated rationales with history-derived "thought tokens" that need only a single causal prefill, eliminating recurrent hidden-state feedback.
   * Key techniques:
     - Step-level CoT diagnosis combining target-SID likelihood, local trace coherence and student retraining: only the history-analysis step contributes positively on both dimensions
     - PHiT (Prefilled, History-Informed Thought Tokens): semantic targets built by aggregating cached sparse item encodings over observed user histories
     - Vocabulary thought tokens inserted as a contiguous block between history and target SID, supervised by a lightweight linear head jointly with the next-item SID objective
     - Teacher-free supervision: frozen sparse encoder and auxiliary head are discarded after training; inference is a standard causal prefill with unmodified token / KV-cache interfaces
     - SFT alone yields best results on all 24 main-table metrics across Beauty, Instruments, Sports and Steam (22 statistically significant); target construction for 131,413 examples in ~113 s on one GPU
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (no GitHub or anonymous repository linked in the paper or on arXiv)
     - **Novelty: 8/10** — first step-level diagnosis of CoT supervision for generative recommendation, plus a teacher-free single-prefill alternative to latent-reasoning loops
     - **Fairness: 3/10** — not addressed; no popularity, exposure or demographic bias analysis
     - **Robustness: 8/10** — four benchmarks, 24 metrics, five-seed controlled ablations and explicit supervision-cost measurements
     - **Impact: 8/10** — removes both CoT-generation cost and specialized decode loops, a direct serving win for deployed SID-based recommenders

2. **Generative Search and Recommendation at Shopify**
   * Affiliation: Shopify — *(Juhana Kangaspunta, Khalil Hajji, Darshan Fofadiya)*
   * Link: [arxiv.org/abs/2611.08804](https://arxiv.org/abs/2611.08804)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 5 Nov 2026)
   * TL;DR: Shopify casts both search and recommendation as semantic-ID generation with a single jointly pre-trained SID-LLM, then layers on RL, expert distillation and multi-token prediction plus a lightweight ranker to meet production latency over a billion-product catalog.
   * Key techniques:
     - Unified SID-LLM: joint pre-training on catalog and behavioral data gives search and recommendation a shared representation and training objective
     - Reinforcement learning further improves judged search relevance
     - Distillation from task-specific experts lifts recommendation quality over joint SFT with no statistically detected loss in search quality
     - Multi-token prediction paired with a lightweight ranker improves retrieval over the autoregressive baseline while reducing latency
     - Evaluated as a standalone retriever and inside Shopify's production search / recommendation stacks with offline and online A/B gains
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (industrial production system; catalog and behavioral data proprietary)
     - **Novelty: 7/10** — strong systems integration of known ingredients rather than a new algorithm; the unified search + rec SID objective is the distinctive part
     - **Fairness: 3/10** — no bias, exposure or cold-start fairness evaluation reported
     - **Robustness: 8/10** — offline plus online A/B tests at billion-product scale under strict latency budgets, with statistical significance testing
     - **Impact: 9/10** — rare end-to-end production evidence that SID generation can match a mature multi-model search stack

3. **SteerGR: Steering Generative Recommendation via Sparse Autoencoders for Controllable Game Discovery**
   * Affiliation: Sungkyunkwan University, Republic of Korea — *(Sunkyung Lee)* — with Roblox Corporation, USA
   * Link: [arxiv.org/abs/2611.08790](https://arxiv.org/abs/2611.08790)
   * Venue: arXiv preprint, November 2026 (cs.IR, cs.AI, cs.CL; submitted 5 Nov 2026)
   * TL;DR: SteerGR uses sparse autoencoders to expose human-readable concept features inside industrial generative recommenders and intervenes on them to steer game recommendations without retraining the model.
   * Key techniques:
     - Three-stage pipeline: LLM-grounded concept definition, SAE-based feature discovery/selection ranked by steering effect, then sparse feature intervention (amplify / suppress)
     - Connects human-readable concepts to internal features whose interventions measurably change recommended items
     - Concept-level control over SID generation with no retraining of the underlying recommender
     - Validated on two industrial generative recommendation models over a real-world game dataset
     - First extension of SAE-based activation steering from LLMs to industrial generative recommendation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (industrial models and game dataset; no repository linked)
     - **Novelty: 9/10** — first SAE-based concept-level steering for industrial generative recommendation; opens a new controllability axis
     - **Fairness: 5/10** — controllability could in principle support exposure / debiasing goals, but no fairness evaluation is run
     - **Robustness: 7/10** — two industrial models and real-world data, but a single domain and no public benchmark or multi-seed reporting
     - **Impact: 8/10** — a practical interpretability and control lever for deployed GR systems, from a major gaming platform

4. **Memory-Aware Multi-Agent Architecture with LLM-based Orchestration for Conversational Recommendation**
   * Affiliation: Instituto de Ciência e Tecnologia Itaú (ICTi), Brazil — *(Emilly Pitman de Castro)* — with Itaú Unibanco
   * Link: [arxiv.org/abs/2611.08718](https://arxiv.org/abs/2611.08718)
   * Venue: arXiv preprint, November 2026 (cs.AI; submitted 5 Nov 2026)
   * TL;DR: A memory-aware multi-agent conversational recommender in which LLMs orchestrate intent refinement, query construction and interaction flow, with long-term cross-session memory as a first-class routing input.
   * Key techniques:
     - LLM-as-orchestrator coordinating intent refinement, query construction and interaction flow across specialized agents
     - Long-term memory as a first-class component influencing both routing decisions and semantic query formation
     - Semantic Consistency Score (SCS), a complementary evaluation measure beyond Hit@K
     - Cross-session memory experiments, multi-turn conversational simulations and supervisor-driven interaction studies on Amazon Reviews
     - Memory recovers up to 63% of the gap toward explicit-query scenarios; supervisory orchestration adds +28.9 pp user acceptance; an exposure bottleneck between retrieved and displayed candidates is identified
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — system-level orchestration with memory as a first-class component and a new consistency metric, rather than a new recommendation model
     - **Fairness: 4/10** — no formal bias study, but it explicitly surfaces an exposure bottleneck between retrieval and display
     - **Robustness: 7/10** — three complementary evaluation protocols, yet a single dataset and LLM reranking does not improve Hit@K
     - **Impact: 7/10** — concrete deployment lessons for enterprise conversational recommendation from an applied industry group

5. **IDs That Mean Something: A Hands-On Tutorial on Semantic IDs for Recommender Systems**
   * Affiliation: Huawei Ireland Research Center, Dublin, Ireland — *(Roger Zhe Li)* — with University College Dublin
   * Link: [arxiv.org/abs/2611.04140](https://arxiv.org/abs/2611.04140)
   * Venue: CIKM '26 tutorial (35th ACM CIKM, Rome, Italy, 7-11 Nov 2026); arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026)
   * TL;DR: A hands-on CIKM '26 tutorial tracing the evolution from arbitrary raw item IDs to semantic IDs, shipped with self-contained Colab notebooks for RQ-KMeans tokenization, TIGER-vs-SASRec and cross-domain transfer.
   * Key techniques:
     - Semantic ID taxonomy: encoding item content, hierarchy and relationships directly into the item identity; RQ-VAE / RQ-KMeans quantization
     - Coverage of generative and discriminative uses, multimodality, collaborative signals, cold-start mitigation and cross-domain transfer
     - Hands-on sessions: train RQ-KMeans SIDs and inspect token structure against a raw-ID baseline on a generative recommendation task; evaluate cross-domain transfer with Cornac + Amazon Reviews
     - Open challenges: dynamic SIDs under catalog churn, multi-stakeholder utility, semantic planning and evaluation beyond hit rate
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/saghiles/semantic-id-tutorial](https://github.com/saghiles/semantic-id-tutorial) matches the tutorial exactly: three self-contained Jupyter notebooks (SID tokenizer, TIGER vs SASRec, cross-domain transfer), `train_and_save_models.py`, precomputed `item_features/` and `saved_models/` (Git LFS via `.gitattributes`), Colab-friendly; README is only two lines, no LICENSE, no pinned requirements/environment, no tests or CI, and the scope is teaching material rather than a full reproducible training pipeline
     - **Novelty: 6/10** — a tutorial/systematisation rather than a new method, but a timely consolidation of the fast-moving SID literature
     - **Fairness: 4/10** — discusses multi-stakeholder utility and evaluation beyond hit-rate, without any formal fairness analysis
     - **Robustness: 7/10** — runnable on free-tier resources with precomputed embeddings and baselines; no CI or environment pinning
     - **Impact: 8/10** — CIKM '26 tutorial with public teaching materials, likely to become a standard onboarding reference for SID research

6. **Search-Aware On-Policy Self-Distillation with Sibling Alignment for Generative Recommendation**
   * Affiliation: Kuaishou Technology, Beijing, China — *(Rongfeng Guo)* — with University of Amsterdam and Huazhong University of Science and Technology
   * Link: [arxiv.org/abs/2611.01568](https://arxiv.org/abs/2611.01568)
   * Venue: arXiv preprint, November 2026 (cs.LG, cs.AI; submitted 1 Nov 2026; WWW '27 submission noted in the paper)
   * TL;DR: SA-OPSD distils a privileged self-teacher into the states the student's own beam search actually visits, spending a fixed query budget on prefixes near the pruning boundary and decoupling target confidence from sibling-branch preferences.
   * Key techniques:
     - Evolving-Boundary Sampling (EBS): prioritises beam parents whose children sit near the global keep/prune cutoff, plus target-prefix retention-margin decline against an initial reference
     - Confidence-Decoupled Branch Distillation (CDBD): separates target-probability calibration from informative sibling relations
     - Privileged self-teacher (frozen Qwen2.5-1.5B-Instruct) sees the ground-truth item title; the student sees only the interaction history
     - Distillation over both GT-prefix and non-GT-prefix beam states; the deployed student keeps the same constrained beam decoder with no added inference stage
     - NDCG@10 0.1334 vs 0.1277 for Dense Beam / Full KL on Office; evaluated on Industrial, Office and Instruments
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (no repository linked in the paper or on arXiv)
     - **Novelty: 8/10** — first to treat beam search as a set of *competing prefixes* inside on-policy self-distillation, with a budgeted state selector
     - **Fairness: 3/10** — not addressed
     - **Robustness: 8/10** — three benchmarks, controlled ablations, explicit distillation-budget control and zero inference-time overhead
     - **Impact: 8/10** — beam search is the default GR decoder; directly improves a near-universal training/decoding interface

7. **Beyond Semantic IDs: Atomic Creator Tokens for Large-Scale Generative Recommendation**
   * Affiliation: Meta Platforms, Menlo Park, CA, USA — *(Zhuosheng Liu)*
   * Link: [arxiv.org/abs/2611.00323](https://arxiv.org/abs/2611.00323)
   * Venue: arXiv preprint, October 2026 (cs.AI; submitted 30 Oct 2026)
   * TL;DR: Argues the SID layer — not the language model — is the binding constraint in creator recommendation, and replaces many-to-one quantized SIDs with one end-to-end learned token per creator, giving a bijective map and direct top-k over creator logits.
   * Key techniques:
     - Diagnosis: SID collisions force a popularity tie-break that caps creator-level recall and favours already-popular creators; a frozen quantizer also blocks gradients from reaching creator representations
     - Atomic Creator Token (ACT): one vocabulary token per creator trained end-to-end; bijective mapping eliminates collisions
     - Inference becomes a direct top-k over creator logits, with no autoregressive SID decoding
     - +19.8 points (1.84x) creator Recall@15 over a matched SID baseline with the token layer as the only variable; still leads against a 64x larger codebook; ~2.7x lower per-user latency
     - Public KuaiRand validation (only method to beat a global-popularity baseline) plus a live A/B test positive on every reported metric
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (industrial production data; no repository linked)
     - **Novelty: 8/10** — a clean, contrarian challenge to the dominant SID tokenization recipe, backed by a production-scale controlled comparison
     - **Fairness: 6/10** — explicitly targets the popularity favouritism induced by SID collision tie-breaks and improves cold-start creator recall
     - **Robustness: 8/10** — single-variable controlled comparison, 64x codebook ablation, public dataset and live A/B test
     - **Impact: 9/10** — Meta production evidence questioning a core assumption of the entire SID-based generative recommendation line

---

### Papers November 08

*Sunday, November 8, 2026. The live arXiv cs.IR window for the last 24 hours (Nov 7–8) carried **no** new generative-recommendation preprints — arXiv announces Mon–Fri, and the newest submissions are dated Nov 5 (already indexed on Nov 06). Per the fallback rule, this daily section draws 5 strictly on-topic generative-rec preprints from the recent backlog (late Oct–early Nov 2026, cs.IR/cs.AI/cs.CY) that were verified absent from README, the docs indexes, and the monthly archive. Missing dates in the 10-day window (Nov 05, Oct 28) were checked: Nov 05 is represented by the brand-bias audit below and no further on-topic preprint was found for Oct 28. 0 are open-source (all five are very recent preprints, several from industry, with no public code released). By Opensource count unchanged (242). Mindmap unchanged (no new open-source papers; 30-leaf cap retained, all 3 layers kept).*

1. **Where Beam Search Loses Top-Ranked Items: First-Step Coverage in Generative Recommendation**
   * Affiliation: Ant Group, Hangzhou, China — *(Heng Yao)* — with Independent Researcher (Hanwei Zhu)
   * Link: [arxiv.org/abs/2611.01072](https://arxiv.org/abs/2611.01072)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 31 Oct 2026)
   * TL;DR: Identifies a "first-step coverage bottleneck" in beam-search decoding for generative recommendation (TIGER): every pruned exact top-10 path is first lost at the initial decoding step; reallocating beam width to the first SID position recovers wide-beam ranking at roughly half the prefix-capacity budget.
   * Key techniques:
     - First-step coverage bottleneck: empirical finding across 6 TIGER settings (3 domains × 2 SID constructions) that all pruned top-10 paths die at step 1
     - Exact-catalog reference: isolates beam-search losses from model errors
     - Controlled budget intervention: shifts beam width to the first SID position, raising Search Recall@10 by 0.96–10.90 pp at Beam-50's budget; reproduces Beam-100's top-10 at nominal budget 151 vs 301
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (5-page preprint; no repository released)
     - **Novelty: 8/10** — reframes beam width as a per-position allocation problem and gives an actionable serving decision for gen-rec
     - **Fairness: 3/10** — not a focus
     - **Robustness: 7/10** — six settings, 77,373 test users, RQ-VAE tokenization; controlled larger-candidate experiments
     - **Impact: 7/10** — directly affects the serving cost/quality tradeoff for deployed TIGER-style recommenders

2. **SIDRec: End-to-End Semantic ID Representation and Modeling for Recommendation**
   * Affiliation: The Hong Kong Polytechnic University, Hong Kong SAR, China — *(Zhuohang Jiang)* — with University of Electronic Science and Technology of China (Yongsen Pan), Southwest Jiaotong University (Zheng Hu), and others
   * Link: [arxiv.org/abs/2611.01136](https://arxiv.org/abs/2611.01136)
   * Venue: arXiv preprint, October 2026 (cs.IR, cs.AI; submitted 31 Oct 2026)
   * TL;DR: SIDRec is an end-to-end recommendation-aware Semantic ID learning framework that jointly models content and collaborative signals and aligns SID construction with downstream recommendation objectives, fixing the semantic-mismatch and objective-mismatch limitations of prior SID methods.
   * Key techniques:
     - Recommendation-aware SID learning: end-to-end joint content + collaborative modeling
     - Semantic–collaborative alignment: reduces mismatch between content semantics and collaborative preferences
     - Objective alignment: aligns SID construction with downstream recommendation optimization
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (searched GitHub; the unrelated repo "sidivhub/Sidrec" is a JavaScript project, not this paper)
     - **Novelty: 8/10** — end-to-end recommendation-aware SID construction targeting two concrete limitations
     - **Fairness: 3/10** — not a focus
     - **Robustness: 7/10** — multiple datasets and baselines reported
     - **Impact: 7/10** — SID is core gen-rec infrastructure; academic (HK PolyU) contribution

3. **SPADE: Spatiotemporal Preference Alignment and Diversity Enhancement for Local Search**
   * Affiliation: Meituan, Beijing, China — *(Chenxu Wang)* — with one Independent co-author (Shuxian Bi)
   * Link: [arxiv.org/abs/2611.04662](https://arxiv.org/abs/2611.04662)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026)
   * TL;DR: SPADE frames proactive query recommendation on local-service apps as an open-set generation problem (vocabulary of millions), aligning user preference with fine-grained spatiotemporal context, covering long-tail intents, and diversifying candidates within a few slots.
   * Key techniques:
     - Open-set generative query recommendation: generates queries from a million-scale vocabulary
     - Spatiotemporal preference alignment: fine-grained geographic + temporal context modeling
     - Long-tail intent coverage and diversity enhancement within limited candidate slots
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (industrial Meituan; no repository released)
     - **Novelty: 7/10** — frames local-search query rec as open-set generation with spatiotemporal + diversity constraints
     - **Fairness: 4/10** — long-tail intent coverage partially addresses exposure; not a core focus
     - **Robustness: 7/10** — industrial setting with online-oriented evaluation
     - **Impact: 8/10** — Meituan production local search; practical generative ranking/retrieval

4. **IntentGEO: Intent-aware Generative Engine Optimization for Recommendation**
   * Affiliation: Renmin University of China, Beijing, China — *(Runlin Lei)* — with National University of Singapore (Shiqi Zhang, Xiaokui Xiao) and Zhewei Wei (Renmin University of China)
   * Link: [arxiv.org/abs/2611.04225](https://arxiv.org/abs/2611.04225)
   * Venue: arXiv preprint, November 2026 (cs.IR, cs.AI; submitted 3 Nov 2026)
   * TL;DR: IntentGEO formulates intent-aware Generative Engine Optimization for recommendation, evaluating how changing user intent affects item visibility in LLM-generated responses, since a shared item description serves users with different decision goals.
   * Key techniques:
     - Intent-aware GEO: models visibility gain as dependent on user request / intent
     - Intent formulation across dimensions (e.g., need specificity)
     - Evaluation of how intent variation shifts item visibility in generative search
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (searched GitHub; no IntentGEO repository)
     - **Novelty: 7/10** — extends GEO from content-centric to intent-aware for recommendation
     - **Fairness: 5/10** — touches visibility equity across intents; not a deep fairness treatment
     - **Robustness: 6/10** — evaluation-focused; limited method/baseline depth visible
     - **Impact: 7/10** — GEO-for-rec is an emerging, practically relevant area; Renmin + NUS

5. **The Popular Get More Popular: Auditing Brand Bias in Generative Search**
   * Affiliation: Politecnico di Milano, Italy — *(Giorgio Monaco, Jacopo Lenti, Francesco Pierri)*
   * Link: [arxiv.org/abs/2611.07614](https://arxiv.org/abs/2611.07614)
   * Venue: arXiv preprint, November 2026 (cs.CY, cs.AI, cs.SI; submitted 5 Nov 2026)
   * TL;DR: Audits brand popularity and familiarity bias in generative search engines, showing dominant brands are cited 1.4×–2.8× more and that authentic brand signatures give a ranking advantage content rewrites cannot overcome — a "rich-get-richer" dynamic with entry barriers.
   * Key techniques:
     - Two-dimensional brand-bias audit: popularity bias + familiarity (parametric-memory) bias
     - Commercial-query evaluation across major generative engines (1,176 top brands)
     - Controlled in-context experiments holding product attributes constant to isolate brand-signature effect
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code found (searched GitHub; none matching this audit)
     - **Novelty: 7/10** — formalizes brand familiarity bias as a parametric-memory entry barrier in generative search
     - **Fairness: 8/10** — directly audits provider/brand fairness and market-entry barriers
     - **Robustness: 7/10** — large commercial-query sample plus controlled experiments
     - **Impact: 7/10** — policy-relevant audit of LLM-driven product recommendations; Politecnico di Milano

---

### Papers November 07

*Saturday, November 7, 2026. The live arXiv cs.IR/cs.CL/cs.AI/cs.LG window for the last 24 hours (Nov 6-7) carried **no** new generative-recommendation preprints — arXiv announces Mon–Fri, and the newest submissions are dated Nov 5 (already indexed on Nov 06). Per the fallback rule, this daily section draws 5 strictly on-topic generative-rec preprints from the recent backlog (late Oct–early Nov) in cs.AI/cs.CL that were verified absent from README, the docs indexes, and the monthly archive. 1 is open-source (MV-Thinker / City University of Hong Kong + Tencent, 7/10). By Opensource count 241 -> 242. Mindmap updated (+MV-Thinker under Semantic ID & Tokenization; dropped LLM4Rec-CF-Bias to hold the 30-leaf cap; all 3 layers retained).*

1. **LatentRec: Do Recommenders Need to Think in Words? Latent Reasoning for Efficient LLM-Based Recommendation**
   * Affiliation: Tencent, Shenzhen, Guangdong, China — *(Hongyang Su, Beibei Kong, Lei Cheng, Chengxiang Zhuo, Zang Li)*
   * Link: [arxiv.org/abs/2611.07866](https://arxiv.org/abs/2611.07866)
   * Venue: CIKM 2026 (Short Paper)
   * TL;DR: LatentRec replaces inference-time chain-of-thought / latent reasoning with training-time per-step head supervision, so the reasoning module is discarded at deployment and latency drops 18.3x with no accuracy loss.
   * Key techniques:
     - Continuous Thought Module (2.5M params): K latent reasoning steps over the LLM hidden state during training
     - Soft Token Selection: bridges the ~14x norm gap between hidden states and input embeddings
     - Per-step Reasoning Loss (PRL): supervises every intermediate state through the prediction head against the first token of the target Semantic ID
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (CIKM short paper; no repository link released)
     - **Novelty: 7/10** — reframes latent reasoning as training-time supervision rather than inference-time computation; neat "discard-at-inference" idea, but latent reasoning for rec is already an active area
     - **Fairness: 3/10** — not a focus
     - **Robustness: 7/10** — three Amazon benchmarks, consistent gains, 18.3x lower latency at batch=1
     - **Impact: 7/10** — CIKM 2026, Tencent; directly addresses the latency-vs-reasoning tradeoff in production LLM recommenders

2. **MV-Thinker: Think Globally, Generate Personally**
   * Affiliation: City University of Hong Kong, Hong Kong, China — *(Yuxuan Hu, Yingyi Zhang, Wenlin Zhang, Chao Zhang, Haotian Nan, Ziwei Liu, Jiancheng Dong, Tongzhou Wu)* — with Tencent Platform and Content Group, Shenzhen, China (co-authors Beibei Kong, Lei Cheng, Chengxiang Zhuo, Zang Li)
   * Link: [arxiv.org/abs/2611.02463](https://arxiv.org/abs/2611.02463)
   * Venue: arXiv preprint, November 2026 (cs.AI)
   * TL;DR: MV-Thinker coordinates full-history and recent-history views via multi-view temporal thinking and adapts decoder states per user via hierarchical residual adapters, improving both discriminative and generative rec baselines on four datasets.
   * Key techniques:
     - Multi-View Temporal Thinking: view-specific thinking queries/readers over overlapping full-history and recent-history views
     - Hierarchical Residual Adaptation: nested residual adapters before the shared vocabulary projection for personalized SID decisions
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — code + datasets at [anonymous.4open.science/r/MV-Thinker](https://anonymous.4open.science/r/MV-Thinker); anonymous (double-blind) repo, no explicit license / maintenance maturity yet
     - **Novelty: 8/10** — explicitly coordinates complementary temporal views and personalizes progressive SID decoding
     - **Fairness: 4/10** — not a focus
     - **Robustness: 7/10** — four public datasets, beats strong discriminative and generative baselines across ranking metrics
     - **Impact: 7/10** — academic (CityU HK) + industrial (Tencent) backing; practical SID-generation improvement

3. **HiGenTrans: Hierarchical LLM Knowledge Transfer for Generative Recommendation**
   * Affiliation: The Hong Kong Polytechnic University, Hong Kong SAR, China — *(Zhuohang Jiang, Haohao Qu, Wenqi Fan, Qing Li)* — with Kuaishou Technology, Beijing, China (co-authors); first author's internship at Kuaishou
   * Link: [arxiv.org/abs/2611.01129](https://arxiv.org/abs/2611.01129)
   * Venue: arXiv preprint, October 2026 (cs.AI)
   * TL;DR: HiGenTrans injects LLM knowledge into generative recommendation at three levels — input (semantic priming), representation (layer-wise transfer), and decision (Mixture-of-Experts beam reranking) — lifting Recall@10 by up to 12.9% and NDCG@10 by up to 33.7%.
   * Key techniques:
     - Global Semantic Priming (GSP): LLM-derived user representation as BOS embedding prior
     - Hierarchical Representation Transfer (HRT): mean-centered projections + gated residuals into depth-matched GenRec layers
     - Multi-Signal Decision Calibration (MDC): lightweight MoE calibrator reranking beam-search outputs using semantic relevance, generation confidence, candidate context
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 8/10** — hierarchical (input/representation/decision) LLM-to-GenRec knowledge transfer; MDC explicitly recalibrates beam-search ranking
     - **Fairness: 4/10** — not a focus
     - **Robustness: 7/10** — three public benchmarks, strong gains; features computed only from observable prefix (no leakage)
     - **Impact: 8/10** — Kuaishou (major industrial GenRec player); large empirical lifts

4. **UAGR: Utility-Aware Generative Recommendation**
   * Affiliation: Kuaishou Technology, Beijing, China — *(Yang Hu, Duo Wang, Ning Li, Kang Li, Junda She, Chengcheng Guo, Kuo Cai, Bin Liu, Youhua Liu, Xiaoshuang Chen)*
   * Link: [arxiv.org/abs/2611.02981](https://arxiv.org/abs/2611.02981)
   * Venue: arXiv preprint, November 2026 (cs.LG); fully deployed on Kuaishou
   * TL;DR: UAGR aligns both SID construction and beam decoding with downstream multi-objective utility, injecting item-level utility into SIDs and into beam scoring to avoid prematurely pruning high-utility paths; +0.206% online watch time at Kuaishou scale.
   * Key techniques:
     - Utility-Enriched Semantic Codes: inject item-level post-exposure utility into SIDs without increasing SID length or vocabulary, supporting incremental utility updates
     - Utility-Guided Decoding: fuse multiple post-exposure outcome predictions into beam scoring, reducing premature pruning of high-utility paths
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (industrial, fully deployed)
     - **Novelty: 8/10** — jointly fixes SID construction and beam decoding for utility alignment; tackles the premature-pruning failure mode
     - **Fairness: 4/10** — utility-driven objective is not examined for fairness/long-tail side effects
     - **Robustness: 8/10** — offline experiments + online A/B at Kuaishou scale (+0.206% watch time)
     - **Impact: 9/10** — fully deployed in production at Kuaishou; concrete industrial impact

5. **ICE: Beyond Independent Predictions — Learning the Browsing Journey for Sequence-Level Re-ranking**
   * Affiliation: Alibaba Group (Taobao & Tmall), Hangzhou, China — *(Jiayi Zhang, Jingxin Hai, Zhenjia Ma, Hongbin Pei, Dagui Chen, Han Zhu, Jian Xu)*
   * Link: [arxiv.org/abs/2611.07591](https://arxiv.org/abs/2611.07591)
   * Venue: arXiv preprint, November 2026 (cs.IR)
   * TL;DR: ICE replaces the Independent Behavior Modeling paradigm in Generator–Evaluator re-ranking with Joint Behavior Modeling (display -> impression -> click), cutting spurious context and capturing intra-sequence dependencies; +0.70% clicks and +3.67% revenue in a 14-day Taobao A/B.
   * Key techniques:
     - Joint Behavior Modeling (JBM): explicitly models display -> impression -> click to capture causal and competitive dependencies
     - Impression-Click Evaluator (ICE): predicts browsing-depth distribution, suppresses unexposed-item context, click-distribution matching objective
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — reframes sequence-level re-ranking as joint impression/click modeling rather than independent per-item scoring
     - **Fairness: 4/10** — not a focus
     - **Robustness: 8/10** — diverse backbones, 14-day online A/B (Taobao +0.70% clicks, +3.67% revenue) and full-traffic deployment
     - **Impact: 8/10** — Alibaba/Taobao production; strong online revenue uplift

---

### Papers November 06

*Friday, November 6, 2026. The live arXiv cs.IR window for the last 24 hours (papers submitted Nov 4-5) carried 7 strictly on-topic generative-recommendation preprints, all verified absent from README, the docs indexes, and the monthly archive. 3 are open-source (LLM4Rec-CF-Bias / UC San Diego, 6/10; OptST / Shenzhen Technology University, 7/10; LMStaR / Sorbonne University, 7/10). By Opensource count 238 -> 241. Mindmap updated (+LLM4Rec-CF-Bias under Reasoning & RL; +OptST under Semantic ID & Tokenization; +LMStaR under Ranking & Reranking; dropped HARP, Eval4DiRec, RecRSI to hold the 30-leaf cap; all 3 layers retained).*

1. **BRIDGE: Bridging the Semantic Quantization Gap for Generative Recommendation**
   * Affiliation: Kuaishou Technology, Beijing, China — *(Yatong Xiao, Mingjie Sun, Peng Wang, Wenjin Wu, Peng Jiang)*
   * Link: [arxiv.org/abs/2611.07425](https://arxiv.org/abs/2611.07425)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 5 Nov 2026)
   * TL;DR: BRIDGE exposes the Semantic Quantization Gap (SQG) — the decoder sees only discrete SIDs and loses the continuous structure (centroids, neighborhood geometry, level-wise entropy) that produced them — and bridges it via codebook-grounded latent reasoning, privileged EMA self-distillation, and effort-aware recurrence, lifting Recall@10/NDCG@10 by ~10% and eCPM by 0.65% in a one-week online A/B.
   * Key techniques:
     - Semantic Quantization Gap (SQG): grounding gap, neighborhood gap, and difficulty gap
     - Codebook-grounded latent reasoning: inject frozen quantizer centroids as semantic anchors before SID generation
     - Privileged EMA self-distillation: teacher transfers neighborhood-aware knowledge to an on-policy student, mitigating exposure bias
     - Effort-aware recurrence: allocates more compute to early SID levels, less with depth
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available (the GitHub "raochongzhi/BRIDGE" hit is an unrelated job-rec paper; this BRIDGE releases no code)
     - **Novelty: 8/10** — names and attacks the SQG, a concrete bottleneck in SID-based generative recommendation
     - **Fairness: 4/10** — neighborhood-gap analysis mitigates exposure bias, but not a core focus
     - **Robustness: 7/10** — three Amazon benchmarks plus a one-week online A/B (eCPM +0.65%)
     - **Impact: 8/10** — Kuaishou; direct online e-commerce advertising gain

2. **OptST: Optimizing Semantic Tokenization for LLM-Enhanced Recommendation**
   * Affiliation: Shenzhen Technology University, Shenzhen, China — *(Hanchong Chen, Jie Liu, Lingjie Li, Xiuqiang He, Xing Tang)* — with Shenzhen University, The Hong Kong Polytechnic University, McGill University
   * Link: [arxiv.org/abs/2611.07523](https://arxiv.org/abs/2611.07523)
   * Venue: Findings of WSDM 2027 (cs.IR; submitted 5 Nov 2026)
   * TL;DR: OptST makes a frozen pretrained semantic tokenizer task-aware for downstream recommendation via a low-rank deformation (anchor-regularized) plus a straight-through estimator and an interaction-conditioned prefix-depth selector, lifting AUC across 4 datasets and 5 backbones without touching the encoder or codebooks.
   * Key techniques:
     - Low-rank deformation of the assignment geometry with an anchor regularizer (preserves pretrained semantics)
     - Straight-through estimator: hard nearest-code at prediction, surrogate gradient to the deformation
     - Interaction-conditioned prefix-depth selector: per-interaction token depth via a continue-or-stop STE + depth regularization
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/chchchchc1023/wsdm27-optst](https://github.com/chchchchc1023/wsdm27-optst): official implementation releasing prompts and generation settings; deductions: appears to ship prompts/settings rather than the full training pipeline, no explicit LICENSE spotted, niche scope
     - **Novelty: 8/10** — task-aware semantic tokenization as an interface between LLM profiles and rec models
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — four public datasets, five additional backbones, ablations
     - **Impact: 7/10** — WSDM 2027; relevant to LLM-enhanced rec feature interfaces

3. **Deliberate Latent Reasoning for Sequential Recommendation**
   * Affiliation: Renmin University of China, Beijing, China — *(Haobo Zhang, Qiannan Zhu, Yutao Zhu, Zhicheng Dou)*
   * Link: [arxiv.org/abs/2611.06521](https://arxiv.org/abs/2611.06521)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 4 Nov 2026)
   * TL;DR: DESRec performs personalized latent reasoning for sequential recommendation: a reasoning-step selector picks the optimal depth per user during training, self-distillation compresses the most informative state into the final step, and progressive preference extraction segments history into variable-count milestones — beating 8 baselines on 6 datasets.
   * Key techniques:
     - Reasoning step selection module (optimal depth per user sequence)
     - Self-distillation: compress the most informative state into the final reasoning step used as the inference representation
     - Progressive preference extraction: variable-number history segmentation into latent milestones
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 8/10** — moves beyond fixed-depth latent reasoning to deliberate per-user depth
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — six datasets, four backbones, eight baselines
     - **Impact: 7/10** — Renmin University of China; strong sequential-rec results

4. **Generative Retrieval under Real-Time Supply Constraints in Local Commerce**
   * Affiliation: Tsinghua University, Beijing, China — *(Shaopeng Liang, Biao Zhang, Hongzhen Ye, Zeyang Hou, Ma Jiang, Jintao Tu, Zhijia Fang, Jianqiang Cao, Junxue Rao, Jia Jia)* — with a local-commerce / food-delivery platform
   * Link: [arxiv.org/abs/2611.06323](https://arxiv.org/abs/2611.06323)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 4 Nov 2026; v2 5 Nov 2026)
   * TL;DR: RTP-LLM does generative retrieval over a request-time supply snapshot for local commerce: it compiles eligible residual-quantization identifiers into a CSR prefix index, overlaps CPU compilation with model prefill, and shares the index across beams so infeasible (out-of-supply) merchants are pruned before beam capacity is spent.
   * Key techniques:
     - Request-time supply snapshot materialization (snapshot-relative identifier validity)
     - CSR (compressed sparse row) prefix index compiled on CPU, overlapped with model prefill
     - Index shared across beams; constraint states follow selected beam parents; legal expansions retain original-model log-probs
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — frames real-time supply as a decoding-constraint problem for GR in local commerce
     - **Fairness: 3/10** — not addressed
     - **Robustness: 6/10** — system/implementation study on three geo settings; does not establish compute savings at matched quality
     - **Impact: 6/10** — practical industrial system, narrow scope (local retail / food delivery)

5. **Item Representations Matter: Bridging Hard Semantic IDs and Soft Prototype Mixtures for Generative Retrieval**
   * Affiliation: Meta Platforms, Inc., USA — *(Vicente Balmaseda, Dongqi Fu, Jiarui Feng, Ren Chen, Hanqing Zeng, Tianxin Wei, Yinglong Xia, Hong Li)* — with Texas A&M University (Tianbao Yang, Vicente Balmaseda)
   * Link: [arxiv.org/abs/2611.05799](https://arxiv.org/abs/2611.05799)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.LG; submitted 4 Nov 2026)
   * TL;DR: CAP-Mix is a flow recommender that represents each item as a soft mixture of shared prototypes plus an item-specific vector (trained jointly, retained at inference), showing continuous recommenders can gain SID-like parameter tying without a discrete bottleneck — +6.9% HR@5 / +13.6% NDCG@5 over best baselines with 1.4-161x throughput.
   * Key techniques:
     - Soft prototype mixture: assignments, prototypes, and item vectors trained jointly
     - Optional pretrained priors: SID responsibilities as an assignment prior; full content embedding initializes the item vector
     - Flow-based generative retrieval with shared structure and no hard quantization
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code for CAP-Mix (only baseline repos cited)
     - **Novelty: 8/10** — bridges hard SID and flat continuous tables via soft prototype mixtures
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — six benchmarks, throughput analysis vs discrete baselines
     - **Impact: 8/10** — Meta; reframes the hard-SID vs continuous trade-off

6. **What Gets Hacked in a Collaborative Reward for LLM Recommenders: The Part That Does Not Depend on the User**
   * Affiliation: University of California, San Diego, USA — *(Zhuangsheng Li, Liang Dong, Yu Wu, Dailin Li, Yu Xia, Yunhan C. Zhang, Rui Cai, Yi Wu, Julian McAuley)*
   * Link: [arxiv.org/abs/2611.07588](https://arxiv.org/abs/2611.07588)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 5 Nov 2026)
   * TL;DR: Training LLM recommenders with collaborative-filtering (CF) rewards causes exposure collapse; the paper decomposes each CF score into an item-mean and a residual, shows the item-mean drives collapse, and proposes per-item centering / standardization that increases distinct top-1 items by up to 9.8x at comparable accuracy.
   * Key techniques:
     - Decompose CF reward into item-mean (average CF score across users) + residual (per-user deviation)
     - Per-item centering: subtract the estimated item mean
     - Per-item standardization: rescale the residual by its estimated standard deviation
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 6/10** — [anonymous.4open.science/r/LLM4Rec-CF-Bias-27EF](https://anonymous.4open.science/r/LLM4Rec-CF-Bias-27EF/): code release for the reward corrections; deductions: anonymous, doc/quality unverifiable, no explicit LICENSE
     - **Novelty: 8/10** — clean decomposition of why CF rewards cause exposure collapse
     - **Fairness: 7/10** — directly targets exposure evenness / catalog coverage (item-side fairness)
     - **Robustness: 7/10** — two datasets, two identifier schemes, controlled interventions
     - **Impact: 8/10** — McAuley lab; directly actionable for RL-trained LLM recs

7. **Learning to Rank Explanations for Recommendation with Language Models**
   * Affiliation: Sorbonne University, Paris, France — *(Ben Kabongo)* — with AgroParisTech, UMR MIA Paris-Saclay, Palaiseau, France (Vincent Guigue)
   * Link: [arxiv.org/abs/2611.04775](https://arxiv.org/abs/2611.04775)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026)
   * TL;DR: LMStaR formulates personalized explanation ranking as dense retrieval: a query encoder represents user history + target-item metadata and a statement encoder maps candidate explanations into a shared space, jointly adapted via multi-positive contrastive learning — beating CLER by up to 8.25 NDCG@1 points.
   * Key techniques:
     - Fully text-based explanation-ranking as dense retrieval
     - Query encoder (user history + item metadata) + statement encoder (candidate explanations)
     - Multi-positive contrastive learning for personalized relevance
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/BenKabongo25/language-models-statement-ranking](https://github.com/BenKabongo25/language-models-statement-ranking): full code, data, and supplementary materials; deductions: niche explanation-ranking scope, single-maintainer repo
     - **Novelty: 7/10** — adapts LMs to personalized statement ranking for explanations
     - **Fairness: 4/10** — personalized relevance; not a fairness focus
     - **Robustness: 7/10** — three datasets, five backbones, counterfactual analyses
     - **Impact: 6/10** — explanation ranking niche; Sorbonne / AgroParisTech


### Papers November 04

*Wednesday, November 4, 2026. The live arXiv cs.IR / cs.AI / cs.CL window for the last 24 hours (papers submitted Nov 3) carried 7 strictly on-topic generative-recommendation preprints, all verified absent from README, the docs indexes, and the monthly archive. 2 are open-source (HARP / Harbin Institute of Technology, Shenzhen, 7/10; tau-Rec-Books / Princeton University, 7/10). By Opensource count 236 -> 238. Mindmap updated (+HARP under Ranking & Reranking; +tau-Rec-Books under Frameworks & Benchmarks; dropped PFA and SODA to hold the 30-leaf cap; all 3 layers retained).*

1. **ZeroGR: Filtering-First Constrained Decoding for Generative Recommendation**
   * Affiliation: The University of Hong Kong, Hong Kong, China — *(Xiangrui Yang, Jiawei Yang, Liang Zeng, Daqian Ding, Ziqian Liu, Bing Tian, Cheng Peng, Yunfeng Zhao, Fangyu Zhang, Jiaqiang Liu, Xiao Liang, Yiming Qiu)* — with Peking University, Kuaishou Technology, Huazhong University of Science and Technology
   * Link: [arxiv.org/abs/2611.04715](https://arxiv.org/abs/2611.04715)
   * Venue: arXiv preprint, November 2026 (cs.DB; cs.IR; submitted 3 Nov 2026)
   * TL;DR: ZeroGR is a filtering-first constrained-decoding system for generative recommendation that applies validity filtering before relevance scoring, using a step-sliced filtering index, shared-slot execution, and hybrid projection to cut GPU memory and accelerate the filtering/scoring pipeline by up to 9.9x.
   * Key techniques:
     - Filtering-first ordering: validity filtering before relevance scoring in constrained decoding (most sequences are invalid, so scoring-first wastes compute)
     - Step-sliced filtering index: tailors data representations to each decoding step to reduce GPU memory
     - Shared-slot execution: accelerates data exchange across pipeline stages
     - Hybrid projection: adapts computation to workload patterns
     - Layout-guided streaming construction for fast index refresh with limited serving interference
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — system-level insight (filter-first) for genrec constrained decoding
     - **Fairness: 3/10** — not a focus
     - **Robustness: 7/10** — extensive system evaluation; strong engineering but a single-system study
     - **Impact: 7/10** — directly relevant to production genrec serving; from HKU / Kuaishou

2. **ReuseGR: Offline-Online Decoupled Generative Retrieval via Adaptive Prefix Reuse**
   * Affiliation: Xidian University, Xi'an, China — *(Xujing Wang, Yufeng Chen, Boxuan Zhang, Chao Wei, Cai Xu, Jie Zhao, Weiru Zhang, Wei Zhao, Ziyu Guan)* — with Alibaba International Digital Commerce Group; to appear WWW 2027
   * Link: [arxiv.org/abs/2611.04259](https://arxiv.org/abs/2611.04259)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026); to appear WWW 2027
   * TL;DR: ReuseGR decouples generative retrieval into an offline 7B planner that shares SID prefix sets across requests with the same query and a 0.5B online model that personalizes completion, reusing large-model computation while keeping retrieval personalized; uses Path KD and GRPO-based BudgetCut.
   * Key techniques:
     - Offline-online decoupling: query-level candidate planning (offline 7B) vs request-level personalized completion (online 0.5B)
     - Adaptive prefix reuse: ReuseCut picks a cache depth per query by historical coverage
     - Path-level knowledge distillation (Path KD): transfers 7B suffix-scoring knowledge to 0.5B
     - BudgetCut: branch selection under a fixed budget, initialized by on-policy distillation and refined with GRPO
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 8/10** — prefix reuse for genret serving is a fresh efficiency angle
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — industrial dataset plus a 14-day online A/B test
     - **Impact: 8/10** — Alibaba International; online A/B gains (CTR +0.93%, revenue +1.05%)

3. **OneTrans-GSR: A Generative Slate Ranking Paradigm Unifying Reranking and Mix-Ranking with One Autoregressive Transformer**
   * Affiliation: ByteDance, China — *(Global E-Commerce Recommendation Foundation Team; Feng Cheng, Yu-Hsuan Huang, Fengyi Wang, Chaofan Zhou, Zhennan Zhu, Huan He, Bo Zhang, Ruoqi Zhang, Zhanfeng Mo, Ziwei Liu, Lanyi Li, Yifeng Pan, Junhua Long, Ziqiu Zhou, Yue Lin, Shaowei Liu)*
   * Link: [arxiv.org/abs/2611.04720](https://arxiv.org/abs/2611.04720)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026)
   * TL;DR: OneTrans-GSR reformulates reranking and mix-ranking (combining product cards, short videos, livestreams, and ads) as a unified generative slate-ranking problem solved by a single autoregressive transformer that extends the deployed OneTrans backbone, trained with a reward model and RL toward slate-level and long-term objectives, and deployed at ByteDance.
   * Key techniques:
     - Unified reranking plus mix-ranking as one generative slate-generation problem
     - Single decoder-only policy extending the deployed OneTrans backbone
     - Reward model evaluates complete slates; RL optimizes slate-level and long-term objectives
     - Explicit business-constraint enforcement during decoding
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 8/10** — unifies heterogeneous slate generation into one learned policy
     - **Fairness: 4/10** — not a focus (constraint enforcement is business-objective)
     - **Robustness: 7/10** — deployed, large-scale online A/B (GMV/u +2.63%, advertiser value +2.06%, repurchase +2.03%, latency -13%)
     - **Impact: 9/10** — ByteDance industrial deployment with strong online gains

4. **SourceFlow: Collaborative Source Coupling for Flow-Based Recommendation**
   * Affiliation: The Hong Kong University of Science and Technology (Guangzhou), Guangzhou, China — *(Chenghao Wu, Yongqi Zhou, Jin Chen, Yifeng Zhou, Jinchang Zhu, Junwei Pan, Chao Zhou, Zhixiang Feng, Chengguo Yin, Menglin Yang)* — with Tencent Inc., Shenzhen, China
   * Link: [arxiv.org/abs/2611.04455](https://arxiv.org/abs/2611.04455)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026); under review
   * TL;DR: SourceFlow improves flow-based collaborative filtering by injecting collaborative structure directly into the source distribution (Neighborhood Coupling, Collaborative Consensus, Stretched Restoration) instead of conditioning the predictor, yielding a mean +15.7% relative Recall@10 gain over the strongest flow-based baseline.
   * Key techniques:
     - Flow-based collaborative filtering: learns a discrete path from a sampled source to observed interactions (few-step inference)
     - Neighborhood Coupling: constructs displaced binary sources replacing historical items with collaborative alternatives
     - Collaborative Consensus: refines replacement probabilities using evidence from users who share the observed item
     - Stretched Restoration: retains replacements at late flow times during training
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — code will be released upon acceptance (not yet public)
     - **Novelty: 8/10** — reframes source sampling as collaborative-structure modeling for flow-based rec
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — five datasets with controlled experiments; flow-based method
     - **Impact: 7/10** — Tencent; solid empirical gains in an emerging flow-based genrec direction

5. **HARP: Training-Free Dual-Profile Agentic Communication for LLM-Based Recommendation**
   * Affiliation: Harbin Institute of Technology, Shenzhen, China — *(Zhen Tao, Xun Zhou, Xuhui Chen, Ziyue Qiao, Qingqiang Sun)* — with Great Bay University; NeurIPS 2026
   * Link: [arxiv.org/abs/2611.05319](https://arxiv.org/abs/2611.05319)
   * Venue: NeurIPS 2026 (cs.IR; cs.AI; submitted 3 Nov 2026)
   * TL;DR: HARP recasts LLM-based recommendation as agentic communication between user and item agents and adds three training-free operators (symmetric item profile, retrieval-time profile-level homophily gate, reflective profile update) to a frozen LLM backbone, lifting Hit@1 by 6.9%-24.0% over the strongest baseline.
   * Key techniques:
     - Four-stage agentic communication: BUILD, TRANSMIT, UNDERSTAND, SYNC
     - Dual profiles: rule-extracted symmetric item profile (zero extra LLM calls) plus user profile
     - Channel-decomposable profile-level homophily H(phi_u, phi_i) consumed at retrieval time (not inside the reranker prompt)
     - Single-pass reflective profile update (in-context evolution, no gradient step)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/Jove-Zhen/HARP](https://github.com/Jove-Zhen/HARP): clear module structure (profiles / homophily / memory / models), per-dataset configs, conversion + run scripts, and a README with setup/usage that matches the paper (Build/Transmit/Understand/Sync); deductions: very new with few stars, niche LLM-rec scope, and no explicit LICENSE file in the repo
     - **Novelty: 8/10** — agentic-communication framing plus training-free dual-profile homophily
     - **Fairness: 4/10** — not a focus
     - **Robustness: 7/10** — 4 public benchmarks with Holm-corrected p < 1e-9 and ablations
     - **Impact: 7/10** — NeurIPS 2026; training-free and easy to adopt on a frozen LLM backbone

6. **DualEvolve: Dual-Level Self-Evolution of Mechanism and Orchestration for Recommendation**
   * Affiliation: Meituan, China — *(Tianqi Gao [Independent Researcher], Chenxu Wang, Wenxuan Yang, Yueqi Mou, Biao Tang, Ming Liu, Peng Yan)*
   * Link: [arxiv.org/abs/2611.04439](https://arxiv.org/abs/2611.04439)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 3 Nov 2026)
   * TL;DR: DualEvolve is a dual-level self-evolving LLM-agent framework for recommendation that co-evolves inner recommendation mechanisms (model / training code) and outer agent orchestration (harness / skill rules) using task feedback and execution traces, beating OpenEvolve and DeepEvolve in 64 of 64 setting-metric comparisons.
   * Key techniques:
     - Inner evolution: revises model and training code via task feedback to improve recommendation performance
     - Outer evolution: scores the inner-loop experimental process, updates harness and skill rules, and adjusts orchestration choices from next-round scores
     - Recursive self-improvement driven by both task performance and experimentation-quality signals
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — the paper links github.com/ToAdventure/dualevolve, but the repository returns 404 / is not publicly accessible (no usable public code)
     - **Novelty: 8/10** — dual-level (mechanism + orchestration) co-evolution for rec agents
     - **Fairness: 3/10** — not addressed
     - **Robustness: 6/10** — four datasets across 16 settings, but a simulation-based agentic loop
     - **Impact: 7/10** — Meituan; extends the OpenEvolve / DeepEvolve lineage to recommendation

7. **tau-Rec-Books: A Disclosure-Controlled Benchmark for Requirement Elicitation in Agentic Recommender Systems**
   * Affiliation: Princeton University, USA — *(Bharath Sivaram Narasimhan, Karthik R. Narasimhan)*
   * Link: [arxiv.org/abs/2611.04459](https://arxiv.org/abs/2611.04459)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.AI; cs.CL; submitted 3 Nov 2026); submitted to ECIR 2027 (Resource Track)
   * TL;DR: tau-Rec-Books is a benchmark that evaluates how well agentic recommender agents elicit hidden user requirements (volunteer / mixed / hidden disclosure variants) over a 20k-book Wikidata catalog, with a rule-based simulated user and programmatic (non-LLM-judge) scoring.
   * Key techniques:
     - Disclosure-controlled tasks: requirements revealed volunteer / mixed / hidden
     - Hidden requirements discoverable only by proposing books and inferring from accept/reject verdicts
     - Rule-based deterministic simulated user plus programmatic verifiable scoring (no LLM judge)
     - 450 tasks over a 20k-book catalog; extends the tau-Rec harness (also a movies track, RecSys 2026)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/nbharaths/tau-rec](https://github.com/nbharaths/tau-rec): comprehensive MIT-licensed benchmark release (catalog pipeline, task generator, simulated user, validators, reference agents, full traces, analysis code, HuggingFace datasets, leaderboard, v2.0.0); deductions: it is a benchmark / data release rather than a core-method implementation, and the books track depends on external Wikidata
     - **Novelty: 7/10** — controlled-disclosure benchmark for requirement elicitation in agentic CRS
     - **Fairness: 4/10** — not a focus
     - **Robustness: 7/10** — programmatically reproducible scoring across 4 agents and 2 interfaces, with mixed/hidden ablations
     - **Impact: 7/10** — Princeton; extends the RecSys 2026 tau-Rec evaluation resource for agentic rec


### Papers November 03

*Tuesday, November 3, 2026. The live arXiv cs.IR / cs.AI / cs.CL window for the last 24 hours (papers submitted Nov 2) carried 6 strictly on-topic generative-recommendation preprints, all verified absent from README, the docs indexes, and the monthly archive. 1 is open-source (RecRSI / Shanghai Jiao Tong University, 7/10). By Opensource count 235 -> 236. Mindmap updated (added RecRSI under Frameworks & Benchmarks; dropped LLM-Demographic to hold the 30-leaf cap; all 3 layers retained).*

1. **Diverse-Teacher On-Policy Distillation for Generative Recommendation**
   * Affiliation: University of Science and Technology of China (USTC), Hefei, China — *(Zhipeng Yi, Xinyu Lin, Minxuan Shan, Zipeng Chen, Yujiao Zhao, Chuanyu Xu, Wenjie Wang)*
   * Link: [arxiv.org/abs/2611.03272](https://arxiv.org/abs/2611.03272)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 2 Nov 2026)
   * TL;DR: Proposes a diverse-teacher on-policy distillation method for generative recommendation that mitigates the popularity bias aggravated by standard on-policy distillation, covering unpopular SID paths rarely generated or supervised by a single teacher.
   * Key techniques:
     - On-policy distillation (OPD) for generative recommendation (semantic-ID generation) providing denser token-level supervision than target-token-only objectives
     - Identifies that OPD aggravates popularity bias: teacher feedback and student rollout both favor popular-item tokens, leaving unpopular SID paths rarely generated/supervised
     - Diverse-teacher ensembling with diversity-aware regularization to cover unpopular-item token paths
     - Popularity-debiased distillation loss balancing popular vs long-tail SID trajectories
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — reframes the popularity-bias problem of OPD in GR and proposes a diversity-aware mitigation
     - **Fairness: 7/10** — directly targets popularity / long-tail bias introduced by distillation
     - **Robustness: 6/10** — evaluated on SID-based GR benchmarks; limited extreme-long-tail ablations
     - **Impact: 7/10** — relevant to industrial GR training where OPD is increasingly used

2. **Preprocessing Choices in Fine-Tuning Data Matter: Utility and Demographic Sensitivity in LLM-Based Recommendation**
   * Affiliation: Istanbul Technical University, Turkiye — *(Furkan Yasir Goksu, Yaren Yilmaz, Sule Gunduz Oguducu)*
   * Link: [arxiv.org/abs/2611.03113](https://arxiv.org/abs/2611.03113)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.CL; cs.LG; submitted 2 Nov 2026)
   * TL;DR: Systematically studies how preprocessing choices in fine-tuning data (demographic-descriptor handling, output validity, prompt consistency) affect both utility and demographic fairness in a generative LLM-based recommender.
   * Key techniques:
     - Controlled generative LLM-based recommendation pipeline combining supervised fine-tuning, catalog, and generation
     - Systematic variation of preprocessing choices (e.g., inclusion/format of demographic descriptors, output-format validation)
     - Joint measurement of recommendation utility and demographic sensitivity (fairness)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 6/10** — an empirical study reframing data preprocessing as a utility/fairness lever
     - **Fairness: 8/10** — central contribution is the demographic-sensitivity analysis
     - **Robustness: 6/10** — controlled but single-pipeline; limited datasets
     - **Impact: 6/10** — practical guidance for fair LLM-rec fine-tuning

3. **PACERec: Progressive Adaptation of LLM Item Embeddings with Collaborative Evidence for Recommendation**
   * Affiliation: Northeastern University, China (Shenyang) — *(Junzhao Huang, Xi Wu, Zihan Wang, Zijing Wang, Ming Wang, Kang Liu, Xiaocui Yang, Shi Feng, Daling Wang, Yifei Zhang, Ting Yang, Xurui Li)*
   * Link: [arxiv.org/abs/2611.03068](https://arxiv.org/abs/2611.03068)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.AI; submitted 2 Nov 2026)
   * TL;DR: PACERec progressively adapts frozen LLM item embeddings to sequential recommendation by transferring preceding interaction contexts from frequent to long-tail items using collaborative evidence.
   * Key techniques:
     - LLM embeddings encode static item attributes for sequential recommendation (alleviating ID-embedding sparsity)
     - Progressive adaptation that transfers preceding interaction contexts from frequent to long-tail items
     - Collaborative-evidence-guided embedding adaptation under unevenly distributed behavioral evidence
     - Context-transfer objective for long-tail items
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — explicit frequent->long-tail context transfer for LLM embeddings
     - **Fairness: 6/10** — long-tail improvement implies fairness gain but not the explicit focus
     - **Robustness: 6/10** — evaluated on sequential-rec benchmarks; moderate ablations
     - **Impact: 7/10** — addresses the sparse-interaction limitation of LLM embeddings in rec

4. **E-GenRM: Generative Reward Modeling for Open-Ended E-Commerce Shopping Agents**
   * Affiliation: Alibaba (Taobao / Tmall Group), China — *(Ying Sun, Qiuyu Zhao, Xiao Wang, Xiyu Zhao, Gege Shi, Zenghui Sun, Jinsong Lan, Haihong Tang, Bo Zheng)*
   * Link: [arxiv.org/abs/2611.03008](https://arxiv.org/abs/2611.03008)
   * Venue: arXiv preprint, November 2026 (cs.IR; submitted 2 Nov 2026)
   * TL;DR: E-GenRM is a generative reward model for open-ended e-commerce shopping agents that leverages naturally occurring user behavior to provide fine-grained, capability-improving reward signals beyond current bounded agent usage.
   * Key techniques:
     - Generative (not scalar) reward modeling tailored to e-commerce shopping agents
     - Leverages naturally occurring user behavior across the shopping app as supervision
     - Integrated reward framework for open-ended shopping-agent tasks (beyond bounded trajectories / known failures)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — generative reward model for shopping agents using natural user behavior
     - **Fairness: 4/10** — not a focus
     - **Robustness: 6/10** — industrial setting; evaluated on shopping-agent tasks
     - **Impact: 8/10** — Alibaba industrial; high relevance to agentic e-commerce rec / RL

5. **RecRSI: Mechanism-Guided Discovery of Recommendation Algorithms**
   * Affiliation: Shanghai Jiao Tong University, China — *(Tingran Gan, Zhouziyue Lu, Dian Jin, Tao Li, Yang Gao, Ming Liu, Weiwen Liu, Jianghao Lin, Weinan Zhang, Yong Yu)*
   * Link: [arxiv.org/abs/2611.02487](https://arxiv.org/abs/2611.02487)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.AI; submitted 2 Nov 2026)
   * TL;DR: RecRSI is an LLM-based research framework that organizes recommendation-algorithm discovery around mechanism hypotheses (MechSpace, Research Line, Mechanism Feedback) to automatically propose, implement, and evaluate candidate algorithms.
   * Key techniques:
     - MechSpace: derives implementable primitives and composition rules from the task source
     - Research Line: develops/tests mechanism hypotheses linking a proposed mechanism change to a reference design, rationale, and expected observation
     - Mechanism Feedback: carries outcomes and design context into subsequent proposals (recursive self-improvement)
     - Built on SASRec / Amazon CDs&Vinyl with RecBole and a GRPO-based candidate-training backend
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/DynamisG210/RecRSI](https://github.com/DynamisG210/RecRSI): MIT-licensed Python package (src/recrsi) with pyproject.toml, CI tests, docs (host-setup / task-format), and a reproducible CPU demo that runs without API key or GPU; code structure matches the paper (MechSpace / Research Line / Mechanism Feedback, GRPO backend). Deductions: very new (2 stars), niche research-framework scope, limited community adoption
     - **Novelty: 8/10** — frames recsys research as automated mechanism-hypothesis discovery with LLM agents + RL
     - **Fairness: 4/10** — not a focus
     - **Robustness: 6/10** — sandboxed execution (landlock / namespace); empirical breadth limited to the SASRec demo
     - **Impact: 7/10** — novel auto-discovery paradigm; from SJTU / Meituan; open-source

6. **Multi-Teacher Reasoning Distillation for LLM Recommendation with Self-Exploration**
   * Affiliation: The Hong Kong Polytechnic University, Hong Kong SAR, China — *(Liangbo Ning, Siyuan Liang, Yi Zhou, Yifeng Zhang, Qing Li, Wenqi Fan, Dacheng Tao)*
   * Link: [arxiv.org/abs/2611.02457](https://arxiv.org/abs/2611.02457)
   * Venue: arXiv preprint, November 2026 (cs.IR; cs.AI; submitted 2 Nov 2026)
   * TL;DR: Proposes multi-teacher reasoning distillation for LLM recommenders that distills reasoning trajectories from several complementary teachers and uses self-exploration to assess and select the most useful trajectories for downstream recommendation.
   * Key techniques:
     - Reasoning-augmented recommender that generates reasoning trajectories over historical interactions
     - Multi-teacher distillation from several fixed teachers (breaks the single-teacher knowledge ceiling)
     - Self-exploration: the student generates its own trajectories and assesses their utility before distilling (utility-aware selection)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code available
     - **Novelty: 7/10** — multi-teacher + self-exploration utility-aware distillation for reasoning rec
     - **Fairness: 4/10** — not addressed
     - **Robustness: 6/10** — evaluated on rec benchmarks; ablations on teacher selection
     - **Impact: 7/10** — from PolyU / NTU; relevant to reasoning LLM recsys


### Papers November 02

*Monday, November 2, 2026. The live arXiv cs.IR listing for Nov 2 (a Monday announcement day) carried no strictly on-topic generative-recommendation preprints newer than the Oct 30 run already indexed, so per the fallback rule papers were drawn from the last-3-month keyword pool. 5 genuinely-new on-topic papers were verified absent from README, the docs indexes, AND the monthly archive. 1 is open-source (LLM Recommenders Produce Demographic Inequality / University of Zurich, 6/10). By Opensource count 234 -> 235. Mindmap updated (added LLM-Demographic under Feature Quality & Safety; dropped RecToolBench to hold the 30-leaf cap; all 3 layers retained).*

1. **LLM Recommenders Produce Demographic Inequality Through Content Preferences**
   * Affiliation: University of Zurich, Switzerland — *(Nicolò Pagan, Petter Törnberg, Christopher A. Bail, Christopher Barrie)*
   * Link: [arxiv.org/abs/2610.41854](https://arxiv.org/abs/2610.41854)
   * Venue: arXiv preprint, October 2026 (cs.CY; cs.SI; submitted 30 Oct 2026)
   * TL;DR: LLM-based content recommenders surface demographic inequality through the content they surface, not through explicit demographics: a controlled experiment on 10,000 Twitter/X posts from 1,000 survey respondents with nine verified self-reported attributes shows that recommendation objectives and contextual framing systematically shift whose voices get amplified across demographic groups.
   * Key techniques:
     - Controlled recommendation experiment across 3 LLM providers, 6 recommendation objectives, 5 levels of contextual framing
     - 10,000 Twitter/X posts linked to verified self-reported demographic characteristics (9 attributes)
     - Audits demographic inequality emerging from content-preference modeling rather than explicit group membership
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 6/10** — [github.com/paganick/llm-recsys-twitter-yougov-PNAS](https://github.com/paganick/llm-recsys-twitter-yougov-PNAS): Python repo with README, recommendation/features/analysis/utils dirs and env files (0 stars at indexing; PNAS-linked release)
     - **Novelty: 7/10** — reframes demographic bias in LLM recommenders as an emergent content-preference effect with a controlled multi-provider experimental design
     - **Fairness: 9/10** — the paper's central contribution is a direct, empirical measurement of demographic inequality in LLM recs
     - **Robustness: 7/10** — multi-provider (3), multi-objective (6), multi-framing (5) design with survey-linked ground truth
     - **Impact: 8/10** — high relevance for auditing deployed LLM recommenders; PNAS-venue visibility

2. **Category-Anchored Large Language Models for Next POI Recommendation**
   * Affiliation: Harbin Institute of Technology, Shenzhen, China / City University of Hong Kong — *(Lexi Bai, Xiaopeng Zeng, Xun Zhou, Yuanshao Zhu, James Jianqiao Yu)*
   * Link: [arxiv.org/abs/2610.39518](https://arxiv.org/abs/2610.39518)
   * Venue: arXiv preprint, October 2026 (cs.AI; submitted 29 Oct 2026)
   * TL;DR: ANCHOR addresses unreliable direct POI-identifier generation by LLMs (POIs are sparse, localized, long-tailed entities with weak NL semantics) via category-anchored prompting: it first anchors generation on venue categories, then grounds the final POI within the anchored category space for spatio-temporally consistent next-POI prediction.
   * Key techniques:
     - Category-anchored LLM prompting that decouples category reasoning from exact-POI decoding
     - Textualized user trajectory encoding for LLM semantic reasoning
     - Two-stage category-conditioned POI generation for sparse/long-tailed entities
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (arXiv lists no repository)
     - **Novelty: 7/10** — clean fix to the POI-identifier generation unreliability via category anchoring
     - **Fairness: 3/10** — not addressed (standard POI benchmark fairness not studied)
     - **Robustness: 6/10** — evaluated on standard next-POI benchmarks; long-tail handling claimed but limited ablation detail
     - **Impact: 6/10** — from HIT Shenzhen / CityU HK; practical LLM-POI direction

3. **Federated Recommender Agents**
   * Affiliation: POSTECH (Pohang University of Science and Technology), Pohang, South Korea — *(Jaehyung Lim, Woojoo Kim, Junyoung Kim, Dongha Kim, Wonbin Kweon, Hwanjo Yu)*
   * Link: [arxiv.org/abs/2610.39289](https://arxiv.org/abs/2610.39289)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 29 Oct 2026)
   * TL;DR: FedRecAgent formulates a federated setting where local LLM-powered recommender agents collaborate through natural-language knowledge while keeping interaction histories and personal memories local; it enables this collaboration without updating LLM parameters, tackling the central challenge of privacy-preserving cross-agent learning.
   * Key techniques:
     - Federated multi-agent recommendation with natural-language knowledge exchange
     - Local interaction histories and personal memories kept private (no parameter sharing)
     - Collaboration without fine-tuning the underlying LLM
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (arXiv lists no repository)
     - **Novelty: 7/10** — federated formulation of LLM recommender agents with parameter-free collaboration
     - **Fairness: 5/10** — privacy-preserving design implicitly supports user-fair data governance, but group fairness not evaluated
     - **Robustness: 6/10** — method proposed with collaboration protocol; empirical depth on heterogeneous clients limited
     - **Impact: 7/10** — from POSTECH (strong recsys group); addresses a real privacy bottleneck for agentic recs

4. **Read More, Reason Deeper: Latent Workspaces for Long-Sequence Recommendation**
   * Affiliation: Meta Platforms — *(Renzhi Wu, Li Sheng, Zikun Cui, Junjie Yang, Tai Guo, Keke Zhai, et al.)*
   * Link: [arxiv.org/abs/2610.39188](https://arxiv.org/abs/2610.39188)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 29 Oct 2026)
   * TL;DR: LWR (Latent Workspace Ranker) decouples evidence scaling from reasoning scaling for long-sequence recommendation: it keeps typed evidence in persistent banks and propagates a fixed-size candidate workspace through deeper reasoning layers, so later layers can revisit omitted evidence that one-shot selection would discard.
   * Key techniques:
     - Latent workspace: fixed-size persistent candidate/evidence banks across reasoning layers
     - Decoupled evidence scaling (longer histories) from reasoning scaling (deeper interpretation)
     - Revisit-able evidence avoiding one-shot selection's information loss
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (Meta industrial)
     - **Novelty: 8/10** — clean decoupling of evidence vs reasoning scaling with a persistent latent workspace
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — long-sequence benchmarks; principled motivation against coupled encoders
     - **Impact: 8/10** — from Meta; long-sequence rec is an industrial pain point

5. **Modeling Preference Dependencies with Directed Acyclic Graphs for Narrative-Driven Recommendation**
   * Affiliation: Institute of Information Engineering, Chinese Academy of Sciences, Beijing, China / School of Cyber Security, University of Chinese Academy of Sciences / University of Melbourne / Independent Researcher — *(Mingzhe Lu, Jian Qin, Ruize Qin, Jinhao Liu, Yunpeng Li, Hang Su)*
   * Link: [arxiv.org/abs/2610.37280](https://arxiv.org/abs/2610.37280)
   * Venue: arXiv preprint, October 2026 (cs.IR; cs.CL; submitted 27 Oct 2026)
   * TL;DR: PDG-F (Preference Dependency Graph Framework) treats narrative-driven recommendation as an explicit directed acyclic graph of preference dependencies, capturing how stated preferences hierarchically refine and condition one another — instead of flattening narratives into keyword bags or unconstrained generative queries.
   * Key techniques:
     - Directed acyclic graph (DAG) modeling of preference dependencies in free-form narratives
     - Hierarchical refinement / contextualization of preferences as graph edges
     - Narrative-driven recommendation framework centered on structured dependency graphs
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (arXiv lists no repository)
     - **Novelty: 7/10** — structured DAG representation of narrative preference dependencies vs flat/generative baselines
     - **Fairness: 3/10** — not addressed
     - **Robustness: 6/10** — narrative benchmarks; structured-graph ablation limited
     - **Impact: 6/10** — from IIE CAS; advances narrative-driven rec structuring

### Papers November 01

*Sunday, November 1, 2026. The live arXiv cs.IR listing for Nov 1 (a Sunday — arXiv announces Mon–Fri) carried no new on-topic generative-recommendation preprints, so per the fallback rule papers were drawn from the last-3-month keyword pool. 5 genuinely-new on-topic papers were verified absent from README, the docs indexes, AND the monthly archive. 1 is open-source (SODA / USTC & Upwork, 7/10). By Opensource count 233 -> 234. Mindmap updated (added SODA; dropped Octen-WebGR to hold the 30-cap).*

1. **Unified Generative Ranking for Heterogeneous E-commerce Recommendation**
   * Affiliation: Alibaba Group, Hangzhou, China — *(Zonghe Shao, Huabin Chen, Sitong Lu, Fangmei Zhu, Yingcai Ma, Ge Fan, Jinguo Gao, Wei Shi, Yanfang Liu, Huiping Chu)*
   * Link: [arxiv.org/abs/2610.39426](https://arxiv.org/abs/2610.39426)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 29 Oct 2026)
   * TL;DR: UGR performs list-wise generative ranking over the full request-level multi-business heterogeneous candidate set (~1000 candidates in production) and directly generates multi-business ranking lists via candidate-aware autoregressive decoding; beyond exposure-sequence imitation it adds weighted SFT + permutation preference optimization and a training-time ad-debiasing tower while preserving GSP pricing at serving.
   * Key techniques:
     - Candidate-aware autoregressive decoding over ~1000 heterogeneous multi-business candidates
     - Weighted supervised fine-tuning that leverages post-exposure feedback
     - Permutation preference optimization from feedback-derived permutation preferences
     - Training-time advertising debiasing tower + serving-time ad-value modeling (GSP-preserving)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (Alibaba industrial)
     - **Novelty: 7/10** — generative ranking over full heterogeneous multi-business candidate sets with permutation preference optimization; practical but builds on generative-ranking + preference-optimization lines
     - **Fairness: 2/10** — not addressed (ad-debiasing tower targets ad-exposure bias, not demographic fairness)
     - **Robustness: 7/10** — offline ranking-quality gains plus online A/B on Taobao Guess You Like (+1.76% IPV, +3.29% volume, +2.10% GMV)
     - **Impact: 9/10** — deployed A/B on Taobao at scale with real GMV lift; strong industrial relevance

2. **R2QRec: Learning Recommendation Queries from Retrieval Feedback**
   * Affiliation: Kuaishou Technology, Beijing, China / Hong Kong Baptist University — *(Weixin Chen, Shuchang Liu, Hailan Yang, Yuhan Zhao, Li Kang, Li Chen, et al.; 16 authors)*
   * Link: [arxiv.org/abs/2610.39984](https://arxiv.org/abs/2610.39984)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 29 Oct 2026)
   * TL;DR: R2QRec learns to generate recommendation queries from item interactions without query annotations: retrieval verification selects generated expressions that recover observed items as SFT targets, then policy refinement scores query sets by the observed item's rank in their fused list (log-rank feedback, KL penalty); only the query generator is trained.
   * Key techniques:
     - Fixed retriever + item index; only the query generator is trained (no learned reward model, no query annotations)
     - Retrieval verification: keep generated expressions that recover observed items as SFT targets
     - Policy refinement: rank-based (log-rank) feedback beyond the cutoff + KL penalty vs the supervised reference
     - Reciprocal Rank Fusion (RRF) of query-set rankings; LoRA adapters
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (Kuaishou industrial)
     - **Novelty: 8/10** — clean separation of query-expression learning from item location; retrieval verification + log-rank policy refinement with KL constraint, no annotations/reward model
     - **Fairness: 2/10** — not addressed
     - **Robustness: 7/10** — SOTA on three public datasets; generalization across generators and domains
     - **Impact: 7/10** — from Kuaishou; query-based recommendation is industrially relevant

3. **Try Before You Evolve: Ranking-Scored Trials for Recursive Self-Improvement of Recommender Systems**
   * Affiliation: University of Science and Technology of China (USTC), Hefei, China — *(Xu Huang, Jiawei Feng, Jiancan Wu)*
   * Link: [arxiv.org/abs/2610.39352](https://arxiv.org/abs/2610.39352)
   * Venue: arXiv preprint, October 2026 (cs.IR; submitted 29 Oct 2026)
   * TL;DR: RecRSI (Try-Before-You-Evolve) tackles delayed/unreliable ranking feedback in LLM-agent recursive self-improvement of recommenders: it generates diverse candidate edits and selects one for full retraining using early ranking feedback — each candidate gets a short trial (first steps of training) scored by full-ranking NDCG@10 on held-out probe users.
   * Key techniques:
     - LLM-agent proposes diverse candidate recipe edits from a diagnosis of the current model
     - Ranking-scored short trials: first training steps scored by full-ranking NDCG@10 on probe users
     - Selects the best candidate for full retraining; same retraining budget as baselines
     - Evaluated on SASRec & HSTU over three datasets (CDs, Office, LastFM)
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code found (arXiv lists no repository)
     - **Novelty: 8/10** — "try before you evolve" ranking-scored trials directly address the delayed/unreliable-feedback bottleneck in recommender RSI
     - **Fairness: 3/10** — not a focus; RSI loops could amplify bias, unaddressed
     - **Robustness: 7/10** — matches/exceeds baselines with the same retraining budget; on both Amazon datasets reaches in 1 round what baselines need 5
     - **Impact: 8/10** — novel RSI paradigm from USTC (strong recsys group); addresses a real bottleneck

4. **Distribution-Level Contrastive Supervision for Generative Recommendation**
   * Affiliation: University of Science and Technology of China, Hefei, China / Upwork, Seattle, USA — *(Ziqi Xue, Yimeng Bai, Shuai Zhu, Jialei Li, Dingxian Wang, Frank Yang, Andrew Rabinovich, Pablo N. Mendes, et al.)*
   * Link: [arxiv.org/abs/2603.00700](https://arxiv.org/abs/2603.00700)
   * Venue: ACM RecSys 2026 (short paper); arXiv v2 Sep 2026
   * TL;DR: SODA treats multi-level codebook probabilities as soft semantic targets and aligns recommender representations to them with a BPR-style contrastive objective (negative KL to positive, vs in-batch averaged negatives), enriching training with finer semantic cues while leaving decoding unchanged.
   * Key techniques:
     - Distribution-level (soft multi-level codebook) supervision instead of one-hot SID targets
     - BPR-style contrastive alignment via negative KL divergence
     - Plug-and-play auxiliary loss; decoding stage unchanged
     - Applicable across diverse generative-recommendation backbones
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — [github.com/freyasa/SODA](https://github.com/freyasa/SODA): official RecSys'26 code release (complete implementation)
     - **Novelty: 8/10** — moves beyond code-level supervision to distribution-level contrastive alignment
     - **Fairness: 3/10** — not addressed
     - **Robustness: 7/10** — peer-reviewed RecSys'26; plug-and-play gains across backbones
     - **Impact: 7/10** — accepted at RecSys'26 with code; broadly applicable supervision scheme

5. **Unleash the Potential of Long Semantic IDs for Generative Recommendation**
   * Affiliation: Southern University of Science and Technology / Xi'an Jiaotong University / Nanjing University — *(Ming Xia, Guoxin Ma, Zhiqin Zhou, Dongmin Huang)*
   * Link: [arxiv.org/abs/2602.13573](https://arxiv.org/abs/2602.13573)
   * Venue: arXiv preprint, under review (cs.IR; v2 Aug 2026)
   * TL;DR: ACERec keeps the semantic richness of long Semantic IDs while staying efficient: an Attentive Token Merger compresses long SIDs into compact latent tokens, a dedicated Intent Token captures user intent, and a dual-granularity objective combines token-level generation with item-level intent-semantic alignment.
   * Key techniques:
     - Attentive Token Merger compresses long semantic IDs into compact latent tokens
     - Dedicated Intent Token for user intent
     - Dual-granularity objective: token-level generation + item-level intent-semantic alignment
     - Breaks the short-ID efficiency vs long-ID expressiveness dilemma
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (under review; arXiv lists no repository)
     - **Novelty: 9/10** — directly attacks the long-SID granularity-efficiency dilemma with a token merger + intent token + dual-granularity objective
     - **Fairness: 2/10** — not addressed
     - **Robustness: 8/10** — 9 real-world benchmarks, +12.92% NDCG@10 and +7.49% Recall@10 over strongest baselines
     - **Impact: 8/10** — strong empirical gains on long semantic IDs; multi-institution

### Papers October 31

*Saturday, October 31, 2026. The live arXiv cs.IR window (papers dated Oct 30-31) carried no strictly on-topic generative-recommendation submissions newer than the Oct 30 run (the 5 newest cs.IR preprints, 2610.39470/39273/38378/37973/37962, were already indexed Oct 30). Per the fallback rule we drew 9 genuinely-new on-topic papers from the last-3-month keyword pool. All 9 were verified absent from README, the docs indexes, AND the monthly archive (5 of the initially scoped candidates were dropped because they had already been indexed and archived by a prior run). 0 are open-source (no public code). By Opensource count unchanged (233). Mindmap unchanged (it tracks only open-source papers).*

1. **LightCRS: Lightweight Multi-Domain Conversational Recommendation System**
   * Affiliation: University of Sydney, NSW, Australia / Nankai University, Tianjin, China — *(He Ma, Lan You, Qiyang Wu, Chen Liu)*
   * Link: [arxiv.org/abs/2610.26948](https://arxiv.org/abs/2610.26948)
   * Venue: arXiv preprint (cs.IR; cs.MM); under review
   * TL;DR: A lightweight query-conditioned framework for unified multi-domain multimodal conversational recommendation: offline-frozen multimodal product encoders plus a shared 5.3M-parameter query-conditioned cross-attention fusion module and an inter-candidate Transformer, evaluated on a new 25-domain MM-R2A-25 benchmark built from Reddit dialogues and Amazon listings (HR@1 +35.4% over the strongest baseline, 266x lower per-query latency).
   * Key techniques:
     - Precompute multimodal product representations offline with frozen encoders
     - A compact 5.3M-parameter query-conditioned cross-attention fusion shared across all domains
     - Inter-candidate Transformer for joint candidate comparison
     - MM-R2A-25: a 25-domain benchmark pairing Reddit recommendation dialogues with Amazon product listings
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 8/10** — clean multi-domain cost-accuracy solution via a tiny shared fusion module over frozen encoders.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 7/10** — 25-domain benchmark with HR@1/NDCG@5/MRR.
     - **Impact: 7/10** — from U Sydney / Nankai; tackles the per-domain VLM scaling problem in multimodal CRS.

2. **SimInter: Evidence-Grounded User Simulation with Interview-Based Profile Enrichment for Conversational Recommender Systems**
   * Affiliation: University of Tehran, Tehran, Iran — *(Erfan Shahabi, Amirhossein Roshandel, Mohammad Sadegh Sadeghi, Azadeh Shakery; Shakery also Institute for Research in Fundamental Sciences, IPM)*
   * Link: [arxiv.org/abs/2610.18308](https://arxiv.org/abs/2610.18308)
   * Venue: arXiv preprint (cs.CL; cs.IR); under review
   * TL;DR: A CRS user-simulation pipeline that enriches static profiles with implicit behavioral attributes (decision style, aspect-level preferences, domain expertise) via synthetic two-agent LLM interviews grounded in the user's statistical profile and history, with a turn-level audit agent flagging fabrication and stereotyping; on 300 simulated ReDial users it raises aspect entropy 0.859 to 1.619 and humans support 94.3% of enriched claims.
   * Key techniques:
     - Two-agent synthetic interview for profile enrichment
     - Grounding in the user's statistical profile and historical conversational evidence
     - Turn-level audit agent flagging potential fabrication and stereotyping
     - Evaluation against the KBRD and UniCRS recommenders
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (cites Tencent Hy3 as a component, not the paper's own repo).
     - **Novelty: 8/10** — grounds profile enrichment in interviews with an explicit fabrication/stereotyping auditor.
     - **Fairness: 3/10** — the audit agent explicitly counters stereotyping.
     - **Robustness: 7/10** — 300 users, 100 matched subset, paired tests with Holm-adjusted p < 0.001, human evaluation.
     - **Impact: 7/10** — improves CRS evaluation reliability via richer, audited simulators.

3. **Multi-Modal Semantic Expansion with Constrained LLM Reranking for Conversational Music Recommendation**
   * Affiliation: NIT Kurukshetra, India / Queen Mary University of London, UK — *(Naman Garg, Sarika Jain, George Fazekas)*
   * Link: [arxiv.org/abs/2608.23484](https://arxiv.org/abs/2608.23484)
   * Venue: ACM RecSys 2026 TalkPlayData Challenge
   * TL;DR: Team Semiintelligencn's RecSys 2026 TalkPlayData solution: a three-stage conversational music recommender - multi-modal retrieval over seven dense spaces (CF-BPR, Qwen3, CLAP audio, SigLIP visual) plus BM25 fused by Reciprocal Rank Fusion with differential-evolution-tuned weights (+19.5% MRR), lightweight reranking, and persona-diversified GPT-4o-mini response generation; finds that unconstrained LLM artist injection causes -18.9% nDCG while conservative injection on 9 sessions is best.
   * Key techniques:
     - Seven-space multi-modal retrieval with decay-weighted centroids
     - Weighted Reciprocal Rank Fusion tuned by differential evolution
     - History filtering, popularity smoothing, and catalog diversity penalization
     - Persona-diversified response generation with GPT-4o-mini
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 6/10** — solid challenge engineering rather than a new method.
     - **Fairness: 3/10** — catalog diversity penalization.
     - **Robustness: 7/10** — Blind A/B, 500-session dev split, ablation of injection strategies.
     - **Impact: 7/10** — RecSys 2026 challenge; a practical warning about unconstrained LLM injection harming nDCG.

4. **LLM-as-a-Judge for Evaluating System Responses in Conversational Music Recommendation**
   * Affiliation: KAIST (Graduate School of Culture Technology), South Korea / Spotify — *(Seungheon Doh, Bruno Sguerra, Sergio Oramas, Elena V. Epure, Juhan Nam)*
   * Link: [arxiv.org/abs/2607.25640](https://arxiv.org/abs/2607.25640)
   * Venue: ACM RecSys 2026
   * TL;DR: The first user study to empirically assess LLM-as-a-judge for evaluating conversational recommender responses: 20 multi-turn music sessions, four instruction-tuned LLMs, 400 ratings from 20 domain experts on Personalization Quality and Explanation Quality; LLM judges show moderate alignment with humans and outperform reference-based baselines, with guidance on model scale and conditioning.
   * Key techniques:
     - User study with 20 expert annotators and 400 ratings
     - Two evaluation dimensions: Personalization Quality and Explanation Quality
     - Bootstrapped correlation analysis against human judgments
     - Analysis of judge performance by model scale and conditioning information
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 7/10** — first empirical reliability study of LLM-judges for CRS responses.
     - **Fairness: 4/10** — expert-anchored evaluation mitigates judge bias.
     - **Robustness: 8/10** — 20 annotators, bootstrapped correlation, multiple LLM judges.
     - **Impact: 8/10** — RecSys 2026; directly informs CRS evaluation practice.

5. **NEXT: Reasoning-Driven Video Recommendation via a Vision-Language Model**
   * Affiliation: Meta Platforms, Inc., USA — *(Yuming Liu, Hongye Yang, Harrison Zhao, Ellie Zhu, Bokai Cao, Lei Huang, Lizhu Zhang, Xiangjun Fan)*
   * Link: [arxiv.org/abs/2607.24789](https://arxiv.org/abs/2607.24789)
   * Venue: arXiv preprint (cs.IR; cs.CV; cs.LG); under review
   * TL;DR: NEXT (Next-interest EXploration Transformer), a reasoning-driven video recommender that infers a viewer's next intent from the just-watched video and retrieves follow-ups via an Item-to-Intent-to-Item formulation; trains NEXT-8B, a purpose-built 8B VLM with Perception-Enhanced RL, Distribution-Aligned SFT, and GRPO, deployed at Meta as an additional retrieval path with +0.53% watch time and +0.51% distinct video exposure.
   * Key techniques:
     - Item-to-Intent-to-Item reasoning formulation beyond co-engagement correlation
     - NEXT-8B three-stage recipe: Perception-Enhanced RL, Distribution-Aligned SFT, GRPO
     - Intent-query generation for implicit continuations
     - Production deployment as an additional retrieval path
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 8/10** — compact VLM as a production reasoning engine for next-interest exploration.
     - **Fairness: 3/10** — not a focus.
     - **Robustness: 8/10** — best single-model DocVQA, production A/B with significance tests, LLM-as-judge.
     - **Impact: 9/10** — Meta production deployment at social-media scale.

6. **Two Views, One Voice: Evidence-Grounded Conversational Music Recommendation**
   * Affiliation: Naver, South Korea / Samsung, South Korea — *(Sungwook Yoo, Sewook Yoo)*
   * Link: [arxiv.org/abs/2607.24846](https://arxiv.org/abs/2607.24846)
   * Venue: ACM RecSys Challenge 2026 (Proceedings of the Recommender Systems Challenge 2026)
   * TL;DR: Team swyoo's 3rd-place (Blind-B industry) RecSys 2026 TalkPlayData solution that decouples retrieval and response generation into separate pipelines linked only by ranked tracks and metadata; retrieval combines a hybrid lexical-dense pool with a Qwen-8B-adapted pool and LightGBM calibration, then an evidence-grounded propose-assign-select (PAS) framework structures responses (2nd on the explanation-quality leaderboard).
   * Key techniques:
     - Decoupled retrieval and response pipelines connected via ranked tracks and metadata
     - Hybrid lexical-dense pool plus a Qwen-8B-adapted retrieval pool
     - LightGBM candidate calibration
     - Evidence-grounded propose-assign-select (PAS) response structuring
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 7/10** — clean decoupling of retrieval and generation with evidence-grounded structuring.
     - **Fairness: 3/10** — evidence-grounded generation improves explanation credibility.
     - **Robustness: 7/10** — RecSys Challenge Blind-B and explanation-quality leaderboard.
     - **Impact: 7/10** — RecSys 2026 challenge; near-best explanation reliability.

7. **QueryAgent-R1: Bridging Query Generation and Product Retrieval for E-Commerce Query Recommendation**
   * Affiliation: Alibaba International Digital Commerce Group — *(Dike Sun, Zheng Zou, Jingtong Zang, Qi Sun, Huaipeng Zhao, Tao Luo, Xiaoyi Zeng)*
   * Link: [arxiv.org/abs/2606.05671](https://arxiv.org/abs/2606.05671)
   * Venue: arXiv preprint (cs.CL); under review
   * TL;DR: QueryAgent-R1, a memory-augmented agentic framework for e-commerce query recommendation that grounds query generation in real inventory retrieval (chain-of-retrieval) and adds a consistency reward in agentic RL to jointly optimize query relevance and downstream conversion; a memory-abstraction module enables efficient user profiling; +2.9% query CTR and +3.1% guided CVR in online A/B.
   * Key techniques:
     - Memory-augmented agentic query generation grounded in inventory retrieval
     - Chain-of-retrieval optimization
     - Consistency reward in agentic RL (query relevance + downstream engagement)
     - Memory-abstraction module for efficient user profiling
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (uses verl / FAISS / vLLM internally).
     - **Novelty: 8/10** — chain-of-retrieval alignment between query generation and real products.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 8/10** — proprietary and public datasets plus online A/B.
     - **Impact: 8/10** — Alibaba production; aligns query rec with conversion.

8. **BEAR: Towards Beam-Search-Aware Optimization for Recommendation with Large Language Models**
   * Affiliation: Zhejiang University, Hangzhou, China / The Chinese University of Hong Kong, Shenzhen / Hangzhou City University — *(Weiqin Yang, Bohao Wang, Zhenxiang Xu, Jiawei Chen, Shengjia Zhang, Jingbang Chen, Canghong Jin, Can Wang)*
   * Link: [arxiv.org/abs/2601.22925](https://arxiv.org/abs/2601.22925)
   * Venue: arXiv preprint (cs.IR); under review
   * TL;DR: BEAR (Beam-SEarch-Aware Regularization) fixes the training-inference inconsistency in LLM recommenders that decode with beam search at inference: SFT optimizes overall positive probability, but greedy pruning can discard a positive item whose prefix probability is insufficient. BEAR enforces a relaxed necessary condition - each token of a positive item must rank within the top-B candidates at every decoding step - with negligible overhead; four datasets show clear gains. (Code to be released upon acceptance.)
   * Key techniques:
     - Identifies the beam-search training-inference inconsistency
     - Relaxed necessary condition: every positive token in the top-B candidates per step
     - Avoids simulating beam search per instance (computationally prohibitive)
     - Negligible overhead versus standard SFT
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — code promised on acceptance, not yet public.
     - **Novelty: 9/10** — directly targets the SFT-vs-beam-search mismatch in GR/LLM rec.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 8/10** — four real-world datasets.
     - **Impact: 8/10** — Zhejiang U; directly applicable to GR/LLM-rec beam-search decoding.

9. **IB-GRPO: Aligning LLM-based Learning Path Recommendation with Educational Objectives via Indicator-Based Group Relative Policy Optimization**
   * Affiliation: East China Normal University, Shanghai, China — *(Shuai Wang, Yaoming Yang, Bingdong Li, Hao Hao, Aimin Zhou)*
   * Link: [arxiv.org/abs/2601.14686](https://arxiv.org/abs/2601.14686)
   * Venue: arXiv preprint (cs.AI); under review
   * TL;DR: IB-GRPO (Indicator-Based Group Relative Policy Optimization) aligns LLM-based learning-path recommendation with pedagogical objectives (Zone of Proximal Development) under sparse, delayed feedback; it builds hybrid expert demonstrations via Genetic Algorithm search and teacher RL, warm-starts with SFT, and uses an Iε + Iε+ dominance indicator for multi-objective group-relative advantages; it improves over RL/LLM baselines on ASSIST09 and Junyi with a Qwen2.5-7B backbone.
   * Key techniques:
     - Hybrid expert demonstrations via GA search and teacher RL agents
     - SFT warm-start of the LLM
     - Within-session ZPD alignment score for difficulty scheduling
     - Indicator-based (Iε + Iε+) dominance for multi-objective group-relative advantage
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code released.
     - **Novelty: 8/10** — indicator-based multi-objective GRPO for learning-path rec.
     - **Fairness: 3/10** — ZPD-aware difficulty scheduling addresses learner fairness.
     - **Robustness: 7/10** — ASSIST09, Junyi, KES simulator with Qwen2.5-7B.
     - **Impact: 6/10** — East China Normal U; niche learning-path domain but a clean multi-objective GRPO recipe.

---

### Papers October 30

*Friday, October 30, 2026. The live arXiv cs.IR window carried no strictly on-topic generative-recommendation submissions newer than the Oct 29 run (newest cs.IR preprints remain 2610.37584, announced Oct 27). The absolute-newest gen-rec preprints — 2610.37962 / 2610.37973 / 2610.38378 / 2610.39273 / 2610.39470 — were submitted Oct 27-29 but are cross-listed outside cs.IR and were missed by the Oct 29 pass. All 5 below are verified absent from README, the docs indexes, and the monthly archive. 1 is open-source (PFA / Zhejiang U + Alibaba, 7/10). By Opensource count 232 -> 233. Mindmap 30-cap held (+PFA to Efficient Decoding; -AutoRSE, the lowest-scoring leaf).*

1. **RoFiGR: Coarse Routing, Fine Refinement via Level-Adaptive Distillation in Multimodal Generative Recommendation**
   * Affiliation: Beijing University of Posts and Telecommunications / Kuaishou Technology, Beijing, China — *(Ji Dai, Zhipeng Wei, Zhuang Zhuang, Rongfeng Guo, Jie Chen, Quan Fang, Fei Pan)*
   * Link: [arxiv.org/abs/2610.39470](https://arxiv.org/abs/2610.39470)
   * Venue: arXiv preprint (cs.IR)
   * TL;DR: A two-tree multimodal generative recommender that injects collaborative structure into both SID construction and generation via level-adaptive distillation — fixed coarse-level weights preserve routing supervision while a bounded adaptive residual allocates extra weight by teacher-student demand.
   * Key techniques:
     - Two-tree design aligning cumulative L1-L2 SID code vectors with frozen collaborative item embeddings
     - Explicitly encodes item distance and source level into the serialized user history
     - A sequential teacher supervises only legal coarse branches during generation
     - Level-adaptive distillation: fixed coarse weights plus a bounded adaptive residual driven by teacher-student agreement
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code found.
     - **Novelty: 8/10** — clean collaborative-aware two-tree SID with level-adaptive distillation; fills the coarse-routing gap in multimodal GR.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 7/10** — three benchmarks (Instruments, Arts, Games), five ranking metrics, five-seed paired tests with Holm correction.
     - **Impact: 7/10** — from BUPT / Kuaishou; strengthens multimodal generative recommendation.

2. **PFA: Attention Can Be Progressively Focused in Long-Sequence Generative Recommendation**
   * Affiliation: Zhejiang University (Hangzhou, China) / Alibaba Group — *(Pengjie Zhou, Weiqin Yang, Haibo Xing, Hao Deng, Jinxin Hu)*
   * Link: [arxiv.org/abs/2610.39273](https://arxiv.org/abs/2610.39273)
   * Venue: arXiv preprint (cs.IR)
   * TL;DR: Progressively Focused Attention — an efficient sparse decoding framework for long-sequence GR that keeps full attention only at the first beam step, then reuses a shared cross-beam importance ranking and geometrically shrinks the token budget, cutting online latency while preserving semantics; validated with a 7-day online A/B on a large e-commerce ads platform.
   * Key techniques:
     - Empirical analysis of GR decoding attention -> progressive focusing and cross-step ranking consistency
     - Full attention at the first decoding step, then cross-beam weighted aggregation to build a shared importance ranking
     - Reorder the selected tokens' KV cache into a contiguous memory layout
     - Geometric token-budget reduction in later decoding steps
     - 7-day online A/B on a large-scale e-commerce advertising platform
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 7/10** — anonymous.4open.science/r/PFA-review-088D: code released for review (anonymous submission repo, structure not fully auditable, no LICENSE visible); comparable to other anonymous-submission repos.
     - **Novelty: 8/10** — turns an attention-pattern analysis into a practical contiguous-layout sparse decoding scheme for GR beam search.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 8/10** — two public benchmarks plus one large-scale industrial dataset plus a 7-day online A/B.
     - **Impact: 8/10** — from Zhejiang U / Alibaba; strong production evidence for long-sequence GR serving.

3. **Towards Reliable, Scalable, and Value-Aligned Generative Recommendation for Large-Scale Advertising (GR4AD-X)**
   * Affiliation: Kuaishou — *(Yatong Xiao, Yibo Sheng, Lixiang Wang, Mingjie Sun, Yunhao Sha, Pengfei Zhang, Shengyu Wang, Peng Wang, Wenjin Wu, Peng Jiang)*
   * Link: [arxiv.org/abs/2610.38378](https://arxiv.org/abs/2610.38378)
   * Venue: arXiv preprint (cs.IR; cs.LG); under review
   * TL;DR: GR4AD-X extends the deployed industrial GR4AD ad framework with reliable multi-path SID construction, serving-efficient multi-dimensional capacity scaling, and a unified value-aligned generation/discrimination stage (UniVGD: prefix-level reward optimization + value-guided beam pruning + discriminative reranking), lifting cumulative ad revenue +3.07% in online A/B on Kuaishou.
   * Key techniques:
     - Multi-Path SID assignment for deterministic-SID reliability against semantic-boundary sensitivity
     - Multi-dimensional capacity scaling (width/depth/stream) instead of monolithic backbone growth, for a better effectiveness-efficiency trade-off under strict serving constraints
     - UniVGD: prefix-level reward optimization, value-guided beam pruning, and discriminative reranking inside one model
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code (industrial; Kuaishou).
     - **Novelty: 7/10** — multi-path SID plus unified value-guided generation/discrimination reframes the value-credit-assignment problem in production GR.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 8/10** — large-scale online A/B on Kuaishou ads with strict latency/throughput constraints.
     - **Impact: 8/10** — from Kuaishou; real production ad revenue gain (+3.07% cumulative).

4. **Merge and Branch: Efficient Tree-Structured Supervised Fine-Tuning of LLMs for Recommendation**
   * Affiliation: Georgia Institute of Technology (Atlanta, USA) — *(Yunqin Zhu, Yao Xie)*
   * Link: [arxiv.org/abs/2610.37973](https://arxiv.org/abs/2610.37973)
   * Venue: arXiv preprint (cs.IR; cs.AI)
   * TL;DR: Merge and Branch (M&B) cuts LLM-based generative-rec SFT cost by merging each history item's SID+text into a few learned tokens and branching a shared compressed history to predict multiple target SIDs, with a tree FlashAttention that shares history compute and propagates every branch's gradient end-to-end and a tree KV cache for constrained decoding.
   * Key techniques:
     - Merge: compress each historical item's SID and text into a small number of learned tokens
     - Branch: predict multiple target SIDs from the shared compressed history
     - Shallow-wide tree layout plus tree FlashAttention (history computed once, gradients from all branches)
     - Tree-structured KV cache extending history sharing to constrained decoding
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — no public code found.
     - **Novelty: 8/10** — tree-structured SFT that amortizes expensive history encoding across multiple targets is a neat efficiency idea.
     - **Fairness: 2/10** — not addressed.
     - **Robustness: 7/10** — public benchmarks show quality gains plus substantial training/decoding efficiency improvements.
     - **Impact: 7/10** — from Georgia Tech; tackles the input/output asymmetry of LLM-based rec SFT.

5. **Statistical Detection of Positional Bias in LLM-Based Recommender Systems: Methodologies and Empirical Evidence**
   * Affiliation: University of Granada (Spain) — *(Carlos Pelaez-Gonzalez, Francisco Herrera, Andres Herrera-Poyatos)*
   * Link: [arxiv.org/abs/2610.37962](https://arxiv.org/abs/2610.37962)
   * Venue: arXiv preprint (cs.IR; cs.AI)
   * TL;DR: Studies positional bias in top-1 / single-turn LLM-based RS (RAG) - the recommended item's dependence on candidate order in the prompt - and proposes POB-ICM (contingency-matrix + Chi-square) and POB-UNBP (uniformity null model, permutation evaluation, stochastic decoding with guarantees); both reject positional independence in SOTA models and motivate auditing controls (order randomization, standardized prompting).
   * Key techniques:
     - POB-ICM: contingency-matrix analysis plus Chi-square independence testing
     - POB-UNBP: uniformity null model under permutation, sample-efficient, stochastic decoding with formal statistical guarantees
     - Controlled RAG testbed: real product catalog, fixed template, 2000 queries x 20 permutations = 40,000 instances
     - Three metrics: permutation sensitivity, positional bias, strong positional bias
     - Robustness analysis across candidate-set size and decoding temperature
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — abstract states source code is publicly released, but no verifiable public repository URL was located in this pass (treated as not-open until a repo is confirmed).
     - **Novelty: 8/10** — rigorous statistical detection of prompt-order positional bias in LLM-RS with formal guarantees.
     - **Fairness: 8/10** — directly measures and quantifies a positional (order) bias that undermines fairness/robustness of LLM recommenders.
     - **Robustness: 8/10** — 40k-instance controlled study with robustness across candidate-set size and temperature.
     - **Impact: 7/10** — from University of Granada; establishes positional bias as a measurable, reproducible property and motivates governance/auditing.

## Papers Classic Must Read


The list's in no particular order.

1. **OneTrans: Unified Feature Interaction and Sequence Modeling with One Transformer in Industrial Recommender**
   * Affiliation: Alibaba Group (Taobao/Tmall) — (Zhaoqi Zhang, Haolei Pei, Jun Guo, Tianyu Wang, Yufei Feng, Hui Sun, Shaowei Liu, Aixin Sun — Alibaba Group)
   * Link: [arxiv.org/abs/2510.26104](https://arxiv.org/abs/2510.26104)
   * Venue: WWW 2026
   * TL;DR: Unified Transformer backbone replacing the traditional encode-then-interaction pipeline; one tokenizer converts both sequential (user behavior) and non-sequential (user/item attributes) features into a single token sequence with shared params for S-tokens and token-specific params for NS-tokens; cross-request KV caching enables efficient serving; +5.68% per-user GMV in online A/B.
   * Key techniques:
     - Unified Tokenizer: converts sequential S-tokens and non-sequential NS-tokens into a single token sequence for joint processing
     - Mixed Transformer Blocks: shared parameters across homogeneous sequential tokens + token-specific parameters for heterogeneous non-sequential tokens
     - Cross-Request KV Caching: precomputes and caches intermediate representations, reducing costs during both training and inference
     - Causal Attention + Pyramid Stacking: maintains temporal ordering with efficient autoregressive-style processing amenable to FlashAttention
   * Scores (Opensource? / Novelty / Fairness / Robustness / Impact):
     - **Opensource?: 0/10** — No public code available (Alibaba internal production)
     - **Novelty: 8/10** — First to unify feature interaction and sequence modeling under a single Transformer backbone; breaks the encode-then-interaction paradigm
     - **Fairness: 3/10** — Not addressing fairness
     - **Robustness: 8/10** — WWW 2026 peer-reviewed; deployed at Alibaba scale with +5.68% per-user GMV in online A/B tests
     - **Impact: 8/10** — WWW 2026; Alibaba; foundational architecture for unified recommendation Transformers; enables scaling and unified optimization

2. **OpenOneRec Technical Report**
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

3. **OneMall: One Architecture, More Scenarios — End-to-End Generative Recommender Family at Kuaishou E-Commerce**
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

4. **OneRec-Think: In-Text Reasoning for Generative Recommendation**
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

5. **OneRec-V2 Technical Report**
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

6. **MiniOneRec: An Open-Source Framework for Scaling Generative Recommendation**
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

7. **UniGRec: Unified Generative Recommendation with Soft Identifiers for End-to-End Optimization**
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

8. **Rec-R1: Bridging Generative Large Language Models and User-Centric Recommendation Systems via Reinforcement Learning**
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

9. **RelayGR: Scaling Long-Sequence Generative Recommendation via Cross-Stage Relay-Race Inference**
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

10. **Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner)**
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

11. **MuonRec: Shifting the Optimizer Paradigm Beyond Adam in Scalable Generative Recommendation**
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

12. **[STATIC] Vectorizing the Trie: Efficient Constrained Decoding for LLM-based Generative Retrieval on Accelerators**
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

13. **Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization (GRAD)**
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

14. **Rank-GRPO: Training LLM-based Conversational Recommender Systems with Reinforcement Learning (ConvRec-R1)**
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

## By Opensource

Papers whose daily entry lists **Opensource?** strictly above **0/10**. Sorted by score (highest first), then by title.

| Score | Paper |
| --- | --- |
| 10/10 | Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte) |
| 10/10 | MiniOneRec: An Open-Source Framework for Scaling Generative Recommendation |
| 10/10 | RecRM-Bench: Benchmarking Multidimensional Reward Modeling for Agentic Recommender Systems |
| 9/10 | [STATIC] Vectorizing the Trie: Efficient Constrained Decoding for LLM-based Generative Retrieval on Accelerators |
| 9/10 | Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE) |
| 9/10 | Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE) |
| 9/10 | DynamicPO: Dynamic Preference Optimization for Recommendation (DASFAA 2026) |
| 9/10 | FORGE: Forming Semantic Identifiers for Generative Retrieval in Industrial Datasets |
| 9/10 | LLM-as-a-Judge for Reliable and Explainable Offline Evaluation in Top-K Recommendation (LLM Judge) |
| 9/10 | One Pass, Any Order: Position-Invariant Listwise Reranking for LLM-Based Recommendation (InvariRank) |
| 9/10 | OpenOneRec Technical Report |
| 9/10 | Rank-GRPO: Training LLM-based Conversational Recommender Systems with Reinforcement Learning (ConvRec-R1) |
| 9/10 | RPCBench: A Benchmark for Proactive Premise Critique in LLM-based Recommendation (RPCBench) |
| 9/10 | Tencent Advertising Algorithm Challenge 2025: All-Modality Generative Recommendation |
| 9/10 | The Pitfall of Scaling Up: Uncovering and Mitigating Popularity Bias Amplification in Scaling Transformer-based Recommenders (SPRINT) |
| 8.5/10 | Factorized Latent Reasoning for LLM-based Recommendation (FLR) |
| 8/10 | A Standardized Re-evaluation of Conversational Recommender Systems on the ReDial Dataset (APG4RecSim) |
| 8/10 | ACE: Anisotropy-Controllable Embedding for LLM-enhanced Sequential Recommendation |
| 8/10 | Adaptive Autoguidance for Item-Side Fairness in Diffusion Recommender Systems (A2G-DiffRec) |
| 8/10 | APAO: Bridging the Training-Inference Gap in Generative Recommendation via Adaptive Prefix-Aware Optimization (APAO) |
| 8/10 | Attention Calibration for Position-Fair Dense Information Retrieval |
| 8/10 | BRIDGE: Behavior-Guided Candidate Calibration for Multimodal Recommendation |
| 8/10 | Closing the Indexing-Decoding Gap in Multimodal Generative Retrieval via Prefix Retention Optimization (PRO) |
| 8/10 | Cold-Starts in Generative Recommendation: A Reproducibility Study (ColdGenRec) |
| 8/10 | COPF: An Online Framework for Deployment-Stable Counterfactual Fairness in Evolving Graphs |
| 8/10 | Credit-assigned Policy Gradient for Early Stage Retrieval in Two-stage Ranking (CA-PG) |
| 8/10 | Differentiable Semantic ID for Generative Recommendation (DIGER) |
| 8/10 | Do Generative Recommenders Deepen the Information Cocoon? A Closed-Loop Simulation with LLM-powered User Simulators (RecLoop) |
| 8/10 | Drift-Aware Continual Tokenization for Generative Recommendation (DACT) |
| 8/10 | Dynamic Spectral Denoising with Global-Context Attention for Multi-Behavior Recommendation (SpectraMB) |
| 8/10 | Expand More, Shrink Less: Shaping Effective-Rank Dynamics for Dense Scaling in Recommendation (RankElastor) |
| 8/10 | From Noise to Order: Learning to Rank via Denoising Diffusion (DiffusionRank) |
| 8/10 | GCIB: Graph Contrastive Information Bottleneck for Multi-Behavior Recommendation |
| 8/10 | Generative Late-Interaction Embeddings For Visual Document Retrieval (GLIE) |
| 8/10 | GPlan: Generative Spatiotemporal Intent Sequence Recommendation via Implicit Reasoning in Amap |
| 8/10 | Hierarchical Exponential-Gaussian Mixtures for Watch-Time Distribution Prediction (HEGM) |
| 8/10 | How Reliable Are Semantic-ID Tokenizer Comparisons in Generative Recommendation? |
| 8/10 | HRPO: Hierarchical Residual Policy Optimization for Generative Recommendations |
| 8/10 | Intuition-Guided Latent Reasoning for LLM-Based Recommendation (IntuRec) |
| 8/10 | LSREP: A Longitudinal State-Replay Protocol for Evaluating Conversational Memory, with ICE v2 as an Audited Local-First Architecture (LSREP) |
| 8/10 | ManCAR: Manifold-Constrained Latent Reasoning with Adaptive Test-Time Computation for Sequential Recommendation |
| 8/10 | Masked Diffusion for Generative Recommendation (MaskGR) |
| 8/10 | Mult-DPO: Multinomial Direct Preference Optimization for Recommender Systems |
| 8/10 | MuonRec: Shifting the Optimizer Paradigm Beyond Adam in Scalable Generative Recommendation |
| 8/10 | On the Memorization and Generalization of Generative Recommendation (MemGen-GR) |
| 8/10 | On the Memorization Behavior of LLMs in Generative Recommendation: Observations, Implications, and Training Strategies (IIRG) |
| 8/10 | One Polluted Page Is Enough: Evaluating Web Content Pollution in Generative Recommenders (FORGE) |
| 8/10 | OneRec-Think: In-Text Reasoning for Generative Recommendation |
| 8/10 | Preference Shapes Relevance: Cross-component Hierarchical Semantic Alignment for Personalized Generative Retrieval (CHAP) |
| 8/10 | ProRL: Effective Reinforcement Learning for Proactive Recommendation via Rectified Policy Gradient Estimation (ProRL) |
| 8/10 | RAGEAR: Retrieval-Augmented Graph-Enhanced Academic Recommender |
| 8/10 | Rethinking Convolutional Networks for Attribute-Aware Sequential Recommendation (ConvRec) |
| 8/10 | Retrieval, Scoring, and Decoding Shape Performance and Stability in LLM-based Conversational Recommendation (CRS-Performance) |
| 8/10 | SafeGEO: Understanding Generative Engine Optimization Risks in Recommendation Agents |
| 8/10 | Self-Evolving Memory for Generative Recommendation |
| 8/10 | SIDScope: A Diagnostic Resource for Semantic-ID Interfaces in Generative Recommendation |
| 8/10 | TCA4Rec: Token-level Collaborative Alignment for LLM-based Generative Recommendation |
| 8/10 | Time-Aware Diffusion based on Preference Disentanglement for Generative Recommendation (TDPM) |
| 8/10 | TRACE: A Conversational Framework for Sustainable Tourism Recommendation with Agentic Counterfactual Explanations |
| 8/10 | UniGRec: Unified Generative Recommendation with Soft Identifiers for End-to-End Optimization |
| 8/10 | UniRank: Benchmarking Ranking Models for Unified Sequential Modeling and Feature Interaction |
| 8/10 | Unleashing the Native Recommendation Potential: LLM-Based Generative Recommendation via Structured Term Identifiers (GRLM) |
| 8/10 | What Makes a Good Semantic ID for Generative Recommendation? A Reproducibility Study (SID-Repro) |
| 7/10 | Distribution-Level Contrastive Supervision for Generative Recommendation (SODA) — University of Science and Technology of China / Upwork, RecSys 2026 — [github.com/freyasa/SODA](https://github.com/freyasa/SODA) |
| 7/10 | A Redundancy Reduction Approach for Controllable Sequential Recommendations (BT-SR) |
| 7/10 | AdaM-Rec: Adaptive Modality Routing for Multimodal Recommendation (AdaM-Rec) |
| 7/10 | Addressing Cross-Stage Decoupling of Semantic and Collaborative Signals in Generative Recommendation (SCRec) |
| 7/10 | An Efficient and Effective Agentic Group Shilling Attack on Recommender Systems (AGAS) |
| 7/10 | Are We Really Making Progress in Group Recommendation? Unmasking the Tie-Breaking Illusion (Tie-Breaking) |
| 7/10 | Beyond Modality Harmony: Orthogonal Purification and Topology-Guided MoE for Conflict-Aware Multimodal Recommendation (OrthoRec) |
| 7/10 | Beyond Noisy Signals: Dual-Level Denoising for Multi-modal Sequential Recommendation (DDMSR) |
| 7/10 | Beyond Successor Accuracy: State Retention for Recursive Self-Improvement in Recommendation (RecRSI) |
| 7/10 | Can We Steer the Black-Box? Towards Controllability-Centric Evaluation of Recommender Systems with Collaborative Agents (CtrlBench-Rec) |
| 7/10 | CARD: Counterfactual Attention Regulation Diffusion for Diffusion-based Sequential Recommendation (CARD) — Sun Yat-sen University / Peng Cheng Laboratory, ICASSP 2026 — [github.com/yanqilong3321/CARD](https://github.com/yanqilong3321/CARD) |
| 7/10 | Closing the Long-Short View Gap in Sequential Recommendation without Cached History |
| 7/10 | CoFiRec: Coarse-to-Fine Tokenization for Generative Recommendation (CoFiRec) |
| 7/10 | CRAMER: Control via Request-Aware Masking for Editing Recommenders (CRAMER) |
| 7/10 | CutBCE: A Fused Binary Cross-Entropy Loss for Large-Vocabulary Sequential Recommendation (CutBCE) |
| 7/10 | Decision4Rec: A Jev-Inspired Framework of Decision Models on Knowledge and Active Graphs for Multi-Agent Recommender Systems (Decision4Rec) |
| 7/10 | Diagnosing and Mitigating Retrieval Bottlenecks in LLM-Based Cold-Start Recommendation (LHF) |
| 7/10 | DiffGRM: Diffusion-based Generative Recommendation Model (DiffGRM) — Kuaishou, WWW 2026 — [github.com/liuzhao09/DiffGRM](https://github.com/liuzhao09/DiffGRM) |
| 7/10 | Difficulty-Aware Semantic-ID Optimization for Generative Recommendation (DASO) |
| 7/10 | DoPR: Reusable Compressed Document Prefixes for Efficient LLM Reranking (DoPR) |
| 7/10 | Dual-Diffusional Generative Fashion Recommendation (DualFashion) |
| 7/10 | Dual-Stream MLP is All You Need for CTR Prediction (DS-MLP) |
| 7/10 | Embedding Surgery: Localized Updates for Adaptive Ranking Correction in Dense Retrieval |
| 7/10 | Empowering Compact LLMs with Fusion of Layer-wise Exits for Recommendation (FLEXRec) |
| 7/10 | Enhancing Group Recommendation with Memory-Augmented Reasoning in LLM Agent (AGR) |
| 7/10 | Eval4DiRec: A Unified and Systematic Evaluation Framework for Diffusion-based Recommender Systems (Eval4DiRec) |
| 7/10 | Evo-Rec: Learning Better Reasoning for Generative Recommendation with Semantic IDs (Evo-Rec) |
| 7/10 | Fast and Feasible: Permutation-based Constrained Reranking for Revenue Maximization (PermR) |
| 7/10 | FatsMB: From Agnostic to Specific: Latent Preference Diffusion for Multi-Behavior Sequential Recommendation (FatsMB) |
| 7/10 | FAVE: Flow-based Average Velocity Establishment for Sequential Recommendation |
| 7/10 | FedHUR: Learning Hierarchical Utility-Guided Client Relations for Personalized Federated Recommendation |
| 7/10 | FINALLY: A Dataset Recommender System for Recommender-Systems Research |
| 7/10 | FLASH: Rethinking Semantic ID Construction for Generative Recommendation: SimHash with Parallel Decoding and Semantic Alignment (FLASH) |
| 7/10 | Generative Archetype-Grounded Item Representations for Sequential Recommendation (GenAIR) |
| 7/10 | Harmonizing Semantic and Collaborative in LLMs: Reasoning-based Embedding Generator for Sequential Recommendation (ReaEmb) |
| 7/10 | HyCoRec: Hypergraph-Enhanced Multi-Preference Learning for Alleviating Matthew Effect in Conversational Recommendation |
| 7/10 | IDs That Mean Something: A Hands-On Tutorial on Semantic IDs for Recommender Systems (Semantic-ID-Tutorial) — Huawei Ireland Research Center / University College Dublin, CIKM 2026 — [github.com/saghiles/semantic-id-tutorial](https://github.com/saghiles/semantic-id-tutorial) |
| 7/10 | IntBMoE: Integrating Block-Level Conditioning into Expert Composition for Full-Participation Mixture-of-Experts (IntBMoE) |
| 7/10 | ItemRAG: Item-Based Retrieval-Augmented Generation for LLM-Based Recommendation |
| 7/10 | Iterative Semantic Reasoning from Individual to Group Interests for Generative Recommendation with LLMs (ISRF) |
| 7/10 | JBM-Diff: Joint Behavior-guided and Modality-coherence Conditional Graph Diffusion Denoising for Multi-Modal Recommendation (JBM-Diff) |
| 7/10 | JobCCC: A Constraint-Aware Conversational Job Recommendation Benchmark and Method (JobCCC) |
| 7/10 | KL-MOPD: Discrepancy-Aware Multi-Objective On-Policy Distillation for Generative Recommendation (KL-MOPD) — Zhejiang University / Alibaba Group, arXiv 2610.36973 |
| 7/10 | Learning Decomposed Contextual Token Representations from Pretrained and Collaborative Signals for Generative Recommendation (DECOR) |
| 7/10 | Learning Multiresolution Relevance for Hierarchical Generative Retrieval (RARS) |
| 7/10 | Learning to Rotate: Temporal and Semantic Rotary Encoding for Sequential Modeling (SIREN-RoPE) |
| 7/10 | LIME-Rec: Auditing Semantic Gains in Sequential Recommendation — A Lightweight Recovery Test |
| 7/10 | LMStaR: Language Models for Statement Ranking (LMStaR) — Sorbonne University, Paris, France / AgroParisTech, UMR MIA Paris-Saclay, arXiv 2611.04775 — [github.com/BenKabongo25/language-models-statement-ranking](https://github.com/BenKabongo25/language-models-statement-ranking) |
| 7/10 | MemRetriever: Learning to Search, Reflect, and Retrieve from Long-Term Memory |
| 7/10 | Mitigating Popularity Bias in Sequential Recommendations with Sparse Prior-Regularized Objective (PR-entmax) — Sber AI Lab / Lomonosov MSU, CIKM 2026 — [github.com/Antondfger/Sparse-Prior-Regularized](https://github.com/Antondfger/Sparse-Prior-Regularized) |
| 7/10 | Mixture-of-Experts Knowledge Graph Retrieval-Augmented Generation for Multi-Agent LLM-based Recommendation (MixRAGRec) |
| 7/10 | MLLMRec-R1: Incentivizing Reasoning Capability in LLMs for Multimodal Sequential Recommendation (MLLMRec-R1) — Hefei University of Technology — [github.com/wangyu0627/MLLMRec-R1](https://github.com/wangyu0627/MLLMRec-R1) |
| 7/10 | MLPs are Efficient Distilled Generative Recommenders (SID-MLP) |
| 7/10 | MV-Thinker: Think Globally, Generate Personally: Multi-View Thinking with Adaptive Generation for Generative Recommendation (MV-Thinker) — City University of Hong Kong / Tencent Platform and Content Group, arXiv 2611.02463 — [anonymous.4open.science/r/MV-Thinker](https://anonymous.4open.science/r/MV-Thinker) |
| 7/10 | Octen-WebGR: Scaling Generative Retrieval to 200 Million Web Pages (Octen-WebGR) — Octen, arXiv 2610.35256 |
| 7/10 | OptST: Optimizing Semantic Tokenization for LLM-Enhanced Recommendation (OptST) — Shenzhen Technology University / Shenzhen University / The Hong Kong Polytechnic University / McGill University, Findings of WSDM 2027 — [github.com/chchchchc1023/wsdm27-optst](https://github.com/chchchchc1023/wsdm27-optst) |
| 7/10 | OneSearch-V2: The Latent Reasoning Enhanced Self-distillation Generative Search Framework (OneSearch-V2) |
| 7/10 | Popcorn: A Configurable Benchmark for Visual Evidence in Multimodal Movie Recommendation (Popcorn) |
| 7/10 | Prompt Optimization for User Simulation in Conversational Recommender Systems (UserSimulator) |
| 7/10 | Quanta: A Self-Contained Python Library for Hybrid Retrieval over Quantised Embeddings, Lexical Indexes, and Knowledge Graphs (Quanta) |
| 7/10 | R3-VAE: Reference Vector-Guided Rating Residual Quantization VAE for Generative Recommendation |
| 7/10 | RAGR: Review-Augmented Generative Recommendation |
| 7/10 | RAMP: Robust Ad Recommendation Under Limited Personalized-Feature Availability via Masking and Alignment Pathways |
| 7/10 | RAR: Retrieval Augmented Conversational Recommendation with Reinforcement Learning (RAR) — UIUC / Google DeepMind / UC San Diego — [github.com/Yueeeeeeee/RAR](https://github.com/Yueeeeeeee/RAR) |
| 7/10 | Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner) |
| 7/10 | Reasoning Reranking with Semantic IDs as the Sole Item Representation (ReRankID) — Google / University of Toronto — [github.com/lilv98/ReRankID](https://github.com/lilv98/ReRankID) |
| 7/10 | Rec-R1: Bridging Generative Large Language Models and User-Centric Recommendation Systems via Reinforcement Learning |
| 7/10 | RecPFN: Prior-Fitted Networks for In-Context-Based Recommendations (RecPFN) |
| 7/10 | RecRSI: Mechanism-Guided Discovery of Recommendation Algorithms (RecRSI) — Shanghai Jiao Tong University, China — [github.com/DynamisG210/RecRSI](https://github.com/DynamisG210/RecRSI) |
| 7/10 | RecToolBench: Benchmarking Recommendation-Specific Tool Orchestration under Fuzzy User Intent |
| 7/10 | REDSI: Addressing the Reproducibility and Evaluation Consistency of Differentiable Search Indexing for Document Retrieval |
| 7/10 | ReMaRk: Many Right Answers, One Training Example: Removing Responder Noise from GRPO for LLM Recommenders (ReMaRk) — Nanyang Technological University — [github.com/LiXin97/ReMaRk](https://github.com/LiXin97/ReMaRk) |
| 7/10 | Repeated Queries Exhaust an LLM's Brand Recommendations but Not Its Sources |
| 7/10 | REPREC: Representation Driven Parameter-Efficient Recommendation System (REPREC) |
| 7/10 | Reproducing FACTER: Fairness via Conformal Thresholding and Prompt Repair |
| 7/10 | Rethinking Item Tokenization in Generative Recommenders: From Fixed Atoms to Semantic Subwords (SST) |
| 7/10 | RouteRec: Behavior-Guided Sparse Routing for Sequential Recommendation (RouteRec) |
| 7/10 | RSIR: Can Recommender Systems Teach Themselves? A Recursive Self-Improving Framework with Fidelity Control (RSIR) |
| 7/10 | SAERec: Constructing Fine-grained Interpretable Intents Priors via Sparse Autoencoders for Recommendation (SAERec) |
| 7/10 | SafeCRS: Personalized Safety Alignment for LLM-Based Conversational Recommender Systems (SafeCRS) — UIC / UIUC / Amazon, KDD 2026 — [github.com/xxyyffyeah/SafeCRS](https://github.com/xxyyffyeah/SafeCRS) |
| 7/10 | SIDInspector: A Mapping-First Diagnostic Resource for Semantic-ID Tokenizers |
| 7/10 | Skill Is Not Document: A Query-Conditional Benchmark and Two-Stage Retriever for LLM Agent Skill Routing (R3) |
| 7/10 | SPRIG: Semantic-ID-enhanced Paths for Knowledge Graph-based Generative Recommendation (SPRIG) |
| 7/10 | Stream-aware Side Adaptation for Large Pre-trained Multimodal Embedding Models in Sequential Recommendation (Stresa) |
| 7/10 | Structure-Aligned History Learning with Subspace-Structured Semantic IDs for Generative Recommendation (SAHL) |
| 7/10 | SURF: Subtractive Updates for Recommender Forgetting (SURF) |
| 7/10 | SynGR: Unleashing the Potential of Cross-Modal Synergy for Generative Recommendation (SynGR) |
| 7/10 | tau-Rec: A Verifiable Benchmark for Agentic Recommender Systems |
| 7/10 | Teach Multimodal Recommendation Model to See via Personalized Visual Extraction and Adaptive Learning (REVEAL) |
| 7/10 | The Best of Both Worlds: Harmonizing Semantic and Hash IDs for Sequential Recommendation (H²Rec) |
| 7/10 | Think Harder Where It Matters: Item-Level Adaptive Recursion for Sequential Recommendation (LoopRec) — Renmin University of China — [github.com/Elpmis117/LoopRec](https://github.com/Elpmis117/LoopRec) |
| 7/10 | Towards Effective Structured Context Modeling for Conversational Recommender Systems via Dual-node Monte Carlo Tree Search (DREAMS) |
| 7/10 | Two-Sided State-Space Models for Sequential Recommendation with Non-Random Multimodal Review Feedback (TS-SSM) |
| 7/10 | Uncertainty and Fairness Awareness in LLM-Based Recommendation Systems |
| 7/10 | Uncertainty-aware Generative Recommendation (UGR) |
| 7/10 | URecJPQ: Memory-efficient Multimodal Recommendation Models through RecJPQ in Large-Scale Scenarios (URecJPQ) |
| 7/10 | UserArena: Benchmarking Interactive User Simulation for Long-Horizon Shopping Agents (UserArena) — Leiden University / Renmin University of China / Alibaba Group / Institute of Computing Technology, CAS — [github.com/RecGPT-Team/UserArena](https://github.com/RecGPT-Team/UserArena) |
| 7/10 | Who Owns the AI Recommendation? A Multi-Industry Empirical Map of Brand Category Ownership Across Large Language Models (LLM Brand) |
| 7/10 | X-KGRank: A Knowledge Graph RAG Framework for Explainable Recommendations via Pattern Mining and LLM Re-Ranking (X-KGRank) |
| 7/10 | HARP: Training-Free Dual-Profile Agentic Communication for LLM-Based Recommendation (HARP) — Harbin Institute of Technology, Shenzhen / Great Bay University, NeurIPS 2026 — [github.com/Jove-Zhen/HARP](https://github.com/Jove-Zhen/HARP) |
| 7/10 | tau-Rec-Books: A Disclosure-Controlled Benchmark for Requirement Elicitation in Agentic Recommender Systems (tau-Rec-Books) — Princeton University, arXiv 2611.04459 — [github.com/nbharaths/tau-rec](https://github.com/nbharaths/tau-rec) |
| 7/10 | PFA: Attention Can Be Progressively Focused in Long-Sequence Generative Recommendation (PFA) — [anonymous.4open.science/r/PFA-review-088D](https://anonymous.4open.science/r/PFA-review-088D) |
| 6.5/10 | On Efficiency-Effectiveness Trade-off of Diffusion-based Recommenders (TA-Rec) |
| 6.5/10 | RES-MR: Risk-Aware Reasoning for Explainable and Safe Medication Recommendation (RES-MR) |
| 6/10 | AutoRSE: Evaluating LLM Agents as Recommendation Engineers for Self-Evolving Recommender Systems (AutoRSE) — University of Science and Technology of China / National University of Singapore, arXiv 2610.37228 |
| 6/10 | A Behavioral Trait Leaks into Preferences: Diagnosing Trait Interference in LLM User Simulators (PQA) |
| 6/10 | Beyond Centralization: User-Controlled Federated Recommendations |
| 6/10 | Beyond Dense Connectivity: Explicit Sparsity for Scalable Recommendation (SSR) |
| 6/10 | Beyond Uniform Token Training: A Multi-Target Framework for Learning Token-Weighted Objectives in Generative Recommenders (Beyond Uniform Token Training) |
| 6/10 | CARD: Non-Uniform Quantization of Visual Semantic Unit for Generative Recommendation |
| 6/10 | CogRec: Structure-Cognitive Fast-and-Slow Reasoning for Generative Recommendation (CogRec) |
| 6/10 | Computed, not Memorized: Bit-Factorized Identifiers for Efficient Generative Retrieval (Bit-Factorized) — Leiden University / Radboud University — [anonymous.4open.science/r/bit_factorized_token-2C13](https://anonymous.4open.science/r/bit_factorized_token-2C13/) |
| 6/10 | Diffusion Language Model for Recommendation (DLMRec) |
| 6/10 | Empowering Cross-Domain Sequential Recommendation with Hybrid Tokenization and Serial-Parallel Decoding (GenCDSR) |
| 6/10 | Evaluating Brand Retrieval and Ranking in Large Language Model Recommendations |
| 6/10 | From Overlooked to Explored: Recovering Item Relations via Mixture of Perspectives for Sequential Recommendation (PRISM) |
| 6/10 | Generate What You Can Trust: Content Credibility in Generative Recommenders (CreGR) |
| 6/10 | GraphLoRA: Structure-Aware Low-Rank Adaptation for Large Language Model Recommendation |
| 6/10 | HEM-Med: A Hierarchical Agentic Memory Framework for Safe Multi-Center Medication Recommendation (HEM-Med) — Qilu University of Technology / University of Technology Sydney — [anonymous.4open.science/r/anonymous-HEM-Med-0935](https://anonymous.4open.science/r/anonymous-HEM-Med-0935/) |
| 6/10 | HyperTrace: Hypothesis-Based Preference Tracing for Online LLM Personalization |
| 6/10 | HypRQ-VAE: Hyperbolic Item Indexing for Long-Tail-Aware Generative Recommender Systems (HypRQ-VAE) |
| 6/10 | LLM Recommenders Produce Demographic Inequality Through Content Preferences — University of Zurich, arXiv 2610.41854 — [github.com/paganick/llm-recsys-twitter-yougov-PNAS](https://github.com/paganick/llm-recsys-twitter-yougov-PNAS) |
| 6/10 | What Gets Hacked in a Collaborative Reward for LLM Recommenders: The Part That Does Not Depend on the User (LLM4Rec-CF-Bias) — University of California, San Diego, USA, arXiv 2611.07588 — [anonymous.4open.science/r/LLM4Rec-CF-Bias-27EF](https://anonymous.4open.science/r/LLM4Rec-CF-Bias-27EF/) |
| 6/10 | MARS: Multi-rate Aggregation of Recency Signals for Sequential Recommendation across Sparse and Dense Regimes (MARS) |
| 6/10 | Mitigating Matthew Effect: Multi-Hypergraph Boosted Multi-Interest Self-Supervised Learning for Conversational Recommendation (HiCore) |
| 6/10 | MuSID-KD: Multigranularity Knowledge Distillation for Generative Recommendation with Semantic IDs (MuSID-KD) — East China Normal University, arXiv 2610.35218 |
| 6/10 | PAPA: Online Personalized Active Preference Alignment (PAPA) |
| 6/10 | Personalization Matters: Long-Horizon Conversation Agent with User-Centric Information in Online Shopping Interactions (Personalization Matters) |
| 6/10 | PsyBer-Agent: A Psychology-Driven User Agent for Recommender Systems (PsyBer-Agent) — Xi'an Jiaotong-Liverpool University / University of Liverpool / Alibaba Group — [anonymous.4open.science/r/CC66F](https://anonymous.4open.science/r/CC66F/) |
| 6/10 | QD-Rec: Open-Ended Evolution of Recommendations via Quality-Diversity (QD-Rec) — Sakana AI — [github.com/SakanaAI/QD-Rec](https://github.com/SakanaAI/QD-Rec) |
| 6/10 | Recommender System as Slow and Fast Thinkers (DS-Frame) |
| 6/10 | RecSoup: Efficient Model Merging Approach for Controllable Multi-Objective Recommendation (RecSoup) — Renmin University of China, CIKM 2026 — [github.com/35798642/RECSOUP](https://github.com/35798642/RECSOUP) |
| 6/10 | ReGen: Controllable Generative Recommendation via Guided Token Refinement (ReGen) — Xi'an Jiaotong-Liverpool University / University of Liverpool / The Hong Kong Polytechnic University — [github.com/zhang-haichao/ReGen](https://github.com/zhang-haichao/ReGen) |
| 6/10 | Residual Dominance as a Structural Account of Last-Item Reliance in Causal Self-Attention Recommenders (Residual Dominance) |
| 6/10 | Scaling Graph Neural Networks for Friend Recommendation: Multi-Hash User Embeddings and Temporal Neighbor Sampling |
| 6/10 | SemPOI-RL: Aligning LLM Semantic Reasoning for Interpretable Out-of-Town POI Sequential Generation (SemPOI-RL) — Beihang University — [github.com/Wind-Flipped/SemPOI-RL](https://github.com/Wind-Flipped/SemPOI-RL) |
| 6/10 | SG-UMP: Sequence-Guided Universal Multimodal Prioritization Calculation Framework (SG-UMP) |
| 6/10 | SharpRec: Sharpness-aware Model Merging with Salience Recovery for LLM-based Cross-Domain Sequential Recommendation (SharpRec) |
| 6/10 | Tackling the Modality Inhibitance Effect with Wavelet-based Modality Integration in Multi-modal Recommendation (MMWave) — Nanyang Technological University, IEEE TKDE 2026 — [github.com/kennethorq/MMWave](https://github.com/kennethorq/MMWave) |
| 6/10 | TATK: Triple-Aware Top-K Learning with Knowledge-Grounded Verification for LLM-based Sequential Recommendation |
| 6/10 | Tlow: Flow-based Item Tokenizer for Recommendation (Tlow) |
| 6/10 | Trading Engagement for Sustainability: Carbon-Aware Re-ranking for E-commerce Recommendations |
| 6/10 | Understanding and Debugging Failures in N-Gram-Based Generative Retrieval |
| 6/10 | UniLang: A Unified Generative Framework for Integrating Machine-Native Symbols into Pretrained LLMs (UniLang) |
| 6/10 | Vela: User Behavior as Supervision Sparks LLM Intelligence (Vela) — AllSpark at Xiaohongshu (RedNote) — [github.com/AllSpark-Research/Vela](https://github.com/AllSpark-Research/Vela) |
| 6/10 | VirtualMLE: A Virtual ML Engineer that Optimizes Sequential Recommenders (VirtualMLE) |
| 6/10 | When the Label Ignores the Request: Auditing Policy-Selected Targets in Synthetic Conversational Music Recommendation (When-the-Label) |
| 6/10 | Whole-Pool Setwise Reranking with Long-Context Language Models (WP-Setwise / DualEnd) |
| 5.5/10 | PRISM: Purified Representation and Integrated Semantic Modeling for Generative Sequential Recommendation |
| 5/10 | Adaptive Item-based Collaborative Structures via Noise Rescheduling in Diffusion for Generative Recommendation (ANR-DiffRec) |
| 5/10 | Conversational Recommendation over Live E-Commerce Catalogues with Self-Refreshing Retrieval |
| 5/10 | ExPerT: Personalizing LLM Responses to Users' Domain Expertise via Query-Wise Semantic and Keystroke Behavioral Cues (ExPerT) |
| 5/10 | From Feature Interaction to Feature Transport - A Unified Block for Scalable Recommendation Models (CRAFT) |
| 5/10 | Gwhere: Guess Where You Go — Generative Next Point-of-Interest Recommendation in Amap (Gwhere) |
| 5/10 | Hyperbolic RQ-VAE enhanced Generative Recommendation with Differential-Length Codebook Strategy (HG-Rec) |
| 5/10 | Information-Guided Selective Modality-Interest Alignment for Multimodal Recommendation (AMUR) |
| 5/10 | LBR: Towards Mitigating Length Bias in Large Language Models for Recommendation (LBR) |
| 5/10 | OneReason Technical Report |
| 5/10 | Progressive Alignment of Recommender Foundation Model through Multi-Phase Post-Training (Progressive FM Post-Training) |
| 5/10 | SelfDR: Self-Distillation from Reasoning for LLM-Based Recommendation (SelfDR) |
| 5/10 | SimGR: Escaping the Pitfalls of Generative Decoding in LLM-based Recommendation (SimGR) |
| 5/10 | Think2Go: Generative Next POI Recommendation with LLM Reasoning (Think2Go) |
| 4/10 | Cascading Relevance-driven Recommendation Network for CTR Prediction in Trigger-Introduced Recommendation (CRRN) |
| 4/10 | Give the Long-tail More SPACE: Promoting Provider Fairness in Next POI Recommendation (SPACE) |
| 4/10 | GLASS: Coarse-to-Fine Long-term Interest Modeling for Generative Recommendation |
| 4/10 | Multi-Decoder OneRec: Controllable Generative Retrieval for Multi-Objective Industrial Recommendation |
| 4/10 | RecRec: Recursive Refinement for Sequential Recommendation |
| 4/10 | Towards Efficient Reasoning in LLM-Based Recommender Systems via Model Merging (REAM) |
| 4/10 | TRACER: Balancing Stability-Plasticity-Cognitivity Trilemma for LLM Enhanced Continual Recommendation (TRACER) |
| 3/10 | Cheaper is Better: A Discount-Aware Network for Conversion Rate Prediction in E-commerce Recommendation System (DANet) |
| 3/10 | EPIC: Explicit Posterior Item Conditioning for Semantic ID Diffusion Recommendation (EPIC) |
| 3/10 | InforID: Adaptive Semantic Capacity Allocation for Parallel Generative Recommendation (InforID) |
| 3/10 | Mitigating Reward Hacking in LLM-based Recommendation: A Preference Optimization Approach (SIRIUS) |
| 3/10 | PVTG / Personalized Video Thumbnail Generation |
| 3/10 | SAGE: Semantic Attribute Graphs for Multi-Entity Visual Retrieval (SAGE) |
| 3/10 | STORM: Stepwise Token Optimization with Reward-Guided Beam Search |
| 3/10 | Tail-Aware Adaptive-k: Query-Adaptive Context Selection for Retrieval-Augmented Generation (TAA-k) |
| 3/10 | TimeRoute: Time-Aware Modality Routing and Diffusion for Multi-Modal Recommendation (TimeRoute) |
| 2/10 | Verifiable Reasoning for LLM-based Generative Recommendation (VRec) |
| 1/10 | TSPORec: Token Selection via Preference Optimization for LLM-Based Sequential Recommendation (TSPORec) |

**Count:** 243 papers as of November 09.

---
## By Keyword

### Beam Search Decoding
- FedCGR: Federated Cross-Domain Generative Recommendation (FedCGR) — CIKM 2026
- GenRec / LLM-Backed Ranker — Netflix
- Closing the Indexing-Decoding Gap in Multimodal Generative Retrieval via Prefix Retention Optimization (PRO)
- GCRS: Generative Conversational Recommender System
- Generative Recommendation for Large-Scale Advertising (GR4AD)
- ThinkGR: Integrating Chain-of-Thought into Generative Retrieval
- LLaDA-Rec: Discrete Diffusion for Parallel Semantic ID Generation in Generative Recommendation
- MiniOneRec: An Open-Source Framework for Scaling Generative Recommendation
- Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA)
- Objective Shaping with Hard Negatives: Windowed Partial AUC Optimization for RL-based LLM Recommenders
- PROMISE: Process Reward Models Unlock Test-Time Scaling Laws in Generative Recommendations
- SCOReD: Student-Aware CoT Optimization for Recommendation Distillation (SCOReD)
- SmartGR: Hierarchy and Beam-Aware Knowledge Distillation for Generative Recommendation (SmartGR)
- [STATIC] Vectorizing the Trie: Efficient Constrained Decoding for LLM-based Generative Retrieval on Accelerators
- STORM: Stepwise Token Optimization with Reward-Guided Beam Search
- APAO: Bridging the Training-Inference Gap in Generative Recommendation via Adaptive Prefix-Aware Optimization (APAO)
- GR2 Technical Report (GR2)
- UniSGR: Unified Framework for Semantic ID Generation and Ranking (UniSGR)
- PauseRec: Implicit Reasoning for LLM-based Generative Recommendation (PauseRec)
- HoloRec: Holistic Encoding and Interleaved Reasoning for Generative Recommendation (HoloRec)
- AsymRec: Asymmetric Generative Recommendation via Multi-Expert Projection and Multi-Faceted Hierarchical Quantization (AsymRec)
- DeGRe: Dense-supervised Generative Reranking for Recommendation (DeGRe)
- DaV-Gen: End-to-End Generative Retrieval via Draft-and-Verify (DaV-Gen)
- OneReason Technical Report (OneReason)
- Learning Decomposed Contextual Token Representations from Pretrained and Collaborative Signals for Generative Recommendation (DECOR)
- GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation (GenRec)
- LASAR: Latent Adaptive Semantic Aligned Reasoning for Generative Recommendation (LASAR)
- GateSID: Adaptive Gating for Balancing Semantic and Collaborative Signals in Recommendation (GateSID)
- NEO: A Unified Language Model for Large Scale Search, Recommendation, and Reasoning (NEO)
- FORGE: Forming Semantic Identifiers for Generative Retrieval in Industrial Datasets (FORGE)
- Conditional Memory Enhanced Item Representation for Generative Recommendation (ComeIR)
- The Best of Both Worlds: Harmonizing Semantic and Hash IDs for Sequential Recommendation (H²Rec)
- IBA / IG Budget Allocation -- Chongqing U / Griffith U
- RecRec / Recursive Reasoning -- U Glasgow / Amazon / CMU / NUS
- Gryphon / Item-Level Scoring -- Yandex
- PrefixMem / SID Encoder -- Pinterest
- BONSAI / Decoding Trie Optimization -- MSU / Snap

- GenRecEdit: Adapting Model Editing for Generative Recommendation with Cold-Start Items (GenRecEdit)
- GBLA: Gated Bidirectional Linear Attention for Generative Retrieval (GBLA)
- DRQ: Understanding SID Tokenizer Failures via Decoupled Residual Quantization (DRQ)
- HiSAC: Hierarchical Sparse Activation Compression for Recommenders (HiSAC)
- Beyond Item IDs: Scaling Short-Form-Video Recommendation via Semantic-Native Long Sequence Modeling
- RankGR: Rank-Enhanced Generative Retrieval with Listwise Direct Preference Optimization in Recommendation (RankGR)
- OneBar: An End-to-End Content-Grounded Generative Query Recommendation Framework for E-Commerce Video Feeds (OneBar)
- TokenMinds: Pretrained User Tokens and Embeddings for User Understanding in Large Recommender Systems (TokenMinds)
- RecGPT-V3 Technical Report (RecGPT-V3)
- Topology-Aware Tokenization for Generative Recommendation (TopoTok)
- TSGR: Taobao Search Generative Retrieval (TSGR)
- BARGE: Bridging the Structural Gap — Adapting Autoregressive Generation for Recommendation (BARGE)
- DLMRec: Diffusion Language Model for Recommendation (DLMRec)
- CapsID: Soft-Routed Variable-Length Semantic IDs for Generative Recommendation (CapsID)
- GLASS: Coarse-to-Fine Long-term Interest Modeling for Generative Recommendation (GLASS)
- DIG: Discrimination Is Generation — Unifying Ranking and Retrieval from a Tokenizer Perspective (DIG)
- CaLIR: Category-Guided Latent Intent Reasoning for Generative Retrieval in E-Commerce (CaLIR)
- SynGR: Cross-Modal Synergy for Generative Recommendation (SynGR)
- DREAM: Dynamic Refinement of Early Assignment Mappings (DREAM)
- SimGR: Escaping the Pitfalls of Generative Decoding in LLM-based Recommendation (SimGR)
- OneFeed: A Unified Generative Framework for Feed Content Enhancement and Query Generation (OneFeed)
- CogRec: Structure-Cognitive Fast-and-Slow Reasoning for Generative Recommendation (CogRec)
- LaRec: Unleashing LLM-based Latent Reasoning for Generative Recommendation (LaRec)
- OxygenREC-v2: Internalizing Discrimination into Generative Recommendation (OxygenREC-v2)
- EGR: Embedding-Native Generative Retrieval with a Shared LLM (EGR)
- Grevo: A Unified Generative Recommendation Framework with Evolutionary Item Indexing (Grevo)
- VaLiDRec: Variable-Length LLM-Aligned Semantic IDs for Generative Recommendation (VaLiDRec)
- TopoGR: Revealing and Preserving Latent Structure of Semantic ID in Generative Recommendation (TopoGR)
- The Case Against Generation for Retrieval: Discriminative Language Models as Effective Retrievers (Discriminative Retrieval)
- Multi-Decoder OneRec: Controllable Generative Retrieval for Multi-Objective Industrial Recommendation (Multi-Decoder OneRec)
- WhisperRec: Latent Reasoning for Efficient Foundation Recommendation Models (WhisperRec)
- PSG: Pair-Space Generation for Efficient Generative Reranking (PSG)
- DIRECTOR: Dynamic Index-based Recommendation with Transport-Optimized Retrieval (DIRECTOR)
- Feedback-Grounded Policy Discovery / Understanding-Action Gap -- Tianjin U / Kuaishou / HKUST(GZ)
- LoopMemGR / Closed-Loop Experience Memory -- Alibaba
- Restoring Collaborative Signals via Personalized NL -- JD.com / McGill
- HiLaR / Hierarchical Latent Reasoning -- XJTLU / Xiaohongshu / PKU / BJTU
- SPARC / Sequence-aware Progressive Attribute Routing -- Alibaba
- RGD / Reward Guided Decoding -- Kuaishou / CAS IIE
- LGRID / Generative Disentanglement for SID -- Kuaishou
- Intent-Driven SID Generation for News -- Tencent (ACL 2026)
- SID-MLP / Efficient Distilled GenRec -- UCSD / Snap
- TwiSTAR / Adaptive Reasoning -- Tsinghua
- IMFuse / Multi-Layer Fusion -- Zhejiang U
- Dual-purpose Semantic IDs / Dual-purpose SID -- YouTube / Google (RecSys 2026)
- UGR / Uncertainty-aware GenRec -- USTC (KDD 2026)
- RAGR / Review-Augmented GenRec -- Dalian / CityU / Huawei (TOIS 2026)
- PauseRec / Implicit Reasoning -- UVA / Snap
- Gryphon / Item-Level Scoring -- Yandex
- SnapLGR / LLM-Based GR -- Snap Inc.
- Think2Go / Generative POI Rec -- Dalian UT / KDD 2026 Oral
- EvoReason / Self-Evolving Latent Reasoning -- Kuaishou / Shenzhen U
- HRPO / Hierarchical Residual Policy Optimization -- CityU / Kuaishou / KDD 2026
- GRACE / Generative Recommender Acceleration Engine -- Meta
- OMEGA / Collaborative Memory Augmentation -- Renmin / ByteDance / KDD 2026
- LIME-Rec / Auditing Semantic Gains -- Hunan U
- SmartGR / Hierarchy-Aware KD for GR -- Zhejiang U
- UniR² / Unifying Genrec Recall + Ranking -- Kuaishou / CAS IIE
- DEGR / Dual Exploration Generative Re-Ranking -- JD.com / KDD 2026
- SIDReasoner / Reasoning over SIDs -- NUS / USTC / Tencent / KDD 2026
- CARD / Non-Uniform Quantization Visual SID -- UESTC / SWUFE / SIGIR 2026
- DIGER / Differentiable Semantic ID -- U Glasgow / Shandong / Amazon / SIGIR 2026
- S2GR / Stepwise Semantic-Guided Reasoning -- Kuaishou / KDD 2026
- Gryphon-v2 / Generate-and-Rank with Rollout Distillation -- Yandex
- UniGD / Unified Generative-Discriminative Framework -- Kuaishou
- PinRec / Unified Generative Retrieval for Pinterest -- Pinterest (KDD 2026)
- SA2CRQ / Adaptive Semantic Quantization -- JD.com / HIT / PKU / CAS IIE (SIGIR 2026)
- OneLive / Dynamically Unified Generative Live-Streaming -- Kuaishou
- DualGR / Long+Short Interest GR -- USTC / Kuaishou (WWW 2026)
- GRC / Generation-Reflection-Correction -- Alibaba / Wuhan U (KDD 2026)
- SID Staleness / Mitigating Collaborative SID Staleness -- ITMO / VK (SIGIR 2026)
- MDGR / Masked Diffusion GR -- Alibaba International
- MaskGR / Masked Diffusion GR -- Snap Inc.
- Progressive FM Post-Training -- Webtoon (RecSys 2026)
- HD-Rec / Generative Cross-Domain Rec -- CityU / Kuaishou
- SID Understanding / Item-Supported Decoding -- UIUC
- TM20K / 20K Sequence Modeling -- ByteDance
- Preserving Item Semantics for Free / Centroid SID Init -- Snap Inc. / UMich
- PushDualGen / LLM SID Push Rec -- Kuaishou
- Octen-WebGR: Scaling Generative Retrieval to 200 Million Web Pages (Octen-WebGR) — Octen, arXiv 2610.35256
- SLIDE: Search-to-List Item Distillation for Single-Rollout Generative Retrieval (SLIDE) — Alibaba (Taobao & Tmall Group), arXiv 2610.34764
- MetaStrategy / Generative LLM Ranking Strategy -- Alibaba (Taobao)
- TSPORec / Token Selection SeqRec -- ZJU / ByteDance
- IntHQ / Multi-Task Generative Rec -- Amap / Alibaba
- InforID / Adaptive SID Capacity Allocation -- UCAS / CASIA
- HCGRec / Hint-Conditioned GenRec -- SJTU / Huawei Noah's Ark Lab (CIKM 2026)
- Token-Level Credit Assignment / Generative Document Retrieval -- Shandong U
- DrIG / Dual-role Identifiers Multimodal Generative Retrieval -- U Tsukuba
- FlashTrie / GPU-Accelerated Constrained Beam Search -- Microsoft / Nvidia
- TGR / Tencent Generative Recommendation — Unified Generation and Reasoning (TGR)
- hLLM / Single Pass Decoding for Generative Reranking -- Meta
- WIDE / Wildcard Inference with Dynamic Expansion for Cross-Modal Generative Retrieval -- Jilin University
- TAAL / Mitigating Early Beam Pruning via Temporal Autoregressive Alignment -- Harbin Institute of Technology
- OneLA / Scaling Linear-Attention Decoding to Large Beams -- HKU / Kuaishou
- UniPolicy: Unified Objective-Specific Policies for Generative Search Advertising (UniPolicy) — Meituan

- MuSeR: Scalable Long-sequence Recommendation with Multi-interest Modeling (MuSeR) — Baidu / CityU HK / CUHK (hierarchical beam-search retrieval)

- Beyond the Beam: Constructive Repair and Candidate Completion for Generative Recommendation (Beyond the Beam) — Beijing Institute of Technology

- FLASH: Rethinking Semantic ID Construction for Generative Recommendation (FLASH) — U Illinois Chicago / NeurIPS 2026 (SimHash + parallel decoding)

- Beyond Semantic IDs: Finite-Beam Reachability and Continuous-Query Generation in Generative Recommendation (Beyond Semantic IDs) -- Yu Sun et al. (affiliation undisclosed on arXiv); arXiv 2610.12977 (continuous-query paradigms remove the SID finite-beam reachability constraint)

- Personalized LLM Recommendation with Semantic IDs: Autoregressive Beam Search vs. Multi-Token Prediction (Netflix SID Study) — Netflix, NeurIPS 2026 PALM Workshop
- Computed, not Memorized: Bit-Factorized Identifiers for Efficient Generative Retrieval (Bit-Factorized) — Leiden University / Radboud University
- Generative Recommenders Forget the Long Tail: Restoring Memorization in Retrieval and Ranking (CAPE) — University of Science and Technology of China & Ant Group, arXiv 2610.29298
- ReGen: Controllable Generative Recommendation via Guided Token Refinement (ReGen) — Xi'an Jiaotong-Liverpool University / University of Liverpool / The Hong Kong Polytechnic University, arXiv 2610.28642
- Separating Thinking from Spelling for Efficient Generative Recommendation (Deco) — Skolkovo Institute of Science and Technology / AIRI / HSE University, arXiv 2610.32980
- From Item Scores to Semantic Tokens: Test-Time Collaborative Adaptation for Generative Recommendation (TCBSA) — Tencent, arXiv 2610.32098

- PailitaoMMSearch2.0: Scaling Generative Retrieval to Unified End-to-End Multimodal Search (PailitaoMMSearch2.0) — Alibaba (Taobao), arXiv 2610.36958

- PFA: Attention Can Be Progressively Focused in Long-Sequence Generative Recommendation (PFA) — Zhejiang University / Alibaba Group, arXiv 2610.39273
- BEAR: Towards Beam-Search-Aware Optimization for Recommendation with Large Language Models (BEAR) — Zhejiang University / The Chinese University of Hong Kong, Shenzhen / Hangzhou City University, arXiv 2601.22925
- ZeroGR: Filtering-First Constrained Decoding for Generative Recommendation (ZeroGR) — The University of Hong Kong / Kuaishou / Peking University, arXiv 2611.04715
- Where Beam Search Loses Top-Ranked Items: First-Step Coverage in Generative Recommendation — Ant Group, arXiv 2611.01072
- Search-Aware On-Policy Self-Distillation with Sibling Alignment for Generative Recommendation (SA-OPSD) — Kuaishou Technology / University of Amsterdam / HUST, arXiv 2611.01568

### RL / Reinforcement Learning
- VARG: Value-Aware and Ranking-Aligned Generative Retrieval for Dynamic E-commerce Search (VARG) — Taobao & Tmall / USTC (Prefix-GRPO)
- Generate to Explore, Select to Exploit: Aligning LLM-based Headline Generation with Personalized Recommendation (GESE) — Baidu (GSPO)
- Safety as a Constraint: Fine-Tuning a LLM Recommender to Explain Itself — Netflix / UPenn (constrained GRPO)
- TATK: Triple-Aware Top-K Learning with Knowledge-Grounded Verification for LLM-based Sequential Recommendation (TATK) — ECUST / SIAT CAS (EMNLP 2026)
- EAGER: Enrich-and-Align Generative Query Recommendation from Clicked Items in E-commerce Search (EAGER) — Alibaba International
- Ask to Be Sure / Entropy-Reduction Reward for Multi-Turn LLM Rec — Amazon (CIKM 2026)
- ConnectionMind / Social Graph LLM Rec — Meta / MSU
- Efficient and Robust Online Learning to Rank in Decentralized Systems (RankGuard)
- Beyond Static Best-of-N: Bayesian List-wise Alignment for LLM-based Recommendation (BLADE)
- Bridging Passive and Active: Enhancing Conversation Starter Recommendation via Active Expression Modeling (PA-Bridge)
- Bringing Reasoning to Generative Recommendation Through the Lens of Cascaded Ranking (CARE)
- Adaptive Loss Balancing for Noise-Robust GRPO in Generative Recommendation (AdaGRPO)
- Causal Direct Preference Optimization for Distributionally Robust Generative Recommendation (CausalDPO)
- Diffusion-GR2: Diffusion Generative Reasoning Re-ranker (Diffusion-GR2)
- Don't Let Bandit Feedback Pull Continual LLM-Recommender Updates Off Target (ABPO)
- DynamicPO: Dynamic Preference Optimization for Recommendation
- Factorized Latent Reasoning for LLM-based Recommendation (FLR)
- Fairness Attacks on Recommender Systems
- Federated Variational Preference Alignment with Gumbel-Softmax Prior for Personalized User Preferences (FedVPA-GP)
- Affective Music Recommendation: A Rollout-Based World Model for Offline Preference Optimization (AMRS)
- Effective Reinforcement Learning for Agentic Search by Recycling Zero-Variance Queries During Training
- Generative Large-Scale Pre-trained Models for Automated Ad Bidding Optimization (GRAD)
- Generative Reasoning Re-ranker (GR2)
- Graph-GRPO: Dependency-Aware Credit Assignment for Generative E-commerce Search Relevance
- Harmonizing Semantic and Collaborative in LLMs: Reasoning-based Embedding Generator for Sequential Recommendation (ReaEmb)
- Taiji: Pareto Optimal Policy Optimization with Semantics-IDs Trade-off for Industrial LLM-Enhanced Recommendation (Taiji)
- MiniOneRec
- Mixture-of-Experts Knowledge Graph Retrieval-Augmented Generation for Multi-Agent LLM-based Recommendation (MixRAGRec)
- MuChator: Enabling Active Music Discovery via Conversational Music LLMs in Douyin Music
- Mult-DPO: Multinomial Direct Preference Optimization for Recommender Systems
- Unified Value Alignment for Generative Recommendation in Industrial Advertising (UniVA)
- Self-Distilled Reinforcement Learning for Co-Evolving Agentic Recommender Systems (CoARS)
- UniNote: A Unified Embedding Model for Multimodal Representation and Ranking
- Objective Shaping with Hard Negatives
- Once Generated, Ranked / End-to-End Generative Slate Recommendation (OGR) — Kuaishou
- OneMall
- OneBar: An End-to-End Content-Grounded Generative Query Recommendation Framework for E-Commerce Video Feeds (OneBar)
- OneRec-Think
- OneRec-V2
- OpenOneRec
- ProMax: Exploring the Potential of LLM-derived Profiles
- Rank-GRPO
- Reasoning over Semantic IDs Enhances Generative Recommendation (SIDReasoner)
- Rec-R1
- ReCast
- ReRec: Reasoning-Augmented LLM-based Recommendation Assistant
- RPORec: Reinforced Preference Optimization for Reasoning-Augmented Recommendations
- RSIR: Can Recommender Systems Teach Themselves? A Recursive Self-Improving Framework with Fidelity Control (RSIR)
- SCOReD: Student-Aware CoT Optimization for Recommendation Distillation (SCOReD)
- SAGER: Self-Evolving User Policy Skills for Recommendation Agent
- SAPO: Step-Aligned Policy Optimization for Reasoning-Based Generative Recommendation
- Expressiveness Limits of Autoregressive Semantic ID Generation in Generative Recommendation (Latte)
- Planning over Matrix-Factorization MDPs for Candidate Generation (MF-MDP Planning)
- ProRL: Effective Reinforcement Learning for Proactive Recommendation via Rectified Policy Gradient Estimation (ProRL)
- Mitigating Reward Hacking in LLM-based Recommendation: A Preference Optimization Approach (SIRIUS)
- Long-Term Optimization for Large-Scale Generative Retrieval with Off-Policy REINFORCE
- LBR: Towards Mitigating Length Bias in Large Language Models for Recommendation (LBR)
- DeGRe: Dense-supervised Generative Reranking for Recommendation (DeGRe)
- PauseRec: Implicit Reasoning for LLM-based Generative Recommendation (PauseRec)
- OneReason Technical Report (OneReason)
- AgentX: Towards Agent-Driven Self-Iteration of Industrial Recommender Systems (AgentX)
- Recommendation as Generation: Unifying Personalized Video Generation and Recommendation at Industrial Scale (RaG)
- GenRec: A Preference-Oriented Generative Framework for Large-Scale Recommendation (GenRec)
- LASAR: Latent Adaptive Semantic Aligned Reasoning for Generative Recommendation (LASAR)
- ManCAR: Manifold-Constrained Latent Reasoning with Adaptive Test-Time Computation for Sequential Recommendation (ManCAR)
- RankGR: Rank-Enhanced Generative Retrieval with Listwise Direct Preference Optimization in Recommendation (RankGR)
- OneBar: An End-to-End Content-Grounded Generative Query Recommendation Framework for E-Commerce Video Feeds (OneBar)
- RECAP: Feedback-Driven Streaming Semantic User Profiles for Short-Video Recommendation (RECAP)
- Long-History User Transformers for Real-Time Ad Ranking
- DLMRec: Diffusion Language Model for Recommendation (DLMRec)
- DREAM: Dynamic Refinement of Early Assignment Mappings (DREAM)
- SimGR: Escaping the Pitfalls of Generative Decoding in LLM-based Recommendation (SimGR)
- SSR-GRPO / Supervised Retrieval-GRPO with Semantic IDs -- Alibaba
- Think-to-Personalize / Reasoning + GRPO Personalized Dense Retrieval -- USTC / Meituan (CIKM 2026)
- STEPS / Self-Triggered Agentic Push -- ByteDance / PKU
- LaRec: Unleashing LLM-based Latent Reasoning for Generative Recommendation (LaRec)
- OxygenREC-v2: Internalizing Discrimination into Generative Recommendation (OxygenREC-v2)
- RecoReward: Recommender-Guided Multimodal Description Generation for Recommendation (RecoReward)
- Multi-Decoder OneRec: Controllable Generative Retrieval for Multi-Objective Industrial Recommendation (Multi-Decoder OneRec)
- WhisperRec: Latent Reasoning for Efficient Foundation Recommendation Models (WhisperRec)
- PSG: Pair-Space Generation for Efficient Generative Reranking (PSG)
- DIRECTOR: Dynamic Index-based Recommendation with Transport-Optimized Retrieval (DIRECTOR)
- Feedback-Grounded Policy Discovery / Understanding-Action Gap -- Tianjin U / Kuaishou / HKUST(GZ)
- HiLaR / Hierarchical Latent Reasoning -- XJTLU / Xiaohongshu / PKU / BJTU
- RGD / Reward Guided Decoding -- Kuaishou / CAS IIE
- TwiSTAR / Adaptive Reasoning -- Tsinghua
- UGR / Uncertainty-aware GenRec -- USTC (KDD 2026)
- UniR² / Unifying Genrec Recall + Ranking -- Kuaishou / CAS IIE
- PauseRec / Implicit Reasoning -- UVA / Snap
- Think2Go / Generative POI Rec -- Dalian UT / KDD 2026 Oral
- EvoReason / Self-Evolving Latent Reasoning -- Kuaishou / Shenzhen U
- GALA / Generative Aligned Multimodal -- Alibaba (ICDE 2026)
- RecHarness / Bandit Agentic Harness -- Kuaishou
- HRPO / Hierarchical Residual Policy Optimization -- CityU / Kuaishou / KDD 2026
- Exp-RSFT / Exponential Reward-Weighted Fine-Tuning -- Netflix
- DEGR / Dual Exploration Generative Re-Ranking -- JD.com / KDD 2026
- SIDReasoner / Reasoning over SIDs -- NUS / USTC / Tencent / KDD 2026
- S2GR / Stepwise Semantic-Guided Reasoning -- Kuaishou / KDD 2026
- Gryphon-v2 / Rollout Distillation GenRec -- Yandex
- UniGD / CAGE Gradient Coordination -- Kuaishou
- PinRec / Outcome-Conditioned Generation -- Pinterest (KDD 2026)
- OneLive / Multi-Objective Policy Optimization -- Kuaishou
- DualGR / Long+Short Interest GR -- USTC / Kuaishou (WWW 2026)
- GRC / Generation-Reflection-Correction GRPO -- Alibaba / Wuhan U (KDD 2026)
- Progressive FM Post-Training / Three-Phase RL Alignment -- Webtoon (RecSys 2026)
- MetaStrategy / Generative LLM Ranking Strategy -- Alibaba (Taobao)
- TSPORec / Token Selection SeqRec -- ZJU / ByteDance
- PushDualGen / LLM SID Push Rec -- Kuaishou
- HCGRec / Hint-Conditioned GenRec -- SJTU / Huawei Noah's Ark Lab (CIKM 2026)
- Token-Level Credit Assignment / Generative Document Retrieval -- Shandong U
- Gwhere / Generative Next-POI with EAKTO RL -- Amap / Alibaba
- TAGR / Temporally Adaptive Generative Recommendation (IOPO) -- Kuaishou / Tsinghua
- RecGPT-Mobile-V2 / On-Device Query Prediction with Reasoning-Cost RL -- Alibaba (Taobao)
- DCEO / Direct Causal Effect Optimization (actor-critic) for Long-Term User Value -- Alibaba (Taobao & Tmall)
- Astar / Self-Evolving Industrial AI Evolution-Direction Proposal (mid-training + SFT + RL) -- Alibaba (Lazada) / Zhejiang University
- DASO / Difficulty-Aware Semantic-ID Optimization (GRPO rollout-allocation) -- Meta / Penn State — [Also published on 2026-09-23]
- CoGR / It Takes Two to Match: Co-Evolving Generative Retriever with Reinforcement Learning -- UNC Chapel Hill / Apple
- WMG-RL / World Model-Guided Reinforcement Learning via Counterfactual User Engagement Simulation -- CUHK / ByteDance / Zhejiang University
- DMRL / Document-Mediated Reinforcement Learning for Skill Optimization in Advertising Recommendation -- SJTU / Kuaishou
- MemRetriever / Learning to Search, Reflect, and Retrieve from Long-Term Memory (GRPO) -- MemTensor
- Evo-Rec / 3-stage SID-alignment to Best-of-N SFT to ranking-aware GRPO -- Emory U / Microsoft / Cornell
- UniPolicy / Objective-Specific Multi-Policy Alignment with Multi-Policy Beam Search -- Meituan
- Personalized and Trust-Aware Health Recommendation Policies for a Construction Workplace (Trust-Aware Health Rec) — University of Illinois Urbana-Champaign (model-free RL)

- GRP / Snap's Generative Recommendation Paradigm - mGRPO reward-guided post-training, progressive E2E deployment (GRP) - Snap Inc.
- ReMem / Multi-memory GRPO for Long-Context Recommendation Agents (ReMem) - Hong Kong Polytechnic University / NTU
- KUAISHOU Explorer LLM-Rec Challenge 2026: Reasoning Generative Recommendation (OneRec-V2 / OneReason) — Kuaishou (SIGIR 2026 challenge; OneReason uses advanced RL to make CoT reasoning beneficial) — [arxiv](https://arxiv.org/abs/2609.39828)
- SPRINT: Single-Step Generative Recommendation via Average Probability Velocity (SPRINT) — University of Technology Sydney (single-pass SID generation)
- ReliGRec: Reliability-Oriented LLM-Based Generative Recommendation via User-Risk-Aware Prompt Routing (ReliGRec) — Central South University / Beihang / South China Univ. of Tech.

- Reinforcement Learning with Conformal Action Sets: An Application to Sequential Recommendation (RLCP) — University of Pennsylvania, arXiv 2610.08743

- DiffuReason: Bridging Latent Reasoning and Generative Refinement for Sequential Recommendation (DiffuReason) — Tencent (Think-then-Diffuse + GRPO), arXiv 2602.09744

- Personal-Agent Mediated Recommendation with Cross-Platform User History (MediateRec) — UC San Diego / Meta (PAMO policy-optimization mediation) — arXiv 2610.07588

- From Valid to Useful: Post-Verification Acquisition for Recursive Self-Improving Recommendation (DA-RSIR) -- Meta; arXiv 2610.04302 (BALD / MC-dropout post-verification acquisition for recursive self-improving rec)


- MLLMRec-R1: Incentivizing Reasoning Capability in LLMs for Multimodal Sequential Recommendation (MLLMRec-R1) — Hefei University of Technology (GRPO)
- SafeCRS: Personalized Safety Alignment for LLM-Based Conversational Recommender Systems (SafeCRS) — UIC / UIUC / Amazon, Safe-GDPO, KDD 2026
- RAR: Retrieval Augmented Conversational Recommendation with Reinforcement Learning (RAR) — UIUC / Google DeepMind / UC San Diego
- WeGR: Unified Generative Retrieval for Industrial Search Systems in WeChat (WeGR) — Tencent (WeChat), DHPO
- Personalized LLM Recommendation with Semantic IDs: Autoregressive Beam Search vs. Multi-Token Prediction (Netflix SID Study) — Netflix (RL post-training)

See [Full keyword index](docs/by_keyword.md) for all other categories.

- Many Right Answers, One Training Example / Removing Responder Noise from GRPO for LLM Recommenders (ReMaRk) — Nanyang Technological University
- SemPOI-RL: Aligning LLM Semantic Reasoning for Interpretable Out-of-Town POI Sequential Generation (SemPOI-RL) — Beihang University
- Reasoning Reranking with Semantic IDs as the Sole Item Representation (ReRankID) — Google / University of Toronto, arXiv 2610.22797
- RPSD: Retrieval-Privileged On-Policy Self-Distillation with Optimal Transport (RPSD) — Nagoya University / Shenzhen University / Sichuan Agricultural University / Guangdong Laboratory of AI and Digital Economy / Tongji University, arXiv 2610.37281
- IB-GRPO: Aligning LLM-based Learning Path Recommendation with Educational Objectives via Indicator-Based Group Relative Policy Optimization (IB-GRPO) — East China Normal University, arXiv 2601.14686
- Unified Generative Ranking for Heterogeneous E-commerce Recommendation (UGR-Hetero) — Alibaba Group, arXiv 2610.39426 (permutation preference optimization + candidate-aware autoregressive decoding)
- R2QRec: Learning Recommendation Queries from Retrieval Feedback — Kuaishou Technology / Hong Kong Baptist University, arXiv 2610.39984 (GRPO + RRF + LoRA)

- ReuseGR: Offline-Online Decoupled Generative Retrieval via Adaptive Prefix Reuse (ReuseGR) — Xidian University / Alibaba International, WWW 2027
- OneTrans-GSR: A Generative Slate Ranking Paradigm Unifying Reranking and Mix-Ranking with One Autoregressive Transformer (OneTrans-GSR) — ByteDance, arXiv 2611.04720

- What Gets Hacked in a Collaborative Reward for LLM Recommenders: The Part That Does Not Depend on the User (LLM4Rec-CF-Bias) — UC San Diego, arXiv 2611.07588 [opensource]
- Generative Search and Recommendation at Shopify (SID-LLM) — Shopify, arXiv 2611.08804 [RL improves judged search relevance]

## By Affiliation

See [Papers by Affiliation](docs/by_affiliation.md).

