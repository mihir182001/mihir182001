<div align="center">

# Mihir Barve

### AI Engineer & Data Scientist · LLMs, RAG & Agentic AI · Python, SQL & Machine Learning

**MSc Data Analytics · Queen Mary University of London**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mihir_Barve-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/mihir-barve-232930257/)
[![Email](https://img.shields.io/badge/Email-mihirbarve18@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mihirbarve18@gmail.com)
![Location](https://img.shields.io/badge/Based_in-London,_UK-555?style=flat-square)
![Open to work](https://img.shields.io/badge/Open_to-AI_Engineer_·_Data_Scientist_·_ML_Engineer_·_Data_Analyst-2ea44f?style=flat-square)

</div>

---

I build AI and data systems, then test them until the numbers prove they work. Every project below was built from scratch, evaluated against a baseline or a known ground truth, and documented honestly, including the design decisions my own evaluation code reversed.

**Focus areas:** LLM applications · Retrieval-Augmented Generation · agent evaluation and safety · machine learning for risk · experimentation and statistics · analytics engineering

## Featured Projects

| Project | What it proves | Headline result |
|---|---|---|
| [AI Agent Evaluation and Safety Framework](#ai-agent-evaluation-and-safety-framework) | Agentic AI, guardrails, evaluation | 100% across 5 criteria on 175 held-out cases |
| [Neural Information Retrieval and Ranking Platform](#neural-information-retrieval-and-ranking-platform) | Search, RAG, significance testing | MRR@10 0.913 (BM25 baseline 0.724) |
| [Credit and Fraud Risk Modelling](#credit-and-fraud-risk-modelling) | ML for risk, MLOps | AUC-ROC 0.8875, Gini 0.77 |
| [Prompt Mutation and LLM Evaluation Framework](#prompt-mutation-and-llm-evaluation-framework) | LLM-as-judge, robustness testing | Prompt score 43.6 → 100 in 2 iterations |
| [A/B Testing and Experimentation Platform](#ab-testing-and-experimentation-platform) | Statistics, experimentation | False positives 20.7% → ~4% |
| [Data Pipeline, Regression and Anomaly Detection](#data-pipeline-regression-and-anomaly-detection) | SQL, dbt, BigQuery, BI | 3,303 anomalies in 1.5M+ rows |
| [Failure Prediction with Uncertainty Quantification](#failure-prediction-with-uncertainty-quantification) | Survival models, conformal prediction | Cox PH concordance 0.842 |
| [Production REST API for Job Application Management](#production-rest-api-for-job-application-management) | Backend engineering, CI/CD | JWT auth, Docker, GitHub Actions |

---

### AI Agent Evaluation and Safety Framework
**Repo:** [agentguard](https://github.com/mihir182001/agentguard)

Evaluation and governance framework for LLM agents, built on one principle: *the LLM is not the security boundary.* An Action Guard and Executor architecture separates agent reasoning, policy validation and tool execution, so unauthorised actions are blocked before they run.

```
Evaluation scenarios     1,700 synthetic cases
Held-out evaluation      175 cases, 100% across 5 criteria
                         (action correctness, evidence grounding, policy
                          compliance, safety, human escalation)
Adversarial API tests    20 cases
Policy retrieval         FAISS-based RAG
```
`Python` `Qwen2.5-3B-Instruct` `LangGraph` `FAISS` `FastAPI` `Docker`

### Neural Information Retrieval and Ranking Platform
**Repo:** [searchlens](https://github.com/mihir182001/searchlens)

BM25, dense bi-encoder retrieval, cross-encoder reranking, hybrid Reciprocal Rank Fusion and RAG with citations, built over 11 weeks behind a FastAPI service. A paired bootstrap significance test (p = 0.0039) showed dense-only beats hybrid on this corpus, so the routing design was reversed on the evidence.

```
BM25 baseline          MRR@10  0.7238
Cross-encoder rerank   MRR@10  0.8977   (+24%)
Dense retrieval        MRR@10  0.9130
Hybrid RRF             MRR@10  0.8980   (reversed by significance test)
Recall@50              0.9250
RAG faithfulness       98% over 100 real queries
```
`Python` `PyTorch` `FAISS` `sentence-transformers` `FastAPI` `Docker` `GitHub Actions`

### Credit and Fraud Risk Modelling
**Repo:** [fraudlens](https://github.com/mihir182001/fraudlens)

End-to-end fraud and credit risk platform on 590,540 IEEE-CIS transactions and 307K Home Credit applications, with point-in-time-correct features, chronological validation, MLflow versioning, drift monitoring and an audit log.

```
XGBoost fraud classifier   AUC-ROC 0.8875   Gini 0.77   KS 0.626
WoE credit scorecard       AUC-ROC 0.7374
Active learning            Full AUC-PR with 5.6% of labels
Research modules           GraphSAGE fraud rings, uplift modelling
Test suite                 306 automated tests in CI
```
`Python` `SQL` `XGBoost` `GraphSAGE` `MLflow` `FastAPI` `Docker`

### Prompt Mutation and LLM Evaluation Framework
**Repo:** [prompt-mutation-tester](https://github.com/mihir182001/prompt-mutation-tester) · [Live demo](https://prompt-mutation-tester.onrender.com)

Mutation testing for LLM prompts. Generates adversarial variants across 10 strategies, scores each with an LLM-as-judge, then repairs and re-tests fragile prompts automatically. Includes RAG prompt testing, multi-model comparison and latency and cost tracing.

```
Prompt robustness      43.6/100 → 100/100 in two iterations
Mutation strategies    10
```
`Python` `Groq API` `GPT-OSS` `Claude API` `Flask` `SQLAlchemy` `Render`

### A/B Testing and Experimentation Platform
**Repo:** [ABTest-Lab](https://github.com/mihir182001/ABTest-Lab)

Frequentist (Welch's t, chi-squared, Mann-Whitney U) and Bayesian engines, a power calculator and multiple-testing correction, each validated against simulated ground truth.

```
Null experiments       500, false-positive rate calibrated to 5%
Peeking problem        14.3% false positives (5 looks)
Multiple metrics       20.7% false positives → ~4% with Bonferroni
Test suite             59 pytest tests
```
`Python` `SciPy` `FastAPI` `SQLite` `Streamlit` `Docker`

### Data Pipeline, Regression and Anomaly Detection
**Repo:** [supplylens](https://github.com/mihir182001/supplylens) · [Live dashboard](https://datastudio.google.com/s/liBPla3WNg4)

Fulfilment analytics on the real Olist e-commerce dataset (1.5M+ rows): a BigQuery and dbt semantic layer, regression and Isolation Forest root-cause analysis, a public Looker Studio dashboard and Claude-generated recommendations.

```
Regression MAE         6.70 days (110K+ orders)
Anomalies flagged      3,303 (3.0% of volume)
dbt model              Staging and mart layers with data quality tests
```
`SQL` `BigQuery` `dbt` `Python` `Looker Studio` `Claude API`

### Failure Prediction with Uncertainty Quantification
**Repo:** [Rolloutguard](https://github.com/mihir182001/Rolloutguard)

Decides whether a canary deployment should continue, pause or roll back, combining a sequential statistical test, a Cox survival model, an XGBoost classifier with conformal prediction intervals and a Thompson Sampling bandit.

```
Cox PH concordance     0.842
XGBoost AUC            > 0.85 with conformal prediction intervals
Thompson Sampling      150x lower regret than uniform random
Test suite             49 tests across 9 modules
```
`Python` `XGBoost` `lifelines` `FastAPI` `Docker` `GitHub Actions`

### Production REST API for Job Application Management
**Repo:** [Job-Tracker](https://github.com/mihir182001/Job-Tracker)

Job application tracking API with JWT authentication, modular routes, schemas and models, external job-recommendation integration, audit logging, automated tests and containerised deployment.

`Python` `FastAPI` `SQLAlchemy` `JWT` `Pydantic` `pytest` `Docker` `GitHub Actions`

---

### More work
- **Client-Based Agentic Open-Source Intelligence (OSINT) Platform** (MSc dissertation, private client work): multi-agent OSINT risk scoring with QMUL's cybersecurity team, using NVIDIA Nemotron and full source traceability.
- **Clinical Document Intelligence and RAG**: BioBERT medical NER (F1 0.88) and a FAISS RAG pipeline over 500 ClinicalTrials.gov protocols (91% retrieval hit rate).
- [Multimodal Meeting Intelligence Platform](https://github.com/mihir182001/Multimodal-Meeting-Intelligence-with-NLP-RAG-Transformer-Models): ASR, NLP, RAG and Transformer models turning meeting audio into structured insights.
- [AI Medical Imaging Assistant](https://github.com/mihir182001/AI-Medical-Imaging-Assistant): EfficientNetB0 brain MRI classifier with Grad-CAM explanations and a Streamlit app.

## Tech Stack

```python
languages   = ["Python", "SQL", "R"]
ml          = ["PyTorch", "TensorFlow", "Scikit-learn", "XGBoost", "LightGBM",
               "Hugging Face", "sentence-transformers"]
llm         = ["Claude API", "Groq API", "LangChain", "LangGraph", "RAG",
               "FAISS", "ChromaDB", "QLoRA", "PEFT"]
forecasting = ["NeuralForecast", "N-BEATS", "N-HiTS", "TFT",
               "DeepAR", "ARIMA", "LSTM"]
statistics  = ["A/B testing", "Bayesian inference", "Survival analysis",
               "Conformal prediction"]
data        = ["PySpark", "BigQuery", "dbt", "Snowflake",
               "PostgreSQL", "GCP"]
mlops       = ["Docker", "GitHub Actions", "MLflow",
               "FastAPI", "pytest", "Git"]
bi          = ["Power BI", "Tableau", "Looker Studio", "Excel"]
tools       = ["Cursor", "Claude Code", "GitHub Copilot"]
```

## Education

**MSc Data Analytics**, Queen Mary University of London · Sep 2025 – Sep 2026
Modules: Advanced Machine Learning · Neural Networks and Deep Learning · Probability and Statistics · Computational Statistics with R · Machine Learning with Python · Programming in Python

**BE**, AISSMS Institute of Information Technology · 2021 – 2024

## Publication

**Semantic Segmentation of Retinal Arteries and Veins**, ISTE Journal · Vol. 47, Special Issue No. 1 · June 2024

## Achievements

- **QHack, Queen Mary University of London:** Best Idea award (team)
- **STEM Ambassador**, STEM Learning UK (2026 – present)
- **Data Analytics Certification**, ETLHive
- **Data Science Certification**, Acmegrade

---

<div align="center">

*All projects built from scratch. All numbers come from real evaluation runs. Failures are documented alongside successes.*

</div>
