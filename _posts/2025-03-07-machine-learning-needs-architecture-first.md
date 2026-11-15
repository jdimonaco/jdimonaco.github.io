---
layout: post
title: Machine Learning Needs Architecture First
date: 2025-09-25 15:01:35 +0100
image: '/images/machine_learning.jpeg'
tags: [Architecture]
---
When people talk about machine learning projects, the conversation often starts with models: which algorithm to use, which framework performs best, which library is most “production ready”.

It’s an understandable instinct. Models are visible. They’re measurable. They feel like progress.

But over time, I’ve come to realise that most machine learning projects don’t succeed or fail because of model choice. They succeed or fail because of the systems built around those models — and the tools chosen to support them.

## The model is rarely the problem

In isolation, many models work surprisingly well.

Given a clean dataset and a clear objective, it’s often possible to train something that performs convincingly. Accuracy looks good. Validation metrics behave. The notebook tells a reassuring story.

The problems tend to appear later.

Predictions can’t be reproduced. Training data drifts silently. Pipelines break when volumes increase. Outputs stop being trusted because no one is quite sure how they were produced.

At that point, attention shifts away from the model and toward everything else — data, infrastructure, orchestration, deployment. That’s where most of the real complexity lives.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/architecture.jpeg" loading="lazy" alt="Connected wooden blocks laid out like a system diagram">
  </div>

</div>

## Why data architecture comes first

Before choosing any machine learning framework, it’s worth understanding the shape of the data system the model will live in.

Where does the data originate?
How frequently does it change?
Is it raw, partially transformed, or heavily curated?
Who owns it, and how is quality enforced?

These questions aren’t peripheral. They determine whether a model can be trained reliably, retrained consistently, and trusted over time.

Without a clear data architecture, tool choices become guesses. You may end up optimising for experimentation when you need stability, or building for scale before you understand behaviour.

Understanding how data flows through the system provides the constraints that make sensible tool selection possible.

<div class="gallery-box">
  <div class="gallery gallery-columns-1">
    <img src="/images/cubes.jpeg" loading="lazy" alt="A hand placing a block labelled BI on top of a stack of icon blocks">

  </div>

</div>

## How tools shape outcomes quietly

Tools do more than enable functionality — they encode assumptions.

Some tools prioritise flexibility, allowing transformations to evolve close to analysis. Others enforce structure early, trading agility for consistency. Some scale effortlessly but require strong governance to avoid chaos. Others are rigid but safe.

These choices shape three things that matter far more than model performance:

**Reliability**
Can the system produce the same result tomorrow that it produced today? Can failures be detected and diagnosed quickly?

**Scalability**
Can the system cope when data volumes grow, features expand, or retraining becomes more frequent?

**Trust**
Can stakeholders understand where predictions come from, and feel confident using them in decisions?

When tools are chosen without architectural clarity, these qualities emerge by accident — if at all.

## From experiments to systems

One of the biggest mindset shifts in applied machine learning is recognising when experimentation ends and system design begins.

Notebooks are excellent for exploration. They’re less effective as production artefacts. Moving from one to the other requires different tools, different structures, and different expectations.

This is where understanding data architecture becomes essential. It guides decisions about where transformations live, how pipelines are orchestrated, how models are deployed, and how performance is monitored over time.

The goal isn’t to eliminate flexibility — it’s to place it deliberately.

## In practice: the same model, three different systems

I saw this first-hand in my [airline review sentiment project](/project/sentiment-analysis). The analysis began as a single notebook, and it worked. But every rerun meant scrolling, re-executing cells in the right order and hoping nothing had changed on the website.

Rebuilding it as a modular pipeline changed very little about the analysis itself and a great deal about the system around it. Each step now has one job: one module checks the site's rules, one downloads the pages, one stores the reviews, one scores sentiment, and a Prefect flow runs them in order. Raw pages are saved locally, so the analysis can be rerun without touching the website again, and the sentiment model could be swapped for a better one without rewriting the scraping code.

My [fleet performance app](/project/fleet-performance-forecasting) followed the same principle. The analysis classes know nothing about the Streamlit interface, so the same code runs in the web app, from the command line and in the tests.

## Closing thought

Machine learning maturity isn’t measured by how advanced your models are. It’s measured by how well your systems support them.

Choosing the right tools matters, but only after the data architecture is understood. When tools are selected to reinforce reliability, scalability, and trust, models have the space to do what they’re meant to do — inform better decisions, consistently and transparently.

In the end, machine learning isn’t just about prediction. It’s about building systems people can rely on.

---

## Key takeaways

- Most machine learning problems appear after the notebook: reproducibility, drift, scale and trust.
- Understand where the data comes from, how often it changes and who owns it before choosing tools.
- Separate the steps of a pipeline so each one can be tested, rerun or replaced on its own.

