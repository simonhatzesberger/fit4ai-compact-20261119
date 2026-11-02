# Fit4AI compact – companion notebooks (Zurich, 19/20 November 2026)

Companion code for the **European Actuarial Academy (EAA)** in-house seminar **“Fit4AI compact”** for the Swiss Association of
Actuaries (SAV), Zurich, 19/20 November 2026. Lecturers: **Dr Simon Hatzesberger** and **Dr Johannes Schupp**.

The notebooks accompany the seminar modules. They favour small, transparent implementations with
[NumPy](https://numpy.org/), [pandas](https://pandas.pydata.org/) and [scikit-learn](https://scikit-learn.org/), so that you can
follow every step from the slides – with actuarial and insurance examples throughout. All notebooks are saved **with their
outputs**, so you can also read them directly on GitHub.

---

## Notebooks

| Module | Notebook | Topic | Open in Colab |
|---|---|---|---|
| 3 | [`Fit4AI_3_Data_Science_and_AI_in_Insurance_Practice.ipynb`](Fit4AI_3_Data_Science_and_AI_in_Insurance_Practice.ipynb) | Hands-on: Python and Jupyter basics, data handling and visualisation, first models on the Titanic and Medicare data | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonhatzesberger/fit4ai-compact-20261119/blob/main/Fit4AI_3_Data_Science_and_AI_in_Insurance_Practice.ipynb) |
| 5 | [`Fit4AI_5_Supervised_Learning.ipynb`](Fit4AI_5_Supervised_Learning.ipynb) | Supervised learning on the French motor claims data (freMTPL2freq): decision trees, random forests, neural networks | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonhatzesberger/fit4ai-compact-20261119/blob/main/Fit4AI_5_Supervised_Learning.ipynb) |
| 6 | [`Fit4AI_6_Unsupervised_Learning.ipynb`](Fit4AI_6_Unsupervised_Learning.ipynb) | Unsupervised learning: hierarchical clustering and k-means, interactive step-by-step demos, portfolio consolidation | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonhatzesberger/fit4ai-compact-20261119/blob/main/Fit4AI_6_Unsupervised_Learning.ipynb) |
| 7 | [`Fit4AI_7_GenAI_Companion.ipynb`](Fit4AI_7_GenAI_Companion.ipynb) | Generative AI from scratch: training a small neural network with the numbers from the slides, word embeddings (skip-gram), temperature and sampling, GPT-2 run locally | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonhatzesberger/fit4ai-compact-20261119/blob/main/Fit4AI_7_GenAI_Companion.ipynb) |

---

## Getting started

### Option A – Google Colab (recommended, no installation)

1. Click the **Open in Colab** badge of the notebook.
2. Sign in with a Google account.
3. Run the cells with **Shift + Enter** (or **Runtime → Run all**). The first cell of each notebook installs only what Colab
   lacks and fetches the data files from this repository.

Notes: Module 5 downloads the freMTPL2freq data from OpenML; Module 7 downloads **GPT-2 medium (~1.5 GB)** from the Hugging Face
Hub on first use. A GPU is not required.

### Option B – locally

Requires **Python 3.10–3.13** and `pip`. A fresh virtual environment is recommended.

```bash
# 1. Clone the repository
git clone https://github.com/simonhatzesberger/fit4ai-compact-20261119.git
cd fit4ai-compact-20261119

# 2. Create and activate a virtual environment
python -m venv .venv
# Windows (PowerShell):
.venv\Scripts\Activate.ps1
# Linux / macOS:
# source .venv/bin/activate

# 3. Install the dependencies
pip install -r requirements.txt

# 4. Start Jupyter
jupyter lab
```

Then open a notebook and run it from top to bottom.

---

## Prerequisites

- **No prior machine-learning knowledge** – the notebooks introduce the concepts as they go.
- **Basic Python** helps but is not required.
- **No API keys.** Everything runs locally or in Colab; the language model in Module 7 (GPT-2, an open-weights model) runs via
  Hugging Face [`transformers`](https://huggingface.co/docs/transformers) on your own machine.
- For a quicker Module 7 run, set the environment variable `FIT4AI_MODEL_NAME=openai-community/gpt2` (~124 M parameters,
  ~500 MB) before starting Jupyter.

---

## Repository structure

```
fit4ai-compact-20261119/
├── README.md
├── LICENSE                                                  ← MIT (code)
├── requirements.txt                                         ← packages for local use
├── Fit4AI_3_Data_Science_and_AI_in_Insurance_Practice.ipynb ← Module 3
├── Fit4AI_5_Supervised_Learning.ipynb                       ← Module 5
├── Fit4AI_6_Unsupervised_Learning.ipynb                     ← Module 6
├── Fit4AI_7_GenAI_Companion.ipynb                           ← Module 7
├── data/                                                    ← data files used by the notebooks
└── images/                                                  ← pictures shown in the Module 3 notebook
```

---

## License

The **code** in this repository is released under the [MIT License](LICENSE). The **seminar slides** are provided to
participants by the European Actuarial Academy and are not part of this repository.

Data: `titanic.csv` (Titanic passenger data, a widely used teaching dataset), `Medicare.txt` (Medicare hospital charges by US
state, 1990–1995) and `cluster_vec_050Tsd.txt` (a portfolio of 50,000 life-insurance policies for the portfolio-consolidation
example) are included for teaching purposes. The
freMTPL2freq data (Module 5) is loaded from OpenML; GPT-2 (Module 7) is downloaded from the Hugging Face Hub and is subject to its
own (MIT) licence.

---

## Background

Prepared for the [European Actuarial Academy](https://actuarial-academy.com/) seminar “Fit4AI compact”. Earlier versions of the
notebooks were published for other runs of the seminar (e.g.
[simonhatzesberger/fit4ai-compact](https://github.com/simonhatzesberger/fit4ai-compact)).
