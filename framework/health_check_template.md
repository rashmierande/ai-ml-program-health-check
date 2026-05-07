# AI/ML Program Health Check

> A structured framework for early-stage AI/ML startups to identify success metrics, map risks, and build quality loops.
>
> *Prepared by Rashmi Erande | eranderashmi25@gmail.com | [LinkedIn](https://linkedin.com/in/rashmierande)*

---

## 📌 1. Product & Stage Snapshot

| | Details |
|---|---|
| **Company / Product** | |
| **Stage** | ☐ Pre-MVP  ☐ MVP  ☐ Beta  ☐ Post-Launch |
| **AI/ML Core** | *What does the model do?* |
| **Team Size** | Eng: ___  ML/Data: ___  Product: ___ |
| **Users** | ☐ Internal only  ☐ Beta users  ☐ Production traffic |
| **Biggest Worry Right Now** | |

---

## 🎯 2. Success Metrics

*What does "working" look like? Define metrics before building more.*

| Metric Type | What to Measure | Current State | Target |
|---|---|---|---|
| **Output Quality** | Hallucination rate, toxicity rate, refusal/redirection rate, response relevance | | |
| **User Impact** | Engagement, retention, task completion rate | | |
| **Business Outcome** | Revenue, cost savings, conversion | | |
| **Performance** | Inference latency (p50/p95), throughput, error rate, uptime | | |
| **Data Quality** | Coverage, freshness, labeling accuracy | | |

---

## ⚠️ 3. Risk Map

*Rate each: 🟢 Low  🟡 Medium  🔴 High*

| Risk Area | Key Questions | Rating | Notes / Mitigation |
|---|---|---|---|
| **Data** | Do you have enough quality training data? Data pipeline reliable? Labeling consistent? | ☐🟢 ☐🟡 ☐🔴 | |
| **Model** | How do you know the model is good enough? Regression testing? Versioning? | ☐🟢 ☐🟡 ☐🔴 | |
| **Evaluation** | How do you measure quality today? Automated evals? Human review? | ☐🟢 ☐🟡 ☐🔴 | |
| **Infrastructure** | Can you deploy reliably? CI/CD? Scaling plan? Cost monitoring? | ☐🟢 ☐🟡 ☐🔴 | |
| **Timeline** | Realistic milestones? Dependencies clear? What blocks launch? | ☐🟢 ☐🟡 ☐🔴 | |
| **Team** | Right skills in place? Key-person risk? ML vs Eng bandwidth balanced? | ☐🟢 ☐🟡 ☐🔴 | |

---

## 🔄 4. Evaluation & Quality Feedback Loop

*The #1 gap in early-stage AI products: no systematic way to know if the model is getting better or worse.*

| Component | Question | Current State | Recommendation |
|---|---|---|---|
| **Automated Eval** | Do you have automated quality scoring on model outputs? | ☐ Yes  ☐ Partial  ☐ No | |
| **Human Review** | Who reviews model outputs for quality? How often? What criteria? | ☐ Founders  ☐ Team  ☐ Users  ☐ Nobody | |
| **Feedback → Retraining** | Does feedback flow back into training data or model tuning? | ☐ Yes  ☐ Manual  ☐ No loop exists | |
| **Regression Detection** | Would you know if the model got worse after a change? | ☐ Automated  ☐ Manual  ☐ We wouldn't know | |
| **Eval Dataset** | Do you have a curated test set for consistent benchmarking? | ☐ Yes  ☐ Ad-hoc  ☐ No | |

---

## 🛡️ 5. Responsible AI & Compliance

> ⚠️ **EU AI Act — Full enforcement Aug 2, 2026:** Fines up to €35M or 7% of global turnover for high-risk AI systems. If your AI touches employment, credit, healthcare, education, or critical infrastructure — conformity assessments, technical documentation, and human oversight are required.

| Checkpoint | Key Question | Status | Notes |
|---|---|---|---|
| **Bias & Fairness** | Tested for bias across user demographics? | ☐ Yes  ☐ No  ☐ N/A | |
| **Transparency** | Can you explain how the model makes decisions to users? | ☐ Yes  ☐ No | |
| **Data Privacy** | Training data compliant with GDPR / privacy laws? Consent obtained? | ☐ Yes  ☐ No | |
| **Human Oversight** | Human-in-the-loop for high-stakes decisions? | ☐ Yes  ☐ No | |
| **Risk Classification** | Do you know your EU AI Act risk tier? (Prohibited / High / Limited / Minimal) | ☐ Yes  ☐ No | |
| **Documentation** | Technical docs sufficient for conformity assessment? | ☐ Yes  ☐ No | |
| **Incident Reporting** | Process for reporting serious AI incidents? | ☐ Yes  ☐ No | |

---

## 🚀 6. Launch Readiness Signals

*Not a gate — a conversation starter. Which of these can you confidently say yes to?*

| Signal | Ready? | Notes |
|---|---|---|
| Success metrics defined and measurable | ☐ Yes  ☐ No | |
| Model quality meets minimum bar (you defined what "good" means) | ☐ Yes  ☐ No | |
| Evaluation loop exists (automated + human) | ☐ Yes  ☐ No | |
| Known failure modes documented | ☐ Yes  ☐ No | |
| Rollback plan if model degrades | ☐ Yes  ☐ No | |
| Monitoring/alerting on key metrics | ☐ Yes  ☐ No | |
| Data pipeline reliable and tested | ☐ Yes  ☐ No | |
| User feedback mechanism in place | ☐ Yes  ☐ No | |

---

## ✅ 7. Top 3 Action Items

*Filled in together during the call — the 3 highest-impact things to do next.*

| # | Action Item | Owner | By When |
|---|---|---|---|
| 1 | | | |
| 2 | | | |
| 3 | | | |

---

*AI/ML Program Health Check Framework v1.0*

*Feedback? I'd love to hear what worked and what didn't → eranderashmi25@gmail.com*
