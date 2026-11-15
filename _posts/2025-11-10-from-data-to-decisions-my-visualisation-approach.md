---
layout: post
title: "From Data to Decisions: My Visualisation Approach"
date: 2026-01-22 15:01:35 +0100
image: '/images/linegraph.jpg'
tags: [Visualisation]
---
When I first started working with data, I thought visualisation was the final step, something you did once the “real” analysis was finished. Clean charts, tidy dashboards, maybe a bit of colour, and you’re done.

Over time, I realised that this way of thinking was backwards.

For me, data visualisation is not about presentation first. It’s about understanding, questioning, and communicating — often all at the same time.

Much like learning to code, I found that starting simple and building complexity gradually made a huge difference.

---

## Start simple: visualisation as exploration

My first visualisations are rarely pretty. They’re basic charts, quick plots, sometimes even messy. But that’s intentional.

At this stage, I’m not trying to impress anyone. I’m trying to answer simple questions:

* What does the data actually look like?

* Are there obvious trends or gaps?

* Does anything feel wrong or unexpected?

Simple visualisations help surface issues that tables often hide: missing values, outliers, strange distributions. They also help me build intuition before I draw conclusions.

Just like writing a simple script before refactoring, this step is about clarity, not polish.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/dashboard.jpg" loading="lazy" alt="A hand using a tablet that shows a dashboard">
  </div>

</div>


### Build understanding through iteration

As patterns start to emerge, visualisations evolve.

I might:

* Add time to see how things change

* Compare groups to spot differences

* Layer context to explain anomalies

Each iteration is driven by a question, not by design aesthetics. If a chart doesn’t help answer something meaningful, it usually doesn’t belong.

This step-by-step refinement mirrors how real understanding develops. Jumping straight to a fully formed dashboard often skips the thinking that matters most.

At this point, visualisation shifts from exploration to explanation, helping focus attention on what really matters.

## Define KPIs before designing dashboards

One of the biggest lessons I’ve learned is that dashboards don’t create clarity, KPIs do.

Before deciding what to visualise, I try to be explicit about:

* What problem are we trying to influence?

* What decision needs to be supported?

* What behaviour should change if this number moves?

Good KPIs are focused, actionable, and tied to outcomes. Bad ones are vague, static, or interesting but irrelevant.

Once KPIs are clear, visualisation becomes much easier. The chart isn’t there to show everything, it’s there to show what matters.

---

## Communicating with stakeholders, not just charts

A technically correct visualisation can still fail if it doesn’t land with the audience.

Different stakeholders care about different things:

* Operational teams want clarity and immediacy

* Managers want trends and risks

* Leadership wants impact and direction

That means the same data often needs to be framed differently. Sometimes the most effective “visualisation” is a single number with a short explanation.

I’ve learned that good communication often involves:

* Reducing complexity, not adding it

* Explaining why something matters, not just what it shows

* Being comfortable leaving details out

A chart should support the message, not compete with it.

---

## Less can be more

It’s tempting to add more charts, more filters, more metrics. But over time, I’ve found that the most useful dashboards often get smaller, not bigger.

Removing noise forces better questions:

* If I had to keep just one chart, which would it be?

* What would I look at if I only had 30 seconds?

* What would actually prompt action?

Visualisation isn’t about showing how much data you have. It’s about helping someone decide what to do next.

---

## In practice

You can see this approach in my [data visualisation portfolio](/project/data-visualisation). Each dashboard starts from one question and one audience. Global Disaster Hotspots, for example, uses a table of bars rather than a stacked chart, so every disaster type can be compared on the same starting line, and a single "Sort By" control replaces what would otherwise be six separate dashboards.

---

## Closing thought

Data visualisation sits at the intersection of analysis, communication, and decision-making. Done well, it turns complexity into clarity. Done poorly, it becomes decoration.

For me, the most effective approach mirrors how I learned to code:

* start simple

* build understanding

* add structure only when it earns its place

When visualisation is treated as a thinking tool rather than a finishing touch, data stops being something you report on — and starts becoming something you act on.

---

## Key takeaways

- Use quick, simple charts to understand the data before designing anything polished.
- Agree the KPIs and the decision a dashboard supports before choosing charts.
- If you could keep only one chart, which would it be? Start there.
