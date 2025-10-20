# Awesome Biopharma Foundation Models [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of foundation models and AI/ML tools for biopharma applications, including drug discovery, antibody design, genomics, and protein engineering.

## 📋 Table of Contents

- [Genomic & Target Analysis](#genomic--target-analysis)
- [Antibody Sequence Modeling](#antibody-sequence-modeling)
- [Antibody Structure Prediction](#antibody-structure-prediction)
- [Generative Antibody Design](#generative-antibody-design)
- [Small Molecule & Linker Design](#small-molecule--linker-design)
- [Integrated ADC & Complex Prediction](#integrated-adc--complex-prediction)
- [Contributing](#contributing)
- [License](#license)

---

## Genomic & Target Analysis

Foundation models for analyzing genomic data, transcriptomics, and identifying therapeutic targets.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **Geneformer** | In silico gene perturbation, target discovery, cell-type classification | Transformer Encoder (BERT-style) | Single-cell transcriptomes (Rank-Value Encoding) | [GitHub](https://github.com/ctheodoris/Geneformer) | [Theodoris et al., Nature (2023)](https://www.nature.com/articles/s41586-023-06139-9) |
| **Bulkformer** | Prognosis modeling, drug response prediction, transcriptome imputation | Hybrid GNN & Performer | Bulk transcriptomes (Continuous Expression Values) | [GitHub](https://github.com/KangBoming/BulkFormer) | [Kang et al., bioRxiv (2025)](https://www.biorxiv.org/content/10.1101/2025.01.04.631088v1) |
| **scGPT** | Multi-omic integration, cell-type annotation, perturbation prediction | Generative Pre-trained Transformer (GPT) | Single-cell multi-omics (Cell x Gene Matrix) | [GitHub](https://github.com/bowang-lab/scGPT) | [Cui et al., Nat Methods (2024)](https://www.nature.com/articles/s41592-024-02201-0) |
| **scBERT** | High-accuracy cell type annotation | Transformer Encoder (BERT-style) | Single-cell transcriptomes | [GitHub](https://github.com/TencentAILabHealthcare/scBERT) | [Yang et al., Nat Mach Intell (2022)](https://www.nature.com/articles/s42256-022-00534-z) |
| **Nicheformer** | Spatial composition and label prediction, integrating spatial context | Transformer | Dissociated single-cell & spatial transcriptomics | Not publicly available | [Kubler et al., bioRxiv (2024)](https://www.biorxiv.org/content/10.1101/2024.03.12.584114v1) |
| **TranscriptFormer** | Cross-species cell type classification and annotation transfer | Generative Transformer | Single-cell transcriptomes (multi-species) | Not publicly available | [He et al., bioRxiv (2025)](https://www.biorxiv.org/content/10.1101/2025.01.10.632323v1) |
| **DeepSomatic** | Somatic small variant calling from tumor-normal or tumor-only data | Convolutional Neural Network (CNN) | Aligned reads (BAM/CRAM) | [GitHub](https://github.com/google/deepsomatic) | [Shafin et al., bioRxiv (2024)](https://www.biorxiv.org/content/10.1101/2024.08.23.609422v1) |
| **FluxRETAP** | Suggests metabolic engineering targets to increase metabolite production | Constraint-Based Algorithm (COBRA/FBA) | Genome-Scale Models (GSMs) | [GitHub](https://github.com/JBEI/FluxRETAP) | [Czajka et al., Bioinformatics (2025)](https://academic.oup.com/bioinformatics/article/41/1/btae778/7934754) |
| **GeneGPT** | Answering genomics questions by augmenting LLMs with NCBI APIs | LLM (Codex) + API Integration | Natural language questions | [GitHub](https://github.com/ncbi/GeneGPT) | [Jin et al., Bioinformatics (2024)](https://academic.oup.com/bioinformatics/article/40/7/btae075/7612193) |

---

## Antibody Sequence Modeling

Models for analyzing, embedding, and understanding antibody sequences.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **AbLang** | Sequence completion, generating embeddings and likelihoods | RoBERTa | Unpaired Antibody Sequences | [GitHub](https://github.com/oxpig/AbLang) | [Olsen et al., Bioinformatics Advances (2022)](https://academic.oup.com/bioinformaticsadvances/article/2/1/vbac046/6609807) |
| **AntiBERTy** | Generating embeddings, mask filling, sequence classification | BERT | Unpaired Antibody Sequences | [GitHub](https://github.com/jeffreyruffolo/AntiBERTy) | [Ruffolo et al., arXiv (2021)](https://arxiv.org/abs/2112.07782) |
| **BALM** | Function prediction, structure prediction (BALMFold), embeddings | ESM-based | Unpaired Antibody Sequences | [GitHub](https://github.com/BEAM-Labs/BALM) | [Jing et al., Brief Bioinform (2024)](https://academic.oup.com/bib/article/25/6/bbae481/7801513) |
| **IgT5** | Paired sequence encoding, property prediction (affinity, expression) | T5 (Transformer) | Paired & Unpaired Antibody Sequences | [HuggingFace](https://huggingface.co/Exscientia/IgT5) | [Kenlay et al., PLoS Comput Biol (2024)](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1012446) |
| **IgBLAST** | Germline V(D)J gene alignment and annotation | BLAST Algorithm | FASTA (Nucleotide or Protein) | [GitHub](https://github.com/ncbi/igblast) | [Ye et al., Nucleic Acids Res (2013)](https://academic.oup.com/nar/article/41/W1/W34/1079645) |
| **MiXCR** | Immune repertoire profiling from raw FASTQ data | Java-based pipeline | FASTQ files | [GitHub](https://github.com/milaboratory/mixcr) | [Bolotin et al., Nat Methods (2015)](https://www.nature.com/articles/nmeth.3364) |
| **ANARCI** | Applies standardized numbering schemes (Kabat, IMGT, etc.) | Hidden Markov Models (HMMER) | FASTA (Amino Acid) | [GitHub](https://github.com/oxpig/ANARCI) | [Dunbar & Deane, Bioinformatics (2016)](https://academic.oup.com/bioinformatics/article/32/2/298/1743894) |
| **KA-Search** | Rapid sequence identity search across billion-scale antibody databases | Optimized Search Algorithm | FASTA (Amino Acid) | Not available | [Wong et al., bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.04.26.489511v1) |

---

## Antibody Structure Prediction

Models for predicting 3D structures of antibodies and related immune receptors.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **IgFold** | Rapid prediction of antibody and nanobody structures | Deep Learning (AntiBERTy embeddings) | Paired Heavy/Light Sequences | [GitHub](https://github.com/Graylab/IgFold) | [Ruffolo et al., Nat Commun (2023)](https://www.nature.com/articles/s41467-023-38063-x) |
| **ABodyBuilder2** | High-accuracy prediction of antibody Fv region structure | Deep Learning | Paired Heavy/Light Sequences | [GitHub](https://github.com/oxpig/ImmuneBuilder) | [Abanades et al., Commun Biol (2023)](https://www.nature.com/articles/s42003-023-04927-7) |
| **ImmuneBuilder** | Suite for predicting structures of antibodies, nanobodies, and TCRs | Deep Learning | Paired/Unpaired Immune Receptor Sequences | [GitHub](https://github.com/oxpig/ImmuneBuilder) | [Abanades et al., Commun Biol (2023)](https://www.nature.com/articles/s42003-023-04927-7) |
| **Ibex** | Pan-immunoglobulin structure prediction (Ab, Nb, TCR) for apo/holo states | Deep Learning (AlphaFold2-based) | Paired/Unpaired Immune Receptor Sequences | [GitHub](https://github.com/prescient-design/ibex) | [Kenlay et al., arXiv (2025)](https://arxiv.org/abs/2501.02517) |
| **AlphaFold2** | State-of-the-art, high-accuracy prediction of protein structures | Deep Neural Network (Evoformer) | Multiple Sequence Alignments (MSAs) & templates | [GitHub](https://github.com/deepmind/alphafold) | [Jumper et al., Nature (2021)](https://www.nature.com/articles/s41586-021-03819-2) |
| **RoseTTAFold** | High-accuracy prediction of protein structures and complexes | Three-track Neural Network | MSAs | [GitHub](https://github.com/RosettaCommons/RoseTTAFold) | [Baek et al., Science (2021)](https://www.science.org/doi/10.1126/science.abj8754) |
| **ESMFold** | End-to-end, single-sequence protein 3D structure prediction | ESM-2 Protein Language Model | Single Protein Sequence | [GitHub](https://github.com/facebookresearch/esm) | [Lin et al., Science (2023)](https://www.science.org/doi/10.1126/science.ade2574) |
| **OmegaFold** | High-resolution structure prediction from a single primary sequence | Protein Language Model + Geoformer | Single Protein Sequence | [GitHub](https://github.com/HeliXonProtein/OmegaFold) | [Wu et al., bioRxiv (2022)](https://www.biorxiv.org/content/10.1101/2022.07.21.500999v1) |

---

## Generative Antibody Design

Models for designing novel antibody sequences and structures de novo.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **p-IgGen** | De novo generation of paired antibody sequences | Autoregressive Transformer (GPT-like) | (Optional) Paired Antibody Sequences | [GitHub](https://github.com/oxpig/p-IgGen) | [Turnbull et al., Bioinformatics (2024)](https://academic.oup.com/bioinformatics/article/40/6/btae278/7667098) |
| **RFantibody** | Structure-based de novo antibody design against a specific epitope | RFdiffusion + ProteinMPNN | Target epitope structure | [GitHub](https://github.com/RosettaCommons/RFantibody) | [Bennett et al., bioRxiv (2025)](https://www.biorxiv.org/content/10.1101/2025.01.08.631944v1) |
| **IgLM** | Generative design and infilling of antibody sequences (e.g., CDRs) | Language Model (GPT-2-like) | Antibody Sequences | [GitHub](https://github.com/Graylab/IgLM) | [Ruffolo et al., Cell Systems (2023)](https://www.cell.com/cell-systems/fulltext/S2405-4712(23)00003-6) |
| **Germinal** | Epitope-targeted de novo antibody design with high success rates | Design Pipeline (Structure Predictor + PLM) | Epitope structure | [GitHub](https://github.com/SantiagoMille/germinal) | [Santiago et al., bioRxiv (2025)](https://www.biorxiv.org/content/10.1101/2025.01.09.632111v1) |
| **FAbCon** | De novo design and antigen binding prediction | Generative Transformer (Falcon-based) | Antibody Sequences | [HuggingFace](https://huggingface.co/alchemab/fabcon-small) | [Leem et al., ICML (2024)](https://icml.cc/virtual/2024/poster/33582) |
| **IgGM** | Multi-task generative design (de novo, affinity maturation, humanization) | Generative Foundation Model | Antigen/Epitope structure, Antibody sequence | [GitHub](https://github.com/TencentAI4S/IgGM) | [Wang et al., ICLR (2025)](https://openreview.net/forum?id=LYNceIgPXE) |
| **ESM-IF1** | Inverse folding: designing a sequence for a given protein backbone | GVP-GNN | Protein structure coordinates | [GitHub](https://github.com/facebookresearch/esm) | [Hsu et al., ICML (2022)](https://proceedings.mlr.press/v162/hsu22a.html) |
| **ProteinMPNN** | High-fidelity sequence design for a given protein backbone structure | Graph Neural Network | Protein backbone structure (PDB) | [GitHub](https://github.com/dauparas/ProteinMPNN) | [Dauparas et al., Science (2022)](https://www.science.org/doi/10.1126/science.add2187) |

---

## Small Molecule & Linker Design

Models for designing small molecules, linkers, and predicting molecular properties.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **DrugEx v3** | Scaffold-constrained de novo small molecule design | Graph Transformer + Reinforcement Learning | SMILES strings | [GitHub](https://github.com/CDDLeiden/DrugEx) | [Liu et al., J Cheminform (2023)](https://jcheminf.biomedcentral.com/articles/10.1186/s13321-023-00712-1) |
| **REINVENT4** | De novo design, scaffold hopping, R-group replacement, linker design | RNN/Transformer + Reinforcement Learning | SMILES strings | [GitHub](https://github.com/MolecularAI/REINVENT4) | [Atz et al., ChemRxiv (2024)](https://chemrxiv.org/engage/chemrxiv/article-details/65e1706fe9ebbb4db91f8861) |
| **Drugsniffer** | Virtual screening of billion-scale small molecule libraries | Nextflow Workflow | Protein Structure (PDB) + SMILES library | [GitHub](https://github.com/TravisWheelerLab/drug-sniffer) | [Venkatraman et al., Front Pharmacol (2022)](https://www.frontiersin.org/articles/10.3389/fphar.2022.855036/full) |
| **Linker-GPT** | Generative design of novel linkers for Antibody-Drug Conjugates | Transformer (GPT-based) + Reinforcement Learning | SMILES strings | [GitHub](https://github.com/su-group/Linker-GPT) | [Su et al., Sci Rep (2025)](https://www.nature.com/articles/s41598-024-81397-9) |
| **LigUnity** | Binding affinity prediction for virtual screening and lead optimization | Foundation Model (details proprietary) | Protein pockets, Ligand structures | [GitHub](https://github.com/IDEA-XL/LigUnity) | [Feng et al., bioRxiv (2025)](https://www.biorxiv.org/content/10.1101/2025.01.08.631939v1) |
| **MMELON** | Multi-view embeddings for molecular property prediction | Multi-modal (Image, Graph, Text) | SMILES strings | [GitHub](https://github.com/BiomedSciAI/biomed-multi-view) | [A. C. et al., arXiv (2024)](https://arxiv.org/abs/2406.09028) |
| **SMILES-Mamba** | ADMET property prediction | Mamba Architecture | SMILES strings | Not publicly available | [Li et al., arXiv (2024)](https://arxiv.org/abs/2409.13696) |

---

## Integrated ADC & Complex Prediction

Models for predicting properties of complete antibody-drug conjugates and biomolecular complexes.

| Model | Primary Use Case | Architecture | Input Type | Links | Key Paper |
|-------|-----------------|--------------|------------|-------|-----------|
| **ADCNet** | Predicts anticancer activity of a complete ADC construct | Multi-channel DNN (ESM-2, FG-BERT) | Multi-modal (Protein Sequences, SMILES, DAR) | [GitHub](https://github.com/idrugLab/ADCNet) | [Chen et al., arXiv (2024)](https://arxiv.org/abs/2409.16577) |
| **Boltz** | Prediction of biomolecular complex structures and binding affinities | Deep Learning (AlphaFold3-like) | Multi-modal (Sequences, SMILES) | [GitHub](https://github.com/jwohlwend/boltz) | [Wohlwend et al., bioRxiv (2024)](https://www.biorxiv.org/content/10.1101/2024.11.19.624167v1) |

---

## Contributing

Contributions are welcome! If you know of a foundation model or AI tool relevant to biopharma that's not listed here, please submit a pull request. Please ensure:

- The model/tool is publicly documented (paper, preprint, or documentation)
- You include the primary use case, architecture type, and relevant links
- You maintain the existing table format

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

---

**Last Updated:** October 2025

*Maintained by the Vaibhav Kulkarni. Star ⭐ this repository if you find it useful!*
