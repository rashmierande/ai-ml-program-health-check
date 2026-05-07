# AI/ML Program Health Check Framework

> A structured framework to help early-stage AI/ML teams define success metrics, identify risks, and build quality feedback loops - before launch, not after.

---

## The Problem

Early-stage AI/ML startups often struggle with:
- "How do I know if my model is good enough to launch?"
- "What should I measure  and when?"
- "What's going to break that I'm not seeing?"

Most teams ship based on gut feel, then scramble when quality issues surface in production. By then, it's expensive to fix and trust is already damaged.

## What This Framework Does

It gives founders and engineering leads a structured way to:

1. **Define the quality bar**: what "good enough" actually means in measurable terms
2. **Map risks early** : data, model, evaluation, infrastructure, timeline, team
3. **Build evaluation loops**: so the product improves with every cycle, not just every hire
4. **Check responsible AI readiness**: bias, transparency, compliance (EU AI Act Aug 2026)
5. **Assess launch readiness**: clear signals, not vibes

All designed to work **without third-party annotators or large QA teams**  because startups don't have those.

---

## What's Included

### 📋 [Health Check Template](https://github.com/rashmierande/ai-ml-program-health-check/blob/main/framework/health_check_template.md)
A fillable one-page framework covering 7 dimensions:
- Product & Stage Snapshot
- Success Metrics (output quality, user impact, business, performance, data)
- Risk Map (rated 🟢🟡🔴 with mitigations)
- Evaluation & Quality Feedback Loop
- Responsible AI & Compliance
- Launch Readiness Signals
- Top 3 Action Items

### 📊 [Launch Readiness Metrics](framework/launch_readiness_metrics.md)
Detailed metrics cheat sheet- what to measure, how to track it, and target ranges across:
- Output Quality (hallucination, toxicity, relevance, groundedness)
- Business Impact (retention, conversion, NPS, cost per inference)
- System Performance (latency, throughput, uptime)
- Data Pipeline (freshness, drift, labeling accuracy)
- Evaluation Loop (regression rate, human-AI agreement, fix rate)
- Responsible AI (bias score, PII exposure, incident response)
- Launch Readiness Scorecard (🟢🟡🔴 go/no-go)

---

## Who Is This For?

- **Founders** building AI/ML products at MVP → early post-launch stage
- **Engineering leads** who need to define "done" for model quality
- **TPMs/PMs** driving AI product launches without dedicated QA teams

---

## How to Use

1. Open the [Health Check Template](framework/health_check_template.md)
2. Fill it in for your product alone or with your team
3. Identify your top 3 risks and action items
4. Use the [Launch Readiness Metrics](framework/launch_readiness_metrics.md) to go deeper on what to track

---

## Background

Built from experience shipping AI/ML systems at Amazon — including GenAI pipelines with ML classifiers, evaluation systems combining automated scoring with human-in-the-loop review, and IoT product launches with AI-powered field support.

The Responsible AI section reflects the upcoming **EU AI Act** (full enforcement August 2, 2026) requirements for high-risk AI systems.

---

## Feedback

This is a living framework — I'm actively iterating based on real conversations with founders. If you've used it, I'd love to hear what worked and what didn't.

📧 eranderashmi25@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/rashmierande)

---

*Created by Rashmi Erande — Technical Program Manager specializing in AI/ML program delivery and evaluation systems*
