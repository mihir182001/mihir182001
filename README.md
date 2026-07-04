# Mihir Barve

**MSc Data Analytics @ Queen Mary London**  
Building production AI systems, evaluation frameworks, LLM pipelines, and end-to-end ML applications that ship.

---

## Featured Projects

###  [Prompt Evaluation Testing Framework](https://github.com/mihir182001/prompt-mutation-tester)
An autonomous LLM evaluation system that generates adversarial prompt variants across 10 mutation strategies, scores outputs using an LLM-as-judge layer, and self-optimises fragile prompts from **43.6 → 100/100 in 2 iterations** without human intervention.

- Adaptive agent selects mutation strategies based on prior failure patterns
- Multi-model comparison, RAG prompt testing, latency and cost tracking per API call
- Production dashboard with analytics, batch testing, history tracking, PDF/CSV export
- **Live:** [prompt-mutation-tester.onrender.com](https://prompt-mutation-tester.onrender.com)

`Python` `Groq API` `LangChain` `RAG` `LLM Evaluation` `Flask` `Render`

---

###  [Multimodel Meeting Intelligence System](https://github.com/mihir182001/Multimodal-Meeting-Intelligence-with-NLP-RAG-Transformer-Models)
End-to-end multimodal meeting intelligence platform processing audio through a 15-feature pipeline — real-time transcription, speaker diarisation, NLP analytics, RAG-powered Q&A, and meeting quality scoring across 5 dimensions.

- Fine-tuned **DistilBERT** from scratch for action item classification → **F1: 0.83**
- Completion risk predictor with cross-validation **F1: 0.93** using 8 engineered NLP features
- FAISS vector search + sentence-transformers for RAG Q&A
- Real speaker diarisation using MFCC embeddings + agglomerative clustering
- CI/CD pipeline with automated F1 quality gates — **build fails if F1 drops below 70%**
- Zero paid APIs for any ML component

`Python` `DistilBERT` `FAISS` `WebRTC` `Groq Whisper` `Docker` `GitHub Actions`

---

###  [Job Tracker API](https://github.com/mihir182001/Job-Tracker)
Production-grade REST API managing structured workflows across users, job applications, interviews, and scheduling — deployed with Docker, CI/CD, and automated quality validation.

- FastAPI + SQLAlchemy ORM + JWT authentication + Alembic migrations
- Pytest + FastAPI TestClient covering edge cases and performance monitoring
- Swagger UI documentation for efficient API testing

`Python` `FastAPI` `SQLAlchemy` `Docker` `GitHub Actions` `Pytest` `Render`

---

###  [AI Medical Imaging Assistant](https://github.com/mihir182001/AI-Medical-Imaging-Assistant)
End-to-end computer vision system classifying 6,400+ brain MRI scans across four diagnostic categories — **96% precision** for No Tumour, **93% F1** for Pituitary Tumour.

- EfficientNetB0 with transfer learning and systematic failure-mode analysis
- Grad-CAM explainability to make model decisions auditable and interpretable
- Deployed as a live Streamlit application

`Python` `TensorFlow` `EfficientNetB0` `Grad-CAM` `OpenCV` `Streamlit`

---

## Technical Skills

```
Languages      Python (OOP, SOLID, production) · SQL · JavaScript (basic)
AI & LLMs      LLM Evaluation · LLM-as-judge · Prompt Engineering · RAG · LangChain · Groq API · Anthropic Claude
ML & DL        PyTorch · TensorFlow · Keras · DistilBERT · FAISS · LSTMs · Transformers · Scikit-learn · XGBoost
Data           Pandas · NumPy · EDA · Feature Engineering · Time Series · ARIMA
DevOps         Docker · GitHub Actions CI/CD · Automated Quality Gates · Render
Tooling        Git · Jupyter · Streamlit · Flask · Plotly · Swagger UI · Copilot · Cursor
```

---

## Stats

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=mihir182001&layout=compact&theme=default&hide_border=true&langs_count=6)

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=mihir182001&show_icons=true&theme=default&hide_border=true&count_private=true&hide=stars&rank_icon=github)

---

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mihirbarve-0077B5?style=flat&logo=linkedin)](https://linkedin.com/in/mihirbarve)
[![Email](https://img.shields.io/badge/Email-mihirbarve18@gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:mihirbarve18@gmail.com)
