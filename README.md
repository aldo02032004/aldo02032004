## Hi, I'm Naufaldo Indra Pratama

[![LinkedIn](https://img.shields.io/badge/LinkedIn-naufaldo--pratama-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/naufaldo-pratama/)

I build **quantitative risk models** for credit and energy supply, and **data and NLP pipelines** for Indonesian news and social media. Each project starts from raw data and ends with something people can act on: a score cutoff, a cost-at-risk figure, issue maps, influencer rankings, stance summaries, forecasts, and training data for language models.

Every project opens in **Google Colab with one click**.

### Risk models

| Project | Question it answers | What's inside | Stack |
|---|---|---|---|
| [**Credit Risk Model**](https://github.com/aldo02032004/credit-risk-model) | Which applicants should a lender approve, and how much can the loan book lose in a bad year? | PD model on 150,000 real borrowers (logistic regression vs gradient boosting), bank-style validation (AUC 0.853, KS, calibration, PSI), a break-even score cutoff that cuts expected loss by 41%, and a Vasicek Monte Carlo with VaR 99 and stress test. | scikit-learn, SciPy, pandas, Matplotlib |
| [**LNG Supply Risk Analysis**](https://github.com/aldo02032004/lng-supply-risk-analysis) | How far can next year's LNG cost overshoot the budget, and how much does hedging help? | ISO 31000 cycle on real Brent and USD/IDR data: risk register, 10,000-scenario Monte Carlo, VaR / CVaR / Cost-at-Risk, hedging effect, volatility KRI and BCMS. | pandas, NumPy, Matplotlib, Gemini API |

Results in both projects end as 16:9 charts whose title states the main message, ready for a slide.

### Data and NLP pipelines

**Monitoring export → clean → classify (rules first, LLM for the hard cases) → network / map / forecast → report**

The LLM steps run a local open model ([Gemma 2 9B SahabatAI](https://huggingface.co/faizonly5953/gemma2-9b-cpt-sahabatai-v1-instruct-GGUF) with llama.cpp) on the free Colab GPU, so no API key is needed.

| Project | Question it answers | What's inside | Stack |
|---|---|---|---|
| [**Social Media KOL Analysis**](https://github.com/aldo02032004/social-media-kol-analysis) | Who drives a topic, and which side are they on? | Top 5 news and social issues, a retweet/reply network per theme, KOL score from PageRank, eigenvector, engagement and followers, and each KOL's stance. | NetworkX, llama.cpp, pandas |
| [**LLM Topic Classification**](https://github.com/aldo02032004/llm-topic-classification-pipeline) | Which themes does a topic split into, and who leads each? | Type a topic in one sentence; the LLM writes themes and keywords, labels posts, ranks top authors per theme and summarises their stance. | llama.cpp, Pydantic, pandas |
| [**Environmental Issue Monitoring**](https://github.com/aldo02032004/environmental-issue-monitoring) | Which environmental issues, and where in Indonesia? | Rule-based issues plus a province resolver feed a map dashboard. One real day: 1,826 mentions → 532 documents → 17 issue types in under 3 s. | pandas, GeoPandas, Matplotlib |
| [**Sentiment Volume Forecast**](https://github.com/aldo02032004/sentiment-volume-forecast) | How many positive, negative and neutral posts are coming? | Five methods backtested on rolling windows, scored on runs they never saw, with an interactive chart and 80% range. | scikit-learn, sktime, ipywidgets |
| [**Indonesian Political-Economic NER**](https://github.com/aldo02032004/NER_env) *(in progress)* | Which people, agencies, parties and policies are named? | GLiNER tags posts, the LLM checks uncertain ones, and checked posts train a smaller IndoBERT. Package with 91 tests. | GLiNER, llama.cpp, pytest |

Smaller notebooks (daily report, weekly visualisation, word clouds, figurative-language classification) live in [naufaldo.github.io](https://github.com/aldo02032004/naufaldo.github.io).

### How I work

- **Honest evaluation.** Models are validated on data they never saw, backtests never grade their own choices, and limitations sit next to the results.
- **Simple where possible.** A readable model wins unless a complex one is clearly better; rules handle the easy cases and the LLM only sees what is left, with answers forced into a schema.
- **Runs for other people.** One-click notebooks, few explicit assumptions, and results written so a non-specialist can read them.

### Tools

**Languages & data:** Python, pandas, NumPy<br>
**Risk & finance:** credit risk (PD, LGD, EAD, expected loss), model validation (AUC, KS, PSI, calibration), Monte Carlo simulation, Vasicek model, VaR / CVaR, ISO 31000, yfinance, FRED<br>
**ML & analysis:** scikit-learn, SciPy, sktime, NetworkX<br>
**NLP & LLM:** Hugging Face Transformers (IndoBERT), GLiNER, llama.cpp (GGUF), Pydantic / JSON schema<br>
**Visualisation:** Matplotlib, seaborn, GeoPandas, ipywidgets<br>
**Workflow:** Jupyter / Google Colab, Git & GitHub, pytest
