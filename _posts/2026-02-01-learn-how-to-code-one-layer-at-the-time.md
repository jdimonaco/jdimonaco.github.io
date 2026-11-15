---
layout: post
title: Learning to Code, One Layer at a Time
date: 2026-07-01 15:01:35 +0100
image: '/images/fotis.jpg'
tags: [Coding]
---
When I first started coding, my instinct was to jump straight into “proper” solutions - modular code, reusable functions, clean structure. That’s what good code looks like, right?

What I didn’t realise at the time was that jumping too early into abstraction actually made things harder to understand. I could follow patterns, but I didn’t always understand why the code worked.

I was writing code that looked organised, but I wasn’t always confident I could explain it line by line. When something broke, debugging felt more like trial and error than reasoning. I could make changes, but I wasn’t always sure what the knock-on effects would be.

That gap between writing code and understanding it became increasingly obvious as projects grew. As soon as logic was hidden behind functions or spread across files, small mistakes became harder to trace, and learning slowed down instead of speeding up.

Over time, I realised the issue wasn’t the concepts themselves, it was the order I was learning them in. Abstraction is powerful, but only when it’s built on a solid mental model of how the code behaves.

That’s when I started to approach coding differently: not by aiming for the cleanest structure upfront, but by letting structure emerge once the logic was clear. The result was a simple three-step approach that worked far better for me, and fundamentally changed how I think about coding.

<div class="gallery-box">
  <div class="gallery">
    <img src="/images/laptopbnw.jpg" loading="lazy" alt="Black and white photo of code on a laptop screen">
  </div>

</div>

## Step 1: Start with simple, visible code

I began with small, linear blocks of code. No functions. No clever structure. Just code that runs from top to bottom.

At this stage, the goal wasn’t elegance, it was clarity.

Simple scripts made it easy to:

* See exactly what each line was doing

* Debug errors without jumping between files

* Experiment freely without worrying about design

This stage helped me build intuition. I could trace the flow of data, understand how variables changed, and develop confidence that I knew what was happening, not just that the code worked.

## Step 2: Turn repetition into functions

Once the logic made sense, patterns started to emerge. The same blocks of code appeared again and again, with small variations.

That’s when I introduced functions.

Refactoring working code into functions helped me:

* Reduce duplication

* Give meaningful names to pieces of logic

* Think in terms of inputs and outputs

At this point, functions weren’t about optimisation - they were about expressing intent. Naming a function forced me to articulate what the code was actually doing, which often exposed gaps in my understanding.


## Step 3: Move to modular code

Only after I was comfortable with functions did modular coding really click.

Breaking code into modules, separate files with clear responsibilities, brought obvious benefits:

* Better maintainability

* Cleaner structure

* Easier testing and reuse

But it also introduced new complexity. Understanding how data moves across modules, how dependencies are managed, and where logic should live isn’t always intuitive, especially for beginners.

Because I’d already worked through the logic step by step, modularisation felt like a natural progression, not a leap into abstraction.


> Programs must be written for people to read, and only incidentally for machines to execute.
> <cite>Harold Abelson</cite>

---

## Why this approach worked for me

Modular code is powerful, but it hides detail. That’s great for maintenance, but challenging when you’re still learning how code behaves.

By moving from:
scripts → functions → modules,
I learned not just how to write code, but how to reason about it.

This approach helped me:

* Debug more effectively

* Read other people’s code with confidence

* Design solutions rather than just implement them

It also reinforced an important lesson: good code isn’t just about structure - it’s about understanding.

---

## In practice: one project, three versions

My [airline review sentiment project](/project/sentiment-analysis) went through exactly these three stages:

1. **Blocks of code.** Every step, from checking the site's rules to plotting the word clouds, ran as simple blocks of code from top to bottom. Easy to follow, easy to debug, and the place where I learned what each line was doing.
2. **Functions.** Repeated blocks became named functions, such as checking the site's rules, extracting reviews and saving them, with clear inputs and outputs.
3. **A modular program.** Each function moved into a module with one job (`scraping.py`, `storage.py`, `nlp.py` and so on), and a Prefect flow in `main.py` runs the whole pipeline in order.

Because I had built the first two versions, the third was a reorganisation of logic I already understood, not a leap into the unknown.

---

## A mindset shift, not just a technique

Looking back, this wasn’t really about Python syntax or best practices. It was about learning to manage complexity incrementally.

* Starting simple gave me visibility.
* Refactoring into functions gave me structure.
* Modularising gave me scale.

That progression mirrors how real systems grow, and learning to code the same way made the process far more intuitive.

## Closing thought

There’s a lot of pressure to write “clean” or “professional” code from day one. But clarity comes before elegance.

For me, building from simple scripts toward modular systems wasn’t a shortcut, it was the path that finally made coding make sense.

---

## Key takeaways

- Write simple, linear code first, so you understand exactly what it does.
- Turn repetition into named functions once the logic is clear.
- Move to modules when the code needs to be maintained, tested or reused.

