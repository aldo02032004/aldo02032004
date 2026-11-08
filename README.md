## Hi, I'm Naufaldo Indra Pratama

[![LinkedIn](https://img.shields.io/badge/LinkedIn-naufaldo--pratama-0A66C2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/naufaldo-pratama/)

I build data and NLP pipelines for **Indonesian news and social media**. Each project starts from a raw media-monitoring export and ends with something people can act on: issue maps, influencer rankings, stance summaries, forecasts, and training data for language models.

**Monitoring export → clean → classify (rules first, LLM for the hard cases) → network / map / forecast → report**

Every project opens in **Google Colab with one click**. The LLM steps run a local open model ([Gemma 2 9B SahabatAI](https://huggingface.co/faizonly5953/gemma2-9b-cpt-sahabatai-v1-instruct-GGUF) with llama.cpp) on the free Colab GPU, so no API key is needed.

### Projects

| Project | Question it answers | What's inside | Stack |
|---|---|---|---|
| [**Social Media KOL Analysis**](https://github.com/aldo02032004/social-media-kol-analysis) | Who drives a topic, and which side are they on? | Top 5 news and social issues, a retweet/reply network per theme, KOL score from PageRank, eigenvector, engagement and followers, and each KOL's stance. | NetworkX, llama.cpp, pandas |
| [**LLM Topic Classification**](https://github.com/aldo02032004/llm-topic-classification-pipeline) | Which themes does a topic split into, and who leads each? | Type a topic in one sentence; the LLM writes themes and keywords, labels posts, ranks top authors per theme and summarises their stance. | llama.cpp, Pydantic, pandas |
| [**Environmental Issue Monitoring**](https://github.com/aldo02032004/environmental-issue-monitoring) | Which environmental issues, and where in Indonesia? | Rule-based issues plus a province resolver feed a map dashboard. One real day: 1,826 mentions → 532 documents → 17 issue types in under 3 s. | pandas, GeoPandas, Matplotlib |
| [**Sentiment Volume Forecast**](https://github.com/aldo02032004/sentiment-volume-forecast) | How many positive, negative and neutral posts are coming? | Five methods backtested on rolling windows, scored on runs they never saw, with an interactive chart and 80% range. | scikit-learn, sktime, ipywidgets |
| [**Indonesian Political-Economic NER**](https://github.com/aldo02032004/NER_env) *(in progress)* | Which people, agencies, parties and policies are named? | GLiNER tags posts, the LLM checks uncertain ones, and checked posts train a smaller IndoBERT. Package with 91 tests. | GLiNER, llama.cpp, pytest |

Smaller notebooks (daily report, weekly visualisation, word clouds, figurative-language classification) live in [naufaldo.github.io](https://github.com/aldo02032004/naufaldo.github.io).

### How I work

- **Honest evaluation.** Backtests never grade their own choices, and limitations sit next to the results.
- **Cheap where possible, LLM where it pays.** Keyword and rule filters handle the easy cases; the LLM only sees what is left, with answers forced into a schema.
- **Runs for other people.** One-click notebooks, a form for the inputs, and progress saved to Drive so a dropped session can continue.

### Tools

**Languages & data:** Python, pandas, NumPy<br>
**NLP & LLM:** Hugging Face Transformers (IndoBERT), GLiNER, llama.cpp (GGUF), Pydantic / JSON schema<br>
**ML & analysis:** scikit-learn, sktime, NetworkX<br>
**Visualisation:** Matplotlib, GeoPandas, ipywidgets<br>
**Workflow:** Jupyter / Google Colab, Git & GitHub, pytest
