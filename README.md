## Hi, I'm Naufaldo Indra Pratama

I build data and NLP pipelines for **Indonesian news and social media**: turning raw monitoring exports into issue maps, influencer rankings, sentiment forecasts, and training data for language models.

What I care about in my work:

- **Honest evaluation.** Backtests that never grade their own choices, and limitations written down next to the results.
- **Tools other people can run.** One-click Colab notebooks, sample data, and clear inputs and outputs.
- **Cheap where possible, LLM where it pays.** Keyword and rule filters first, large language models only for the hard cases.

### Featured projects

| Project | What it does | Stack |
|---|---|---|
| [**Sentiment Volume Forecast**](https://github.com/aldo02032004/sentiment-volume-forecast) | Forecasts daily post volume per sentiment. Five methods are backtested and the best is picked automatically (70–75% accuracy), beating XGBoost and LightGBM on small data. | scikit-learn, sktime, ipywidgets |
| [**Environmental Issue Monitoring**](https://github.com/aldo02032004/environmental-issue-monitoring) | Classifies environmental issues in news and social media, locates them by province, and draws a map dashboard. 1,826 mentions → 532 unique documents → 17 issue types in under 3 seconds. | pandas, GeoPandas, Matplotlib |
| [**LLM Topic Classification Pipeline**](https://github.com/aldo02032004/llm-topic-classification-pipeline) | Type a topic in one sentence; Gemini builds the themes, labels posts, ranks the top accounts per theme, and summarises each account's stance. | Gemini API, Pydantic, pandas |
| [**Indonesian Political-Economic NER**](https://github.com/aldo02032004/NER_env) *(in progress)* | Entity extraction with GLiNER, checked by Gemini, building training data for a smaller IndoBERT model. Tested Python package. | GLiNER, Gemini, pytest |

### Tools

**Languages & data:** Python, pandas, NumPy<br>
**ML & NLP:** scikit-learn, sktime, Hugging Face Transformers (IndoBERT), GLiNER, Gemini API<br>
**Visualisation:** Matplotlib, GeoPandas, ipywidgets<br>
**Workflow:** Jupyter / Google Colab, Git & GitHub, pytest
