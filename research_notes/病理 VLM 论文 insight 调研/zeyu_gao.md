# Zeyu Gao (University of Cambridge, computational pathology): pathology VLM / multimodal-LLM / foundation-model papers, 2023 – Nov 2026, with insight-centred notes

Source-access note for the report writer (applies to everything below):
- Full text actually read: ALPaCA (Nature Communications HTML, first ~100k chars + closing section; Supplementary Notes not accessible), SMMILe (Europe PMC open-access full text, PMC12727519, incl. Methods theorems), PathNavigate (arXiv HTML incl. appendix), PathCTM (arXiv HTML v4), CARE (arXiv HTML v3, first ~100k chars), TMEvolve (arXiv HTML, first ~100k chars; Appendix G limitations truncated).
- Not accessible: Google Scholar profile (not fetched; link taken from homepage), ScienceDirect review "From cells to patients" (HTTP 403), medRxiv full texts (403).
- Short quoted fragments are verbatim from the papers as returned by the fetch tool; longer statements are close paraphrase.

---

## 1. Who exactly is Zeyu Gao, and what is the full list of his relevant papers (title, venue, date, arXiv id, code, author position)?

### Takeaway
Zeyu Gao is a Research Associate / postdoc in the Department of Oncology, University of Cambridge (Crispin Lab of Mireia Crispin-Ortuzar; CRUK Cambridge Centre; Early Cancer Institute), PhD 2023 from Xi'an Jiaotong University under Chen Li and Deyu Meng; he remains tightly coupled to Chen Li's XJTU group, where he acts as (co-)corresponding/last author on most 2025–2026 papers. His verified first-author flagship works are **SMMILe** (Nature Cancer 2025) and **ALPaCA** (Nature Communications 2026); his verified senior-author VLM/agent/foundation-model works are **PathNavigate** (NeurIPS 2026), **PathCTM** (ICML 2026), **CARE** (CVPR 2026), **TMEvolve** (NeurIPS 2026) and **HAAF** (WWW 2026). **PathGen-1.6M, CPath-Omni and CaseScope are NOT his.**

### Cited Findings

**Identity**
- Position: Research Associate and postdoctoral researcher, Department of Oncology, University of Cambridge; affiliated with the Crispin Lab, the CRUK Cambridge Centre and the Early Cancer Institute; research supported by GE HealthCare. Postdoctoral Fellow of Trinity College Cambridge (2024–2026). — [Homepage](https://zeyugaoai.github.io)
- Education: PhD in Computer Science, Xi'an Jiaotong University, 2023 (supervisors Prof. Chen Li and Prof. Deyu Meng); MS (supervisor Xiangrong Zhang) and BS at Xidian University. — [Homepage](https://zeyugaoai.github.io)
- Stated interests: machine learning for whole-slide pathology, multimodal foundation models and spatial omics, "clinically relevant prediction from histopathology". — [Homepage](https://zeyugaoai.github.io)
- Links: email zg323@cam.ac.uk; Google Scholar https://scholar.google.com/citations?user=CeP6dkcAAAAJ ; ORCID 0000-0003-2365-8318; GitHub https://github.com/ZeyuGaoAi . — [Homepage](https://zeyugaoai.github.io)
- Funding/honours: CRUK Early Detection and Diagnosis Primer Award, PI, £100,000 (2026–2027) "for multimodal pathology foundation models"; Royal Society Research Grant 2025 (co-led, £30,000); EPSRC HPC project (40,000 GPU hours). — [Homepage](https://zeyugaoai.github.io)
- GitHub popular repos: SMMILe (33 stars), plus pre-2023 repos for IBViT, SSMTL, CHRNet, G2LContrast, HMIL-HIB. — [GitHub](https://github.com/ZeyuGaoAI)
- Recurring collaborators (from author lists): Chen Li (XJTU, PhD supervisor, co-corresponding on most papers), Mireia Crispin-Ortuzar (Cambridge, PI), Di Zhang, Jiashuai Liu, Jiusong Ge, Chunze Yang, Lei Wu, Yi Niu, Tieliang Gong (XJTU), Kai He and Mengling Feng (NUS), Ines P. Machado (Cambridge), Chengzu Li (Cambridge Language Technology Lab); on ALPaCA also Ming Y. Lu and Faisal Mahmood (Harvard). — [Publications page](https://zeyugaoai.github.io/publications/); [ALPaCA, Nat Commun](https://www.nature.com/articles/s41467-026-76372-z)
- Name-collision warning: the arXiv author-id page `gao_z_3` belongs to a condensed-matter physicist (Zhi-Qiang Gao), not this researcher; arXiv full-text search for "Zeyu Gao" + pathology returned nothing, so the homepage publication list is the authoritative source. — [arXiv a/gao_z_3](https://arxiv.org/a/gao_z_3)

**Relevant paper list, 2023 – Nov 2026** (homepage legend: `*` = corresponding author; all positions below are as listed on the homepage unless another source is given)

A. VLM / multimodal-LLM / agent / WSI-language (core to this survey)

| # | Paper | Venue / date | arXiv / DOI | Code | Gao's position |
|---|---|---|---|---|---|
| 1 | ALPaCA: Adapting Llama for Pathology Context Analysis to enable slide-level question answering | Nature Communications 17:9943, published 20 Aug 2026 (received 31 Mar 2025); medRxiv 22 Apr 2025 | DOI 10.1038/s41467-026-76372-z; medRxiv 10.1101/2025.04.22.25326190 (no arXiv) | github.com/ZeyuGaoAi/ALPaCA; weights huggingface.co/CNX-PathLLM/Llama-slideQA | **First author** (18 authors; corresponding: M. Feng, C. Li, M. Crispin-Ortuzar) |
| 2 | PathNavigate: A Training-Free Pathology Agent with Surprise-Guided Scan and Shared Slide Memory for Whole-Slide Image VQA | NeurIPS 2026 (accepted); arXiv 22 May 2026 | arXiv 2605.23559 | github.com/Pureeeee/PathNavigate_ | Penultimate author (Yang C … Wu X, **Gao Z**, Li C); no corresponding star on homepage |
| 3 | Thinking in Scales: Accelerating Gigapixel Pathology Image Analysis via Adaptive Continuous Reasoning (PathCTM) | ICML 2026 (accepted) | arXiv 2605.19491 | github.com/JSGe-AI/PathCTM | **Last author, co-corresponding** (with Qidong Liu, Chen Li) |
| 4 | HAAF: Hierarchical Adaptation and Alignment of Foundation Models for Few-Shot Pathology Anomaly Detection | WWW 2026 (accepted) | arXiv 2601.17405 | not listed | Corresponding (`*`), penultimate |
| 5 | TMEvolve: Modeling Whole-Slide Images as Dynamic Tumor Microenvironment Fields (text-concept-guided region evolution) | NeurIPS 2026 (accepted) | arXiv 2609.34451 | "in supplement" (no public URL found) | **Last author, co-corresponding** (with Chen Li) |
| 6 | From cells to patients: Multiscale computational pathology in the era of foundation models and vision-language systems (review) | Intelligent Oncology 2(3):100074, 2026 | ScienceDirect S2950261626000373 | – | **First author** |
| 7 | LLM-based reconstruction of longitudinal clinical trajectories in chronic liver disease (clinical-text LLM, not pathology imaging) | npj Precision Oncology, 2026 | nature.com/articles/s41698-026-01650-4 | – | Second author |

Sources: [Publications page](https://zeyugaoai.github.io/publications/); [ALPaCA](https://www.nature.com/articles/s41467-026-76372-z); [PathNavigate](https://arxiv.org/abs/2605.23559); [PathCTM](https://arxiv.org/abs/2605.19491); [TMEvolve](https://arxiv.org/abs/2609.34451)

B. Slide-level foundation models / weak supervision / spatial quantification (closely related)

| # | Paper | Venue / date | arXiv / DOI | Code | Gao's position |
|---|---|---|---|---|---|
| 8 | SMMILe enables accurate spatial quantification in digital pathology using multiple-instance learning | Nature Cancer 6(12):2025–2041, published 19 Nov 2025; medRxiv 26 Apr 2024 | DOI 10.1038/s43018-025-01060-8; PMC12727519 | github.com/ZeyuGaoAi/SMMILe | **First author** (Gao, Mao, Dong, Clayton, Wu, Liu, Wang, He, Gong, Li, Crispin-Ortuzar) |
| 9 | CARE: A Molecular-Guided Foundation Model with Adaptive Region Modeling for Whole Slide Image Analysis | CVPR 2026; arXiv 25 Feb 2026 | arXiv 2602.21637 | github.com/zdipath/CARE; huggingface.co/Zipper-1/CARE | **Last author, co-corresponding** (with Chen Li) |
| 10 | AGE-MIL: Anchor-Guided Evidence Learning for Patient-Level Prediction | MICCAI 2026 | arXiv 2606.12126 | github.com/wodeniua/AGE-MIL | Co-corresponding, penultimate |
| 11 | Learnable frozen feature augmentation for few-shot biomarker prediction from pathology WSIs (LFFA) | Bioinformatics 2026 (btag597) | – | github.com/zdipath/LFFA | Last author, co-corresponding |
| 12 | PH2ST: Prompt-Guided Hypergraph Learning for Spatial Transcriptomics Prediction in WSIs | Medical Image Analysis 2026:104008 | – | – | Last author, corresponding |
| 13 | MegaSeg: Towards Scalable Semantic Segmentation for Megapixel Images | Medical Image Analysis 2026:103933 | – | – | Co-corresponding |
| 14 | ProGIS: Prototype-Guided Interactive Segmentation for Pathological Images | IEEE TMI 2025 | – | – | Last author, corresponding |
| 15 | StaDis: Stability distance to detecting OOD data in computational pathology | Medical Image Analysis 2025:103774 | – | – | Co-corresponding |
| 16 | From patches to WSIs: A systematic review of deep MIL in computational pathology | Information Fusion 2025:103027 | – | – | **Co-first** (equal contribution with Zhang Y) |
| 17 | PAMIL: Prototype attention-based MIL for WSI classification | MICCAI 2024 | – | – | Last author, corresponding |
| 18 | Learning Heterogeneous Embedding with Prototype-Aware Graph Attention for WSI Classification | BIBM 2025 | – | – | Last author, corresponding |
| 19 | Childhood leukemia classification via information-bottleneck-enhanced hierarchical MIL | IEEE TMI 42(8), 2023 | – | github.com/ZeyuGaoAi/HMIL_HIB | First author |
| 20 | A semi-supervised multi-task learning framework for cancer classification with weak annotation in WSIs | Medical Image Analysis 83:102652, 2023 | – | github.com/ZeyuGaoAi/SSMTL_CancerClassification | First author |

Sources: [Publications page](https://zeyugaoai.github.io/publications/); [SMMILe, Europe PMC](https://europepmc.org/article/MED/41258398); [CARE](https://arxiv.org/abs/2602.21637); [GitHub](https://github.com/ZeyuGaoAI)

C. Checked and excluded (do not attribute to him)
- **PathGen-1.6M** (arXiv 2407.00203, ICLR 2025 oral): authors Yuxuan Sun, Yunlong Zhang, Yixuan Si, Chenglu Zhu, Zhongyi Shui, Kai Zhang, Jingxiong Li, Xingheng Lyu, Tao Lin, Lin Yang (Zhejiang/Westlake/OSU) — no Zeyu Gao. — [arXiv 2407.00203](https://arxiv.org/abs/2407.00203)
- **CPath-Omni** (arXiv 2412.12077): author list begins Yuxuan Sun, Yixuan Si, Chenglu Zhu, Xuan Gong, Kai Zhang, Pingyi Chen … (Westlake group); not on Gao's publication list. — [arXiv 2412.12077](https://arxiv.org/html/2412.12077v1); [Publications page](https://zeyugaoai.github.io/publications/)
- **CaseScope** (arXiv 2611.15325): authors are Wenchuan Zhang, Chengyang Zhang, Fengling Li … Yuhao Yi, Hong Bu (West China Hospital / Sichuan University); Zeyu Gao appears only in the reference list. A web-search summary wrongly suggested he was an author. — [arXiv 2611.15325](https://arxiv.org/html/2611.15325)
- **EviPathBench** (arXiv 2607.19261): the "Zeyu" there is Zeyu Liu, not Zeyu Gao. — [arXiv 2607.19261](https://arxiv.org/abs/2607.19261)
- Other 2026 homepage items outside scope (not VLM/foundation-model): PSMA PET/CT + mpMRI benchmark (npj Digital Medicine 2026, co-corresponding), CoxKAN (Bioinformatics 2025, co-corresponding), gastric-cancer annotated dataset (Scientific Data 2025). — [Publications page](https://zeyugaoai.github.io/publications/)

### Inferences
- His role shifted around 2025: first-author on the two "big journal" methodological papers (SMMILe, ALPaCA), then senior/corresponding author directing XJTU students (Di Zhang → CARE/LFFA/StaDis; Jiusong Ge → PathCTM/ProGIS; Chunze Yang → PathNavigate/HAAF; Lei Wu & Jiashuai Liu → TMEvolve/PAMIL; Yi Niu → PH2ST). The "Gao" research line is therefore best read as a Cambridge–XJTU joint lab output.
- The brief's guessed themes "CPath agents" → PathNavigate fits; "work on what pathology VLMs actually learn or where they fail" → I found no such paper by him. The closest are (a) SMMILe's theoretical critique of attention heatmaps and (b) ALPaCA's text-only/random-image controls (Supplementary Note 2, results not accessible).

### Gaps
- Google Scholar was not directly fetched; there may be 2026 preprints not yet on the homepage. The alphaXiv profile claims 81 papers but showed only 10, and probably merges several people named Zeyu Gao (it lists a non-pathology time-series paper and 11Plus-Bench, arXiv 2508.20068, whose visible authors do not include him) — treat 11Plus-Bench authorship as **unverified**. — [alphaXiv profile](https://www.alphaxiv.org/@zeyu-gao)
- The "From cells to patients" review (first-author, most likely his explicit statement of views on VLMs) could not be read (ScienceDirect 403); no arXiv version was found.
- HAAF, AGE-MIL, PH2ST, LFFA were not read in full; only bibliographic data is verified.
- PathNavigate author order differs slightly between the homepage (Yang C, Liu Q, Zhao W, …, Wu X, Gao Z, Li C) and the order returned from the arXiv HTML extraction; corresponding-author markers for that paper are unverified.

---

## 2. For each key paper: problem framing, motivating observation, central insight, and the method that follows

### Takeaway
Across six papers the framing is the same: prevailing WSI pipelines (attention-MIL, patch-level VLMs, flat patch→slide foundation models, question-first agents, exhaustive patch processing) ignore how a pathologist actually organises a slide — spatially, hierarchically, across magnifications, and "what is typical here first, what is asked second". Each paper turns one such observation into a structural prior of the model rather than into more data or a bigger backbone.

### Cited Findings

#### 2.1 SMMILe (Nature Cancer 2025; first author) — "attention maps are not measurements"
- Framing: modern MIL "can accurately predict whole-slide image labels, albeit at the expense of losing their spatial awareness"; the paper claims to "prove mathematically that a model using instance-level aggregation could achieve superior spatial quantification without compromising on whole-slide image prediction performance." — [SMMILe abstract, PMC12727519](https://europepmc.org/article/MED/41258398)
- What is wrong with prevailing practice: attention maps from representation-based MIL "can only be qualitatively interpreted through manual analysis"; "attention scores are not directly correlated with the slide-level labels and can be misled by confounding factors", which leads to "overfitting on irrelevant regions or only a subset of discriminative areas". Discussion: representation-based MIL "seems capable of achieving spatial quantification, [but] few works quantitatively assess their interpretability." — [SMMILe main text](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Central insight (two halves):
  1. Theorem 1: representation-based attention MIL (RAMIL) "is rigorously equivalent to a specialized variant of IAMIL, wherein aggregation is conducted at the logit level" — so the *only* real difference between the two families is whether the sigmoid is applied before or after attention aggregation. Theorems 2–3: because of the sigmoid's convex/concave shape, instance-based MIL (IAMIL) gives higher attention to highly discriminative instances and "markedly lower attention scores—often several times lower" to low/non-discriminative ones. Hence IAMIL = low false positives but low recall ("highly skewed attention maps"); RAMIL = diffuse attention with false positives. — [SMMILe Methods](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
  2. The paper explicitly "disproves some previous interpretations" of RAMIL's inaccurate attention: it is not due to "conflicting instance contributions or interactions at the classification stage"; bag logits decompose exactly into instance contributions, but "the properties of the output activation function result in a diminished contribution of these attention scores to the bag-level prediction score", so "the loss constraint provides limited guidance for attention score allocation". — [SMMILe Methods](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Method that follows: start from IAMIL (the right side of the precision/recall trade-off for localisation) and add modules that each repair its diagnosed recall deficit: NIC-style compressed WSI + convolution (local receptive field); superpatches (over-segmentation); consistency constraint (for datasets with normal slides); parameter-free instance dropout (drop the most discriminative instances so less discriminative positives must carry the label); delocalised instance sampling (one instance per superpatch into sub-bags); an instance refinement network self-trained on pseudo-labels with an MRF smoothness energy, which learns "a unified decision boundary across different WSIs". Extended to multilabel bags (mixed histotypes, Gleason patterns). — [SMMILe Results/Discussion](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)

#### 2.2 ALPaCA (Nature Communications 2026; first author) — "slide-level QA is an adaptor (compression) problem, and one adaptor is not enough"
- Framing: "most pathology LVLMs analyse small regions of interest rather than pyramidal, gigapixel-scale whole-slide images (WSIs)"; the patch-LVLM recipe (frozen encoder + linear adaptor) "is restricted to region-of-interest (ROI) analysis, focusing on small, predefined areas in isolation", whereas diagnosis integrates sub-regions and magnifications. — [ALPaCA](https://www.nature.com/articles/s41467-026-76372-z)
- What is wrong with existing slide-level models: vision foundation models — "most of these models disregard textual pathology knowledge" and need task-specific heads; PRISM, PathAlign and the multimodal whole-slide foundation model "lack integration with powerful LLMs and focus on generating simple slide descriptions"; WSI-VQA and SlideChat "support tumour-focused question-answering" only. — [ALPaCA Introduction](https://www.nature.com/articles/s41467-026-76372-z)
- Central insight: the crux is how tens of thousands of multi-magnification patch embeddings are compressed into a few dozen LLM tokens. A *vision-only* prototype summary and a *question-conditioned* summary carry different information: "GMM effectively captures global visual information for addressing coarse-grained questions", while a vision-text interactive adaptor extracts question-specific local detail; summing both (ALPaCA-Hybrid) is best. Discussion: "connecting a foundation pathology vision encoder with an LLM via specialised adaptors enables effective slide-level QA". — [ALPaCA Results/Discussion](https://www.nature.com/articles/s41467-026-76372-z)
- Method: frozen CONCH patch features at three pseudo-magnifications (patch sizes 1024/2048/4096 px at 40× resized to 224, mimicking 40×/20×/10×); six adaptors compared systematically (Sampling, KMeans, GMM, ABMIL = vision-only; QFormer, LongFormer = vision-text interactive; LongFormer is a two-layer LongNet with dilated sparse attention); each yields 32/16/8 tokens for 40×/20×/10×; Llama-3.1-8B; three training stages (caption comprehension with LLM frozen → instruction tuning on 341,051 QA → disease-specific specialisation). — [ALPaCA Methods](https://www.nature.com/articles/s41467-026-76372-z)
- Data idea: 35,913 WSIs from TCGA (32 studies) **and GTEx normal tissue (40 sites)** — deliberately including non-tumour tissue, which earlier tumour-only slide VLMs lacked; QA generated by GPT-4o from pathologist-designed prompts. — [ALPaCA Methods](https://www.nature.com/articles/s41467-026-76372-z)

#### 2.3 PathNavigate (NeurIPS 2026; senior author) — "scan before you search: establish what is typical for this slide first"
- Framing: "training-free pathology agents avoid this cost by keeping core models frozen, but often follow a question-first design"; "This can miss decisive morphology that is not named in the question, and force heavier inference-time scaffolding." "A query-dependent scan can therefore retrieve generally relevant tumor regions while missing decisive morphology." — [PathNavigate abstract/intro](https://arxiv.org/html/2605.23559)
- Motivating observation: "pathologists usually scan a slide broadly to establish what is typical in the current case before searching for the finding most relevant to the question." — [PathNavigate intro](https://arxiv.org/html/2605.23559)
- Central insight: region proposal should be driven by a **slide-specific content prior** (what is atypical *relative to this slide*), with the question used only to rerank; and the same state that guides navigation should be exposed to the answerer, so no second memory store or long trajectory is needed. — [PathNavigate](https://arxiv.org/html/2605.23559)
- Method (scan–search–readout, all models frozen): a fresh two-layer reconstruction MLP per slide over CONCH tile features; "surprise" = gradient norm of the reconstruction (Huber) loss measured before the tile updates the memory; tiles above μ+λs trigger an update; thresholding + distance-NMS gives a diverse ROI pool; PLIP image–text similarity only reranks within the pool (fused score α·PLIP + (1−α)·surprise, α=0.5); high-magnification readout by a pathology MLLM perceptor (Patho-R1-7B) and adjudication by Qwen3.5-4B, which receives a short "Navigation Summary" of the surprise statistics. — [PathNavigate method](https://arxiv.org/html/2605.23559)

#### 2.4 PathCTM "Thinking in Scales" (ICML 2026; senior/corresponding) — "more thinking on the same pixels cannot add missing detail; reasoning must move across magnification"
- Framing: "such exhaustive patch-level processing is computationally expensive, severely limiting the efficiency and scalability of WSI analysis"; prior acceleration methods "often rely on fine-grained annotations or rigid cascade structures". — [PathCTM](https://arxiv.org/html/2605.19491)
- Motivating observation: the Continuous Thought Machine premise that "extending thinking time on a fixed tensor enables deeper information extraction" fails for WSIs, because a low-resolution view does not contain cellular detail no matter how long one "thinks"; the authors call the mismatch with the pathologist's coarse-to-fine workflow a "Reasoning Gap". — [PathCTM intro](https://arxiv.org/html/2605.19491)
- Central insight: diagnosis = sequential information pursuit across scales; "thinking in time" must be coupled to "thinking in scales", with the decision to zoom driven by the model's own uncertainty and attention, and stopping as soon as it is confident. — [PathCTM](https://arxiv.org/html/2605.19491)
- Method: CTM-style latent recurrence at low magnification → if confidence (1 − normalised entropy) < δ after n steps, take attention from the most confident step, keep top-K regions, re-encode only those at the next magnification (O(N)→O(K)), fuse fine-scale state with the most confident coarse-scale output; early stop when confidence ≥ δ; loss averaged over the min-loss and max-confidence step per scale. — [PathCTM method](https://arxiv.org/html/2605.19491)

#### 2.5 CARE (CVPR 2026; senior/co-corresponding) — "slide foundation models lack an ROI concept; regions are the missing 'words'"
- Framing: "existing models overlook the heterogeneous and non-uniform organization of regions of interest (ROIs)"; "they fail to capture the coherent tissue architecture beyond patches"; "typical foundation models lack an explicit ROI concept". — [CARE](https://arxiv.org/html/2602.21637)
- Motivating analogy: patches are like character-level tokens (fine-grained but myopic); regular grid regions are like fixed-length chunking — "broader yet prone to semantic misalignment". Direct patch→WSI aggregation forces long-range interactions among thousands of patches, which is hard to learn and data-hungry. — [CARE intro](https://arxiv.org/html/2602.21637)
- Central insight: a patch→**adaptive region**→WSI hierarchy, with regions shaped by morphology and semantically grounded by molecular profiles (RNA, protein), is a better-matched tokenisation of tissue and therefore far more data-efficient than scaling slide counts. — [CARE](https://arxiv.org/html/2602.21637)
- Method: on frozen CONCH v1.5 features, an Adaptive Region Generator assigns each patch to one of its top-3 candidate sub-regions by feature similarity × soft spatial inclusion; attention is computed within regions (ARSA); a Region Structuring Loss stops collapse to the nearest grid cell; a Semantic-and-Prior Fusion pools regions and designates the top-weighted region as "the ROI". Two-stage pretraining: iBOT on 34,277 WSIs (11,463 TCGA + 22,814 GTEx), then CLIP-style alignment to RNA (13,289 pairs, scGPT-initialised encoder) and then protein (8,225 pairs, ESM-2-initialised). — [CARE method](https://arxiv.org/html/2602.21637)

#### 2.6 TMEvolve (NeurIPS 2026; senior/co-corresponding) — "a slide is a field, not a bag; regions should form and interact"
- Framing: "most existing WSI-level models still lack an explicit mechanism to organize patches into tissue-level structures"; MIL "treats a WSI as a static collection of weakly related instances"; "fixed grids, heuristic partitions, or static neighborhoods may cut across natural tissue boundaries". — [TMEvolve](https://arxiv.org/html/2609.34451)
- Central insight: "A WSI can be regarded as a spatial tissue field whose latent state varies over tissue coordinates." Homogeneous tissue should be smoothed (diffusion); heterogeneous interfaces (tumour–stroma, tumour–immune) need directional, concept-guided exchange (flux + reaction) — a reaction–diffusion view in which text-encoded pathology concepts act as the source term. — [TMEvolve](https://arxiv.org/html/2609.34451)
- Method: soft adaptive regions (farthest-point seeds, feature + spatial similarity) → intra-region diffusion with membership-overlap edge weights → LLM-generated, pathologist-reviewed concept descriptions embedded by a text encoder (Qwen3-Embedding-8B) anchor each region → boundary conductivity from heterogeneity and concept-response contrast → iterative "pseudo-time" updates with regions re-estimated each step → gated-attention pooling. The paper states pseudo-time denotes iterative refinement, not disease progression, and that the PDE is not actually solved but used as the structure of a learnable message-passing process. — [TMEvolve method/appendix](https://arxiv.org/html/2609.34451)

### Inferences
- Why each "sounds right" (my reading):
  - SMMILe: it converts a vague community suspicion ("attention ≠ explanation") into a one-line structural cause (where the sigmoid sits) that predicts *both* failure modes (RAMIL false positives, IAMIL low recall) and tells you which side to start from and what to fix. A critique with a mechanism is much more persuasive than a new architecture.
  - ALPaCA: the coarse-vs-fine question dichotomy maps onto how pathologists use low vs high power, so "global prototype tokens + question-conditioned tokens" reads as the minimal sufficient representation rather than an ad-hoc ensemble.
  - PathNavigate: questions rarely name the decisive morphology (a question about subtype does not say "look for the comedo necrosis"), so text–image retrieval is structurally blind to it; novelty relative to the slide's own background is a question-independent proxy for "diagnostically unusual".
  - PathCTM: the argument is information-theoretic in spirit — computation cannot substitute for resolution — and yields a natural stopping rule.
  - CARE: the NLP tokenisation analogy (characters / fixed chunks / semantic units) makes "adaptive region" feel like the obviously missing level, and the 10×-less-data result is the kind of evidence that an inductive bias, not scale, is doing the work.
  - TMEvolve: pathologists' prognostic reasoning is about interfaces (invasion front, immune infiltration), which a bag model cannot express; treating boundaries as the place where information flows operationalises that.
- A shared rhetorical template: (i) name what the pathologist does; (ii) show the dominant pipeline structurally cannot do it; (iii) add exactly the missing structure; (iv) report efficiency (data, tokens, patches) as the main proof.

### Gaps
- ALPaCA's Introduction, as extracted, does not discuss hallucination, language priors or text-only shortcuts; those controls are in Supplementary Note 2, which I could not access.
- For PathNavigate the paper gives no mechanistic explanation of *why* reconstruction-gradient surprise should correlate with diagnostic relevance (as opposed to artefacts, folds, pen marks); it is asserted via the pathologist analogy and supported only by ablation.

---

## 3. What evidence supports each insight (analyses, ablations, surprising findings, key numbers)?

### Takeaway
The strongest evidence is in SMMILe (theorems + synthetic experiment + 8 datasets with held-out spatial annotations + pathologist re-review of contested patches) and ALPaCA (six-adaptor comparison, external cohorts, pathologist re-scoring that overturns the LLM judge). The 2026 conference papers support their insights mostly with "structure beats scale/cost" numbers: CARE with ~1/10 of TITAN's slides, PathCTM with ~96% fewer patches, PathNavigate with frozen models beating supervised slide MLLMs; their ablation margins are real but sometimes small.

### Cited Findings

**SMMILe**
- Scale: 6 cancer types, 3 task types (binary, multiclass, multilabel), 8 datasets, 3,850 WSIs; 9 baselines; two encoders (ImageNet ResNet-50 and CONCH); spatial annotations used only for evaluation. — [SMMILe abstract](https://europepmc.org/article/MED/41258398)
- Synthetic experiment confirming the theorems: IAMIL assigned negative instances attention "mostly below 0.002, whereas RAMIL often assigned scores above 0.01"; IAMIL's scores on highly discriminative instances were "often twice as high". — [SMMILe Results](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Key surprising finding — foundation encoders do not fix localisation: with CONCH most methods exceed 97% slide-level AUC, yet existing methods' "spatial quantification capabilities are inadequate for clinical applications and downstream analysis, even when integrated with powerful pathology foundation models." The foundation encoder raises spatial *precision* of baselines to SMMILe's level but "does not yield similar improvements in spatial recall"; SMMILe beats CLAM and DTFD-MIL by 5–15% and 9–40% in spatial recall. — [SMMILe Results/Discussion](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Metric critique: "AUC alone is insufficient to determine the real spatial quantification performance" because baselines need "WSI-specific optimal thresholds"; with CONCH SMMILe gains 3–6% spatial AUC over the top-4 but 5–20% spatial F1 and 7–20% spatial accuracy. On Camelyon16 SMMILe beats DSMIL by ~1% spatial AUC but 23.56% spatial F1 (ResNet-50). — [SMMILe Results](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Honest exceptions: on Camelyon16 with CONCH, DSMIL/RAMIL/CLAM are comparable, explained by tiny tumour fractions making missed detection less of an issue; with CONCH "SMMILe did not perform best on every dataset" for slide classification. — [SMMILe Results](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Ablations: instance refinement adds 3–6% spatial AUC (ResNet-50) and >20% spatial F1 on Prostate; removing instance dropout or delocalised sampling costs ~17% spatial F1 on Prostate (ResNet-50); modules matter little for slide AUC, a lot for spatial F1. — [SMMILe ablation](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Annotation-precision check: an experienced pathologist reviewed "contentious patches" (SMMILe right, three runner-ups wrong): only 2/42 (lung) and 2/37 (gastric) had ambiguous labels, so wins are not annotation artefacts. — [SMMILe Results](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)

**ALPaCA**
- Adaptor comparison on 337 hold-out slides: close-ended accuracy (n=2,403) best for Hybrid at 91.76%; Sampling and KMeans below 90%; LongFormer best on open-ended lexical metrics (F1 59.82%, CIDEr 2.55); Hybrid best by GPT-4o judge (70.67% totally+partially correct vs 66–67% for GMM or LongFormer alone). — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- Non-tumour vs tumour: tumour MC 91.20%, tumour TF 89.05%, non-tumour MC 96.60%, non-tumour TF 92.80%; 24/28 TCGA projects and 36/40 GTEx sites above 85%. — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- Difficulty, not data volume: variability tracked question difficulty rather than training-set size; hardest categories were grading/staging, invasion and tumour microenvironment. — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- Versus general LVLMs and SlideChat: general models (Gemini-2.0, GPT-4o, QwenVL-Plus, MedGemma-4B) did better with 32 representative patches than with thumbnails; Hybrid led the strongest general model (Gemini-2.0) by 28.21 points close-ended; SlideChat was competitive on TCGA tumours "but dropped sharply on GTEx" (tumour-only training). — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- External cohorts without clinical context: XJTU-RG (renal + gastric, 20 patients) 82% close-ended vs 49% for the best baseline (SlideChat), open-ended 75/97 vs 47/97; CUH-OV (ovarian, 10 patients) 77.22%. — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- Evaluation finding: pathologist review of all 1,641 open-ended answers upgraded many answers the GPT-4o judge marked incorrect (less granular but correct subtype; guideline changes); the judge tended to mark unanswerable tumour questions as incorrect rather than indeterminate; expert–judge agreement was higher for GTEx than TCGA. — [ALPaCA Results](https://www.nature.com/articles/s41467-026-76372-z)
- Label-noise findings: QC on 40 cases found ~5% of captions with hallucination (mostly plausible inferences), ~98% of QA answers correct but only ~88% answerable from the slide; a "necrosis absent" label contradicted by the model was confirmed by pathologists to be the model's win (small necrosis present). — [ALPaCA Methods/Results](https://www.nature.com/articles/s41467-026-76372-z)
- Cost: ~634 GPU-h for the instruction stage on two 80 GB A100s; inference 0.22 s per question on cached features, ~37–38 GB. — [ALPaCA Methods](https://www.nature.com/articles/s41467-026-76372-z)

**PathNavigate**
- Frozen-model agent vs trained slide MLLMs on SlideBench-BCNB (7,274 MCQ): PathNavigate 59.42 vs PathAgent 55.72, SlideChat 54.07, WSI-LLaVA 52.68, GPT-5.4 45.85. Not best everywhere: SlideChat leads Tumor (89.90 vs 88.28) and PR; PathAgent leads Grading (55.95 vs 52.58). — [PathNavigate Table 1](https://arxiv.org/html/2605.23559)
- WSI-VQA (735 TCGA-BRCA questions): Total 56.34 (MCQ 52.21, Open 61.00) vs PathAgent controlled rerun 33.88 (MCQ 51.54, Open 13.91). The gain is almost entirely on open-ended questions (+47.09) while MCQ is +0.67. — [PathNavigate Table 2 / appendix](https://arxiv.org/html/2605.23559)
- The proposal step is the failure point: Random ROI −6.84 Total; PLIP-only (question-first, no surprise) 52.20 vs surprise-only 53.42 vs fused 56.34; on BCNB a random pool costs 5.26 Total and 12.38 on Grading, a PLIP-built pool costs 1.81 Total and 7.98 on Grading. — [PathNavigate Tables 3, 10, 11](https://arxiv.org/html/2605.23559)
- Cost: ~17K tokens per question vs ~30K for PathAgent at similar latency. — [PathNavigate appendix Table 12](https://arxiv.org/html/2605.23559)
- Documented negative results: consolidating only low-surprise ("normal") tissue gave no reliable gain; prepending the full episodic trace to the adjudicator lengthened prompts without accuracy gain; a single adjudication pass matched or beat multi-round variants; free-text perceptor evidence matched or beat strict JSON. — [PathNavigate appendix C.6](https://arxiv.org/html/2605.23559)

**PathCTM**
- BRACS-3 with CONCH: AUC 93.1 using 183 patches in 5.34 s vs CLAM 92.0 using 2,606 patches in 74.43 s; with UNI: 93.6 / 349 patches / 7.95 s vs CLAM 92.0 / 9,484 / 210.15 s. Best in 7 of 8 task×encoder settings (ABMIL slightly ahead on SETD2 mutation with CONCH: 74.2 vs 73.9). Homepage headline: ~96% reduction in patch usage and inference time. — [PathCTM Table 1](https://arxiv.org/html/2605.19491); [Homepage](https://zeyugaoai.github.io)
- Beats slide-level foundation models CHIEF, GigaPath, PRISM, TITAN on AUC in all four tasks at ~5–7 s vs ~20–280 s. — [PathCTM Table 2](https://arxiv.org/html/2605.19491)
- Adaptive depth matches task semantics: subtype/BRACS-3 cases often stop at coarse scales, while RCC staging and mutation prediction mostly go to the highest magnification — i.e., the model "decides" that molecular/staging questions need cells. — [PathCTM Sec. 4.2–4.3](https://arxiv.org/html/2605.19491)
- Ablation (BRACS-3): pruning alone cuts 3,529→246 patches with ACC 78.32→76.28; multi-scale fusion restores ACC to 78.31; early stopping cuts to 183 patches with unchanged ACC. — [PathCTM Table 3](https://arxiv.org/html/2605.19491)

**CARE**
- Data efficiency: 34,277 pretraining WSIs, ~18.8M parameters, versus TITAN 335,645 WSIs, PRISM 587,196, GigaPath 171,189. Across 33 tasks (9 datasets): LR-probe morphology 85.7 (TITAN 85.4), molecular 69.5 (TITAN 67.8), survival C-index 58.0 (PRISM 54.3). — [CARE Table 1](https://arxiv.org/html/2602.21637)
- Not uniformly best: TITAN leads kNN morphology (83.1 vs 82.3) and fine-tuned morphology (87.7 vs 87.0); TANGLE leads fine-tuned molecular (75.6 vs 74.7). — [CARE Table 1](https://arxiv.org/html/2602.21637)
- ROI-vs-slide evidence: the single top-weighted region embedding beats the whole-slide embedding on CCRCC-BAP1 (ACC 61.0 vs 58.7), HNSCC-CASP8 (53.7 vs 51.7) and cross-cohort lung subtyping (AUC 81.2 vs 77.0), but not on all tasks. — [CARE Table 2](https://arxiv.org/html/2602.21637)
- Adaptive vs fixed regions: fixed sub-regions lower EBRAINS-fine ACC 72.5→71.6 and BCNB-HER2 ACC 64.8→61.4; the rank target E*=0 (≈ fixed grid) and E*=2 (farthest candidate) both hurt. — [CARE Tables 3–4](https://arxiv.org/html/2602.21637)
- Molecular stage: EBRAINS-fine ACC 72.2 (iBOT) → 73.7 (+RNA) → 74.0 (+protein); on BCNB-HER2 the RNA stage does not help (60.3 → 59.7 → 59.8). — [CARE Table 5](https://arxiv.org/html/2602.21637)

**TMEvolve**
- Survival C-index: LUAD 69.5 (next 66.8), BLCA 65.9 (TITAN 63.0), private gallbladder cohort 77.4 (VLSA 76.1), BRCA 70.3 (ProtoSurv 70.4). Subtyping: BRACS-fine AUC 89.4 / ACC 65.4 (best), EBRAINS-fine AUC 98.8 (best) but ACC 79.0 < TITAN 79.2. — [TMEvolve Tables 1–2](https://arxiv.org/html/2609.34451)
- Semantic-prior control: replacing pathology concepts with random concepts drops LUAD C-index 0.6952→0.6728; removing pseudo-time evolution drops BLCA 0.6589→0.6421. — [TMEvolve Table 3](https://arxiv.org/html/2609.34451)
- Light model: 5.18M parameters, 6.48 ms per slide on pre-extracted features. — [TMEvolve Table 8](https://arxiv.org/html/2609.34451)

### Inferences
- The evidence style is consistent: (a) a *control that isolates the claimed mechanism* (synthetic bags in SMMILe; random-ROI / PLIP-only pools in PathNavigate; random concepts in TMEvolve; fixed-vs-adaptive regions in CARE; six adaptors in ALPaCA) and (b) an *efficiency headline* that makes the inductive-bias claim concrete.
- The most transferable empirical lessons for pathology VLM work: (1) slide-level accuracy saturates with foundation encoders while spatial recall does not (SMMILe) — heatmap-based "grounding" in slide VLMs inherits this problem; (2) tumour-only training data make slide VLMs brittle on normal tissue (ALPaCA vs SlideChat on GTEx); (3) LLM judges systematically under-score pathologically acceptable answers and mishandle unanswerable questions (ALPaCA); (4) in agents, *where to look first* dominates everything downstream, and question-conditioned retrieval is a worse first step than question-agnostic novelty (PathNavigate); (5) less scaffolding (single pass, free text, no trace memory) was as good or better (PathNavigate negatives).
- PathNavigate's gain concentrated in open-ended questions (+47 points) with near-zero MCQ gain suggests part of the benefit may come from answer-format/readout behaviour of the controlled PathAgent rerun rather than navigation alone; the ablations (2–7 points) are the more trustworthy size of the navigation effect.

### Gaps
- ALPaCA text-only and random-image baseline numbers, alternative-encoder results (UNI, MUSK, PathGen-CLIP), attention visualisations and low- vs high-power question analysis are in Supplementary Notes 1–4 and were not retrievable. No comparison with WSI-LLaVA appears in the main text I read.
- No OpenReview reviews were retrieved for the NeurIPS/ICML/CVPR 2026 papers; the Nature Communications peer-review file exists (reviewer Ruijiang Li, co-reviewed with Yijiang Chen) but was not read. — [ALPaCA](https://www.nature.com/articles/s41467-026-76372-z)
- PathCTM's headline 95.95% / 95.62% reductions could not be reconciled exactly with a single table row from the text retrieved (per-setting reductions range ≈93–96%).

---

## 4. Limitations, unstated assumptions, and open questions each paper leaves

### Takeaway
The stated limitations cluster around supervision granularity (slide- vs patient-level labels, no region grounding in ALPaCA), H&E's information ceiling (PathNavigate, HER2/IHC-like labels), and narrow task coverage (SMMILe on classical tasks only). The unstated ones are that "pathologist-like" structure is validated by downstream metrics rather than against pathologist behaviour, and that everything sits on frozen CONCH features.

### Cited Findings

**SMMILe**
- Stated: evaluation "remains focused on traditional computational pathology tasks owing to dataset availability"; spatial quantification of IHC or genomic biomarkers from H&E is left as future work to be validated with IHC images or spatial sequencing. — [SMMILe Discussion](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- Stated: results depend on patch size and patch-label criteria (any tumour cell → tumour for binary/multiclass; dominant category for multilabel), which "require further standardization". — [SMMILe Discussion](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)
- The theory rests on explicit idealisations: Assumption 1 (both models share encoder and linear projection) and Assumption 2 (identical bag predictions and equal loss gradients for the two attention networks). — [SMMILe Methods](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/)

**ALPaCA**
- Stated: limited data for rare tumours and real-world non-tumour tissue; TCGA/GTEx may not reflect clinical diversity (GTEx is largely post-mortem donor tissue). — [ALPaCA Discussion](https://www.nature.com/articles/s41467-026-76372-z)
- Stated: patient-level reports mismatched to single slides — "some generated questions cannot be reliably answered using a single WSI" (only ~88% of QA judged answerable from the slide). — [ALPaCA Discussion/Methods](https://www.nature.com/articles/s41467-026-76372-z)
- Stated: "ALPaCA does not incorporate explicit spatial grounding or region-level supervision"; training is instruction tuning only, with no preference-based or RL optimisation for consistency or uncertainty handling; larger drop on the external ovarian cohort. — [ALPaCA Discussion](https://www.nature.com/articles/s41467-026-76372-z)
- Stated future work: multi-slide / patient-level reasoning; detection, segmentation or region-aware supervision for traceability; swapping encoder/LLM (modular design). — [ALPaCA Discussion](https://www.nature.com/articles/s41467-026-76372-z)

**PathNavigate**
- Stated: labels depending on IHC-like or diffuse grading cues remain hard; better navigation "cannot fully substitute for missing modality evidence"; "H&E-weak labels motivate richer modality-aware evidence for future training-free agents". Efficiency claims are limited to tokens/storage, not peak GPU memory. — [PathNavigate](https://arxiv.org/html/2605.23559)
- Molecular subtype accuracy on BCNB is only 32.33 and HER2 48.40. — [PathNavigate Table 1](https://arxiv.org/html/2605.23559)

**PathCTM**
- No dedicated limitations section; the impact statement says "further validation on diverse clinical datasets is required before deployment". Evaluated on four classification tasks from three public datasets; the two propositions (attention as influence; Fano-based error floor) are informal motivations. — [PathCTM](https://arxiv.org/html/2605.19491)
- Early stopping slightly lowers AUC (93.59 → 93.10 on BRACS-3). — [PathCTM Table 3](https://arxiv.org/html/2605.19491)

**CARE**
- Gains are mixed across probes (see Table 1 exceptions above); the RNA/protein stage gives little on some tasks (BCNB-HER2); ROI features do not uniformly beat slide features; the authors caution that tumour-vs-normal heatmap contrast alone does not guarantee clinical relevance. — [CARE](https://arxiv.org/html/2602.21637)

**TMEvolve**
- The reaction–diffusion PDE is not solved; pseudo-time is iterative refinement, not disease progression; concept banks are GPT-5-generated then pathologist-reviewed; one survival cohort is private; no public code URL in the text. — [TMEvolve](https://arxiv.org/html/2609.34451)
- Many ablation differences are within fold standard deviations (e.g., BLCA std ≈ 0.05–0.06). — [TMEvolve Table 3](https://arxiv.org/html/2609.34451)

### Inferences
- Unstated assumption common to all six: frozen CONCH / CONCH v1.5 patch features are an adequate substrate; none of the papers asks what the patch encoder fails to encode (stain, rare morphology, artefacts). The "structure" contributions are all above the patch encoder.
- SMMILe: assumes the bag label's discriminative evidence is patch-local and that patch-level correctness is the right notion of "quantification"; diffuse or architecture-level signals (e.g., growth pattern across many patches, molecular status) may not have a patch-level ground truth at all — exactly the regime the authors defer.
- ALPaCA: QA is LLM-generated from reports, so the benchmark partly tests agreement with report language; compressing a slide into 32/16/8 tokens presumes most questions are answerable from a summary — the lack of grounding means a correct answer cannot be traced to tissue. This is the gap PathNavigate (evidence acquisition) and CARE (explicit ROI) later address from other directions.
- PathNavigate: "surprise" is statistical atypicality within the slide; it should fail when the diagnostic tissue is the *majority* (tumour-dominated slides, where normal or artefact becomes "surprising") or when artefacts are rare — the authors' own failed "norm-preserving consolidation" variant targeted the first case and did not help, so this is an open problem. The scan order and warm-up set also matter in a streaming memory, which is not analysed.
- PathCTM: attention-guided zooming assumes low-magnification attention reliably points at regions whose high-magnification content matters — the very attention-reliability assumption SMMILe criticises; the two papers are in mild tension. It also needs the WSI pyramid on disk and does encoder inference online, which changes the usual offline-feature workflow.
- CARE / TMEvolve: "adaptive regions" are validated by downstream accuracy and heatmaps, not by agreement with pathologist-drawn tissue compartments; CARE's "the ROI" is a single region, which is odd for multifocal or heterogeneous tumours.
- Open question spanning the line of work: can the instance-level, measurable localisation of SMMILe be carried into slide-level LLMs so that answers are *grounded and quantified* rather than attended? None of the VLM papers yet do this.

### Gaps
- TMEvolve's Appendix G (limitations) and CARE's final ~27k characters (possible limitations section) were truncated and not read.
- No independent third-party replication or critique of any of these papers was searched for.

---

## 5. What common thread runs through his work — his research taste?

### Takeaway
Gao's signature is "structure over scale under weak supervision": he identifies a structural mismatch between the dominant WSI pipeline and how tissue/diagnosis is organised (spatial, regional, multi-scale, scan-then-search), explains the mismatch with a simple mechanism, and fixes it with an inductive bias that also makes the model cheaper — then evaluates on what the field usually does not measure (spatial recall, normal tissue, pathologist re-scoring, tokens/patches used).

### Cited Findings
- Stated agenda: whole-slide pathology ML, multimodal foundation models and spatial omics, and "clinically relevant prediction from histopathology"; current funding is specifically for "multimodal pathology foundation models". — [Homepage](https://zeyugaoai.github.io)
- Weak-supervision lineage: PhD-era first-author work is on minimal point annotation, semi-supervised multi-task WSI classification, hierarchical MIL with information bottleneck, unsupervised tissue segmentation "from global to local contrast"; plus a co-first MIL review (Information Fusion 2025). — [Publications page](https://zeyugaoai.github.io/publications/)
- Recurrent "region / prototype between patch and slide" motif: superpatches (SMMILe), GMM morphological prototypes as LLM tokens (ALPaCA), prototype attention MIL (PAMIL), prototype-guided interactive segmentation (ProGIS), prototype-aware graph attention (BIBM 2025), adaptive regions (CARE), evolving regions (TMEvolve). — [Publications page](https://zeyugaoai.github.io/publications/); [CARE](https://arxiv.org/html/2602.21637); [TMEvolve](https://arxiv.org/html/2609.34451)
- Recurrent "pathologist workflow as algorithm" motif: scan broadly before searching (PathNavigate); coarse-to-fine magnification with stopping (PathCTM); multi-magnification tokens with coarse vs fine questions (ALPaCA). — [PathNavigate](https://arxiv.org/html/2605.23559); [PathCTM](https://arxiv.org/html/2605.19491); [ALPaCA](https://www.nature.com/articles/s41467-026-76372-z)
- Recurrent "efficiency as proof" motif: CARE with 34,277 slides vs TITAN's 335,645; PathCTM with ~183–408 patches per slide; PathNavigate with frozen models and ~17K vs ~30K tokens; TMEvolve with 5.18M parameters. — [CARE](https://arxiv.org/html/2602.21637); [PathCTM](https://arxiv.org/html/2605.19491); [PathNavigate](https://arxiv.org/html/2605.23559); [TMEvolve](https://arxiv.org/html/2609.34451)
- Recurrent "question what is measured" motif: SMMILe — "few works quantitatively assess their interpretability" and "AUC alone is insufficient"; ALPaCA — pathologists overturn the GPT judge, questions are audited for answerability, and tumour-only models are tested on normal tissue. — [SMMILe](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/); [ALPaCA](https://www.nature.com/articles/s41467-026-76372-z)
- Recurrent "molecular / spatial biology as the semantic target": CARE aligns regions to RNA and protein; PH2ST predicts spatial transcriptomics; SMMILe names spatial sequencing of sub-regions and IHC validation as the intended downstream use; LFFA does few-shot biomarker prediction. — [CARE](https://arxiv.org/html/2602.21637); [SMMILe Discussion](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/); [Publications page](https://zeyugaoai.github.io/publications/)
- Willingness to report where the method does not win and what did not work: SMMILe's Camelyon/Ovarian exceptions; CARE's losses to TITAN under kNN/fine-tuning; PathNavigate's negative-results appendix. — [SMMILe](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/); [CARE](https://arxiv.org/html/2602.21637); [PathNavigate](https://arxiv.org/html/2605.23559)

### Inferences
- **Style of argument that makes the papers feel insightful** (distilled):
  1. *Diagnose before prescribing.* The first-author papers open with a mechanism-level account of why the standard tool fails (SMMILe: the activation function's position starves attention of gradient; ALPaCA: single-adaptor compression loses either global or question-specific information). The method then reads as a consequence, not an invention.
  2. *Reduce two camps to one axis.* SMMILe shows RAMIL = logit-level IAMIL; ALPaCA frames six adaptors as vision-only vs vision-text interactive; PathNavigate frames agents as question-first vs slide-first; CARE frames tokenisation as character / fixed chunk / semantic unit. A single axis makes the proposed point on it look inevitable.
  3. *Borrow the pathologist's procedure, not their labels.* The clinical prior enters as control flow (scan→search→readout; zoom when uncertain; region then slide), which needs no extra annotation — consistent with his weak-supervision roots.
  4. *Make the claim falsifiable with a cheap control.* Synthetic bags, random ROI pools, random concepts, fixed grids.
  5. *Let frugality carry the argument.* If the inductive bias is right, it should need less data/compute; he reports that number in the abstract.
  6. *Evaluate the thing that actually matters clinically* (spatial recall, normal tissue, unanswerable questions, expert re-scoring), which simultaneously exposes weaknesses of competing methods that their own metrics hid.
- **Trajectory**: 2020–2023 weak supervision and MIL → 2024–2025 "MIL should be measurable" (SMMILe) → 2025–2026 "slides for LLMs" (ALPaCA: compress the slide for an LLM) → 2026 "don't compress, organise and navigate" (CARE/TMEvolve regions; PathCTM/PathNavigate active, budgeted evidence acquisition). The move from ALPaCA (fixed 56-token summary, no grounding) to PathNavigate (question-time evidence gathering with frozen models) is effectively a self-critique: ALPaCA's own stated limitation — no spatial grounding or region-level supervision — is what the later papers attack.
- **For someone trying to write in this style**: the reusable recipe is "find a place where the community trusts a by-product (attention heatmap, slide embedding, question-conditioned retrieval, LLM judge) as if it were a measurement; show with a simple analysis that it is not; restore the missing structure with the lightest possible mechanism; and prove it by needing less." The weakest instances of the style are those where the analogy carries more weight than the analysis (TMEvolve's PDE framing, PathCTM's informal propositions, PathNavigate's unexplained surprise signal).
- Caveat on attribution: for the 2026 conference papers he is senior/corresponding author and the first authors are XJTU students; the "taste" above is the group's (Gao + Chen Li), most confidently attributable to Gao personally in SMMILe and ALPaCA, where he is first author and is listed under conception/design, model development and theoretical derivation. — [SMMILe author contributions](https://pmc.ncbi.nlm.nih.gov/articles/PMC12727519/); [ALPaCA author contributions](https://www.nature.com/articles/s41467-026-76372-z)

### Gaps
- His own explicit statement of views (the first-author review "From cells to patients: Multiscale computational pathology in the era of foundation models and vision-language systems", Intelligent Oncology 2026) was not readable; the "research taste" characterisation is therefore inferred from the primary papers rather than from his stated position. — [ScienceDirect (403)](https://www.sciencedirect.com/science/article/pii/S2950261626000373)
- No talks, interviews or OpenReview discussions were found/read that would confirm how he himself describes the common thread.
- I found no paper by him that directly studies "what pathology VLMs actually learn or where they fail" as a stand-alone analysis/benchmark paper; if one exists (e.g., a late-2026 preprint), it was not on the homepage as of 20 Nov 2026.
