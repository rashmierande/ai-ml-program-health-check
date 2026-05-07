# AI/ML Launch Readiness Metrics Cheat Sheet

> Companion to the AI/ML Program Health Check Framework
> Detailed metrics to track before, during, and after launch - both business and technical.
>
> *Prepared by Rashmi Erande | eranderashmi25@gmail.com | [LinkedIn](https://linkedin.com/in/rashmierande)*

---

## 🎯 Output Quality Metrics

*Is the AI producing good, safe, trustworthy outputs?*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Hallucination Rate** | How often the model generates factually incorrect information | Sample-based human review or automated fact-checking | < 5% (P0), < 2% (P1) |
| **Toxicity Rate** | Harmful, offensive, or inappropriate outputs | Toxicity classifier on outputs (e.g., Perspective API) | < 0.1% |
| **Refusal / Redirection Rate** | How often model correctly refuses unsafe or out-of-scope requests | Log analysis on refusal triggers | Depends on use case - track trend |
| **Response Relevance** | Does the output actually answer the user's question? | Human eval on sample set or LLM-as-judge scoring | > 85% relevant |
| **Consistency** | Same input → similar output across sessions | Automated regression tests on golden dataset | > 90% consistency |
| **Groundedness** | Is the output grounded in provided context / source data? | RAG faithfulness scoring (e.g., RAGAS framework) | > 80% grounded |

---

## 💰 Business Impact Metrics

*Is the AI driving the outcomes the business cares about?*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Task Completion Rate** | Can users accomplish their goal using the AI? | Funnel analysis: start → success | > 70% for v1 |
| **User Retention** | Do users come back after first interaction? | D1, D7, D30 retention cohorts | D7 > 40% for early product |
| **Time to Value** | How quickly does the user get a useful result? | Time from first input to first useful output | < 30 seconds for most use cases |
| **Conversion Rate** | Free → paid, or trial → active user conversion | Funnel tracking | Benchmark against industry |
| **Cost per Inference** | How much does each AI call cost? | Cloud billing / token usage per request | Track trend - should decrease |
| **Revenue per User** | Revenue attributed to AI-powered features | Attribution modeling or A/B test lift | Positive lift vs. non-AI baseline |
| **Support Ticket Deflection** | Does AI reduce human support volume? | Ticket volume before/after AI deployment | > 20% reduction |
| **NPS / CSAT on AI Features** | User satisfaction with AI specifically | In-app survey after AI interaction | NPS > 30, CSAT > 4.0/5 |

---

## ⚡ System Performance Metrics

*Is the system fast, reliable, and scalable?*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Inference Latency (p50/p95)** | Response time for model predictions | APM tools (Datadog, CloudWatch, etc.) | p50 < 500ms, p95 < 2s |
| **Throughput** | Requests handled per second | Load testing + production monitoring | Based on expected user volume |
| **Error Rate** | % of requests that fail | Error logging + alerting | < 1% |
| **Uptime / Availability** | System availability | Health checks + uptime monitoring | > 99.5% for v1, > 99.9% at scale |
| **Token Usage per Request** | LLM cost efficiency | Token counting per request type | Track trend - optimize over time |
| **Cold Start Time** | Time to first response after idle period | Synthetic monitoring | < 5s |

---

## 🔄 Data Pipeline & Quality Metrics

*Is the data feeding the model reliable and fresh?*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Data Freshness** | How old is the data the model uses? | Timestamp monitoring on data sources | Depends on use case (real-time vs. daily) |
| **Pipeline Uptime** | Is the data pipeline running without failures? | Pipeline monitoring (Airflow, etc.) | > 99% |
| **Data Coverage** | % of expected data sources actually flowing | Source-level health checks | 100% of critical sources |
| **Labeling Accuracy** | Quality of human-labeled training data | Inter-annotator agreement or audit sampling | > 90% agreement |
| **Data Drift** | Has the input data distribution changed from training? | Statistical drift detection (KL divergence, PSI) | Alert on significant drift |
| **Feedback Loop Cycle Time** | Time from user feedback to model improvement | Track end-to-end: feedback → retrain → deploy | < 2 weeks for early stage |

---

## 🔍 Evaluation & Quality Loop Metrics

*Can you systematically measure if the model is getting better or worse?*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Eval Dataset Coverage** | % of known use cases / edge cases in your test set | Manual audit of eval dataset vs. production queries | > 80% of known use cases |
| **Human Review Rate** | % of outputs reviewed by a human | Sampling rate tracking | > 5% ongoing, > 20% at launch |
| **Human-AI Agreement** | How often human reviewers agree with model output | Compare human labels vs. model outputs | > 85% |
| **Regression Rate** | % of previously passing test cases that now fail | Automated regression suite run on every deploy | 0% on P0 cases, < 5% overall |
| **Model Version Comparison** | Is the new model better than the previous one? | A/B eval on same test set across versions | New ≥ Previous on all key metrics |
| **Time to Detect Degradation** | How quickly do you notice model quality dropped? | Alerting on quality metrics | < 24 hours |

---

## 🛡️ Responsible AI & Compliance Metrics

*Is the AI safe, fair, and compliant? (EU AI Act full enforcement: Aug 2, 2026)*

| Metric | What It Measures | How to Track | Target Range |
|---|---|---|---|
| **Bias Score** | Performance disparity across demographic groups | Disaggregated eval metrics by group | < 5% variance across groups |
| **Explainability Coverage** | % of decisions that can be explained to users | Audit of explanation capability per feature | 100% for high-risk decisions |
| **PII Exposure Rate** | How often model leaks personal data in outputs | PII detection on outputs (regex + NER) | 0% |
| **Consent Coverage** | % of training data with proper consent / licensing | Data provenance audit | 100% |
| **Human Override Rate** | How often humans override AI decisions | Log human overrides vs. AI suggestions | Track trend - high = quality issue |
| **Incident Response Time** | Time to respond to reported AI safety incidents | Incident tracking system | < 4 hours for critical incidents |

---

## 🚀 Launch Readiness Scorecard

*Rate each area. All 🟢 = ready to launch. Any 🔴 = must fix before launch.*

| Area | Key Metric to Gate On | Status | Owner |
|---|---|---|---|
| **Output Quality** | Hallucination rate < threshold | ☐🟢 ☐🟡 ☐🔴 | |
| **Business Impact** | Task completion rate > threshold | ☐🟢 ☐🟡 ☐🔴 | |
| **Performance** | p95 latency < threshold, uptime > 99.5% | ☐🟢 ☐🟡 ☐🔴 | |
| **Data Pipeline** | Pipeline uptime > 99%, no critical drift | ☐🟢 ☐🟡 ☐🔴 | |
| **Evaluation Loop** | Regression rate = 0% on P0 cases | ☐🟢 ☐🟡 ☐🔴 | |
| **Responsible AI** | Bias score < 5%, PII exposure = 0% | ☐🟢 ☐🟡 ☐🔴 | |
| **Monitoring** | Alerts on all key metrics, < 24hr detection | ☐🟢 ☐🟡 ☐🔴 | |
| **Rollback** | Rollback tested and < 15 min to execute | ☐🟢 ☐🟡 ☐🔴 | |

---

*AI/ML Launch Readiness Metrics Cheat Sheet v1.0*

*Companion to the AI/ML Program Health Check Framework*

*Feedback? → eranderashmi25@gmail.com*
