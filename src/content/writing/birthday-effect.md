---
title: "Do Indonesians Die More on Their Birthday? I Tested It."
description: "I found a study claiming you're more likely to die on your birthday. I didn't believe it. So I pulled 3,924 names from a public database and ran the math myself."
date: 2026-06-12
tags: ["data", "statistics", "indonesia"]
draft: false
---

Here's a fun fact to ruin (liven) birthday parties with: you are statistically more likely to die on your birthday than any other day of the year.

Researchers in Switzerland tested this on 2.4 million people. The result: a 13.8% spike in deaths on birthdays. American researchers confirmed it. British researchers too. It just keeps showing up.

Nobody fully agrees on why. Some people psychologically hold on — refuse to die before reaching a milestone they cared about. Others blame the birthday itself: celebration, alcohol, the emotional weight of getting older. Whatever the reason, the data says birthdays are weirdly dangerous.

I found out about this through [The Pudding](https://pudding.cool/2025/04/birthday-effect), a data journalism site that tested it on 57,000 Massachusetts death records and got a clean 7% birthday spike. Reading it, I had one question:

*Has anyone tested this in Indonesia?*

As far as I could find — no. So I did it myself. I'm unemployed. I have time.

---

## Step 1: Get the Data (This Part Was Harder Than It Sounds)

The proper way to do this is to get government death records — tens of thousands of death certificates, each with a birth date and death date. Indonesia has this data in the Dukcapil civil registration system. It is not public. I am not the government. Moving on.

Instead I used **Wikidata** — the structured database behind Wikipedia. Every notable Indonesian with a Wikipedia page potentially has a birth date and death date recorded there. Politicians, athletes, writers, musicians, generals. Anyone significant enough for someone to have bothered writing a Wikipedia page about them.

I wrote a script, hit their free API, and got the data.

Here's where I almost embarrassed myself.

The first time I ran the analysis, I got a **+2,161% birthday effect**. More than 21 times the expected rate. I spent about 10 minutes feeling like I had discovered something incredible before realizing the data was completely broken.

The problem: Wikidata stores some dates with only year-level accuracy. If they know someone died in 1952 but don't know exactly when, they store it as `1952-01-01` — January 1st as a default. If that person was also born on January 1st (or their birth date had the same problem), the system sees them as dying on their birthday. Multiply that across hundreds of records and you get a fake spike so large it should have immediately told me something was wrong.

I fixed it by filtering for only records where the exact day is actually known. The dataset went from 4,684 to **3,924 people**. The fake birthday spike disappeared. We could proceed with our lives.

---

## The Actual Test

For each of the 3,924 people, I calculated one number: how many days from their nearest birthday did they die? Born March 7th, died March 10th — that's +3. Born March 7th, died February 28th — that's -7. Everyone gets mapped onto a scale from -182 to +182 days (about six months either side of their birthday).

If birthdays don't matter, deaths should spread pretty evenly. About **10.7 people per day**.

Here's what actually happened:

![Distribution of 3,924 deaths across the year, relative to each person's birthday. The red bar is the birthday.](/images/birthday/01_birthday_distribution.png)

The red bar is the birthday. Day zero.

**17 people** died on their birthday. Against an expected 10.7.

That's +58% above average. The statistical test (a binomial test — basically asking "how likely is this if the birthday is just a random day?") returned **p = 0.047**.

P-value means: how likely is this result if nothing special is actually happening? P = 0.047 means 4.7% likely — which sounds small, but the cutoff for "statistically significant" is 5%. So we technically passed. By a margin so thin you could slide it under a door.

Remove two people from that birthday count and the result flips. Not great.

---

## Okay But What If I'm Looking at This Wrong

Here's the thing. The birthday effect — if it's real — probably doesn't work like a countdown timer. You don't die exactly at midnight on your birthday. If the effect exists, it probably spreads across the days around the birthday. Stress in the days before. Celebration and alcohol on the night. Emotional crash after.

So I tried the birthday week: three days before, the birthday, three days after.

![Zoomed view of deaths in the ±30 days around the birthday](/images/birthday/02_birthday_zoomed.png)

**93 people** died in that seven-day window. Expected: 75.3.

**+23.6% above average. P = 0.025.**

Now we're talking. 2.5% chance this is random noise. Removing ten people from the count doesn't flip the conclusion. This is the more convincing result, and honestly the more believable one — because "people die more in the vague week around their birthday" makes a lot more biological sense than "people die on the exact calendar date of their birthday."

---

## The Finding That Made Me Confused

When I broke the results down by age group, I expected the elderly to show the strongest effect. That's what every global study finds — older people holding on to reach one more milestone.

Our data said the opposite.

![Birthday effect by age group — under 60, 60-74, and 75+](/images/birthday/04_birthday_by_age.png)

Under 60 showed the biggest spike. The 75+ group actually had *fewer* birthday deaths than average, which is the exact opposite of what the theory predicts.

My best guess: recording bias. When a young prominent Indonesian dies unexpectedly, people pay attention. The exact date gets documented carefully. When an 80-year-old politician quietly passes, the date might get rounded to the nearest month in the records. So our dataset just has cleaner data for younger notable people — and cleaner data shows the birthday pattern more clearly.

Which is a long way of saying: the data has limits and I cannot fully trust this finding. Very honest of me.

---

## So What Did We Learn

Look, I'm going to be real with you.

The birthday effect is probably real in Indonesia, at least directionally. Deaths cluster around the birthday more than random chance predicts. The birthday week result holds up pretty well. P = 0.025.

But this is 3,924 notable people from a public database — not a representative sample of 270 million Indonesians. The finding is suggestive, not conclusive. A proper study would need access to actual national mortality records, cause-of-death data, and more rigorous statistical controls.

Indonesia has all of that data. It's just not public. Until it is, this is the best I can do with what's available.

The 17 people who died on their exact birthday are real names in a real database. Arif Rahman Hakim, student activist, born February 24th, died February 24th 1966, age 23. Ramadhan K.H., poet and novelist, born March 16th, died March 16th 2006, age 79. Oemar Seno Adji, legal scholar, born December 5th, died December 5th 1984, age 69.

Real people. Real dates. A pattern that shows up in the data.

Make of that what you will. 

---

*Data: Wikidata via SPARQL, filtered for day-level precision only. Statistical method: one-sided binomial test. n = 3,924 notable Indonesians, 1902–2026. Full code on [GitHub](https://github.com/rvldsgl/birthday-effect-id).*
