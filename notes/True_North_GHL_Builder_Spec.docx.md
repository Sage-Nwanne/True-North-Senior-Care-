  
**TRUE NORTH SENIOR CARE**

GHL Builder Specification Document

Landing Page \+ Lead Magnet Funnels \+ Nurture Email Sequences

March 2026  |  v1 Build Spec  |  Confidential

Platform: GoHighLevel  |  Domain: truenorthseniorcare.com  
Funnels: /quiz  •  /calculator  •  /guide  •  /book

**TABLE OF CONTENTS**

1\. Project Overview & Scope

2\. Brand Identity & Color Palette

3\. Typography & Voice Guidelines

4\. Landing Page (/) — Copy & Structure

5\. Quiz Funnel (/quiz) — Copy & Structure

6\. Calculator Funnel (/calculator) — Copy & Logic

7\. Guide Funnel (/guide) — Copy & Structure

8\. Nurture Email Sequences (Cold / Warm / Hot)

9\. Insurance CTA Integration & Compliance

10\. HTML Source Files (Reference Implementations)

11\. Technical Spec Cross-Reference (Stage 3 Doc)

12\. QA Checklist

# **1\. Project Overview & Scope**

This document contains everything needed to build the True North Senior Care landing page and lead capture funnels in GoHighLevel. It includes all copy, design specifications, page structures, email sequences, and reference HTML implementations.

**What You Are Building**

* Main landing page (/) — the primary content and CTA hub

* Quiz funnel (/quiz) — 9-question care readiness assessment with 3 results pages

* Calculator funnel (/calculator) — cost estimator with timeline-adjusted projections and transparent factor breakdown

* Guide funnel (/guide) — PDF opt-in with qualifying questions and thank-you page

* Booking page (/book) — GHL calendar or Calendly embed for consultations

**What Is NOT in Scope for This Build**

* Content creation (blog posts, social media, video) — handled by Stages 1-2

* Planning Guide PDF creation — content outline provided but PDF will be delivered separately

* Meta ads, retargeting, or paid traffic setup

* Advanced AI agent orchestration or reporting dashboards

**Reference Documents**

This document should be used alongside the Stage 3 Detailed Project Spec, which defines the CRM backend: custom fields, tags, lead scoring model, classification thresholds, workflow specifications, and duplicate handling logic. This document covers the front-end (copy, design, pages) while Stage 3 covers the back-end (workflows, scoring, automation).

# **2\. Brand Identity & Color Palette**

All pages must use this exact color palette. No substitutions. The palette was selected to convey trust, warmth, and stability — critical attributes for a senior care brand.

| \#123332 | Deep Green | \--deep-green | Primary brand color. Headlines, CTA buttons, section headers, left-border accents, nav logo. The dominant color on every page. |
| :---- | :---- | :---- | :---- |

| \#292929 | Charcoal | \--charcoal | Body text and secondary headings. Use instead of pure black for a warmer, more approachable feel. |
| :---- | :---- | :---- | :---- |

| \#728698 | Slate Blue | \--slate-blue | Secondary CTAs, sub-labels, metadata text, hint text, form labels, and supporting UI elements. |
| :---- | :---- | :---- | :---- |

| \#BDB2A7 | Warm Tan | \--warm-tan | Dividers, borders, card outlines, subtle accents. Also used for pill/tag borders and progress bar backgrounds. |
| :---- | :---- | :---- | :---- |

| \#FFFAE9 | Cream | \--cream | Feature cards, callout boxes, highlighted sections, lead magnet CTA cards, quiz result backgrounds, badges. |
| :---- | :---- | :---- | :---- |

| \#FAF8F5 | Off-White | \--off-white | Page background on all pages. Warmer than pure white. Signals a home-like (not clinical) environment. |
| :---- | :---- | :---- | :---- |

| \#FFFFFF | White | \--white | Card backgrounds, form fields, nav background (with transparency), content containers. |
| :---- | :---- | :---- | :---- |

# **3\. Typography & Voice Guidelines**

**Fonts**

**Headlines:** Playfair Display (Google Fonts, free). Weights: 400, 500, 600, 700\. Includes italic variants. Used for all page titles, section headers, card titles, and result headlines.

**Body:** DM Sans (Google Fonts, free). Weights: 300–700. Used for all body copy, buttons, form labels, nav links, meta text, and UI elements.

**Code / Monospace:** Courier New (system font). Used only for technical references in this document — not on the live site.

Google Fonts import URL for GHL:

*https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,500;0,600;0,700;1,400;1,500\&family=DM+Sans:ital,wght@0,300;0,400;0,500;0,600;0,700;1,400\&display=swap*

**Brand Voice**

**Always:** Warm, knowledgeable, honest, patient, respectful of the family’s emotional state. We speak as a trusted advisor, not a salesperson.

**Never:** Salesy, clinical, condescending, fear-mongering, or pressuring. Never use jargon without explaining it. Never make families feel guilty for not acting faster.

**The test:** Would you feel good about a friend reading this? Would you feel good about your parent reading this? If either answer is no, rewrite.

**Sign-off:** All emails sign off as “The True North Team” with “Warmly,” or “With care,” as the closing.

# **4\. Landing Page (/) — Copy & Structure**

*The landing page is the primary hub. All traffic from content, social media, and ads lands here. It follows a proven conversion sequence: empathize → differentiate → establish credibility → present tools → handle objections → close.*

## **Section 1: Navigation Bar**

Fixed top nav, transparent initially, adds white background with blur on scroll. Left: “True North Senior Care” logo text. Right: links to Assessment, Cost Calculator, Free Guide, FAQ, and a “Get Started” CTA button (deep green background, white text).

## **Section 2: Hero**

**Layout**

Two-column grid. Left column: tag \+ headline \+ sub-copy \+ 2 CTA buttons. Right column: 3 stat cards stacked vertically. Background: off-white with a subtle diagonal cream overlay on the right side.

**Tag**

**Free Senior Care Planning Resources**

**Headline**

**Nobody tells you how hard it is to watch your parents age.**

**Sub-copy**

You’re the one Googling symptoms at midnight. The one carrying a weight you didn’t expect — and can’t put down. You don’t need another article. You need a plan, real numbers, and someone in your corner.

**CTA Buttons**

* Primary (deep green): “Take the Free Assessment” → links to /quiz

* Secondary (outlined): “Estimate Care Costs” → links to /calculator

**Stat Cards (Right Column)**

* “10,000 Americans turn 65 daily” — The demand for quality senior care is growing faster than supply.

* “$3,500 – $9,000/month” — The typical range for assisted living and memory care in Georgia.

* “72 hours” — How fast most families are forced to decide when they haven’t planned ahead.

## **Section 3: Value Proposition (4 Cards)**

**Intro Text (Centered)**

*This isn’t a facility tour. It’s not a sales pitch.*

And it’s definitely not another website that makes you feel worse about a decision you haven’t made yet. True North is where families come to:

**Card 1**

**Get honest about what’s actually happening**

Not what you’re hoping is “just aging.” A clear-eyed look at the signs and what they mean for your family’s next chapter.

**Card 2**

**Understand the real cost of care**

Real numbers for Georgia families, with the funding options — including insurance strategies — nobody explains clearly.

**Card 3**

**Make a plan before a crisis makes one for you**

Most families wait until a fall or a diagnosis forces the decision. Planning ahead changes everything.

**Card 4**

**Get support that’s actually supportive**

No pressure. No upsells. Just straight talk from people who believe every family deserves better than panic and guesswork.

**Section CTA**

Italic text: “You don’t need more advice. You need a plan.”

Button: “Find Your Starting Point” → scrolls to lead magnets section

## **Section 4: How It Works (4 Steps)**

Four numbered circles connected by a horizontal line. Each step has a title and short description.

* Step 1: Choose Your Tool — Take the quiz, use the calculator, or download the guide.

* Step 2: Get Clarity — Receive personalized results based on your family’s actual situation.

* Step 3: Learn Your Options — We’ll walk you through costs, timelines, and funding strategies.

* Step 4: Take Your Next Step — Book a free call, explore insurance options, or keep learning. Your pace.

## **Section 5: Lead Magnets (3 Cards)**

**Section Header**

**Not sure where to start? Pick the one that fits.**

Every family’s situation is different. That’s why we’ve built three free tools to help you figure out yours.

**Card 1: Quiz**

**Badge:** Most Popular

**Title:** “Is It Time?” Care Readiness Assessment

**Description:** A 2-minute quiz that helps you understand where your family is on the caregiving timeline — and what to do next.

**Button:** Take the Assessment → /quiz

**Footer:** Takes about 2 minutes

**Card 2: Calculator**

**Badge:** Data-Driven

**Title:** Care Cost Calculator

**Description:** See what assisted living and memory care actually cost in Georgia — and how families typically pay for it.

**Button:** Estimate Your Costs → /calculator

**Footer:** Takes about 90 seconds

**Card 3: Guide**

**Badge:** Comprehensive

**Title:** The Senior Care Planning Guide

**Description:** A free downloadable guide covering the signs, the costs, the conversations, and the plan most families wish they had.

**Button:** Download Free Guide → /guide

**Footer:** Free PDF download

## **Section 6: Credibility (Dark Background)**

Full-width section with deep green (\#123332) background, white text.

**Header**

**Built by people who chose this work on purpose.**

**Body Copy**

True North Senior Care was founded by Winston Nwanne and Michael Ogunfowora — two operations leaders who spent years building complex systems at companies like Amazon, Google, and Microsoft. They could have stayed in tech. They chose senior care instead.

Why? Because Michael watched his mother spend 30+ years as a home health caregiver — and saw firsthand how the system fails families when they need it most. Because Winston saw an industry that runs on crisis instead of planning, and believed families deserve better.

True North is backed by a team of clinical experts, finance professionals, and senior care operators who share one belief: aging should feel guided, not abandoned.

**Logo Bar**

Display previous employer names in muted white text: Amazon | Google | Microsoft | ExxonMobil | AWS

## **Section 7: FAQ (Accordion)**

Each question expands/collapses on click. Only one open at a time.

**Q: Is True North a senior living facility?**

Not yet — and we’re upfront about that. True North is building a new kind of senior care community in the Atlanta area. Right now, our mission is to help families plan ahead with better information, honest guidance, and free tools. When our residences open, you’ll already know us as the people who helped you before they needed to sell you anything.

**Q: Who are these resources for?**

Primarily for adult children who are starting to worry about an aging parent — or adults planning ahead for their own care. Whether you’re in “just researching” mode or actively making decisions, we built these tools for you.

**Q: Is any of this a sales pitch for insurance?**

No. Our educational resources are genuinely free, no strings attached. We do believe that understanding how families pay for care — including long-term care insurance and life insurance options — is a critical part of planning. If you want to explore those options, we can connect you with a licensed specialist. But that’s always your choice, never our agenda.

**Q: How does True North make money if everything is free?**

Great question. Our long-term business is senior care residences. These free tools are how we build trust with families before we ever have a building to show you. We also work with licensed insurance partners and may receive referral compensation if you choose to explore a policy — but that never influences the guidance we give you.

**Q: I’m not in Georgia. Can I still use these tools?**

Absolutely. The quiz and guide are relevant to any family in the U.S. The cost calculator defaults to Georgia data, but the concepts apply nationally. We’re happy to help point you toward resources in your area.

## **Section 8: Final CTA (Dark Background)**

Deep green background. Centered layout.

**Headline:** Planning ahead is an act of love.

**Sub-copy:** Let us help you do it well. Start with the tool that fits your family’s situation, and we’ll guide you from there.

**Primary CTA (white button):** Take the Free Assessment → /quiz

**Secondary CTA (ghost button):** Download the Planning Guide → /guide

## **Section 9: Footer**

Dark charcoal (\#292929) background. Centered: brand name, copyright, Atlanta GA, and insurance compliance disclosure (see Section 9 of this doc for exact language).

# **5\. Quiz Funnel (/quiz) — Copy & Structure**

The quiz is built as a GHL survey. It presents one question at a time with a progress bar. After the final question (contact info), the user sees a personalized results page based on their lead score classification.

## **Quiz Landing Header**

**Tag:** Free Assessment

**Headline:** “Is It Time?” — The Care Readiness Assessment

**Sub-copy:** Most families don’t realize their parent needs more help until something goes wrong. This quick, private assessment helps you understand where your family is — and what to do next.

**Meta:** 9 questions  |  About 2 minutes  |  Completely private

## **Questions**

See the HTML reference implementation (Section 10\) for exact question text, options, and scoring values. Questions map to the custom fields defined in the Stage 3 spec. Summary:

* Q1: Who are you planning care for? (care\_for)

* Q2: How old is the person? (age\_range) — scored

* Q3: How independent are they? (independence\_level) — scored, highest weight

* Q4: Safety concerns? (safety\_concerns) — multi-select, scored additively

* Q5: How soon is care needed? (care\_timeline) — scored

* Q6: Have you discussed assisted living? (assisted\_living\_discussed)

* Q7: How familiar with AL options? (assisted\_living\_familiarity) — scored

* Q8: How are you thinking about paying? (care\_payment\_plan) — scored

* Q9: Contact information (name, email, phone, SMS consent)

## **Results Pages**

Three distinct results pages based on lead classification. Each includes a score meter visual, personalized copy, CTAs to other lead magnets, and a recommendation card.

**Result: Cold (Score under 40\) — “Planning Phase”**

**Headline:** Your Family Is in the Planning Phase

Body: Based on your answers, your loved one appears to be largely independent right now. That’s great news — and it’s also the perfect time to start understanding your options. Families who plan early make better decisions, spend less, and experience far less stress when care needs increase.

**Primary CTA:** Download the Free Planning Guide → /guide

**Secondary CTA:** Curious what care costs? Try the calculator → /calculator

**Result: Warm (Score 40–70) — “Exploration Phase”**

**Headline:** It May Be Time to Start Exploring Options

Body: Your answers suggest your loved one may benefit from additional support in the near future. You’re not in crisis — but you’re past the “just wondering” stage. The most important thing you can do right now is understand what care costs and how families typically pay for it.

**Primary CTA:** See What Care Costs in Georgia → /calculator

**Secondary CTA:** Or book a free 15-minute planning conversation → /book

**Result: Hot (Score over 70\) — “Action Recommended”**

**Headline:** Your Family May Need Support Sooner Than You Think

Body: Based on your answers, your loved one may be facing safety concerns that warrant immediate attention. You’re not alone in this — and the fact that you’re here means you’re already doing the right thing. The best next step is a brief, no-pressure conversation.

**Primary CTA:** Book a Free 15-Minute Planning Call → /book

**Secondary CTA:** Want to see cost estimates first? → /calculator

# **6\. Calculator Funnel (/calculator) — Copy & Logic**

## **Calculator Landing Header**

**Tag:** Free Calculator

**Headline:** What Does Senior Care Actually Cost in Georgia?

**Sub-copy:** Get a realistic estimate for your situation — not a national average that doesn’t mean anything. Takes about 90 seconds.

## **Calculator Questions**

* Who is care being planned for? (care\_for)

* How old is the person? (age\_range)

* How independent are they? (independence\_level)

* What level of care is needed? (level\_of\_care) — Assisted living / Memory care / Not sure

* When might care be needed? (care\_timeline) — Immediately / 12 months / 1-3 years / Just researching

* How are you thinking about paying? (care\_payment\_plan)

* Estimated monthly budget range (budget\_range)

* Contact information (name, email, phone, SMS consent)

## **Cost Calculation Logic**

**Step 1: Base Rates (2026 Georgia)**

Assisted Living: $3,500 – $6,500/month

Memory Care: $5,000 – $9,000/month

Not Sure: $3,500 – $9,000/month (full range)

**Step 2: Acuity Adjustment (from independence level)**

* Cannot safely live alone: \+15% to both low and high

* Needs help with daily activities: \+8%

* Needs occasional help: No adjustment

* Fully independent: \-5%

**Step 3: Timeline Projection (\~9% annual growth)**

* Immediately: No adjustment (2026 rates)

* Within 12 months: 1 year forward (+9%)

* Within 1–3 years: 2 years forward (+19%, midpoint)

* Just researching (3+ years): 4 years forward (+41%)

Formula: adjusted\_cost \= acuity\_adjusted\_cost × (1.09 ^ years\_out)

## **Results Page Structure**

The results page has four sections:

* 1\. Cost Display (dark green card): Shows the projected monthly range, annual equivalent, projected year label, and inflation note.

* 2\. Factor Breakdown (collapsible accordion): Maps each user response to its impact on the estimate with color-coded badges, dollar amounts where applicable, and plain-English explanations. See the HTML reference for exact rendering.

* 3\. How Families Typically Pay: Five funding options (savings, LTC insurance, life insurance with LTC riders, Medicaid, VA benefits) with highlight boxes on the insurance items.

* 4\. Insurance CTA: Cream-background card with headline “Want to understand your insurance options?” and CTA button “Learn About Your Insurance Options.”

# **7\. Guide Funnel (/guide) — Copy & Structure**

## **Page Layout**

Two-column layout on desktop. Left column: value proposition and table of contents. Right column: sticky opt-in form card. Collapses to single column on mobile with form below content.

## **Left Column Content**

**Tag:** Free Download

**Headline:** The Assisted Living Planning Guide

***Subtitle:*** Everything your family needs to know — before you need to know it.

**Intro Copy**

Nobody hands you a roadmap when your parents start aging. One day everything’s fine, and the next you’re fielding questions you never expected: Is Mom safe alone? What does memory care even mean? How does anyone afford this?

We built this guide because every family deserves answers before they’re in crisis mode.

**Inside the Guide (6 items with icons)**

* The 7 signs it may be time for more help (and what each one really means)

* A clear breakdown of care types: independent living, assisted living, memory care, and home health

* What senior care costs in Georgia — real numbers, not vague national averages

* 5 ways families pay for care (including options most people don’t know about)

* How to have “the conversation” with a parent who doesn’t want to talk about it

* A simple planning timeline so you know what to do and when

**Promise Box**

**Free. No email sequence tricks. No 47-email sales funnels. Just a resource we wish every family had.**

## **Right Column: Opt-In Form**

**Form Header:** Get your free copy

Fields: First Name, Last Name, Email (required), Phone (optional), Who are you planning care for? (dropdown, required), How soon might care be needed? (dropdown, required), SMS consent checkbox.

**Button:** Download the Free Guide

**Trust bar below form:** Private & secure  |  Instant delivery  |  No spam

## **Thank-You Page**

**Headline:** Your guide is on its way.

Sub-copy: Check your inbox in the next few minutes. If you don’t see it, check your spam folder.

PDF download card with direct download button.

**Cross-promotion CTA:** Take the Care Readiness Assessment → /quiz

**Alt links:** Estimate care costs → /calculator  |  Book a free planning call → /book

Email expectations note: “Over the next few weeks, we’ll send you a handful of helpful resources about senior care planning. Nothing salesy — just straight talk. You can unsubscribe anytime.”

# **8\. Nurture Email Sequences**

All emails use the True North brand voice. Merge fields shown in \[brackets\]. Load these into GHL workflows per the Stage 3 spec.

## **8A. Cold Nurture (5 Emails)**

Audience: Early-stage, low urgency. Goal: Build trust, move toward quiz or calculator.

**Email — Day 0**

**Subject:** Your planning guide is here, \[First Name\]

Thank you for downloading The Assisted Living Planning Guide. The fact that you’re thinking about this now — before a crisis forces the conversation — puts you ahead of most families.

Inside the guide, you’ll find a clear breakdown of care types, costs, funding options, and a planning timeline. It’s designed to be the resource we wish every family had before they needed it.

Take your time with it. And if anything raises questions, simply reply to this email. We read every one.

Warmly,

The True North Team

**Email — Day 3**

**Subject:** The \#1 mistake families make with aging parents

The most common mistake we see? Waiting.

Not waiting because families don’t care — waiting because they convince themselves the situation isn’t “that bad yet.” A parent compensates well. They insist they’re fine. And everyone agrees to believe it because the alternative is a conversation nobody wants to have.

Then something happens. A fall. A forgotten stove. A call from a neighbor. And suddenly, a family that had months or years to plan is making the most important decision of their parent’s life in 72 hours.

We’re not saying this to scare you. We’re saying it because we’ve watched it happen hundreds of times — and because the families who do even a little planning have a dramatically better experience.

If you haven’t had a chance to look at the planning guide, now’s a good time.

Talk soon,

The True North Team

**Email — Day 7**

**Subject:** How families actually pay for assisted living

If there’s one topic that catches families off guard, it’s cost. Not because the numbers are shocking — but because nobody explains the options clearly.

Here’s the quick version: In Georgia, assisted living typically runs $3,500–$6,500/month. Memory care is $5,000–$9,000/month. Those numbers are real, and they add up fast.

But here’s what most families don’t realize: there are more ways to fund care than you think. Personal savings, long-term care insurance, life insurance policies with LTC riders, Medicaid planning, and VA benefits each play a role depending on your family’s situation.

We built a free calculator that shows you where your family stands. It takes 90 seconds.

\[Button: See What Care Costs for Your Family\]

And if you want to explore whether an LTC or life insurance policy might help protect your family’s savings, we can connect you with a licensed specialist who will answer your questions with zero pressure. Just reply to this email.

Warmly,

The True North Team

**Email — Day 14**

**Subject:** 5 signs your parent may need more help than you think

Sometimes the signs are obvious. Sometimes they’re not. Here are five things families often notice in hindsight:

1\. The house looks different. Clutter accumulates. Dishes pile up. The yard gets neglected.

2\. They repeat themselves. Not the occasional forgotten word — but the same story three times in one visit.

3\. They’re losing weight. Cooking becomes a chore. Meals get skipped.

4\. They’ve had a near-miss. A stumble. A missed medication. A stove left on.

5\. You feel it in your gut. You can’t always articulate it, but something feels different. Trust that instinct.

If you recognized your family in any of those, our quick assessment can help you understand where things stand.

\[Button: Take the 2-Minute Assessment\]

With care,

The True North Team

**Email — Day 21**

**Subject:** When you’re not sure what to do

We want to be honest about something: most families reaching out to us don’t have a clear picture of what they need. They just know something has to change.

Maybe your parent is showing signs but insists they’re fine. Maybe your siblings disagree about what to do. Maybe you’ve been the one handling everything and you’re running out of bandwidth.

That’s all okay. You don’t need a plan to start a conversation.

If it would help to talk this through with someone who’s seen every version of this situation — no agenda, no pitch — we’re here.

\[Button: Book a Free 15-Minute Planning Conversation\]

Or, if you’re not quite there yet, our readiness assessment and cost calculator are always available.

Warmly,

The True North Team

## **8B. Warm Nurture (5 Emails)**

Audience: Moderate urgency, evaluating options. Goal: Move toward calculator or consultation.

**Email — Day 0**

**Subject:** What your answers tell us, \[First Name\]

Thank you for completing the care readiness assessment. Based on your answers, it looks like your family may be approaching a transition point — not a crisis, but a stage where the right information and a little planning could make a real difference.

Over the next couple of weeks, we’re going to send you a handful of resources specifically relevant to families in your situation. Cost data, decision frameworks, and guidance on the conversations that matter most.

Nothing generic. Nothing salesy. Just straight talk.

Warmly,

The True North Team

**Email — Day 2**

**Subject:** How do you know when “researching” becomes “it’s time”?

There’s a moment in every family’s caregiving journey where the question shifts from “Should we be thinking about this?” to “We need to figure this out.”

That shift usually happens when daily routines are getting harder, safety concerns are more frequent, or you’re spending more time managing your parent’s life than living your own.

If you’re somewhere in that territory, get concrete about costs. Knowing the real numbers turns an overwhelming situation into a manageable one.

\[Button: See What Care Costs in Georgia\]

Warmly,

The True North Team

**Email — Day 5**

**Subject:** What assisted living actually costs in Georgia

Let’s talk numbers. In the greater Atlanta area, assisted living typically costs $3,500–$6,500 per month. Memory care runs $5,000–$9,000 per month. Over a year, that’s $42,000 to $108,000.

Those numbers catch most families off guard — not because they’re unaffordable, but because nobody explains the options early enough.

Families who plan for funding before they need care have dramatically more options — and dramatically less stress. Long-term care insurance, life insurance with LTC benefits, Medicaid planning, and VA benefits are all tools that work best when you have time on your side.

If you haven’t explored whether an insurance policy might help protect your family’s savings, it’s worth a conversation. We can connect you with a licensed specialist with zero obligation.

\[Button: Learn About Insurance Options\]  \[Alt: Use the Cost Calculator\]

Warmly,

The True North Team

**Email — Day 9**

**Subject:** The conversation most families put off too long

If you haven’t talked to your parent about care yet, you’re not alone. It is the hardest conversation in family caregiving.

A few things that help: Don’t lead with logistics — lead with love. Don’t have the conversation once — have it in small pieces, over time. And don’t try to get agreement — try to get understanding.

Something like: “Mom, I’m not trying to take anything away from you. I just want to make sure we have a plan so that if things change, nobody’s scrambling.”

Our planning guide covers this in detail.

\[Button: Download the Free Guide\]

With care,

The True North Team

**Email — Day 14**

**Subject:** Would it help to talk this through with someone?

Over the last two weeks, we’ve shared what we know about costs, timing, conversations, and planning. We hope it’s been helpful.

If you’re at a point where it would be useful to talk through your specific situation with someone who’s guided families through this before — we’d welcome the conversation.

It’s 15 minutes. It’s free. And it’s not a sales call. It’s a planning conversation.

\[Button: Book a Free 15-Minute Planning Conversation\]

Warmly,

The True North Team

## **8C. Hot Lead Follow-Up (3 Emails \+ SMS)**

Audience: High urgency, ready to act. Goal: Book consultation. Tone is helpful and prompt.

**Email — Day 0 (Immediate)**

**Subject:** Your next best step, \[First Name\]

Thank you for completing the assessment. Based on your answers, it sounds like your family may be navigating a time-sensitive situation — and we want to make sure you have the support you need.

The most helpful thing we can offer right now is a brief conversation. In 15 minutes, we can help you understand your options, clarify costs, and think through a realistic timeline.

No pressure. No pitch. Just someone in your corner.

\[Button: Book Your Free Planning Call\]

If you prefer to start with the numbers, our cost calculator is here: \[link\]

Warmly,

The True North Team

**Email — Day 1**

**Subject:** The 3 questions families in your situation always ask

When families reach the stage you’re at, three questions come up almost every time:

1\. What’s this actually going to cost? In Georgia, depending on the level of care, you’re looking at $3,500–$9,000/month. We can help you narrow that range.

2\. How do we pay for it? Most families use a combination of savings, insurance, and benefits. There are more options than you’d expect.

3\. How do I bring this up with my parent? This is the hardest part. And it’s something we can actually help with.

\[Button: Book a Free 15-Minute Call\]

The True North Team

**Email — Day 3**

**Subject:** We’re here when you’re ready

We know this is a lot. And we know that even when the need feels urgent, it’s hard to take the next step when you’re not sure what that step looks like.

There’s no wrong way to move forward. You can book a quick call, reply to this email with questions, use the cost calculator, or download the planning guide.

Whatever feels right for where you are, that’s the right next step.

\[Button: Book a Call\]  \[Alt: Explore Resources\]

We’re not going anywhere. When you’re ready, we’re here.

Warmly,

The True North Team

**SMS Template (Hot Leads Only)**

Only send if sms\_consent \= true. Send 10 minutes after first email. Do not send before 8am or after 9pm local time.

| SMS Text Hi \[First Name\], thanks for completing the assessment. Based on your answers, it may help to speak with someone. Here’s a link to book a free 15-min call: \[link\] — True North Senior Care. Reply STOP to unsubscribe. |
| :---- |

# **9\. Insurance CTA Integration & Compliance**

## **Where Insurance CTAs Appear**

* Calculator results page — in the “How Families Pay” section and the dedicated insurance CTA card

* Cold nurture Email \#3 (Day 7\) — soft CTA within the “how families pay” content

* Warm nurture Email \#3 (Day 5\) — direct CTA with urgency framing

* Planning Guide PDF — in the chapter on paying for care (out of scope for this build but noted for content team)

## **Handoff Flow**

Family clicks insurance CTA → Short form (name, email, phone, “what prompted your interest?”) → CRM tags lead as insurance\_interest → Internal notification to licensed partner → Partner contacts family within 24 hours → True North receives referral compensation on closed policies.

## **Required Compliance Disclosure**

| Footer Disclosure (Required on All Pages with Insurance CTAs) True North Senior Care provides educational resources about senior care planning. We are not a licensed insurance agency. When families express interest in exploring long-term care insurance or life insurance options, we connect them with licensed, independent insurance professionals. True North may receive referral compensation if a policy is purchased. This does not affect the cost of any policy or the guidance we provide. All insurance recommendations are made by the licensed agent based on your specific needs and circumstances. |
| :---- |

# **10\. HTML Source Files (Reference Implementations)**

Four complete, fully functional HTML files are included as separate attachments alongside this document. Each is a self-contained page that can be opened in any browser to preview the exact design, layout, interactions, and copy. Your GHL build should replicate these as closely as possible.

**File 1: True\_North\_Landing\_Page.html**

The main landing page (/). Includes: fixed nav with scroll effect, two-column hero with stat cards, four value proposition cards, four-step process, three lead magnet cards, credibility section (dark bg), FAQ accordion with 5 questions, final CTA (dark bg), and footer with compliance disclosure. Fully responsive.

**File 2: True\_North\_Quiz\_Page.html**

The quiz funnel (/quiz). Includes: progress bar, 9-question assessment (one question at a time), single-select and multi-select question types, contact form with TCPA consent, and three segmented results pages (cold/warm/hot) with score meters, personalized copy, and cross-promotion CTAs.

**File 3: True\_North\_Calculator\_V2.html**

The calculator funnel (/calculator). Includes: 7-question form with pill selectors, contact capture, results display with projected cost range, collapsible factor breakdown showing exactly how each response influenced the estimate (with color-coded impact badges and explanations), “How Families Pay” section, and insurance CTA card. Cost logic includes acuity adjustment and \~9% annual growth projection based on timeline.

**File 4: True\_North\_Guide\_Page.html**

The guide funnel (/guide). Includes: two-column layout with sticky form, table of contents with icons, opt-in form with qualifying questions, and thank-you page with PDF download card and cross-promotion to quiz.

| Important Note for Builder These HTML files are pixel-perfect reference implementations. They include all CSS styling, JavaScript interactions, and responsive breakpoints. Open each file in Chrome and use it as your visual blueprint while building in GHL. The fonts (Playfair Display \+ DM Sans), colors, spacing, animations, and interaction patterns should be matched as closely as GHL allows. Where GHL limitations prevent exact replication, prioritize: (1) copy accuracy, (2) color accuracy, (3) layout structure, (4) interaction patterns. |
| :---- |

# **11\. Technical Spec Cross-Reference**

This document covers front-end only (copy, design, pages). The Stage 3 Detailed Project Spec (provided separately) covers the back-end. Here is how they connect:

**Stage 3 Custom fields (Section G):** Form fields in quiz, calculator, and guide map directly to these CRM fields.

**Stage 3 CRM tags (Section F):** Applied by workflows on form submission. Source tags, classification tags, nurture tags.

**Stage 3 Lead scoring (Section H):** Quiz and calculator answers feed the scoring model. Point values are in the Stage 3 doc.

**Stage 3 Classification (Section I):** Hot (\>70), Warm (40-70), Cold (\<40). Determines which results page is shown and which nurture sequence fires.

**Stage 3 Workflows (Section J):** Each funnel has an intake workflow. Hot/warm/cold routes to different nurture sequences.

**Stage 3 Nurture sequences (Section K):** Email copy is in this document (Section 8). Timing and automation logic is in Stage 3\.

**Stage 3 Booking (Section L):** Hot lead CTAs point to /book. Pre-call questionnaire auto-sent on booking.

**Stage 3 Duplicate handling (Section M):** Match on email. Create-or-update on all intake workflows.

# **12\. QA Checklist**

Complete this checklist before going live. Every item must pass.

1. All pages render correctly on desktop (1440px+), tablet (768px), and mobile (375px)

2. Brand colors match exactly: \#123332, \#292929, \#728698, \#BDB2A7, \#FFFAE9, \#FAF8F5

3. Fonts load correctly: Playfair Display for headlines, DM Sans for body

4. Landing page: all internal links work (nav, CTAs, FAQ accordion, footer)

5. Quiz: all 9 questions display correctly with proper field mapping

6. Quiz: results page displays correctly for each classification (test with different score combinations)

7. Quiz: contact form requires all fields, SMS consent checkbox works

8. Calculator: all 7 questions \+ contact form work correctly

9. Calculator: cost calculation matches the logic in Section 6 (test all timeline options)

10. Calculator: factor breakdown accordion opens/closes and displays correct impacts

11. Calculator: insurance CTA and compliance disclosure are present

12. Guide: two-column layout works on desktop, collapses on mobile

13. Guide: form submits correctly, thank-you page displays with PDF download

14. Guide: qualifying dropdowns (care\_for, timeline) are required fields

15. All forms: TCPA SMS consent checkbox is present wherever phone is collected

16. All forms: data flows to GHL CRM with correct custom field mapping

17. Lead scoring workflow: calculates correctly and classifies (spot-check 5 test leads)

18. Email sequences: all 13 emails loaded, merge fields work, timing is correct

19. Hot lead workflow: immediate email \+ SMS (if consented) \+ internal notification

20. Insurance CTA: form works, tags lead as insurance\_interest, notifies partner

21. Compliance disclosure appears in footer of landing page, calculator results, and relevant emails

22. Booking page (/book): calendar loads, confirmation triggers tag \+ notification

23. Duplicate handling: re-submission with same email updates (not duplicates) the contact

24. All pages: no broken images, no console errors, no layout shifts on load