# Sensor Data Engineer — Written Submission

Sri Harshanadh Reddy Chinthala

**Briefly describe an instrument or measurement you are deeply familiar with. What was its most important (or most confounding) source of error, and how did you account for it?**

I am deeply familiar with measuring buying intent from sales-call and CRM data. At Salesable, I built Python NLP and speech-to-text pipelines processing more than 100,000 call recordings per month, extracting buying signals for lead qualification. This was an inferred measurement: a score derived from recorded conversations and customer records, rather than a direct observation of a customer's intent.

One of the most confounding sources of error was the underlying CRM data. Duplicate records, missing fields, and inconsistent formats could distort the inputs used for scoring. A plausible model output was therefore not enough to establish that the measurement was reliable.

I accounted for this by validating more than 10 million multi-source CRM records for those issues before engineering features for scoring, churn, and segmentation models. I also monitored production model outcomes and Looker KPI data, checked results against real business outcomes, and coordinated data definitions with research and lead-generation teams.

The central lesson was that measurement quality depends on the entire path from source data to interpretation. Checking a model's output in isolation would miss errors introduced upstream. My approach was to combine input validation with outcome checks so that the team could assess whether the extracted signals were useful in practice.
