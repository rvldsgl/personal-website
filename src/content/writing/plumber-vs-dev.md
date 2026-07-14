---
title: "Is Being a Plumber Better Than Being a Software Engineer in 2026?"
description: "I've been applying for tech jobs for months. One night I had a weird thought. So I looked it up."
date: 2026-07-14
tags: ["data", "career", "tech"]
draft: false
---

I've been applying for software engineering jobs for a while now.

Mostly silence. Occasional rejections. The rare first-round interview that goes nowhere.

At some point around midnight, I had a thought that felt slightly embarrassing to have: *what if I had just become a plumber?*

Not seriously. Just — the thought showed up. And once it did, I couldn't stop thinking about it. So I did what I always do when I can't stop thinking about something. I pulled the data.

---

## The advice wasn't wrong

Here's the thing I want to be clear about before anything else: the people who told me to go into tech weren't lying.

In 2019, the data genuinely supported it. Coding bootcamps were reporting placement rates above 80%. Graduates were getting hired. The "learn to code and get a job" narrative was everywhere — LinkedIn posts, YouTube videos, your uncle at family dinner. And it made sense, because it was roughly true.

Bootcamp enrollment numbers backed it up. According to Course Report, about 18,000 people graduated from full-time coding bootcamps in 2019. By 2020 that number jumped to 25,000 — a 39% increase in a single year, partly because COVID pushed everything online.

People were betting on tech. And at that point, the bet was paying off.

---

## Then two things happened at the same time

The first thing: supply kept going up.

More bootcamps. More CS graduates. More people pivoting into tech during the pandemic, learning to code from YouTube, finishing online courses, adding Python to their LinkedIn. The number of people competing for junior developer jobs kept climbing.

The second thing: demand for junior work started going away.

GitHub Copilot launched in June 2022. ChatGPT came out in November 2022. GPT-4 in March 2023. These tools didn't replace senior engineers — they replaced the kind of work that used to be a good first job. Writing boilerplate. Generating CRUD operations. Fixing basic bugs. The stuff you learned in a bootcamp.

Junior developers got hit from both sides. More competition coming in. Less work available on the other end.

And more recently, companies have started saying it out loud. Layoffs explicitly attributed to AI have been rising fast — Q1 and Q2 2026 are the biggest quarters on record for AI-cited workforce reductions.

![Tech layoffs attributed to AI vs non-AI, quarterly. AI-attributed share growing rapidly in 2026.](/images/plumber-vs-dev/layoffs_ai.png)

---

## The numbers

I want to be careful here. I'm one person with publicly available datasets, not a labor economist. But the direction is pretty clear.

**Tech layoffs:** According to layoffs.fyi, about 265,000 tech workers were laid off in 2023 alone. That's the peak — before that, 165,000 in 2022. After that, 153,000 in 2024, 123,000 in 2025. We're talking about roughly 700,000 tech workers losing their jobs in four years.

![Tech layoffs since COVID-19 — quarterly. The peak is clearly visible around Q1 2023.](/images/plumber-vs-dev/layoffs_covid.png)

**Bootcamp outcomes:** The Council on Integrity in Results Reporting (CIRR) audits bootcamp placement data independently. Their number: 71% of graduates get a job within 180 days. That's often presented as a success story. But it also means 29% don't get a qualifying job within six months. That number never shows up in the marketing.

**Junior salaries:** I ran the Stack Overflow Developer Survey data — they've published it annually since 2019. In 2019, the median salary for US developers with 0–2 years of experience was $75,000. In 2025: $74,000. Sounds fine. But the floor dropped — the 25th percentile went from $60,000 to $40,000. The people at the bottom got hit hardest.

![Junior developer salary comparison 2019 vs 2025 — floor dropped from $60k to $40k](/images/plumber-vs-dev/03_salary.png)

Here's the one that actually surprised me though: in the 2019 survey, there were **1,857 junior US developers** who responded. In 2025, that number is **58**.

![Junior US developers in SO Survey (0-2 years experience): 1,857 in 2019 vs 58 in 2025](/images/plumber-vs-dev/02_junior_count.png)

Fifty-eight.

I'm not entirely sure what that means. Maybe junior developers stopped taking surveys. Maybe they don't identify as developers yet because they're still looking. Maybe there just aren't that many of them actively working. Probably some combination. But 1,857 down to 58 is hard to explain away.

One more thing worth noting honestly: BLS projects software developer jobs to grow 15% through 2034. That's "much faster than average." So tech isn't dying. It's just that the growth is happening at the senior end. The entry-level pipeline has tightened.

---

## So what about the plumber

I actually looked this up. Here's what BLS says about plumbers, pipefitters, and steamfitters in 2024:

Median pay: **$62,970 per year.**

Projected annual job openings: **44,000.**

The 4% job growth projection sounds modest, but those 44,000 openings per year aren't mainly from growth — they're from retirement. The existing workforce is aging out and there aren't enough people coming in to replace them. It's a shortage, not a boom.

The entry path is also different from what I expected. You do an apprenticeship — which typically takes 4 to 5 years. But you get paid while you're doing it. Compare that to a coding bootcamp where you pay $15,000 upfront, or a four-year degree that costs considerably more.

The work can't be done remotely. It can't be offshored. And for now at least, it can't be automated — pipes break in specific locations, in specific conditions, in ways that require someone to physically be there and figure it out.

![Plumber vs Software Developer 2024 — median pay and annual job openings](/images/plumber-vs-dev/04_comparison.png)

I'm not saying it's easy work. I'm not saying it's for everyone. I'm saying I never actually thought to compare these things side by side when I was deciding what to do.

---

## Why didn't anyone say this

I think the answer is pretty simple: the people giving career advice mostly live in the same world as the people getting it.

Everyone online works in tech. Career advice content is made by people in tech. Bootcamps had VC money and a strong incentive to run aggressive marketing. The "learn to code" narrative dominated because the people repeating it were the people who had already won from it.

There's also a lag. The advice that got handed down in 2022 was based on 2019 conditions. By the time the job market actually shifted, the advice hadn't caught up. It takes years for a narrative to update. People are still sending their kids to bootcamp.

I followed advice that was reasonable when it was given. It just might have been two or three years out of date by the time I followed it.

---

## What I actually think

I'm not going to tell you to become a plumber. That would be a weird conclusion to draw from a survey dataset and some BLS tables.

What I think is this: I asked "should I go into tech?" and compared it to basically nothing. I didn't look at the trades. I didn't run the numbers on anything else. I just followed the gravity of the advice around me.

If I was making the same decision today, I'd at least ask the question.

The data is what it is. Tech still has a higher ceiling if things go well. Plumbing has a more predictable floor. For someone going in because it seemed safe — which is why most people do anything — the floor matters more than the ceiling.

---

*Data sources: Stack Overflow Developer Survey 2019 and 2025 (raw CSV). Bureau of Labor Statistics Occupational Outlook Handbook. Layoffs.fyi. CIRR audited bootcamp outcomes via Course Report. All analysis done in Python.*
