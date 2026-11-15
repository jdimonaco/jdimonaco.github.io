---
layout: post
title: Data Science in the Age of AI Regulation
date: 2025-09-05 15:01:35 +0100
image: '/images/chain.jpeg'
tags: [Ethics]
---
Since I started working in data, the pace of the field has felt one-directional: build, ship, iterate, repeat. Regulation, when it came up at all, felt like something that happened to other industries. That's changed quickly, and I've noticed my own instincts changing with it.

With frameworks such as the EU AI Act now in force and scrutiny around automated decision-making growing everywhere else too, I've started asking a different first question on new projects. It's no longer just "does this work?" It's "can I explain why it works, to someone who isn't going to take my word for it?"

That shift hasn't slowed me down as much as I expected it to. If anything, it's made the work feel more solid.

## From proof of concept to something I can defend

Early in a project, the questions used to be simple: can the model predict, can it classify, does it beat a baseline? Those are still the first questions I ask, but they're no longer the last ones.

Now I find myself asking whether the system can be explained, whether it can be audited, whether someone could challenge a specific output and get a real answer, and whether it fails safely when it's wrong. For anything touching finance, healthcare, recruitment, or public services, that traceability isn't optional; every data source, feature decision, and evaluation choice needs to be something I could stand behind months later, not just something that worked in a notebook once.

Reproducibility used to be good practice. Now it's closer to a requirement, and honestly, I think that's made me a better practitioner.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/alexander-sinn-YYUM2sNvnvU-unsplash.jpg" loading="lazy" alt="Binary code with a gap cut into it">
  </div>
  <em>Photo by <a href="https://unsplash.com/@swimstaralex">Alexander Sinn</a> on <a href="https://unsplash.com/photos/YYUM2sNvnvU">Unsplash</a></em>
</div>

## Governance stopped being someone else's job

A few years ago, "AI governance" sounded like a job title in a different department. Now it shows up in my own workflow: model registries, risk classification, sign-off steps before something goes live, monitoring that doesn't stop once a model ships.

None of that has to mean slower innovation. What it actually means, in practice, is that structure gets built in from the start instead of bolted on after something goes wrong. Clear ownership of each model, ongoing performance monitoring, bias and fairness checks, version control on both data and models, and a defined path for escalating a problem, those things used to feel like overhead. Now they feel like the difference between a model I trust and one I'm hoping works.

## Explaining why is now part of the job

The more complex a model gets, the harder, and the more important, it becomes to explain what it's doing. Stakeholders don't want a black box with good metrics. They want to know why a particular decision came out the way it did, and that question doesn't go away just because the model performs well.

I've come to see explainability as less of a compliance checkbox and more of a genuinely useful discipline. Feature importance, interpretable models where they're a real option, post-hoc explanation techniques where they're not, these aren't extras I add if there's time. They're part of how I build trust with the people who actually have to use what I've made.

## In practice: explaining a model, not just scoring it

In my [early warning model for air cargo delays](/project/early-warning-air-cargo-delays/), the headline result was a modest ROC-AUC of 0.628. On its own, that number would not convince anyone to act. What made the project useful was being able to explain it.

Using SHAP, I could show which features drove each prediction, and that for shipments where a handling note contradicted a clean milestone record, the model relied on exactly the contradiction flags built to catch that. I could also show the uncomfortable part: across all shipments, most of the signal came from the meaning of the notes, and the model caught fewer than a third of delays.

That combination, a clear reason for every flag and an honest account of what the model misses, is what turns a prediction into something a team can trust. It is also exactly what a regulator, or a sceptical manager, would ask for.

## What this means for how I work now

The tension between moving fast and building things properly hasn't disappeared, and I don't think it should. But I've started designing with regulation in mind from the outset rather than retrofitting it later, and the systems that come out the other end are usually more robust for it. Documentation stops being a chore I put off. Risk gets managed as I go, not discovered in a review meeting.

I don't think of regulation as a constraint on the work anymore. I think of it as a signal that the field is growing up, and that being good at this job now means being good at more than just the modelling part.

## Closing thought

The role I trained for was mostly about building things that work. The role I'm actually doing now asks something more: build things that work, and be ready to explain, defend, and stand behind how they got there. That's a higher bar. I'm glad it's the one we're being held to.

---

## Key takeaways

- Ask "can I explain why it works?" as early as "does it work?".
- Build traceability in from the start: data sources, feature choices and evaluation decisions should all be easy to defend later.
- Explainability tools such as feature importance and SHAP are not extras. They are how people come to trust a model.

