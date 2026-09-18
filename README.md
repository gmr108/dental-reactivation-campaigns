# Dental database reactivation: how to turn a 12–24 month lapsed patient list into booked hygiene visits

Most dental practices are sitting on a reactivation campaign they never ran. A few hundred — sometimes a few thousand — patients who already know the office, already have a chart, and simply drifted. No new marketing spend required, no ad auction to bid on.

The reason those lists sit untouched isn't that nobody wants the revenue. It's that reactivation dies in the reply. Someone sends the first text, a patient answers at 8:40pm, and there's nobody at the front desk to catch it. Multiply that by 400 contacts and the campaign quietly stalls out.

This guide walks through the parts that actually matter: building a clean list, tiering it by reason instead of just recency, getting the first message out legally, and what happens to the hundreds of replies that arrive after hours. CloseBot, an AI agent platform used by healthcare and dental offices, comes in at that last step — so it's worth being specific about where it helps and where it doesn't.

## What dental database reactivation actually means

A working definition most practice management systems can produce in a few clicks: a patient who has visited at least once, has no future appointment scheduled, and hasn't been seen in 12 months or longer.

That's broader than the "18 to 24 months" cut many offices use, and the difference matters. A patient at month 13 still feels connected to your practice. A patient at month 34 may have moved, changed insurance, or forgotten the office exists.

Two things get confused as the same thing:

- **Hygiene drift.** A patient who was on a six-month recall and slowly stopped coming. Contact data is usually good, and a simple scheduling message often does the job.
- **Unfinished treatment.** A crown prep, phase-two perio, or an implant consultation that never got scheduled. These patients have a clinical reason to return, which makes them the highest-priority group in nearly every campaign.

Practices that lump all inactive patients into a single bucket end up sending generic "we miss you" messages to people with wildly different reasons for leaving. That's the fastest way to get ignored.

## Why the old playbook stalls at the front desk

The traditional reactivation sequence — pull a list, call the highest-value patients, follow up by email, then mail a postcard — still works. The problem is throughput.

A four-week multi-touch sequence across text, email, phone, and mail can reasonably book 8–15% of contacted patients within 60 days, based on figures WEO Media reports from its dental clients. Single-channel campaigns, by contrast, often land in the 1–3% range. So the math pushes you toward multi-channel, and multi-channel pushes you toward volume.

Here's where it breaks. If you contact 50–75 patients a week, your front desk can probably keep up. Send 500 texts on a Monday morning and replies arrive faster than anyone can answer them. Patients wait hours, momentum dies, and the practice concludes "reactivation doesn't work here."

Consent and compliance raise the bar further. Dental guidance from the California Dental Association is blunt about SMS not being inherently HIPAA-compliant, and reactivation texts generally require prior express consent and a clean opt-out. Any vendor touching patient data needs a signed business associate agreement in place.

## The four steps of a campaign that holds up

### Step 1: Build the list, then clean it

Pull everyone with no scheduled appointment and no visit in the last 12–24 months. Then subtract:

- Formally dismissed patients
- Deceased patients
- Patients who told you they moved out of the area
- Anyone flagged do-not-contact or who previously opted out

One practical warning: contact data decays. Practices commonly find that 15–25% of records for patients inactive longer than two years are out of date. Scrubbing phone numbers and emails before you launch saves your team from chasing dead lines and protects email deliverability.

### Step 2: Tier by reason, not just by date

A four-tier split that holds up in practice:

| Tier | Who's in it | Why they matter |
| --- | --- | --- |
| 1 | Incomplete treatment (pending crown, phase 2 perio, unscheduled implant consult) | Strongest clinical reason to return, highest urgency |
| 2 | Overdue hygiene, 12–18 months | Easiest to book, usually current contact info |
| 3 | Long-lapsed, 18–36 months | Needs a stronger value hook, some bad numbers |
| 4 | Very long-lapsed, 36+ months | Lowest priority, highest share of dead contact data |

The tier determines the message, not just the order. Tier 1 patients should hear that Dr. So-and-so asked about their treatment. Tier 4 patients need a genuine reason to care — updated technology, expanded hours, or a reminder that their insurance benefits reset.

### Step 3: Send the first message on purpose

Text performs best for reactivation, but only when it reads like a person, not a blast. Keep it short, use the first name, name the practice and the staff member, and offer a reply path. Something in the shape of:

> "Hi [First Name], this is [Staff Name] from [Practice Name]. We noticed it's been a while since your last visit and wanted to make it easy to get back on the schedule. We have openings this week. Reply YES to book or call us at [Phone]."

For incomplete-treatment patients, swap in the clinical reference instead. And check whether your existing intake consent actually covers marketing texts — the answer is worth confirming before you send anything.

### Step 4: Handle the replies — this is where campaigns live or die

Everything above is preparation. The campaign is decided in the hours after the first message goes out, and that's the part most practices under-resource: 200 replies arriving across three days, a front desk already handling phones, and nobody available at 9pm when a patient finally answers.

This is also the point where an AI agent becomes a reasonable piece of infrastructure rather than a novelty.

## Where CloseBot fits in a dental reactivation campaign

CloseBot is an agentic conversational AI that qualifies leads, follows up, and books appointments. It isn't a chatbot that walks patients through a button tree. You describe the objective — confirm interest, collect the missing details, offer a time — and the agent works the conversation toward it.

Two architectural details matter before anything else:

- **CloseBot doesn't send the first message.** It takes over once a patient replies. Outbound is still yours, sent through a workflow in your CRM (HighLevel, HubSpot, or a custom stack) that drips messages out in waves. If you were hoping for a tool that blasts 800 texts overnight, that's not this, and honestly that's fine — the drip approach is what keeps the front desk from drowning.
- **It's CRM-native, not PMS-native.** CloseBot connects to HighLevel, HubSpot, and custom CRMs, or runs standalone with a HIPAA-compliant web widget. There's no native Dentrix, Eaglesoft, or Open Dental connector, so a practice that wants to run reactivation through CloseBot is looking at exporting a list, loading it into a CRM, and working from there. For a DSO or a marketing agency with an existing CRM, that's a small lift. For a solo practice with no CRM at all, it's an extra subscription and an extra setup step, and that should factor into the decision.

On compliance, CloseBot says it maintains HIPAA compliance with signed BAAs, encrypts data, keeps an audit trail, and doesn't train AI models on your data. One thing to catch: **HIPAA is available on Growth plans only**, not on the standard business tiers. A dental practice can't run a compliant reactivation campaign on the $64 plan. That's a real constraint, not a footnote.

## What the reactivation workflow looks like in practice

CloseBot has published its own database reactivation build, and the structure is worth copying regardless of which tool you use:

1. **Tag-triggered drip.** Contacts get a tag, a workflow pulls 50 per day, holds them until business hours (9am–5pm), and spaces sends out one every two minutes.
2. **First message, then two follow-ups.** If there's no reply, the contact gets a second message one day later and a third a day after that. Then the sequence stops.
3. **Reply hands off to the agent.** The moment a message comes in, a tag fires, the workflow removes the contact, and the AI takes the conversation.
4. **Disqualification is designed in.** A custom scenario listens for signs of disinterest or irritation anywhere in the flow. If triggered, the agent tags the contact "not interested" and stops responding entirely. If a STOP comes in, the same thing happens.
5. **Booking happens conversationally.** The agent collects what it needs (timezone, a couple of qualifying questions), offers windows, and books to the calendar.

CloseBot ran that play on roughly 15,000 of its own old leads, starting at 50 contacts a day and noting it wouldn't push past a few hundred a day without iterating first. That ceiling isn't a technical limit — it's the same front-desk bandwidth problem every practice hits, stated out loud.

If you'd rather see the agent in action before exporting patient data, 👉 [start on the free plan](https://app.closebot.com/a?fpr=li87) — 100 messages a month, no card, no contract.

## What results have actually been reported

Vendor-published numbers deserve a caveat: these come from CloseBot and its agency partners, not from an independent study. Treat them as directional.

| Source | Setup | Reported outcome |
| --- | --- | --- |
| Brand Boost AI (chiropractic client) | ~6,000 untouched contacts, reactivation campaign | 10+ bookings in 24 hours, ~40 by end of week one, ~100 in two weeks, then paused because the practice couldn't handle volume |
| Brand Boost AI (90-day data) | Same client | 56% of AI opportunities engaged; 82% of closed deals came from AI-engaged leads; those leads were 2.4x more likely to close and 1.8x more likely to show up |
| Wonder System AI (roofing, not dental) | 773 "dead" leads | 16% response rate, 12 appointments, 2 closed jobs worth $53,000 plus a $25,000 estimate |

The chiropractic case is the most useful one for a dental office, and the headline isn't the 100 bookings. It's that the practice had to hit pause and hire. If your reactivation campaign suddenly works, who answers the phone?

For context on the size of the prize, one healthcare reactivation vendor puts average annual revenue per dental patient at roughly $500–$800, and multiple reactivation firms estimate that winning back a lapsed patient costs 5–25x less than acquiring a new one through ads or SEO. Those are vendor figures, but the direction is consistent across every source that publishes on the topic.

## CloseBot pricing, plan by plan

Two separate tracks: business plans for your own practice, agency plans if you're building and reselling AI agents for dental clients. Current plans page, monthly and annual options:

| Plan | What's included | Price | Billing | Get started |
| --- | --- | --- | --- | --- |
| Free | 100 AI messages/month, 1 agent, 1 user seat, 1 MB knowledge storage, unlimited account connections | $0 | Always free; overage at $0.08/message | [Start free — no card needed](https://app.closebot.com/a?fpr=li87) |
| Core (business) | Message costs included in the base price, 500 messages included at the entry tier with higher volume tiers selectable, 15+ templates, human support; add-on users $5 each, extra storage $0.10–$3.00 per MB/month | From $64/mo, or $53/mo billed annually as $640/yr | Monthly or annual (annual unlocks the larger 50+ template library) | [See the business plan options](https://app.closebot.com/a?fpr=li87) |
| Agency (Core, agency track) | Unlimited agents, re-bill all costs at $0.012/message, white-label client portal, additional users $5 each | $397/mo flat | Monthly or annual (annual billing effectively gives two months free) | [Check the agency plan](https://app.closebot.com/a?fpr=li87) |
| Growth | HIPAA compliance with BAAs, quarterly audits, 99.99% priority uptime, priority support, 50+ templates, custom volume | Custom quote | Negotiated | [Request pricing for the HIPAA plan](https://app.closebot.com/a?fpr=li87) |

Three things that catch people out:

- **HIPAA sits on Growth only.** If patient data touches the campaign, the $64 tier isn't the one you want.
- **Annual billing is genuinely cheaper.** On the business track it works out to roughly two months free, plus the bigger template library.
- **Message overages come from a wallet.** Business plans include 500 messages at the entry tier; going over is charged at a 2x rate unless you raise the monthly ceiling in advance. Agency accounts pay a flat $0.012 per message and can mark that up to clients.

## Which setup actually fits

**A single-location practice** with 800 lapsed patients and no CRM: the honest answer is that CloseBot adds a CRM subscription and setup work on top. If a front desk can handle 50 texts a week, start there. If you're already paying for HighLevel or HubSpot, the free plan plus a contacted-patient list is a cheap way to test the reply-handling layer before committing.

**A DSO or multi-location group** is the better fit. One agent can serve unlimited accounts within a niche, reactivation lists are large enough to justify the Growth tier for HIPAA, and the volume math works in your favor. 👉 [Look at what the HIPAA plan covers](https://app.closebot.com/a?fpr=li87) before you export anything.

**An agency running dental marketing** is CloseBot's core audience. The $397 agency plan exists specifically so you can charge clients for reactivation and keep the margin, with white-labeled portals and $0.012/message usage you control the markup on.

## Mistakes that quietly kill dental reactivation

- **Blasting the whole list at once.** Your team can't answer 500 replies, and slow responses convert worse than no campaign.
- **One channel only.** A lone postcard or email is a 1–3% play. Sequencing text, email, phone, and mail over four to six weeks is what gets you into double digits.
- **Guilt messaging.** "It's been two years since your cleaning" gives a patient a reason to feel bad, not a reason to book. Lead with what's new or what they're owed.
- **Quitting after one wave.** Most responses land in weeks two through four. Teams that judge the campaign on week one usually kill it just before it works.
- **No tracking.** Log every patient through contacted → reached → responded → booked → kept. Without that, you can't tell whether you have a data problem, a messaging problem, or a scheduling problem.
- **Ignoring the capacity question.** Reactivation generates inbound calls. If nobody can take them, you've built a machine that produces frustrated patients.

## FAQ

**Does CloseBot send the first text to dormant patients?**
No. Outbound comes from a workflow in your CRM. CloseBot takes over the moment a patient replies, which is deliberate — it keeps your send rate human and your front desk in control.

**Can a dental practice use CloseBot on the cheap plan?**
Only if protected health information isn't involved. HIPAA compliance and business associate agreements are on Growth plans, which are custom-quoted.

**What reactivation rate should a practice expect?**
A well-run multi-channel campaign commonly books 8–15% of contacted patients within 60 days, according to dental marketing firms publishing on the topic. Results vary widely based on how old the list is, how clean the contact data is, and how fast replies get answered.

**Is texting lapsed patients legal?**
Reactivation texts generally require prior express consent, plus a working opt-out. Compliance guidance from dental associations notes that SMS is not inherently HIPAA-compliant, so review your consent forms and any vendor agreements before launching.

**How does CloseBot handle patients who are annoyed you contacted them?**
The standard build includes an aggression-detected scenario that tags the contact, turns the AI off, and stops responding. Any STOP also removes the patient from outreach.

## Where to start

The cheapest test isn't a full campaign. Pull 50 patients from Tier 2 with verified phone numbers, write a first message that sounds like a person, and see what happens to the replies. If your team can keep up, you've learned something useful with zero software spend.

If the replies are the bottleneck — that's the specific problem CloseBot was built for. 👉 [Run your first reactivation agent on the free plan](https://app.closebot.com/a?fpr=li87) and see how it handles a conversation before you put 5,000 patient records anywhere near it.
