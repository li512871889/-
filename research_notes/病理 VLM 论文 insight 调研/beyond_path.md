# "Beyond Path" = BeyondPath ("Look Beyond the Question: Preserve–Focus–Fuse for Whole-Slide Image Question Answering", arXiv 2610.29431)

Research date: 2026-11-20. Primary source read in full (main text + appendices A–F) from the arXiv HTML v2; first PDF page read for affiliations. Secondary candidates were read at abstract level (BEACON also intro + conclusion).

## Which paper(s) is "Beyond Path"? (identification, bibliographic details, confidence)

### Takeaway
"Beyond path" is almost certainly **BeyondPath**, the method name of the arXiv preprint "Look Beyond the Question: Preserve–Focus–Fuse for Whole-Slide Image Question Answering" (arXiv:2610.29431, Oct 2026, Xiangyu Li et al., Tianjin University / Shanghai AI Lab). Confidence about 95%: it is the only arXiv record matching the string "BeyondPath", it is a WSI-VQA MLLM paper from the same month-range and sub-area as SlideBank, LoC-Path and Zeyu Gao's PathNavigate, and its contribution is explicitly a conceptual insight (the "Relevance–Sufficiency Gap").

### Cited Findings
- Title: "Look Beyond the Question: Preserve-Focus-Fuse for Whole-Slide Image Question Answering"; the abstract says "we introduce BEYONDPATH, a Preserve-Focus-Fuse framework for whole-slide image question answering". — [arXiv abs 2610.29431](https://arxiv.org/abs/2610.29431)
- Authors (arXiv order): Xiangyu Li, Jincheng Li, Tianle Du, Yanheng Li, Haoxuan Che, Yuxin Sun, Long Bai, Liangliang Liu, Ran Su. — [arXiv abs 2610.29431](https://arxiv.org/abs/2610.29431)
- Affiliations on the PDF title page: Tianjin University; Shanghai AI Laboratory; University of Science and Technology of China; Nantong University; City University of Hong Kong; HKUST; CUHK; Henan Agricultural University. Xiangyu Li and Jincheng Li are marked equal contribution; Ran Su (Tianjin University) is corresponding author. — [arXiv PDF 2610.29431v2](https://arxiv.org/pdf/2610.29431v2)
- Dates and category: submitted 21 Oct 2026 (v1), v2 on 27 Oct 2026, primary class cs.CV. No "Comments" field, so no venue is stated. — [arXiv abs 2610.29431](https://arxiv.org/abs/2610.29431)
- An arXiv API full-text-field query for `BeyondPath OR "Beyond-Path"` returns this paper as the only pathology hit; all other hits are unrelated (graph theory, path loss, etc.). — [arXiv API query](https://export.arxiv.org/api/query?search_query=all:BeyondPath+OR+all:%22Beyond-Path%22&max_results=50)
- Other pathology papers with "Beyond" in the title, 2024–Nov 2026 (arXiv title search, ranked by likelihood of being meant):
  1. **2610.29431 – BeyondPath** (above). Near-certain.
  2. **2608.05757 – "Beyond Relevance: Bayesian Evidence Acquisition for Agentic Whole-Slide Image Reasoning" (BEACON)**; Bryan Wong, Xun Xu, Huazhu Fu, Nancy F. Chen, Mun Yong Yi; 6 Aug 2026; code github.com/bryanwong17/BEACON. Training-free agent that replaces relevance-based patch retrieval with expected-information-gain acquisition over competing diagnostic hypotheses. Low likelihood (method name is BEACON, not "Beyond…"), but it is the closest conceptual sibling. — [arXiv 2608.05757](https://arxiv.org/abs/2608.05757)
  3. **2610.17233 – "Beyond Sparse Captions: Aligning Slide-Level Text and Patch-Level Vision in Pathology" (LIMIT / CONCH-Z)**; Daniel Shao, …, Richard J. Chen, Faisal Mahmood; 12 Oct 2026; "NeurIPS 2026 Spotlight"; code github.com/mahmoodlab/LIMIT. Freezes the vision encoder and fine-tunes only the text encoder on 335k clinical reports, with report embeddings as cross-attention queries over patch bags. A contrastive-pretraining paper, not a WSI-VQA MLLM; low likelihood. — [arXiv 2610.17233](https://arxiv.org/abs/2610.17233)
  4. **2510.23807 – "Beyond the Failures: Rethinking Foundation Models in Pathology"**; Hamid R. Tizhoosh; 27 Oct 2025. Position paper arguing pathology FMs fail from conceptual mismatches. Very low likelihood (not a VLM method). — [arXiv 2510.23807](https://arxiv.org/abs/2510.23807)
  5. Not plausible: 2403.04865 "Beyond Multiple Instance Learning: Full Resolution All-In-Memory End-To-End Pathology Slide Modeling" (2024, not VLM); 2609.05937 "Beyond Classification: Structured Supervision Aligns Visual Evidence with Medical Semantics" (BMVC 2026, general medical ViT pretraining); 2603.08328 "Beyond Attention Heatmaps" (MIL explanation). — [arXiv title search](https://export.arxiv.org/api/query?search_query=ti:Beyond+AND+%28abs:pathology+OR+abs:histopathology+OR+abs:%22whole+slide%22+OR+abs:%22whole-slide%22%29&max_results=200&sortBy=submittedDate&sortOrder=descending)
- The companion names in the researcher's grouping resolve to the same sub-area: SlideBank = "SlideBank: A Persistent Hierarchical Evidence Bank for Consistent Whole-Slide Reasoning" (arXiv 2609.00342); LoC-Path = "LoC-Path: Learning to Compress for Pathology Multimodal Large Language Models" (arXiv 2512.05391, Stony Brook / Harvard); Zeyu Gao co-authors "PathNavigate: A Training-Free Pathology Agent with Surprise-Guided Scan and Shared Slide Memory for Whole-Slide Image VQA" (arXiv 2605.23559) and "Thinking in Scales" (arXiv 2605.19491). — [SlideBank](https://arxiv.org/pdf/2609.00342); [LoC-Path](https://arxiv.org/abs/2512.05391); [PathNavigate](https://arxiv.org/abs/2605.23559); [arXiv author query Zeyu Gao](https://export.arxiv.org/api/query?search_query=au:%22Zeyu+Gao%22+AND+%28abs:pathology+OR+abs:histopathology+OR+abs:%22whole+slide%22+OR+abs:WSI%29&max_results=100&sortBy=submittedDate&sortOrder=descending)

### Inferences
- All four names the researcher grouped (SlideBank, LoC-Path, PathNavigate/Zeyu Gao, BeyondPath) are 2025-12 to 2026-10 papers on *how a gigapixel slide should be presented to an LLM for question answering*; BeyondPath fits the grouping exactly, which raises confidence beyond the name match alone.
- BeyondPath cites PathNavigate (for its BCNB baseline protocol) and HistoSelect (same Stony Brook group as LoC-Path) but not SlideBank or LoC-Path, so the grouping is the researcher's, not the paper's.
- The paper never explains the name "BeyondPath"; it reads as "beyond the question" + "path(ology)".

### Gaps
- No venue, OpenReview page or reviews found; it appears to be a preprint only. A web search for a code repository returned nothing, and the arXiv HTML contains no GitHub/HuggingFace link. Code availability is therefore unconfirmed (probably not released).
- Google Scholar, OpenReview and conference proceedings could not be queried directly; candidate discovery relied on the arXiv API and web search. A non-arXiv paper with a similar name cannot be fully excluded, but nothing suggests one exists.

## What is the problem framing and motivating observation in the introduction?

### Takeaway
The framing is that a question is an *underspecified retrieval key*: it says what must be decided, not which morphology is needed to decide it. So both dominant ways of shrinking a slide for an LLM fail in opposite directions: question-guided selection drops unnamed supporting morphology, and question-agnostic compression dilutes focal evidence. The authors name this the "Relevance–Sufficiency Gap".

### Cited Findings
- Opening observation (abstract): "A question about a whole-slide image rarely names every morphological finding needed to answer it. Question-guided patch selection can therefore overlook supporting morphology, while slide-level compression can dilute focal evidence." — [arXiv 2610.29431](https://arxiv.org/abs/2610.29431)
- Introduction: "a question specifies what must be answered without necessarily naming every morphological finding needed to answer it. A question about tumor grade, for example, may leave the relevant tissue architecture and cellular features implicit. Selecting regions that match the question can thus leave out supporting morphology." — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)
- Diagnosis of existing methods: "Broad compression can dilute small informative regions, whereas question-conditioned selection can omit morphology not explicitly named in the query. Moreover, restricting question-specific retrieval to an already compressed candidate set prevents it from recovering excluded regions." — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)
- The named concept: "These difficulties motivate the Relevance–Sufficiency Gap: question-matched patches may provide an incomplete set of findings for answering the question." — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)
- The pathologist analogy used as design cue: "Broad inspection forms an initial morphological impression; question-directed examination then seeks pertinent findings; and the observed patterns are brought together when interpreting the slide." This "motivates preserving morphology before narrowing attention to a particular question, while keeping further inspection open to regions beyond those initially selected." — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)
- The stated requirement: "Effective WSI-VQA must look beyond the question's explicit cues while remaining focused on the requested decision." — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)
- Scale context: a WSI has "thousands to tens of thousands of foreground patches", which is why prior work uses long-context processing, slide encoders, pooling, resampling and patch selection. — [arXiv HTML §1](https://arxiv.org/html/2610.29431v2)

### Inferences
- The framing is a pathology instance of a general retrieval lesson: *relevance to the query is not sufficiency for the answer* (cf. multi-hop RAG). The paper's novelty is noticing that this bites especially hard in pathology because diagnostic questions are short while the evidence they depend on is compositional (grade = architecture + nuclear features + mitoses; invasion = tumor + stroma relation).
- Three distinct failure modes are identified, and the third is the subtle one: (i) compression dilutes; (ii) question-matching omits; (iii) cascades (compress first, then retrieve inside the compressed set) make omission irreversible. Point (iii) is what rules out the obvious "coarse-to-fine" fix and forces a two-stream design.
- The motivation is argued by example and analogy; the introduction contains no measurement of how often the gap occurs.

### Gaps
- The paper gives no quantitative characterization of the Relevance–Sufficiency Gap itself (e.g., what share of answer-supporting regions lie outside the top-K question-matched patches). Evidence for it is indirect (ablations, four cases).

## What is the central insight (one or two sentences) and the method that follows from it?

### Takeaway
Insight: *the evidence needed to answer a question about a slide is a superset of what the question names, so a slide interface must carry two things at once: a question-agnostic "initial impression" learned to be useful for every question one might ask of that slide, and question-specific evidence retrieved from the whole slide rather than from the compressed impression.* The method (Preserve–Focus–Fuse) is a direct transcription: a cross-question-supervised Morphology Bank, a full-slide question-conditioned retriever, and a fusion step that writes the bank's context into the retrieved evidence positions, giving a 96-token visual prefix.

### Cited Findings
- **Preserve (question-agnostic Morphology Bank).** The selector never sees the question; one Bank per slide is paired with every training question for that slide and the answer losses are averaged ("cross-question answer supervision", Eq. 2). "The selector is therefore question-agnostic by construction, while its Bank learns to support different questions about the same slide." — [arXiv HTML §3.1](https://arxiv.org/html/2610.29431v2)
- Bank structure: six "experts" with fixed quotas of 16 patches each (96 tokens). Four are anchored to tumor, stroma, immune infiltration and necrosis through CONCH text-prompt ensembles; two are "free" experts with no anchor so that answer supervision can retain morphology outside that vocabulary. A soft "presence" estimate interpolates each semantic expert with a learned null bank when the morphology is absent. — [arXiv HTML §3.1, App. A.5, B.3](https://arxiv.org/html/2610.29431v2)
- **Focus (question-conditioned retrieval over everything).** "A Bank learned to support multiple questions can omit a finding required by a particular question. Focus therefore scores all N_s retained foreground patch embeddings for the current question. Its candidate set includes patches both inside and outside the Bank." Score = frozen CONCH image–text cosine similarity plus a learned question–patch compatibility term; top-96 selected. — [arXiv HTML §3.2](https://arxiv.org/html/2610.29431v2)
- **Fuse (MoV, Morphology-on-Visual-Evidence).** Evidence tokens are the queries; expert banks are keys/values in cross-attention; each evidence position has its own gate over the six experts plus a null path. "Direct concatenation would expose 192 tokens to the language model. MoV places morphology updates at the K_q=96 evidence positions." Two blocks; output stays 96 tokens. — [arXiv HTML §3.3, App. B.4](https://arxiv.org/html/2610.29431v2)
- Selection is discrete but trainable: hard top-K in the forward pass, sequential-softmax relaxation in the backward pass (straight-through). — [arXiv HTML §3.1, App. B.2](https://arxiv.org/html/2610.29431v2)
- Two-stage training: Stage I trains Preserve with frozen CONCH and frozen Qwen2.5-7B-Instruct (gradients flow through the frozen LLM to the prefix); Stage II freezes Preserve and trains Focus, MoV, projector and rank-32 LoRA, with an auxiliary Focus-only answer loss sampled with probability 0.5. — [arXiv HTML §3.4, App. A.4](https://arxiv.org/html/2610.29431v2)
- Backbone and inputs: non-overlapping 224×224 patches at 20×, frozen CONCH v1 features (512-d), Qwen2.5-7B-Instruct, three A100-40GB GPUs; trained only on the WSI-Bench training split (9,642 WSIs, 175,450 QA pairs). — [arXiv HTML §4.1, App. A.1, A.4](https://arxiv.org/html/2610.29431v2)
- The closing principle: "look beyond explicit cues: retain broad morphology, seek the findings needed for each question, and bring them together when answering." — [arXiv HTML §5](https://arxiv.org/html/2610.29431v2)

### Inferences
- Why the idea "sounds right":
  1. *It turns an annotation accident into supervision.* WSI-VQA datasets carry many questions per slide (175,450 / 9,642 ≈ 18 per training slide). Treating them as independent samples wastes the fact that they share one slide. Averaging their losses onto one question-blind Bank is multi-task learning of a slide summary that is "sufficient" for the question distribution, a clean operationalization of a pathologist's gestalt.
  2. *It separates two things previously conflated in one token budget*: what the slide is (context) and what this question needs (evidence). Prior single-stream selectors make these compete for the same slots.
  3. *It keeps retrieval lossless with respect to the candidate set.* Focus scans all foreground patches, so nothing the Bank dropped is unrecoverable; this is the direct answer to the cascade failure mode.
  4. *Fusion direction encodes a prior about reasoning*: evidence tokens read context (not vice versa), i.e. "interpret this focal finding in light of the slide's overall morphology", which is how grade or invasion is actually judged.
- The semantic experts (tumor / stroma / immune / necrosis) are a hand-coded prior of what "broad morphology" means; the free experts are the hedge. This is engineering in service of the insight, not the insight itself.
- Conceptual siblings: BEACON's "relevance ≠ diagnostic informativeness" attacks the same assumption from the agentic/Bayesian side; SlideBank's persistent question-independent evidence bank shares the "build the slide's memory before the question arrives" idea. BeyondPath is the trained, single-forward-pass version of that family.

### Gaps
- The paper does not say why the Bank is rebuilt per request rather than cached per slide, although it is question-independent by construction (it only states that the implementation rebuilds it).

## What evidence supports the insight itself (analyses, ablations, surprising findings, key numbers)?

### Takeaway
The insight is supported mainly by same-backbone ablations on WSI-Bench (Avg-9): both streams are needed (0.769 vs 0.721 Focus-only and 0.713 Preserve-only), retrieval must not be confined to the compressed set (0.718), the Bank must be trained on many questions (0.736 → 0.769, monotonic in questions per slide) and must be slide-specific (wrong-slide Bank 0.677), and fusing at evidence positions beats giving the LLM both streams concatenated with twice the tokens (0.769 at 96 tokens vs 0.739 at 192). Headline benchmark margins are modest.

### Cited Findings
- **Complementarity of the two streams:** full model 0.769; Focus only 0.721; Preserve only 0.713; single-stream question-conditioned selector 0.739. — [arXiv HTML Table 4, Table 9](https://arxiv.org/html/2610.29431v2)
- **Cascade failure mode confirmed:** "Bank-restricted Focus" (retrieval limited to patches Preserve selected) scores 0.718, i.e. 0.051 below full-slide Focus. — [arXiv HTML Table 4, App. C.1](https://arxiv.org/html/2610.29431v2)
- **Cross-question supervision dose-response:** Bank trained with 1 / 2 / 4 / all QA pairs per WSI gives 0.736 / 0.749 / 0.758 / 0.769, with slide-level epochs and loss normalization held fixed. — [arXiv HTML Table 9, App. C.1](https://arxiv.org/html/2610.29431v2)
- **Bank content matters (inference-time interventions on the full checkpoint):** random same-slide Bank 0.713; wrong-slide Bank 0.677; random Focus patches (with the correct Bank) 0.682. — [arXiv HTML Table 9, App. C.1](https://arxiv.org/html/2610.29431v2)
- **Fusion form matters more than token count:** MoV 0.769 (96 tokens) vs concatenate + resampler 0.727 (96), direct concatenation 0.739 (192), global-pooled Bank + residual 0.719, uniform expert gate 0.756, shared expert FFN 0.748. — [arXiv HTML Table 9](https://arxiv.org/html/2610.29431v2)
- **Budget saturates early:** tokens per stream 32 / 64 / 96 / 128 / 192 → 0.742 / 0.760 / 0.769 / 0.771 / 0.772; 96→192 adds 0.003 Avg-9 for +25.6% TFLOPs. — [arXiv HTML Table 10, Table 11](https://arxiv.org/html/2610.29431v2)
- **Expert prior:** 2 semantic experts 0.748; 4 semantic / 0 free 0.759; 4/2 (default) 0.769; 4/4 0.767. Removing prompt anchoring (λ_p = 0) gives 0.751; over-weighting it (0.1) gives 0.752. — [arXiv HTML Table 10](https://arxiv.org/html/2610.29431v2)
- **Main results (WSI-Bench VQA, Avg-9, LLM visual tokens):** BeyondPath 0.769 (96); WSI-LLaVA 0.754 (576); MLLM-HWSI 0.745 (1,941); HistoSelect 0.734 (5,000); Quilt-LLaVA 0.721 (576); WSI-VQA 0.590; GPT-4o 0.507; SlideChat 0.495 (20,480). BeyondPath leads WSI-Precision/WSI-Relevance for morphological analysis and diagnosis, but MLLM-HWSI has higher closed-ended accuracy (morphology 0.989 vs 0.945; diagnosis 0.962 vs 0.875). — [arXiv HTML Table 1](https://arxiv.org/html/2610.29431v2)
- **Report generation with the same VQA checkpoint:** leads all eight metrics, e.g. BLEU-4 0.313 vs 0.287 (MLLM-HWSI), WSI-P 0.525 vs 0.447, WSI-R 0.552 vs 0.479. — [arXiv HTML Table 3](https://arxiv.org/html/2610.29431v2)
- **Zero-shot SlideBench-BCNB:** overall 0.639 vs MLLM-HWSI 0.612, HistoSelect 0.558, SlideChat 0.544, WSI-LLaVA 0.527, TITAN 0.444; leads on HER2 expression (0.380), HER2 status (0.763) and molecular subtype (0.344), not on tumor type, ER, PR or grading. The paper itself says "the best-performing model varies by endpoint". — [arXiv HTML Table 2, §4.2](https://arxiv.org/html/2610.29431v2)
- **Cost:** 15.95 GB peak memory and 3.304 TFLOPs at 20,480 patches vs SlideChat 269.80 TFLOPs, HistoSelect 67.80, MLLM-HWSI 28.40, WSI-LLaVA 10.49; latency at 32,768 patches 2.65 s vs 10.72 s for SlideChat (but 2.05 s vs 1.68 s at 1,024 patches). — [arXiv HTML Tables 12–13](https://arxiv.org/html/2610.29431v2)
- **Qualitative cases (pathologist-reviewed, 2 main + 2 appendix):** Nottingham grading where Focus-only says Grade 3, Preserve-only Grade 1, full model the correct Grade 2; invasive ductal carcinoma where Focus-only sees DCIS but "lacks evidence for stromal invasion" and Preserve-only sees invasion but cannot separate ductal from lobular. — [arXiv HTML §4.4, App. E](https://arxiv.org/html/2610.29431v2)

### Inferences
- The most insight-bearing results are the three that are *not* about beating baselines: (a) Bank-restricted Focus (0.718) shows the cascade really loses information; (b) the 1→2→4→all dose-response shows the Bank's value comes from being trained to serve many questions; (c) 96-token MoV beating 192-token concatenation shows the gain is about how context and evidence are related, not about more tokens.
- Surprising and under-discussed: Preserve-only (a question-blind 96-token summary) scores 0.713, nearly the same as question-directed Focus-only (0.721). Either a good question-agnostic summary already answers most WSI-Bench questions (supporting the "broad morphology" half of the thesis) or WSI-Bench is not very sensitive to question-specific retrieval. Random Focus with a correct Bank still reaches 0.682, well above GPT-4o (0.507), which points the same way.
- The DCIS/invasion case is the cleanest illustration of the Relevance–Sufficiency Gap: the question ("histological classification") matches glandular patterns, but the deciding fact (stromal invasion) lives in context the question never names.
- The headline margin is small: +0.015 Avg-9 over WSI-LLaVA, single seed. The ablation deltas (0.03–0.09) are larger than the cross-method margin, so the paper is more convincing as evidence for the decomposition than as a state-of-the-art claim.
- Treatment-planning accuracy values (0.917, 0.958, 0.979, 1.000) are consistent with multiples of 1/48, suggesting about 48 closed-ended test questions in that group; that column is too coarse to discriminate methods, yet it contributes 1/9 of Avg-9.

### Gaps
- No multi-seed variance or confidence intervals for any predictive metric (acknowledged by the authors), so the significance of the 0.015 headline margin and of small ablation gaps (e.g. 0.765 vs 0.769) is unknown.
- No direct test of whether Focus actually retrieves patches *outside* the Bank in practice (overlap statistics between Bank and Focus selections are not reported).
- No evaluation of selection quality against expert-annotated regions.

## Limitations, unstated assumptions, weak points, and open questions

### Takeaway
The authors concede single-seed results, one backbone, one magnification, one external cohort, unverified patch localizations, and that retrieval still scans every patch. Beyond that, the central claim rests on indirect evidence, the "Bank" is a learned hand-structured prior tied to a four-term tumor-centric vocabulary, and the benchmark (WSI-Bench) may not stress the gap the paper is about.

### Cited Findings
- Author-stated limitations: retrospective public cohorts with external transfer only on SlideBench-BCNB; "one CONCH–Qwen configuration and a single 20× scale"; "All reported training and evaluation runs use random seed 42; we do not report multi-seed performance variance or confidence intervals". — [arXiv HTML App. F](https://arxiv.org/html/2610.29431v2)
- "the selected patches are not pathologist-verified localizations… selections across the full test set have not been systematically validated against expert-annotated regions. The resulting correspondence is functional, not a claim of clinical equivalence to expert review." — [arXiv HTML App. F](https://arxiv.org/html/2610.29431v2)
- "Focus scans all retained foreground patches per question, so the 96-token fused prefix reduces decoder context rather than slide-wide retrieval cost; Focus is compact at the language interface but not a substitute for efficient slide indexing." — [arXiv HTML App. F](https://arxiv.org/html/2610.29431v2)
- The Bank is recomputed for every request: "no Bank is cached across questions". — [arXiv HTML App. B.5](https://arxiv.org/html/2610.29431v2)
- Parameter sweeps (budget, depth, experts, λ_p, τ_q) are reported on the *test* split "descriptively"; the paper states they were not used for checkpoint selection. — [arXiv HTML §4.1, Table 10](https://arxiv.org/html/2610.29431v2)
- General-purpose baselines on BCNB (GPT-4o, GPT-5.4, Gemini-3.1-Pro-preview, Qwen3.5) were fed one slide thumbnail per question and are "local or reproduced evaluations", not published scores. — [arXiv HTML App. A.3](https://arxiv.org/html/2610.29431v2)
- Open-ended metrics WSI-P and WSI-R are computed with GPT-4o claim-scoring prompts released with WSI-LLaVA. — [arXiv HTML App. A.4](https://arxiv.org/html/2610.29431v2)
- Absolute patch coordinates are kept only for visualization: "absolute coordinates are not encoded into the model." — [arXiv HTML §3](https://arxiv.org/html/2610.29431v2)
- Semantic experts are fixed to tumor, stroma, immune infiltration, necrosis prompt ensembles. — [arXiv HTML App. A.5, Table 7](https://arxiv.org/html/2610.29431v2)

### Inferences
- **Unstated assumption 1: the training question set spans what users will ask.** "Question-agnostic" really means "agnostic within the WSI-Bench question distribution" (morphology, diagnosis, treatment planning on TCGA tumors). A Bank trained by cross-question supervision is only as general as the questions; rare-finding or non-tumor questions may fall to Focus alone.
- **Unstated assumption 2: top-K patches by a text-anchored router equal "broad morphology".** Sixteen patches per expert is a sparse sample; nothing enforces spatial coverage, and there is no spatial or multi-scale modelling (no coordinates, single 20× scale), so architecture-level patterns larger than a patch are represented only implicitly.
- **Unstated assumption 3: 96+96 patches at 20× suffice.** For needle-in-haystack tasks (micrometastasis, rare mitoses) a fixed top-K retriever driven by CONCH similarity is unlikely to be sufficient; the benchmarks used do not test this.
- **Weak point: the ablation that should isolate "two streams vs one" is ambiguous.** "Single-stream scoring" (0.739) and "Focus only" (0.721) are both described as 96 question-selected tokens without a Bank, yet differ by 0.018; the paper does not explain the difference in training that produces this gap. The fairest single-stream comparator is therefore unclear; against 0.739 the two-stream gain is 0.030, not 0.048.
- **Weak point: intervention ablations are out-of-distribution for the trained fuser.** Random or wrong-slide Banks are swapped in at inference into a MoV trained to trust the Bank, so the drops (0.713, 0.677) partly measure sensitivity to corrupted input rather than the information value of the Bank. Preserve-only vs full (0.713 vs 0.769) is the cleaner number.
- **Weak point: benchmark fit.** WSI-Bench answers derive from slide-level report content, so slide-gestalt goes a long way (Preserve-only 0.713; random Focus 0.682). The Relevance–Sufficiency Gap would be more convincingly shown on a benchmark requiring spatially localized multi-step evidence.
- **Weak point: the pathologist analogy is loose.** Real review is iterative (impression → look → revise impression → look again); BeyondPath is one-shot with a frozen impression. Agentic systems (PathNavigate, BEACON, SlideBank) keep the loop; BeyondPath trades it for a single cheap forward pass.
- **Open questions:** (1) Can the Bank be cached per slide and reused across a dialogue, as SlideBank does, given that it is question-independent? (2) Does cross-question supervision still help when questions are few or homogeneous? (3) Would making the Bank's content inspectable (text descriptions, coordinates) add verifiability? (4) How should Focus be made sub-linear (indexing) without reintroducing the cascade problem? (5) Does the two-stream advantage persist with a stronger slide encoder (TITAN-class) supplying the "impression"?

### Gaps
- Whether WSI-Bench QA pairs are LLM-generated from TCGA reports was not re-verified in this session (it is my recollection of the WSI-LLaVA paper); treat the "benchmark fit" criticism as an inference to check against [WSI-LLaVA](https://arxiv.org/abs/2412.02141).
- No third-party commentary, reviews or replications of BeyondPath were found; all assessments of weak points above are my own reading.

## Positioning relative to prior pathology VLMs (CONCH, PLIP, PathChat, SlideChat, PRISM, TITAN, WSI-LLaVA, CPath-Omni, Quilt-LLaVA)

### Takeaway
BeyondPath positions itself not as a new foundation model but as a new *slide-to-LLM interface*: it reuses frozen CONCH features and a general LLM, and argues that prior WSI MLLMs each pick one side of a false choice (compress everything: SlideChat, WSI-LLaVA, CPath-Omni, TITAN; or select by question: HistoSelect). PathChat and PRISM are neither cited nor compared.

### Cited Findings
- CONCH and PLIP are cited as the image–text pretraining that pathology assistants build on; CONCH v1 is BeyondPath's frozen patch encoder and its text encoder supplies both the question embedding for Focus and the prompt anchors for the semantic experts. — [arXiv HTML §2, §3, §4.1](https://arxiv.org/html/2610.29431v2)
- Quilt-LLaVA and LLaVA-Med are described as improving representation learning and language interaction, "but WSI-VQA also requires organizing slide-level morphological evidence for each question." As a baseline Quilt-LLaVA (576 tokens) scores 0.721 Avg-9 and 0.341 on BCNB. — [arXiv HTML §2, Tables 1–2](https://arxiv.org/html/2610.29431v2)
- SlideChat: "encodes long patch sequences with LongNet"; listed at 20,480 LLM visual tokens, 0.495 Avg-9 on WSI-Bench, 0.544 on BCNB, 269.80 TFLOPs. — [arXiv HTML §2, Tables 1, 2, 12](https://arxiv.org/html/2610.29431v2)
- WSI-LLaVA: "aligns global slide representations with text"; 576 tokens, 0.754 Avg-9 (the strongest prior baseline on WSI-Bench), 0.527 on BCNB. — [arXiv HTML §2, Tables 1–2](https://arxiv.org/html/2610.29431v2)
- CPath-Omni: "combines multiscale regional pooling with learned query-token compression"; discussed in related work only, no numbers reported. — [arXiv HTML §2](https://arxiv.org/html/2610.29431v2)
- TITAN: appears only as a zero-shot BCNB baseline (overall 0.444). — [arXiv HTML Table 2](https://arxiv.org/html/2610.29431v2)
- HistoSelect ("Act like a pathologist: Tissue-aware whole slide image reasoning", CVPR 2026, from the Stony Brook group behind LoC-Path) is the nearest prior: it "draws inspiration from pathological slide review and retrieves evidence through a question-guided group sampler followed by patch selection within selected tissue regions." BeyondPath's stated difference: a separate Bank learned from answers across a slide's questions, a retriever that "scores the full foreground set", and fusion at evidence positions. HistoSelect scores 0.734 Avg-9 with 5,000 tokens. — [arXiv HTML §2, Table 1](https://arxiv.org/html/2610.29431v2)
- MLLM-HWSI (CVPR 2026; 1,941 tokens) is the strongest competitor on closed-ended accuracy and several BCNB endpoints (tumor type 0.980, ER 0.793, PR 0.796) but trails on Avg-9 (0.745) and BCNB overall (0.612). — [arXiv HTML Tables 1–2](https://arxiv.org/html/2610.29431v2)
- Versus general visual-token pruning (FastV, PACT, DivPrune, CDPruner, ToDRE): "These methods primarily express context and question evidence through one reduced stream or through a staged candidate set. Our focus is the organization of morphological evidence under a fixed language-side token budget." — [arXiv HTML §2](https://arxiv.org/html/2610.29431v2)
- A text search of the full paper finds no mention of PathChat, PRISM, SlideBank or LoC-Path. — [arXiv HTML 2610.29431v2](https://arxiv.org/html/2610.29431v2)
- For context on the two neighbours in the researcher's grouping: LoC-Path replaces the heavy slide-level encoder with redundancy-reducing compression modules (Sparse Token Merger, MAE-pretrained resampler, token importance scorer); SlideBank stores a WSI as a persistent, concept-indexed, spatially grounded evidence bank reusable across questions. — [LoC-Path arXiv 2512.05391](https://arxiv.org/abs/2512.05391); [SlideBank arXiv 2609.00342](https://arxiv.org/pdf/2609.00342)

### Inferences
- A useful map of the design space the paper implies:
  - *Question-agnostic compression only*: SlideChat (long sequence), WSI-LLaVA / TITAN / PRISM-style slide encoders, CPath-Omni pooling, LoC-Path learned compression. Risk: dilution of focal evidence.
  - *Question-conditioned selection only*: HistoSelect, generic instruction-aware pruning, relevance-driven agents. Risk: omission of unnamed supporting morphology.
  - *Both, decoupled, fused*: BeyondPath (trained, one pass); SlideBank and PathNavigate reach a similar "slide memory + question-time lookup" split in training-free agentic form.
- Relative to LoC-Path, the insight is complementary rather than competing: LoC-Path says "slides are redundant, so learn to compress"; BeyondPath says "compression alone is the wrong objective because what to keep depends on a question you have not seen, so keep a question-robust summary *and* leave the full slide open to retrieval".
- BeyondPath's contribution is orthogonal to encoder quality: it holds CONCH features fixed across all ablations, so its claims are about evidence organization. It does not show that the same gain holds on top of slide-level foundation models (TITAN, PRISM).
- Not comparing against PathChat / PRISM / CPath-Omni numerically is unsurprising (closed weights or ROI-level models) but leaves the positioning against Mahmood-lab and Paige systems unargued.

### Gaps
- No head-to-head comparison between BeyondPath and SlideBank, LoC-Path or PathNavigate on a shared benchmark and protocol was found; BeyondPath reports only that its thumbnail-baseline BCNB scores "agree, after rounding" with PathNavigate's.
- Because no code or checkpoints were found, the baseline numbers for HistoSelect and MLLM-HWSI on WSI-Bench could not be traced to their original papers in this session; the BeyondPath paper says published baseline results "follow their respective official protocols".

## Appendix-style note: the runner-up candidate BEACON ("Beyond Relevance", arXiv 2608.05757)

### Takeaway
If the researcher did not mean BeyondPath, BEACON is the only other "Beyond …" paper with a comparable insight-first pitch in WSI reasoning: semantic relevance is not diagnostic informativeness, so an agent should pick patches by expected information gain over competing diagnoses. Only abstract, introduction and conclusion were read.

### Cited Findings
- Core claim: relevance-based strategies "implicitly assume that semantically relevant patches are diagnostically informative. This assumption often fails in computational pathology, where competing diagnostic hypotheses may exhibit similar and overlapping morphological patterns… causing many patches to appear relevant while providing limited evidence for differentiating among them." — [arXiv HTML 2608.05757 §1](https://arxiv.org/html/2608.05757v1)
- Reframing: "the central challenge in agentic WSI reasoning is not merely to narrow the search space based on semantic relevance but to identify observations that are expected to reduce diagnostic uncertainty"; patch acquisition is cast as Bayesian experimental design with a belief over hypotheses and EIG scoring, plus an evidence controller (answer / acquire more / zoom). Training-free, built from off-the-shelf models; evaluated zero-shot on five WSI-VQA benchmarks; code at github.com/bryanwong17/BEACON. — [arXiv abs 2608.05757](https://arxiv.org/abs/2608.05757)

### Inferences
- BEACON and BeyondPath criticize the same hidden assumption (question relevance as the selection criterion) with different remedies: BEACON changes the *criterion* (discriminativeness between hypotheses); BeyondPath changes the *architecture* (add a question-blind stream). They are compatible.

### Gaps
- BEACON's experiments, ablations and limitations were not read; no numbers are reported here.
