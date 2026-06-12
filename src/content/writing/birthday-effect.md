---
title: "Do Indonesians Die More on Their Birthday? I Tested It."
description: "I found a study claiming you're more likely to die on your birthday. I didn't believe it. So I pulled 3,924 names from a public database and ran the math myself."
date: 2026-06-12
tags: ["data", "statistics", "indonesia"]
draft: false
---

There's a study that claims you are more likely to die on your birthday than any other day of the year.

Not slightly more likely. Measurably, statistically more likely. Researchers in Switzerland tested it on 2.4 million people. The result: a 13.8% spike in deaths on birthdays. American researchers found the same thing. British researchers too. The effect keeps showing up, across countries, across decades.

The theory is strange but weirdly believable. Some people psychologically hold on — delay death just long enough to reach a milestone they cared about. Others drink too much at the party. The stress of turning 60, or 70, or 80 tips something over the edge. Your body knows what day it is, in some biological or emotional way we don't fully understand.

I read about this a few months ago in [a piece by The Pudding](https://pudding.cool/2025/04/birthday-effect) — a data journalism publication that visualizes ideas with evidence. They tested it on 57,000 Massachusetts death records and found a 7% birthday spike. Immediately I thought: *has anyone tested this in Indonesia?*

As far as I could find — no.

So I did it myself.

---

## Getting the Data

The original studies used government mortality records — tens of thousands of death certificates with both a birth date and a death date on file. Indonesia has this data too, held in the Dukcapil civil registration system. It's just not public.

So I went with what was available: **Wikidata**, the structured database that sits behind Wikipedia. Every notable Indonesian — every politician, athlete, writer, musician, general, anyone significant enough to have a Wikipedia page — potentially has a birth date and death date recorded there.

I wrote a script to pull all of them. The query was simple: give me every person with Indonesian citizenship, a precise birth date, and a precise death date. I asked for day-level precision specifically, which matters more than it sounds.

Here's why: Wikidata stores some dates with only year-level accuracy. If they know someone died in 1952 but not exactly when, they'll store it as `1952-01-01`. If that person was also born on January 1st — or if their birth date similarly defaults to January 1st — the system would record them as dying on their birthday. Multiply that across hundreds of records and you get a completely fake birthday spike.

The first time I ran my analysis without that precision filter, I got a **+2,161% birthday effect**. Which is obviously wrong.

After filtering for only records where the exact day is known: **3,924 people**, deaths from 1902 to 2026, average age at death 67 years.

---

## The First Test

The logic is straightforward. For each person, I calculated one number: how many days was their death from their nearest birthday? Someone born March 7th who died March 10th gets +3. Someone who died February 28th gets -7. Every death gets mapped onto a scale from -182 to +182 days (roughly six months either side of the birthday).

If birthdays don't matter at all, deaths should spread roughly evenly. About **10.7 people per day**.

Here's what actually happened:

![Distribution of deaths relative to birthday, from -6 months to +6 months. The red bar at the center is the birthday.](/images/birthday/01_birthday_distribution.png)

The red bar at the center is day zero — the birthday itself.

**17 people** died on their birthday. Against an expected 10.7.

That's +58% above average. The statistical test came back with **p = 0.047** — which means there's a 4.7% chance this result happened purely by random luck. The standard cutoff for calling something significant is 5%. So technically, we crossed the line.

But barely. This is the weakest possible version of a significant result. If two of those 17 birthday deaths turned out to be data entry errors, the finding evaporates. I wasn't satisfied.

---

## What If It's Not One Exact Day?

Think about what the birthday effect actually describes. It's not a timer that goes off at midnight. It's a fuzzy psychological and physiological phenomenon — stress building in the days before, celebration and alcohol on the day itself, emotional letdown after. That doesn't land on one precise calendar date.

So I widened the window. Instead of just day 0, I looked at the whole birthday week: three days before, the birthday itself, three days after.

![Zoomed view of deaths ±30 days around the birthday](/images/birthday/02_birthday_zoomed.png)

**93 people** died in that seven-day window. Expected: 75.3.

That's **+23.6% above average**, with **p = 0.025**.

This is more convincing. P = 0.025 means there's only a 2.5% chance this is random noise. And unlike the single-day result, removing five or ten people from the window wouldn't flip the conclusion. The birthday week effect is more stable, more biologically intuitive, and statistically stronger.

---

## The Part That Confused Me

When I broke the results down by age group, something unexpected happened:

![Birthday effect broken down by age group — under 60, 60-74, and 75+](/images/birthday/04_birthday_by_age.png)

Every global study shows the birthday effect strongest in the elderly. The theory makes intuitive sense — an 80-year-old holding on to reach their 81st birthday is a real psychological phenomenon called the "anniversary reaction."

Our data shows the opposite. The strongest effect is in people **under 60**, and it disappears entirely in the 75+ group.

My best explanation: recording bias. When a young, prominent Indonesian dies unexpectedly — an accident, an illness, an assassination — the event gets documented carefully, the exact dates get recorded precisely. When an 80-year-old politician dies quietly, the date might get rounded to the nearest month or year in the records. So our "under 60" group has cleaner data, which happens to show the birthday signal more clearly.

This is the limitation of working with Wikidata instead of proper mortality records.

---

## What Can We Actually Conclude?

Let me be straight about what this data can and cannot say.

**What it suggests:** There is a birthday effect in Indonesian notable people. Deaths cluster around the birthday more than random chance predicts. The birthday week result is statistically meaningful.

**What it can't prove:** Whether this is true for all Indonesians. Whether the effect is driven by psychology, biology, behavior, or some combination. Whether the under-60 finding is real or an artifact of how data gets recorded.

**What a proper study would need:** Access to actual Indonesian civil registration data — millions of records, not thousands, with cause-of-death information and a correction for seasonal death patterns. Indonesia has this data. It's just not public.

The 17 Indonesians who died on their exact birthday are real people. Arif Rahman Hakim, the student activist killed during the 1966 demonstrations — born February 24th, died February 24th, age 23. Ramadhan K.H., the poet and novelist — born March 16th, died March 16th, age 79. Oemar Seno Adji, the legal scholar — born December 5th, died December 5th, age 69.

Real names. Real dates. A pattern that, across 3,924 people, shows up more than chance would predict.

Is the birthday effect real in Indonesia? Probably yes — at least directionally. Is this analysis definitive proof? No. But it's a start, and the data is there for anyone who wants to do it properly.

---

*Data: Wikidata via SPARQL, filtered for day-level precision dates only. Statistical test: one-sided binomial test. Sample: 3,924 notable Indonesians, 1902–2026. Full code on [GitHub](https://github.com/rvldsgl).*
