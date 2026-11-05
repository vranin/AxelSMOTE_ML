**AxelSMOTE: Axelrod-Guided Synthetic Oversampling for Imbalanced Learning**

**📌 Project OverviewIn** real-world machine learning tasks (e.g., medical diagnoses, software defect prediction), dataset imbalance causes standard classifiers to bias toward the majority class while failing to spot critical minority-class instances.AxelSMOTE is a novel synthetic oversampling framework inspired by Axelrod's Cultural Dissemination Model. Rather than relying purely on simple distance interpolation, AxelSMOTE models feature interaction using:Feature Grouping & Trait Alignment: Partitioning features to compute structured similarity.Probabilistic Feature Exchange: Exchanging feature traits based on agent similarity thresholds.Gaussian Noise Injection: Adding slight variance to prevent deterministic over-fitting along exact linear interpolation lines.📊 Key Results & Comparative SummaryThe framework was benchmarked against standard SMOTE and Class Weight approaches across four real-world datasets (Wisconsin Breast Cancer, KC1, ADS, ILPD) using Logistic Regression, Random Forest, and Support Vector Machines (SVM) across 10 random seeds.MethodMinority F1-ScoreMinority PrecisionMinority RecallPR-AUCAvg Execution Time (s)Class Weight0.7066——0.73320.74Standard SMOTE0.7082—0.8390—1.09AxelSMOTE (Proposed)0.71110.6464——4.31Key TakeawaysClassification Balance: AxelSMOTE achieved the highest overall Minority F1-Score (0.7111) and Precision (0.6464), making it effective at reducing false positive rates in rare event detection.Computational Cost: AxelSMOTE takes ~4.31 seconds per run due to feature-matching and similarity calculations, introducing a speed-vs-precision trade-off compared to basic SMOTE (1.09s).

**📁 Repository StructurePlaintext.**
├── appendix/                   # Supplemental sections & SDG goal mappings
├── chapters/
│   ├── chapter1_introduction.tex         # Background, problem statement, & objectives
│   ├── chapter2_literature_review.tex    # Literature review (SMOTE, ADASYN, Axelrod)
│   ├── chapter3_proposed_methodology.tex # AxelSMOTE algorithm formulation
│   ├── chapter4_system_design.tex        # System architecture & pipeline
│   ├── chapter5_implementation.tex       # Experimental setup & parameters
│   ├── chapter6_results_discussion.tex   # Quantitative evaluation & benchmarking
│   └── chapter7_conclusion.tex           # Findings, limitations, & future work
├── figures/                    # System diagrams & performance plots
├── frontmatter/                # Title page, abstract, certificate, logbook
├── main.tex                    # Master LaTeX file
├── project_details.tex         # Team info, supervisor, & course details
└── references.bib              # BibTeX citation database
**
**🛠️ Installation & Setup1****. Running the LaTeX Documentation (Overleaf / Local TeX)Overleaf: Import this repository as a .zip or link it directly to your GitHub repository. Ensure the compiler is set to pdfLaTeX or XeLaTeX with main.tex marked as the root document.Local LaTeX Engine:Bashpdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
🔬 AxelSMOTE Core Pipeline AlgorithmPlaintextInput: Minority Class Samples (S_min), Similarity Threshold (θ), Noise Factor (σ)
Output: Synthetic Minority Samples (S_synth)

1. Group input features into trait vectors.
2. For each sample x_i in S_min:
    a. Find k-nearest neighbors in S_min.
    b. Compute cultural/trait similarity S(x_i, x_j).
    c. If S(x_i, x_j) >= θ:
        i. Perform probabilistic feature exchange between x_i and x_j.
        ii. Inject small Gaussian noise N(0, σ^2).
    d. Append generated sample to S_synth.
3. Return S_synth.
🎯 Sustainable Development Goals (SDGs)This research aligns with the following UN Sustainable Development Goals:SDG 3: Good Health & Well-being: Enhanced diagnostic precision on medical datasets like Wisconsin Breast Cancer and ILPD.SDG 8: Decent Work & Economic Growth: Improved automated software bug prediction (KC1 dataset).SDG 9: Industry, Innovation & Infrastructure: Advanced algorithmic techniques for imbalanced datasets.
**📜 Authors & AcknowledgmentsDepartment: Department of AI & DS,
VESITProject Type: Mini Project Report**
