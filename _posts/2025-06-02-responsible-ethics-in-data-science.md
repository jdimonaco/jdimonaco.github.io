---
layout: post
title: Responsible Ethics in Data Science
description: Every dataset and algorithm carries human impact. Why ethics has to be designed into data science from the start, not checked at the end.
date: 2025-11-25 15:01:35 +0100
image: '/images/Ethics.jpeg'
tags: [Ethics]
---
It is easy to think of data science as a technical discipline: statistics, code, models, infrastructure. But every dataset I work with describes people, and every model I build ends up influencing a decision about someone. That is why I see ethics as part of the job, not a box to tick at the end.

Models already shape credit approvals, hiring, medical diagnoses, policing and the content people see every day. The question is no longer whether data science affects people's lives. It is whether we are doing it deliberately and responsibly.

## Bias begins before modelling

Most ethical problems do not start with the algorithm. They start much earlier, in how data is collected, labelled and interpreted.

Data reflects history, and history reflects inequality. If past hiring decisions favoured certain groups, a model trained on those decisions will learn to favour them too. If some communities appear more often in policing data, a predictive system may send even more attention their way.

Before I build anything, I try to ask a few uncomfortable questions:

* Who is represented in this dataset?
* Who is missing?
* What assumptions are built into the labels?
* What historical patterns would a model learn and repeat?

Fixing bias is not just a technical adjustment. It starts with noticing it.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/AI_heart.jpeg" loading="lazy" alt="A green leaf resting on a computer processor socket">
  </div>
</div>

## In practice: when a model learns the wrong lesson

I met this directly in my [employee attrition project](/project/employee-attrition-ann/), a personal project built on a synthetic dataset of 10,000 employees. In that data, 22.8% of women left, compared with 15.2% of men. Gender was one of the model's inputs, which means the model could learn to treat being a woman as a risk factor in itself.

That would be the wrong lesson. In a real organisation, a gap like this would be a reason to investigate what is happening to women, such as promotion, workload or flexibility, not a reason to flag individual women as likely to leave. So the project recommends retraining without protected characteristics and checking that predictions are equally accurate across groups before any real use, with every prediction leading to a supportive conversation, never an automated decision.

The model's accuracy did not change that conclusion. A model can be accurate and still unfair.

## Transparency and explainability

The more complex a model becomes, the harder it is to explain, and the more it matters. People affected by an algorithmic decision deserve an explanation they can understand.

Explainability builds trust, and it makes accountability possible. A highly accurate model that nobody can interpret may look good on paper while quietly undermining confidence in the people who use it. Good practice means balancing performance with clarity, so decision-makers understand both what the model can do and where it falls short.

## Privacy and consent

Data is not abstract. Every row represents a person.

Handling it ethically goes beyond meeting the law. I think about:

* **Consent:** did people understand how their data would be used?
* **Minimisation:** do I need this field at all?
* **Security:** is the data stored safely?
* **Retention:** how long should it be kept?

Just because data can be collected does not mean it should be. Responsible practice involves restraint as well as innovation.

Two of my projects show what this looks like in practice. My [early warning model for air cargo delays](/project/early-warning-air-cargo-delays/) was built on synthetic shipment data, so the whole workflow could be designed and tested without touching any real customer or operational records. And before collecting anything for my [airline review sentiment project](/project/sentiment-analysis), I checked the review site's rules for automated access, collected no personal information, and used the reviews for analysis only.

## Responsibility after deployment

Ethics does not end when a model goes live. Systems need monitoring for drift, unintended consequences and new forms of bias, and there should be a clear way to report and correct mistakes.

Ownership matters too. When an automated decision affects someone, responsibility cannot be handed to "the algorithm". Accountability always stays with people.

> Algorithms are opinions embedded in code.
> <cite>Cathy O'Neil</cite>

## Ethics as a design principle

Ethics works best as part of the design, not a final checklist. It belongs in every stage: how data is collected, which features are used, which model is chosen, how it is deployed and how it is monitored.

Building this way does not slow innovation down. It makes the results stronger. Systems that are fair, transparent and accountable are not only intelligent but trustworthy, and trust is the most valuable output any model can produce.

---

## Key takeaways

- Bias usually enters through the data and the labels, long before the algorithm.
- A pattern in the data, like a gender gap, is a question to investigate, not a feature to predict with.
- Keep people accountable: predictions should support human decisions, not replace them.
