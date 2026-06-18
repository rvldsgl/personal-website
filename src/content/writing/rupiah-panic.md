---
title: "Rupiah Hit 18,000. Did Indonesians Actually Panic?"
description: "I don't know much about economics. But I do know how to check what people were Googling. So I did that instead."
date: 2026-06-18
tags: ["data", "indonesia", "economics"]
draft: false
---

In early June 2026, the rupiah hit Rp18,190 per dollar.

That's a record. The weakest it's ever been in modern Indonesian history.

I'm not an economist. I can't tell you about monetary policy or trade deficits or whatever. But I can tell you what people were Googling — and that's actually kind of interesting.

So that's what I did.

---

## The idea

Economists measure currency crises with official data: inflation rates, trade numbers, GDP. That stuff takes months to compile.

But Google Trends is real-time. Every time someone in Indonesia types "beli dolar" into Google, that gets counted. And if a lot of people are suddenly Googling that at the same time — that's a signal. Not a perfect signal, but a signal.

So I grabbed two things:

1. **The actual USD/IDR exchange rate** — daily, January to June 2026
2. **Google Trends data** for a bunch of Indonesian search terms — weekly

Then I put them side by side and asked: *when the rupiah fell, what were people searching for?*

---

## How the rupiah moved

Here's what the exchange rate actually looked like this year:

![USD/IDR exchange rate January to June 2026 — showing the steady rise from Rp 16,668 to the historic peak of Rp 18,190 on June 9](/images/rupiah/01_overview.png)

January: Rp16,668. Pretty normal.

Then it started creeping up. Slowly at first. Then faster in May. Then in the last two weeks of May and early June — it broke through Rp18,000 for the first time ever, and peaked at Rp18,190 on June 9.

Why? Short version: conflict in the Middle East pushed oil prices up. Indonesia imports a lot of oil, so it needed to buy more dollars to pay for that. More dollar demand + shrinking trade surplus = rupiah gets weaker. That's basically it.

---

## What people were actually doing

### The most important chart

This one surprised me:

![Dual-axis chart: USD/IDR rate (red, daily) vs beli dolar Google searches (blue dashed, weekly). Searches peaked May 31 — 9 days before the rate peaked on June 9.](/images/rupiah/02_beli_dolar_vs_rate.png)

The red line is the rupiah getting weaker. The blue dashed line is how many Indonesians were Googling "beli dolar" (literally: "buy dollars").

Notice something? The blue line peaks on **May 31**. The red line peaks on **June 9**.

People were Googling "buy dollars" at maximum intensity **9 days before** the rupiah actually hit rock bottom.

They saw it coming. Or at least, they felt it coming — and they were already trying to protect themselves before it got worst.

---

### All the search terms together

Here's the full picture:

![Panel chart showing all 6 search terms against the exchange rate. beli dolar, kurs dollar, dollar naik, and kurs rupiah all spiked in May-June. Resesi peaked in January and didn't spike with the crash.](/images/rupiah/03_all_terms_panel.png)

Let me walk through what each one means in plain English:

**"Kurs dollar" and "kurs rupiah"** — literally just checking the exchange rate. These had the strongest connection to the rupiah falling (correlation = 0.9 out of 1.0). Makes sense. When the number on the screen goes crazy, people check the number on the screen.

**"Beli dolar"** — buying dollars. When your currency is weakening, one way to protect your money is to convert it to a more stable currency. A lot of people were apparently thinking about this.

**"Dollar naik"** — "dollar is rising." People searching this are basically just noticing what's happening and putting it into words.

**"Inflasi"** (inflation) — weak connection (0.36). People don't immediately think "inflation" when the rupiah falls, even though the two are related. The link isn't obvious to most people.

**"Resesi"** (recession) — this one's the most interesting. It peaked in **January** — months before the actual crisis. When the rupiah was genuinely crashing in May-June, people had basically stopped Googling "recession." They weren't thinking big picture anymore. They were just watching the number go up.

---

## What this actually tells us

When the rupiah hit 18,000, Indonesians didn't respond by thinking about macroeconomics.

They did two things:

1. **Checked the rate** — obsessively, judging by the search data
2. **Looked into buying dollars** — trying to protect whatever savings they had

And they were already doing this before the rupiah hit its lowest point. Which means people were picking up on warning signs from the news and acting on them early — not waiting for official announcements.

That's not panic exactly. It's more like… quiet anticipation. People knew something was wrong before the worst had happened.

---

## Honest caveats

I should be upfront about the limits here.

**Google Trends only captures people who Google things.** Plenty of people worried about the rupiah and didn't search anything — they called their parents, asked in the family WhatsApp group, or just quietly moved money around without Googling first.

**The data is weekly, not daily.** So when I say searches peaked "May 31," I mean in the week starting May 31 — the actual peak could have been any day that week.

**Correlation isn't causation.** The searches and the exchange rate both moved at the same time, probably because they were both reacting to the same news. The searches didn't cause the rupiah to fall. The rupiah didn't cause people to Google things. Something else (geopolitics, oil prices) caused both.

---

## The short version

The rupiah hit its worst level ever in June 2026.

Before it got there, Indonesians were already Googling how to buy dollars.

Nobody was thinking about "recession." They were just watching the number — and quietly trying to figure out what to do about it.

I'm still waiting for it to get back to 16,000.

*(It hasn't.)*

---

*Exchange rate data from Yahoo Finance. Google Trends data from Google Trends. Charts and analysis done in Python. Full code on [GitHub](https://github.com/rvldsgl/rupiah-panic).*
