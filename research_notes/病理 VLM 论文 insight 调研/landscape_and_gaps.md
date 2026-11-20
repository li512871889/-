# Pathology VLM / multimodal-LLM landscape and open conceptual problems (as of 20 Nov 2026)

*Reading note: dates are given per claim. Most 2026 items are unreviewed arXiv preprints, and for many of them only the abstract page was read (marked "abs."). Numbers are the authors' own. Venue labels marked "(venue unverified)" come from other papers' reference lists or from memory, not from the venue page.*

## 1. What are the main paradigms and their representative papers?

### Takeaway
The field moved in four steps: patch-level CLIP (2023–24), slide-level vision-language encoders (2024–25), ROI and slide-level chat models (2024–25), then agents that navigate the slide and RL-trained "reasoners" (2025–26). The 2026 work is mostly about how evidence is acquired, stored and used, with fewer new encoders.

### Cited Findings

**Patch-level CLIP-style models**
- PLIP (Nature Medicine, 2023): CLIP fine-tuned on about 208k pathology image-text pairs from medical Twitter (OpenPath). — [Nature Medicine](https://www.nature.com/articles/s41591-023-02504-3)
- QuiltNet / Quilt-1M (NeurIPS 2023): 1M image-text pairs mined from educational YouTube histopathology videos. — [arXiv 2306.11207](https://arxiv.org/abs/2306.11207)
- CONCH (Nature Medicine, 2024): CoCa-style contrastive plus captioning pretraining on about 1.17M curated pairs. — [arXiv 2307.12914](https://arxiv.org/abs/2307.12914)
- MUSK (Nature, 2025): unified masked modelling on unpaired images and text, then contrastive alignment, aimed at precision-oncology tasks. — [Nature](https://www.nature.com/articles/s41586-024-08378-w)
- KEEP (arXiv Dec 2024, v2 Jan 2026): injects a disease knowledge graph into vision-language pretraining for cancer diagnosis. — [arXiv 2412.13126](https://arxiv.org/abs/2412.13126)

**Slide-level (vision-language or multimodal) pretraining**
- PRISM (arXiv May 2024): slide encoder on Virchow tile embeddings, aligned with clinical reports, and able to generate reports. — [arXiv 2405.10254](https://arxiv.org/abs/2405.10254)
- PRISM2 (arXiv Jun 2025): extends PRISM with clinical-dialogue supervision. — [arXiv 2506.13063](https://arxiv.org/html/2506.13063v2)
- TITAN (arXiv Nov 2024; Nature Medicine 2025, venue unverified): slide encoder pretrained with ROI-level self-supervision plus alignment to synthetic captions and reports. — [arXiv 2411.19666](https://arxiv.org/html/2411.19666v1)
- Prov-GigaPath (Nature, 2024): whole-slide pretraining with a long-context (LongNet) slide encoder on 1.3B tiles. — [Nature](https://www.nature.com/articles/s41586-024-07441-w)
- CHIEF (Nature, 2024): weakly supervised slide-level pretraining with anatomic-site text conditioning. — [Nature](https://www.nature.com/articles/s41586-024-07894-z)
- mSTAR (arXiv Jul 2024; Nature Communications 2025): slide-level pretraining using slides, reports and gene expression. — [arXiv 2407.15362](https://arxiv.org/html/2407.15362v3); [PubMed](https://pubmed.ncbi.nlm.nih.gov/41387679/)
- THREADS (arXiv Jan 2025): "molecular-driven" slide foundation model aligned to genomic and transcriptomic profiles. — [arXiv 2501.16652](https://arxiv.org/html/2501.16652v1)
- PathAlign (arXiv Jun 2024): BLIP-2-style slide-to-report alignment. It notes that slide-to-text association is messy because report text is written at part/block level, not slide level. — [arXiv 2406.19578](https://arxiv.org/pdf/2406.19578)

**Patch / ROI multimodal LLMs**
- PathChat (Nature, 2024): pathology vision encoder plus LLM, instruction-tuned as an ROI-level copilot. — [Nature](https://www.nature.com/articles/s41586-024-07618-3)
- Quilt-LLaVA (CVPR 2024, venue unverified): LLaVA tuned on spatially localised narrations from video (cursor traces). — [arXiv 2312.04746](https://arxiv.org/abs/2312.04746)
- PathGen-1.6M / PathGen-LLaVA (arXiv Jul 2024; ICLR 2025, venue unverified): 1.6M image-caption pairs generated from WSIs by multi-agent collaboration. — [arXiv 2407.00203](https://arxiv.org/pdf/2407.00203)
- CPath-Omni (arXiv Dec 2024; CVPR 2025, venue unverified): one LMM for patch-level and WSI-level tasks. — [arXiv 2412.12077](https://arxiv.org/abs/2412.12077)
- PathChat+ (arXiv Jun 2025, v2 Mar 2026): trained on over 1M instruction samples and about 5.5M QA turns. The authors name limited training data, weak multi-image support and little autonomous diagnostic reasoning as the gaps in prior pathology MLLMs. — [arXiv 2506.20964](https://arxiv.org/abs/2506.20964) (abs.)

**Slide-level multimodal LLMs**
- WSI-VQA (ECCV 2024, venue unverified): generative slide-level VQA, 8,672 QA pairs over 977 WSIs. — [arXiv 2407.05603](https://arxiv.org/pdf/2407.05603)
- SlideChat (arXiv Oct 2024; CVPR 2025; extended version in Nature Cancer 2026): patch encoder plus slide encoder plus LLM, with SlideBench built from TCGA reports using GPT-4. — [arXiv 2410.11761](https://arxiv.org/html/2410.11761v3); [Nature Cancer](https://www.nature.com/articles/s43018-026-01220-4)
- WSI-LLaVA / WSI-Bench (arXiv Dec 2024; ICCV 2025, venue unverified): 180k VQA pairs from 9,850 WSIs across 30 cancer types. — [arXiv 2412.02141](https://arxiv.org/html/2412.02141v4)
- HistoGPT (medRxiv Mar 2024; Nature Communications 2025, venue unverified): report generation from gigapixel dermatopathology WSIs, trained on 15,129 WSIs from 6,705 patients. — [medRxiv](https://www.medrxiv.org/content/10.1101/2024.03.15.24304211.full.pdf)
- ALPaCA (medRxiv Apr 2025): CONCH plus Llama 3.1 with slide-level adaptors, evaluated on 4,044 QA pairs from 337 held-out slides. — [medRxiv](https://www.medrxiv.org/content/10.1101/2025.04.22.25326190.full.pdf)
- Token compression: TCP-LLaVA (Jul 2025) passes only the hidden states of a few trainable compression tokens to the LLM. — [arXiv 2507.14497](https://arxiv.org/html/2507.14497v2)
- LoC-Path (Dec 2025) finds that the top 35.2% of tile tokens account for 90% of total cosine similarity with the report, and replaces the slide encoder with redundancy-reducing modules. — [arXiv 2512.05391](https://arxiv.org/html/2512.05391v2)
- MLLM-HWSI (arXiv Mar 2026; CVPR 2026, venue unverified): aligns four scales to language (cells as words, patches as phrases, regions as sentences, slide as paragraph). It criticises prior models for compressing a WSI into a single embedding. — [arXiv 2603.23067](https://arxiv.org/abs/2603.23067) (abs.)
- HistoSelect, "Act Like a Pathologist" (CVPR 2026): question-guided, tissue-aware coarse-to-fine patch retrieval framed with the Information Bottleneck, cutting visual tokens by about 70%. — [arXiv 2603.00667](https://arxiv.org/abs/2603.00667v2); [CVPR 2026 poster](https://cvpr.thecvf.com/virtual/2026/poster/36280)
- CTIS-QA (arXiv Jan 2026; BIBM 2025): CAP-protocol report templates give 14,879 clinically grounded QA pairs on 977 WSIs, with a dual-stream global/local model. — [arXiv 2601.01769](https://arxiv.org/abs/2601.01769) (abs.)

**Agentic / navigation approaches**
- PathFinder (ICCV 2025): four agents (triage, navigation, description, diagnosis). Reports +8% over prior methods on melanoma. — [arXiv 2502.08916](https://arxiv.org/abs/2502.08916v1); [ICCV poster](https://iccv.thecvf.com/virtual/2025/poster/1318)
- CPathAgent (arXiv May 2025): a trained agent that zooms and pans, with PathMMU-HR2, a benchmark for the intermediate "large region" scale. — [arXiv 2505.20510](https://arxiv.org/abs/2505.20510) (abs.)
- SlideSeek (arXiv Jun 2025): supervisor/explorer multi-agent system on PathChat+, evaluated on the open-ended DDxBench. — [arXiv 2506.20964](https://arxiv.org/abs/2506.20964) (abs.)
- GIANT (arXiv Nov 2025): training-free; a general LMM (GPT-5) iteratively picks crops from a thumbnail for about 20 steps. Introduces MultiPathQA (934 questions, 868 WSIs). — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- PathAgent (arXiv Nov 2025; ECCV 2026, venue unverified): training-free LLM agent with reflective, stepwise magnification changes and re-querying. — [arXiv 2511.17052](https://arxiv.org/abs/2511.17052v1)
- PathReasoning (arXiv Nov 2025): multi-turn, multi-scale query-based ROI navigation. — [arXiv 2511.21902](https://arxiv.org/pdf/2511.21902)
- Pathology-CoT / Pathology-o3 (arXiv Oct 2025): learns a "where to look" predictor from pathologists' viewer logs. — [arXiv 2510.04587](https://arxiv.org/html/2510.04587v2)
- MMNavAgent (arXiv Mar 2026): adaptive magnification selection with memory instead of fixed magnification sequences. Gains are small: +1.45% AUC and +2.93% balanced accuracy over a non-agent baseline. — [arXiv 2603.02079](https://arxiv.org/abs/2603.02079) (abs.)
- PathNavigate (arXiv May 2026): training-free; a low-magnification "surprise field" from a shared feature memory flags abnormal regions before question-conditioned selection. It argues that query-relevance-only agents miss morphology the question does not mention. — [arXiv 2605.23559](https://arxiv.org/abs/2605.23559) (abs.)
- SlideBank (arXiv Aug 2026): question-agnostic exploration builds a persistent, concept-indexed, coordinate-grounded evidence bank per slide. Reports over 99% rephrasing consistency. — [arXiv 2609.00342](https://arxiv.org/abs/2609.00342) (abs.)
- PathoSage (arXiv May 2026): patch-level agent that adjudicates each tool's evidence separately in a fresh context to reduce anchoring, with Beta-Bernoulli tool-reliability tracking. — [arXiv 2606.07549](https://arxiv.org/abs/2606.07549) (abs.)

**Reasoning-oriented models**
- Patho-R1 (arXiv May 2025; AAAI 2026): 3.5M pairs of continued pretraining, 500k chain-of-thought samples, then GRPO/DAPO reinforcement learning. — [arXiv 2505.11404](https://arxiv.org/html/2505.11404v3); [AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/40071)
- SmartPath-R1 (arXiv Jul 2025): reasoning-enhanced MLLM for ROI and WSI tasks that avoids chain-of-thought supervision. — [arXiv 2507.17303](https://arxiv.org/html/2507.17303v1)
- PathReasoner-R1 (arXiv Jan 2026): 20k+ knowledge-graph-guided WSI reasoning samples, with RL using an entity-level reward so that reasoning, not just the answer, is rewarded. — [arXiv 2601.21617](https://arxiv.org/abs/2601.21617) (abs.)

**Benchmarks**
- PathMMU (arXiv Jan 2024; ECCV 2024, venue unverified): expert-validated multimodal QA at patch/figure level. — [arXiv 2401.16355](https://arxiv.org/abs/2401.16355)
- SlideBench: 7,827 TCGA VQAs and about 7.2k BCNB VQAs. — [arXiv 2410.11761](https://arxiv.org/html/2410.11761v3)
- MultiPathQA: five tasks, including 128 pathologist-written ExpertVQA questions. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- 2026 benchmarks (details in sections 2 and 4): DALPHIN, EviPathBench, PathBind, PathView-Bench, CleanSlide, PathoArgus-Bench, ACP-Bench, PathReportEval, PathGLS.

### Inferences
- The slide-level chat models nearly all share one recipe: frozen patch encoder, then an aggregator or compressor, then an LLM, trained on QA generated by an LLM from TCGA reports. The 2026 critiques in section 2 attack exactly that shared recipe (the data source and the single-pass compression).
- Agents split into trained (CPathAgent, Pathology-o3) and training-free (GIANT, PathAgent, PathNavigate, SlideBank). The training-free line is moving from "navigate per question" to "build a reusable slide memory once".
- The intermediate "region" scale is named as a gap by CPathAgent (PathMMU-HR2) and addressed architecturally by MLLM-HWSI, but few benchmarks isolate it.

### Gaps
- Venue labels marked "unverified" were not checked against proceedings.
- PathAgent's and PathReasoning's full texts were not read; only search snippets.
- A search snippet described MMNavAgent as using eye-tracking supervision, but its abstract does not mention eye-tracking. Treat that claim as unconfirmed.

## 2. What critiques and negative findings exist?

### Takeaway
By late 2026 there is converging evidence that answer accuracy on slide-level VQA does not measure use of the slide: benchmarks leak, models answer from priors, and the bottleneck is finding evidence, not reasoning over it. Separately, pathology encoders carry site/scanner signal that standard metrics hide, and confidence estimates in pathology VQA are close to useless for deferral.

### Cited Findings

**Answering without looking (language priors, blind baselines)**
- SlideChat (Oct 2024) itself reports text-only GPT-4 at 37.25% on SlideBench-VQA (TCGA) against 25.02% random. The benchmark was filtered by removing questions that at least three of four LLMs answered from text alone. — [arXiv 2410.11761](https://arxiv.org/html/2410.11761v3)
- PathBind (Jul 2026): Gemini-3-Pro reached about 53.5% average accuracy across five pathology VQA benchmarks with no image. — [arXiv 2607.21065](https://arxiv.org/abs/2607.21065)
- PathBind also reports that Patho-R1-7B had a 5.8-point smaller multimodal gain and 3.7-point lower attention IoU than its general-purpose base Qwen2.5-VL-7B. Domain training raised accuracy without improving image use. — [arXiv 2607.21065](https://arxiv.org/abs/2607.21065)
- PathBind: attention maps on the PathVG grounding benchmark stayed highly correlated across different entity queries (weak query-specific focus). — [arXiv 2607.21065](https://arxiv.org/abs/2607.21065)
- "Contamination, Prior, or Evidence?" (Sep 2026): in a lymph-node metastasis study, most public pathology VLMs performed about the same given a whole slide, an annotated lesion, or no image. — [arXiv 2609.32185](https://arxiv.org/abs/2609.32185)
- Same paper: on its audited CleanSlide benchmark (about 149K MCQs, 9,985 slides, patient- and site-disjoint splits), the best published model gains only 2.81% from image evidence. Their Pair-DPO method (preference training on real counterfactual slide pairs with the same question and source) gains 15.29%. — [arXiv 2609.32185](https://arxiv.org/abs/2609.32185)
- PathoArgus (Aug 2026): on 483 "evidence state quartets" (question fixed; target slides moved, replaced or removed), GPT-5.6 scored 57.04% accuracy but completed only 19/483 quartets consistently (3.93%). Their own improved reader scored 50.39% accuracy and 1.86% quartet-exact. The authors conclude that context access is "necessary but far from sufficient". — [arXiv 2608.17607](https://arxiv.org/abs/2608.17607) (abs.)
- General medical VQA (Jun 2026): on GMAI-MMBench a blank image removes 61% of correct answers, yet no trained confidence probe is less confident on answers that stay the same when the image is replaced. — [arXiv 2606.15910](https://arxiv.org/abs/2606.15910) (abs.)

**Benchmark leakage and saturation**
- Leakage audit (Jul 2026): case-level train-test overlap on TCGA-derived WSI benchmarks is 92.3%–100%, with near-complete tissue-source-site overlap. Both leak levels are linearly decodable from foundation-model features, and the highest reported accuracies concentrate on the most contaminated benchmarks. — [arXiv 2607.12278](https://arxiv.org/abs/2607.12278) (abs.)
- Example given: WSI-VQA-test shares 100% of its cases with WSI-Bench-train. — [arXiv 2607.12278](https://arxiv.org/pdf/2607.12278) (search snippet)
- The audit's claim: current WSI VQA evaluation cannot distinguish multimodal reasoning from nearest-neighbour retrieval over memorised institutional and patient-specific artefacts. — [arXiv 2607.12278](https://arxiv.org/abs/2607.12278)
- GIANT (Nov 2025) notes that SlideBench contains low-resolution slides and at least one single region instead of a WSI, and that its question pipeline matches SlideChat's training data. SlideChat scores 70.5 on SlideBenchVQA but 37.5 on pathologist-written ExpertVQA. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)

**Finding evidence is the bottleneck (grounding, localisation, magnification)**
- EviPathBench (Jul 2026; 1,822 TCGA slides, 17,135 pathologist-annotated diagnostic paths): leading open models exceed 93% when reasoning over curated evidence. Best text-guided localisation mIoU is below 0.09, worse than a centre heuristic. — [arXiv 2607.19261](https://arxiv.org/abs/2607.19261) (abs.)
- EviPathBench: in autonomous exploration the hit rate falls from 0.522 at low magnification to 0.185 at intermediate and 0.020 at high. — [arXiv 2607.19261](https://arxiv.org/abs/2607.19261)
- PathView-Bench (NeurIPS 2026; 14 tasks, 308,070 samples, 28 organs): 18 general, medical and pathology MLLMs show substantial limits on region localisation, quantity estimation, spatial reasoning and insufficient-context judgment. — [NeurIPS 2026 poster](https://neurips.cc/virtual/2026/poster/139172) (abs.)
- A CVPR 2025 multi-resolution pretraining paper argues zero-shot results show the need for multi-resolution VL models, and notes Quilt-LLaVA's descriptions depend considerably on magnification. — [CVPR 2025 supplemental](https://openaccess.thecvf.com/content/CVPR2025/supplemental/Albastaki_Multi-Resolution_Pathology-Language_Pre-training_CVPR_2025_supplemental.pdf) (search snippet)
- Prompt sensitivity (May 2025): the best zero-shot prompt differs by model; CONCH does best with precise anatomical references. — [arXiv 2505.00134](https://arxiv.org/pdf/2505.00134)
- PathoHR-Bench (Findings of EMNLP 2025): pathology VL models fail at hierarchical and compositional cross-modal relations. — [arXiv 2509.06105](https://arxiv.org/html/2509.06105v2)

**General frontier models versus specialists (mixed picture)**
- GIANT (Nov 2025): GPT-5 with thumbnails scores 9.2 on TCGA 30-way diagnosis; with navigation 32.3; TITAN scores 88.8 (with possible pretraining overlap). On pathologist-written ExpertVQA, GIANT+GPT-5 (5 runs) scores 62.5 vs TITAN 43.8 and SlideChat 37.5. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- GIANT: PANDA prostate grading stays near 23–27% for all systems (GIANT 23.4–25.6, TITAN 27.0, SlideChat 17.0). — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- DALPHIN (May 2026; 300 cases, 130 diagnoses, 31 pathologists): no significant difference from expert level on 4/6 tasks for PathChat+, 2/6 for Gemini 2.5 Pro, 1/6 for GPT-5. — [arXiv 2605.03544](https://arxiv.org/abs/2605.03544) (abs.)
- ACP-Bench (Jul 2026; Claude Code, Codex, Open Code harnesses; 369 trajectories on 41 workflow tasks): task interpretation and reporting are more mature than tool-bound execution, result binding and reflective revision; "formal end-to-end completion remained rare". — [arXiv 2607.02598](https://arxiv.org/abs/2607.02598) (abs.)

**Agent failure modes**
- GIANT pathologist review of 28 traces: premature diagnostic anchoring (contradictory findings reinterpreted to fit the early hypothesis), hallucinated adnexal structures, overcalling skin malignancies, benign tissue edges mislabelled as margins. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- GIANT: giving the agent a CONCH tool hurt TCGA (−13.7) and SlideBenchVQA (−4.5); the authors suggest the agent used CONCH to reinforce wrong hypotheses. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)
- GIANT's v2 abstract: the model selects diagnostically relevant regions but often fails to link visual findings to the correct diagnosis. — [arXiv 2511.19652](https://arxiv.org/pdf/2511.19652v2) (search snippet)
- PathoSage (May 2026): agents merge tool outputs and retrieved knowledge into one context, so conflicting evidence contaminates decisions. — [arXiv 2606.07549](https://arxiv.org/abs/2606.07549)
- PathReasoner-R1 (Jan 2026) says Patho-R1 produces superficial reasoning and is limited to isolated ROIs. — [arXiv 2601.21617](https://arxiv.org/html/2601.21617) (search snippet)

**Hallucination in reports**
- Lucassen et al. (arXiv Feb 2025; PMLR 316, 2026): training reports contain information not inferable from the slide (e.g. patient history), which causes hallucinated sentences; text preprocessing reduces this (BLIP-2 model, 42,433 melanocytic WSIs). — [PMLR](https://proceedings.mlr.press/v316/lucassen26a.html); [arXiv 2502.19285](https://arxiv.org/abs/2502.19285)
- PathGLS (Mar 2026): a reference-free grounding/logic/stability score drops 40.2% on hallucinated reports where BERTScore drops 2.1%. — [arXiv 2603.16113](https://arxiv.org/abs/2603.16113) (abs.)
- PathReportEval (Jul 2026): standard NLG metrics overestimate report quality; proposes a metric decomposed into fact coverage, key-information recall, hallucination and clinical discordance. — [arXiv 2607.18448](https://www.alphaxiv.org/abs/2607.18448.md) (search snippet)

**Text overriding vision**
- Pen-mark study (medRxiv Dec 2024; later NEJM AI per search): with a T-stage label written on the slide, Claude-3/3.5 and GPT-4o reached 90–100% when the label was correct and 0–10% when misleading, against 30–65% baselines. — [medRxiv](https://www.medrxiv.org/content/10.1101/2024.12.11.24318840.full.pdf)
- Prompt injection in oncology VLMs (Nature Communications, 2025): injected text can flip accurate diagnoses to harmful ones. — [PMC11785991](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11785991/)
- Medical VLM sycophancy benchmark (2025). — [arXiv 2509.21979](https://arxiv.org/pdf/2509.21979v3)

**Site, scanner and batch shortcuts in the encoders**
- Site identity is easily predicted from foundation-model features and the bias carries downstream (Nov 2024). — [arXiv 2411.05489](https://arxiv.org/pdf/2411.05489v1)
- All ten evaluated models strongly encode medical centre; a Robustness Index is proposed (Jan 2025). — [arXiv 2501.18055](https://arxiv.org/html/2501.18055v2)
- Scanner study (Jan 2026; 14 models, 384 breast WSIs on five scanners): AUC often stable while embeddings and calibration shift; robustness does not track data scale, model size or recency; "none of the models provided reliable robustness". Vision-language models looked more robust but underperformed on downstream supervised tasks. — [arXiv 2601.04163](https://arxiv.org/abs/2601.04163) (abs.)
- 2026 mitigations: fine-tuning-free correction (2602.22347), language-mediated robust embeddings (2606.28697), a distributional robustness margin tracking shortcut learning across 20 tile models (2607.25497), one-slide calibration (2610.08944). — [2602.22347](https://arxiv.org/pdf/2602.22347); [2606.28697](https://arxiv.org/pdf/2606.28697); [2607.25497](https://arxiv.org/pdf/2607.25497); [2610.08944](https://arxiv.org/pdf/2610.08944) (search snippets only)
- Tizhoosh critique (arXiv Oct 2025, v5 Apr 2026) lists, among other causes: no magnification awareness, 224-px patches versus microscope fields of about 2048×1536, self-supervision designed for single-object images, and limits of single dense embeddings for combinatorial tissue content. — [arXiv 2510.23807](https://arxiv.org/html/2510.23807v4)

**Calibration and uncertainty**
- Jun 2026 (v3 Oct 2026): on PATH-VQA, threshold-only confidence estimators certify nothing; adaptation certifies 11.4% of answers and needs about 2,500 local labels. Across datasets nothing is certified at 5% error. — [arXiv 2606.15910](https://arxiv.org/abs/2606.15910) (abs.)
- Apr 2026: overconfidence in medical VQA persists across model families and is not fixed by scaling, chain-of-thought or verbalised confidence; post-hoc calibration works better. — [arXiv 2604.02543](https://arxiv.org/pdf/2604.02543) (search snippet)
- Jun 2026: accuracy collapses when the correct answer is removed, but uncertainty does not rise to match. — [arXiv 2606.16583](https://arxiv.org/html/2606.16583) (search snippet)

### Inferences
- Three independent 2026 groups (PathBind, CleanSlide, PathoArgus) reach the same conclusion with different designs: accuracy conflates contamination, prior and evidence. This is now established enough to build on, not to rediscover.
- The EviPathBench split (93% reasoning on curated evidence versus near-zero high-magnification hit rate) and GIANT's anchoring traces point at two different failures: search (where to look) and belief revision (what to do with a disconfirming view). Most methods address only the first.
- The PathBind result on Patho-R1 versus its base model suggests pathology fine-tuning mainly strengthens priors. That is in tension with DALPHIN, where the specialist PathChat+ is closest to experts. The two are not directly comparable (different models, patch/ROI images versus VQA sets), so the tension is unresolved.
- Specialist slide encoders win on closed-set classification seen in pretraining distributions (TITAN on TCGA), and generalist agents win on novel expert-written questions (ExpertVQA). Neither does grading (PANDA).

### Gaps
- I found no 2026 paper that measures hallucination rates of slide-level chat models directly on real clinical reports with pathologist adjudication at scale; the evidence is metric proposals (PathGLS, PathReportEval).
- No source ties site/scanner shortcuts to failures of specific slide-level chat models, beyond the audit's statement that leakage is decodable from features.
- Many 2026 claims rest on abstracts only; per-model tables in PathBind, EviPathBench, PathView-Bench, DALPHIN and the audit were not read.
- Search hinted that simple MIL baselines are competitive with slide foundation models (nnMIL, [arXiv 2511.14907](https://arxiv.org/html/2511.14907v1); "Do MIL models transfer?", [arXiv 2506.09022](https://arxiv.org/html/2506.09022v1)), but I did not read them and could not map two further 2026 benchmark snippets to arXiv ids.

## 3. What do pathologists do that current models do not, and is viewing behaviour used for training?

### Takeaway
Pathologists run a hypothesis-driven, multi-scale search, revise the differential, and order ancillary tests when H&E is insufficient. Current systems mostly cover the search part, with fixed budgets and no ancillary-test action. Viewing-behaviour datasets exist but are small (tens of pathologists, hundreds of slides) and only one work turns them into agent supervision.

### Cited Findings
- International expert perspective (Mar 2026): human experts resolve ambiguity "through hierarchical reasoning and contextual integration"; current foundation models "largely lack explicit mechanisms for multiscale abstraction and causal interpretation". The same paper says machines should be stronger at quantitative tasks such as tumour burden and mitotic counts. — [arXiv 2603.05884](https://arxiv.org/html/2603.05884) (first 100k characters read)
- Same paper on agents: errors of unreliable component models accumulate across steps; automation bias and deskilling are human-factor risks. — [arXiv 2603.05884](https://arxiv.org/html/2603.05884)
- MMNavAgent (Mar 2026): existing navigation uses one magnification or a predefined sequence, whereas pathologists inspect only the scales they need. — [arXiv 2603.02079](https://arxiv.org/abs/2603.02079)
- PathNavigate (May 2026): agents that pick regions by query relevance miss important morphology the question does not mention (pathologists notice the unexpected). — [arXiv 2605.23559](https://arxiv.org/abs/2605.23559)
- Pathology-CoT (Oct 2025): 8 Stanford pathologists, 25 cases, 137 slides, 921 sessions, 10.6 hours of viewer logs for colorectal lymph-node metastasis. Logs are reduced to "inspect" (low-magnification) and "peek" (high-magnification) commands with pathologist-verified rationales; 5,222 rounds. — [arXiv 2510.04587](https://arxiv.org/html/2510.04587v2)
- Pathology-CoT results: the behaviour-guided agent reaches 84.5% precision / 100% recall / 75.4% accuracy internally against OpenAI o3 at 46.7% / 87.5% / 57.8%. Learned guidance closed most of the gap to real expert guidance. The authors argue expert viewing behaviour is tacit knowledge absent from text corpora. — [arXiv 2510.04587](https://arxiv.org/html/2510.04587v2)
- Pathology-CoT limits: one task, single-centre predictor, and the viewing-order finding may hold only for search-and-find tasks, not grading or mitosis counting. — [arXiv 2510.04587](https://arxiv.org/html/2510.04587v2)
- PathoGaze 1.0 (Oct 2025): 18.69 hours of eye-tracking, mouse, viewport and decision data from 19 pathologists on 397 WSIs. — [arXiv 2510.24653](https://arxiv.org/html/2510.24653)
- Pathologist Attention Transformer (Aug 2025): predicts scanpaths from 1,016 attention trajectories of 43 pathologists at 11 institutions on 123 WSIs; framed as a trainee tool. — [arXiv 2508.01668](https://arxiv.org/abs/2508.01668v1)
- EviPathBench (Jul 2026) has 17,135 diagnostic paths annotated by ten pathologists, used for evaluation. — [arXiv 2607.19261](https://arxiv.org/abs/2607.19261)
- Ancillary testing: DALPHIN includes an ancillary-testing question domain (confirmatory tests, expected marker patterns), as QA and not as an action. — [arXiv 2605.03544](https://arxiv.org/pdf/2605.03544) (search snippet)
- A small 2024 study graded chatbots' differentials and immunostain recommendations on six text vignettes. — [PMC11196119](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC11196119/)
- MTBBench (Nov 2025): sequential tumour-board benchmark with H&E and IHC slides, haematology, genomics and timed clinical events. — [arXiv 2511.20490](https://arxiv.org/html/2511.20490v1)
- Clinical context cuts both ways: reports include history not inferable from the slide, which drives hallucination ([PMLR 316](https://proceedings.mlr.press/v316/lucassen26a.html)), and written text on a slide overrides visual evidence ([medRxiv](https://www.medrxiv.org/content/10.1101/2024.12.11.24318840.full.pdf)).
- Uncertainty expression: PathView-Bench includes an "insufficient-context judgment" task on which models are weak. — [NeurIPS 2026 poster](https://neurips.cc/virtual/2026/poster/139172)
- Stopping: GIANT uses a fixed budget of 20 iterations for every task. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652)

### Inferences
- No system found treats "this H&E is insufficient; order stain X" as an action with a measurable value. Agents answer every question from H&E, with a fixed step budget.
- Behaviour data is two orders of magnitude smaller than the text/image corpora, and comes from narrow tasks. Whether an expert scanpath is even the right target for a model with different perception (no fovea, different cost per view) is untested.
- Models are weak at exactly the quantitative tasks where experts expect machines to beat humans, which argues for explicit tool use for counting, not end-to-end perception.

### Gaps
- I found no benchmark that scores stepwise IHC ordering with a revised differential on real slides. Searches returned only DALPHIN's QA domain, MTBBench, and a non-pathology evidence-seeking RL paper ([arXiv 2607.02983](https://arxiv.org/pdf/2607.02983), not read).
- I found no MLLM trained at scale on gaze data; PathoGaze and the attention transformer are datasets/predictors, not chat-model supervision.
- No cognitive-science sources on pathologist diagnostic reasoning (dual-process, search-satisfaction errors) were retrieved in this pass.

## 4. What trends appeared in 2026, and what do surveys and position papers list as open problems?

### Takeaway
2026 is the year the field audited itself: a cluster of evidence-grounding benchmarks and leakage audits (Jul–Sep), pathologist-referenced evaluation, training-free agents with slide memory, RL reasoners, and hierarchical/compressed slide tokenisation. Reviews still list mostly engineering problems (long sequences, data scarcity, interpretability); the sharper conceptual critiques come from the benchmark papers.

### Cited Findings
- Evidence-grounding wave: EviPathBench (21 Jul), PathBind (23 Jul), PathoArgus (18 Aug), CleanSlide / Pair-DPO (26 Sep), PathView-Bench (NeurIPS 2026). — [2607.19261](https://arxiv.org/abs/2607.19261); [2607.21065](https://arxiv.org/abs/2607.21065); [2608.17607](https://arxiv.org/abs/2608.17607); [2609.32185](https://arxiv.org/abs/2609.32185); [NeurIPS](https://neurips.cc/virtual/2026/poster/139172)
- Leakage audit (14 Jul 2026) with recommendations on benchmark construction, provenance disclosure and automated overlap auditing. — [arXiv 2607.12278](https://arxiv.org/abs/2607.12278)
- Pathologist-referenced and workflow evaluation: DALPHIN (May) with sequestered ground truth; ACP-Bench (Jul) for coding-agent harnesses. — [2605.03544](https://arxiv.org/abs/2605.03544); [2607.02598](https://arxiv.org/abs/2607.02598)
- Training-free agents with memory: PathNavigate (May), SlideBank (Aug); evidence adjudication: PathoSage (May). — [2605.23559](https://arxiv.org/abs/2605.23559); [2609.00342](https://arxiv.org/abs/2609.00342); [2606.07549](https://arxiv.org/abs/2606.07549)
- RL reasoners move from ROI to WSI with knowledge-graph rewards: PathReasoner-R1 (Jan). — [arXiv 2601.21617](https://arxiv.org/abs/2601.21617)
- Multi-scale and compressed slide tokens: MLLM-HWSI (Mar), HistoSelect (CVPR 2026), and TC-SSA, DTC-WSI (MIDL 2026), WSISum (Medical Image Analysis 2026) as named in a March 2026 review. — [2603.23067](https://arxiv.org/abs/2603.23067); [2603.00667](https://arxiv.org/abs/2603.00667v2); [review 2603.18660](https://arxiv.org/html/2603.18660)
- Report-quality evaluation: PathGLS (Mar), PathReportEval (Jul), QCAgent (Mar). — [2603.16113](https://arxiv.org/abs/2603.16113); [2607.18448](https://www.alphaxiv.org/abs/2607.18448.md); [2603.01647](https://arxiv.org/html/2603.01647v1)
- Robustness work shifts from diagnosis to post-hoc fixes (see section 2). — [2610.08944](https://arxiv.org/pdf/2610.08944)
- SlideChat's extended version appeared in Nature Cancer (2026), benchmarked on 27 tasks across 33 cancer types. — [Nature Cancer](https://www.nature.com/articles/s43018-026-01220-4)
- March 2026 review (Wu et al.) open problems: quadratic attention on ultra-long sequences; patching breaks global structure; token compression assumes redundancy and may drop sparse but critical regions; frozen offline extractors in MIL; long-tail subtypes; overconfident VLMs. Future directions include uncertainty-aware evidence fusion and RL-trained agent teams. — [arXiv 2603.18660](https://arxiv.org/html/2603.18660)
- March 2026 expert perspective open problems: benchmark-to-practice gap, pre-analytic variability, "catastrophic inheritance" of label noise, population bias, shortcut learning (e.g. BRAF prediction largely tracking MSI status), hallucination, quantitative reporting precision, agent error propagation, governance. — [arXiv 2603.05884](https://arxiv.org/html/2603.05884)
- 2025 surveys list: pathology-specific methodology, end-to-end pretraining, scalability and model maintenance ([arXiv 2504.04045](https://arxiv.org/html/2504.04045v2)); 32 multimodal models across vision-language, knowledge-graph and gene-expression paradigms ([arXiv 2503.09091](https://arxiv.org/html/2503.09091v2)).
- A July 2026 Chinese-language review of agents in the pathology workflow calls for tests of stability, reproducibility, auditability and clinical benefit. — [DOI 10.12290/xhyxzz.2026-0402](https://www.sciopen.com/article/10.12290/xhyxzz.2026-0402) (abstract only)

### Inferences
- The benchmark side of "does the model use the slide?" became crowded within about three months of 2026. A new paper that only adds another such benchmark would be late; a mechanism or training principle that explains or fixes the effect would not.
- Reviews treat token compression as an efficiency problem. The March 2026 review's own caveat (sparse critical regions) plus EviPathBench's high-magnification collapse suggest compression and evidence-finding are the same problem, which no paper found states directly.
- Position papers discuss shortcut learning for encoders and hallucination for generators separately; none found connects them (e.g. whether site signal in features drives language-side priors).

### Gaps
- I did not find a dedicated 2026 survey of pathology MLLMs or agents with a full open-problems section; the two March 2026 papers are the closest.
- No curated GitHub "awesome" list was checked in this pass.
- Coverage of October–November 2026 is thin: only robustness preprints surfaced (2610.08944). Work from MICCAI 2026 and NeurIPS 2026 beyond PathView-Bench was not searched.

## 5. Which under-explored angles look promising and not yet crowded?

### Takeaway
The most open ground is on the method/mechanism side of evidence use: training signals that make answers depend on the slide, belief revision and stopping in agents, ancillary tests as actions, and how to admit clinical context without letting it override the image. Benchmarks for these are appearing; principled methods are scarce.

### Cited Findings (each angle with the evidence that it is open)
1. **Evidence dependence as a training objective.** Only one method found (Pair-DPO, Sep 2026) trains for image-attributable preference, and the best published model gains 2.81% from the image. — [arXiv 2609.32185](https://arxiv.org/abs/2609.32185). Better context access alone leaves quartet consistency at 1.86%. — [arXiv 2608.17607](https://arxiv.org/abs/2608.17607)
2. **Does domain fine-tuning buy priors and not perception?** Patho-R1 shows smaller multimodal gain and lower attention IoU than its base model. — [arXiv 2607.21065](https://arxiv.org/abs/2607.21065). Contrasting evidence: PathChat+ is nearest to pathologists on DALPHIN. — [arXiv 2605.03544](https://arxiv.org/abs/2605.03544)
3. **Search under scale: low-magnification cues do not lead to high-magnification evidence.** Hit rate 0.522 → 0.185 → 0.020 with magnification; localisation mIoU < 0.09 while reasoning over curated evidence is > 93%. — [arXiv 2607.19261](https://arxiv.org/abs/2607.19261). PathNavigate's question-agnostic "surprise" scan is one early answer. — [arXiv 2605.23559](https://arxiv.org/abs/2605.23559)
4. **Belief revision and anchoring in agents.** Anchoring documented in GIANT traces; an added expert tool reinforced wrong hypotheses. — [arXiv 2511.19652](https://arxiv.org/html/2511.19652). The only mitigation found is patch-level fresh-context adjudication. — [arXiv 2606.07549](https://arxiv.org/abs/2606.07549)
5. **Knowing when the slide is insufficient (stopping, abstention, deferral).** Fixed 20-step budgets ([arXiv 2511.19652](https://arxiv.org/html/2511.19652)); weak insufficient-context judgment ([NeurIPS 2026](https://neurips.cc/virtual/2026/poster/139172)); nothing certifiable on PATH-VQA without about 2,500 local labels, and confidence does not react to image removal ([arXiv 2606.15910](https://arxiv.org/abs/2606.15910)).
6. **Ancillary tests and multi-slide cases as actions.** No sequential IHC-ordering benchmark found; the closest are DALPHIN's QA domain ([arXiv 2605.03544](https://arxiv.org/pdf/2605.03544)), MTBBench ([arXiv 2511.20490](https://arxiv.org/html/2511.20490v1)) and PathoArgus's multi-slide contexts ([arXiv 2608.17607](https://arxiv.org/abs/2608.17607)). PathChat+ authors say most pathology models lack multi-image support ([arXiv 2506.20964](https://arxiv.org/abs/2506.20964)).
7. **What in a report is inferable from H&E?** Non-inferable report content causes hallucination, and only text preprocessing has been tried. — [PMLR 316](https://proceedings.mlr.press/v316/lucassen26a.html). Slide-to-text association is at part/block level, not slide level. — [arXiv 2406.19578](https://arxiv.org/pdf/2406.19578)
8. **Clinical context as prior versus injection channel.** Text on or about the slide overrides vision (90–100% vs 0–10%). — [medRxiv](https://www.medrxiv.org/content/10.1101/2024.12.11.24318840.full.pdf). Experts nonetheless rely on "contextual integration". — [arXiv 2603.05884](https://arxiv.org/html/2603.05884)
9. **Expert behaviour as supervision, beyond one task.** One agent trained on logs from 8 pathologists on one task, with stated limits for grading tasks. — [arXiv 2510.04587](https://arxiv.org/html/2510.04587v2). Larger gaze sets exist but are unused for chat-model training. — [arXiv 2510.24653](https://arxiv.org/html/2510.24653); [arXiv 2508.01668](https://arxiv.org/abs/2508.01668v1)
10. **Persistent slide memory and cross-question consistency.** One training-free system (SlideBank, Aug 2026) with absolute accuracy still near 51–53%. — [arXiv 2609.00342](https://arxiv.org/abs/2609.00342)
11. **Compression versus sparse evidence.** Top 35.2% of tiles carry 90% of report similarity ([arXiv 2512.05391](https://arxiv.org/html/2512.05391v2)), but the redundancy assumption may fail when critical regions are sparse ([arXiv 2603.18660](https://arxiv.org/html/2603.18660)).
12. **Site/scanner signal meeting language.** Leakage is linearly decodable from features and accuracy concentrates on contaminated benchmarks ([arXiv 2607.12278](https://arxiv.org/abs/2607.12278)); vision-language encoders looked more scanner-robust yet weaker downstream ([arXiv 2601.04163](https://arxiv.org/abs/2601.04163)).
13. **Grading and quantification.** All systems sit near 17–27% on PANDA grading ([arXiv 2511.19652](https://arxiv.org/html/2511.19652)); quantity estimation is weak ([NeurIPS 2026](https://neurips.cc/virtual/2026/poster/139172)).

### Inferences
- Angles 1, 2 and 12 could be one thesis: slide-level VQA training on report-derived QA teaches a mapping from site/cancer-type cues to report priors, so the "visual" pathway carries case identity more than morphology. The audit and PathBind each supply half of the evidence; no paper found joins them.
- Angles 3, 5 and 6 could be one decision-theoretic thesis: a slide examination is sequential evidence acquisition with costs, where "zoom here", "stop", and "order a stain" are the same kind of action ranked by expected information. Current agents implement only the first, with a fixed budget.
- Angles 7 and 8 share a missing variable: which statements are supported by the pixels and which by context. Labelling or learning that provenance would serve both hallucination control and safe use of clinical history.
- Least crowded (few or no methods found): 5, 6, 7, 8. Moderately active: 3, 4, 9, 10. Becoming crowded on the benchmark side but still thin on methods: 1, 2.
- Risk for any new paper: TCGA-derived evaluation is now suspect ([arXiv 2607.12278](https://arxiv.org/abs/2607.12278)), so claims will need site-disjoint or non-TCGA tests such as CleanSlide, DALPHIN, or BCNB/CPTAC.

### Gaps
- "Not crowded" is judged from about 30 searches; an exhaustive arXiv listing check for Oct–Nov 2026 was not done, so some angles may already have concurrent work.
- The combined theses in Inferences are my synthesis and are not tested in any source.
- I did not verify whether CleanSlide, EviPathBench's private breast cohort, or DALPHIN's sequestered ground truth are practically usable by outside groups.
