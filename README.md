
# Mihir Barve

**MSc Data Analytics** · Queen Mary University of London · 2025–2026

Data Analyst building production systems across
information retrieval, neural forecasting, credit risk analytics,
agentic AI, and LLM evaluation. Every project here was built
from scratch, evaluated rigorously, and documented honestly
including the failures.

## What I Build

| Domain | Projects |
|--------|----------|
| Search & Retrieval | SearchLens |
| Credit & Fraud Risk | FraudLens|
| Agentic AI | Client-based Dissertation |
| RAG & LLMs | DocLens, Prompt Mutation |
| Analytics Engineering | SupplyLens, ABTestLab|
| AI Safety & Evaluation | AgentGuard, Prompt Mutation, RolloutGuard |


## Featured Projects

### [SearchLens](https://github.com/mihir182001/searchlens)
**Neural Information Retrieval and Ranking Platform**

Built over 11 weeks. Implements BM25, dense bi-encoder retrieval,
cross-encoder reranking, and hybrid Reciprocal Rank Fusion — then
reversed the hybrid routing decision after a paired bootstrap
significance test (p=0.0039, 95% CI [−0.0252, −0.0052]) confirmed
dense-only outperforms hybrid on this corpus.

```
BM25 baseline        MRR@10: 0.7238
Cross-encoder rerank MRR@10: 0.8977  (+24%)
Recall@50            0.9250
Dense retrieval      MRR@10: 0.9130
Hybrid RRF           MRR@10: 0.8980  (worse than dense — reversed by evidence)
RAG faithfulness     98% over 100 real queries
Production bug       Low-confidence threshold caught by live query after shipping
Requirements drift   Caught by from-scratch Docker build — split into two files
```

`Python` `PyTorch` `FAISS` `sentence-transformers` `FastAPI`
`Docker` `GitHub Actions`

### [FraudLens](https://github.com/mihir182001/fraudlens)
**End-to-End Fraud Detection and Credit Risk Scoring Platform**

Built on two real Kaggle datasets 590,540 IEEE-CIS transactions
and 307K Home Credit loan applications covering the full ML
lifecycle from point-in-time-correct feature engineering through
production serving, monitoring, and advanced research modules.

```
XGBoost fraud classifier       AUC-ROC: 0.8875   Gini: 0.77
WoE credit scorecard           AUC-ROC: 0.7374
Active learning                Full AUC-PR with only 5.6% of labels
GraphSAGE fraud ring detection Relational fraud signal detection
Uplift modelling               S/T-Learner evaluated via Qini coefficient
Transfer learning              Across simulated domain shift
CI/CD test suite               306 automated tests on every push
Live demo                      Deployed on Render via Docker Blueprint
```

`Python` `XGBoost` `GraphSAGE` `FastAPI` `MLflow` `Docker`
`GitHub Actions` `Streamlit`


### [ABTestLab](https://github.com/mihir182001/ABTest-Lab)
**Statistical Experimentation Framework**

Frequentist and Bayesian experimentation engines.
Empirically demonstrated the peeking problem — false positive
rates from 5% to 20.7% and fixed with Bonferroni correction
to approximately 4%. Validated across 500+ simulated experiments.

`Python` `FastAPI` `Streamlit` `Docker` `GitHub Actions`

### [SupplyLens](https://github.com/mihir182001/supplylens)
**Supply Chain Analytics and dbt Data Platform**

1.5M+ real e-commerce records. dbt semantic model on
Google BigQuery. Regression, Isolation Forest anomaly
detection, Looker Studio dashboard, Claude API insights.

```
Regression MAE       6.70
Anomalies flagged    3,303  (3.0% of volume)
Outlier finding      167-day average delay from a single seller
dbt model            Staging and mart layers with data quality tests
```

`BigQuery` `dbt` `PySpark` `Python` `Looker Studio` `Claude API`

### [AgentGuard](https://github.com/mihir182001/agentguard)
**AI Agent Evaluation and Safety Framework**

Built an evaluation framework for testing whether AI agents follow
retrieved policies, produce valid evidence, execute authorised tools,
and escalate uncertain or unsafe actions. Uses Qwen2.5-3B-Instruct,
LangGraph, and FAISS to create controlled agent workflows and
structured evaluation scenarios.

```
Evaluation scenarios     1,700 synthetic cases
Held-out evaluation      175 cases
Overall held-out result  100% across 5 evaluation criteria
Adversarial API tests    20 cases
Policy retrieval         FAISS-based retrieval
Action validation        Guard and Executor architecture
Structured outputs       Schema-validated agent responses
```

`Python` `Qwen2.5-3B-Instruct` `LangGraph` `FAISS` `FastAPI`
`Docker` `Structured Outputs` `AI Evaluation`


### [Prompt Mutation](https://github.com/mihir182001/prompt-mutation-tester)
**Responsible AI Evaluation Framework** · [Live Demo](https://prompt-mutation-tester.onrender.com)

Autonomous adversarial evaluation framework.
LLM-as-judge scoring across 10 mutation strategies.
Improved model robustness from 43.6/100 to 100/100 in
two iterations. Real-time latency and cost monitoring.

`Python` `Groq API` `Claude API` `FastAPI` `Render`


### [RolloutGuard](https://github.com/mihir182001/rolloutguard)
**Production ML System with Empirical Validation**

Cox Proportional Hazards, XGBoost with conformal prediction,
Thompson Sampling multi-armed bandit. All empirically validated
against known ground truth with documented design failures.

```
Cox PH concordance   0.842
XGBoost AUC          >0.85 with conformal prediction intervals
Thompson Sampling    150x lower regret vs uniform random
pytest suite         49 tests across 9 modules
Production bug       Discovered and fixed during containerisation
```

`Python` `XGBoost` `FastAPI` `Docker` `GitHub Actions`

## Skills

```python
languages   = ["Python", "R", "SQL"]
ml          = ["PyTorch", "TensorFlow", "Scikit-learn", "XGBoost",
               "Hugging Face", "sentence-transformers"]
llm         = ["Claude API", "LangChain", "LangGraph", "RAG",
               "FAISS", "QLoRA", "PEFT", "MCP"]
forecasting = ["NeuralForecast", "N-BEATS", "N-HiTS", "TFT",
               "DeepAR", "ARIMA", "LSTM"]
data        = ["PySpark", "BigQuery", "dbt", "Snowflake",
               "PostgreSQL", "Databricks"]
mlops       = ["Docker", "GitHub Actions", "MLflow",
               "FastAPI", "pytest", "AWS", "GCP", "Azure"]
tools       = ["Cursor (daily)", "Claude Code (daily)",
               "GitHub Copilot"]
```

## Education

**MSc Data Analytics** — Queen Mary University of London
`Sep 2025 – Sep 2026`

Modules: Programming in Python · Advanced Machine Learning ·
Probability and Statistics · Computational Statistics with R ·
Neural Networks and Deep Learning · Machine Learning with Python

Dissertation: *Client-Based Multi-Agent OSINT Intelligence Platform*
— production three-agent system for a real client using
NVIDIA Nemotron and Anthropic Claude

## Publication

**Semantic Segmentation of Retinal Arteries and Veins**
ISTE Journal · Vol. 47, Special Issue No. 1 · June 2024

## Certifications and Achievements

Data Analytics Certification — ETLHive (2024)

Data Science Certification — Acmegrade (2024)

QHack Hackathon — First Place · Queen Mary University of London

STEM Ambassador — Working with school students to make
technical concepts accessible (2024 – Present)



## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mihir_Barve-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/mihir-barve-232930257/)
[![Email](https://img.shields.io/badge/Email-mihirbarve18@email.com-red?style=flat&logo=gmail)](mailto:mihirbarve18@email.com)

*All projects built from scratch. All numbers from actual evaluation
runs. All failures documented alongside successes.*
