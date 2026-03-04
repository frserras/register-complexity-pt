# Compression-based Language Complexity under Register Variation in Portuguese

![Python](https://img.shields.io/badge/Python-3.11%2B-yellow) ![License](https://img.shields.io/badge/License-MIT-green)

This repository contains the companion code, experiment scripts and plots for the paper **"Compression-based Language Complexity under Register Variation in Portuguese"**, accepted for publication at the **17th International Conference on Computational Processing of Portuguese (PROPOR 2026)**.

## 📄 Abstract

Compression-based language complexity metrics show promise as holistic parameters for measuring linguistic complexity across intra- and cross-linguistic scenarios. Yet, their sensitivity to specific forms of linguistic variation requires further experimental validation. We examine the sensitivity of this metric family to register variation in Portuguese, a phenomenon already established for English. Using a robust statistical methodology, we evaluate both the individual and joint sensitivity of these metrics at the sentence level. Our results confirm they are highly sensitive to functional variation in Portuguese, exhibiting the same morphosyntactic trade-off found in English and in cross-linguistic studies.


## 💻 Usage

To reproduce the experiments, please follow the setup instructions below. This project uses [uv](https://docs.astral.sh/uv/) for fast dependency management and environment setup via `pyproject.toml`.

### 1. Setup

First, clone this repository and navigate into it:

```bash
git clone https://github.com/frserras/register-complexity-pt
cd register-complexity-pt

```

**External Dependency**
This project relies on the `lang_complexity` library. You must clone it directly into the repository root:

```bash
# Clone the library into the current directory
git clone https://github.com/frserras/lang_complexity

```

**Install Dependencies**
Use `uv` to automatically create the virtual environment and install all dependencies defined in `pyproject.toml`:

```bash
uv sync

```

### 2. Running the Experiments

Activate the virtual environment created by `uv`:

```bash
# On macOS/Linux:
source .venv/bin/activate

# On Windows:
.venv\Scripts\activate

```

The experiments are structured as a sequence of Jupyter Notebooks. **Please run them in the following strict order**, as each step generates data required by the subsequent ones:

1. **`00_data_preliminary_analysis.ipynb`**: Performs initial data analysis to set up build parameters.
2. **`01_build_dataset.ipynb`**: Builds the dataset of pseudo-documents used for the experiments.
3. **`02_base_experiments.ipynb`**: Runs the core variance experiments.
4. **`03_anova.ipynb`**: Performs Univariate ANOVA on the experiment results.
5. **`04_correlation_manova_and_lda.ipynb`**: Performs MANOVA and follow-up LDA analysis.


## 📊 Data

The experiments use the [carol-domain-sents](https://huggingface.co/datasets/carolina-c4ai/carol-domain-sents) dataset, based on the [Carolina Corpus](https://huggingface.co/datasets/carolina-c4ai/corpus-carolina). See [Automatic Analysis and Classification of Discourse Domains in Brazilian Portuguese ](https://doi.org/10.21814/lm.17.2.476) for Details


## 🔗 Citation

This paper has been accepted for **PROPOR 2026**. If you use this code or findings in your research, please cite it as follows:

```bibtex
@inproceedings{serras2026compression,
  title={Compression-based Language Complexity under Register Variation in Portuguese},
  author={Serras, Felipe Ribas and Finger, Marcelo},
  booktitle={Proceedings of the 17th International Conference on Computational Processing of Portuguese (PROPOR)},
  year={2026},
  publisher = "Association for Computational Lingustics",
  note={To appear}

```
This reference will be updated after the publication of the proceedings.

## 📜 License

This project is licensed under the MIT License. See [LICENSE](LICENSE)
