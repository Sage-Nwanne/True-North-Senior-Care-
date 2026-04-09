# True North Senior Care — Project Summary

## Objective

Build a lead capture, qualification, and nurture system inside GoHighLevel for **True North Senior Care / True North Memory Manor** that:

- Captures leads across multiple website entry points
- Qualifies those leads based on readiness and urgency
- Routes them into the right nurture path automatically
- Tracks engagement over time
- Creates sales visibility for serious leads
- Supports booking and eventual conversion

---

## Public-Facing Pages

| Page | Purpose |
|---|---|
| `/take-quiz` | Care readiness assessment with scoring |
| `/calculator` | Georgia-specific care cost estimator |
| `/guide` | Free planning guide opt-in |
| `/booking` | Consultation scheduling |

---

## How the System Works

### Submission Flow

```
Custom HTML page
  → JavaScript calculates score + classification
  → Webhook POST sends answers, score, and classification to GHL
  → Inbound webhook workflow creates or updates contact
  → Tags applied (source, quiz-submitted, etc.)
  → Lead Scoring workflow reads lead_score
  → Adds hot / warm / cold tag
  → Email workflow sends first response
  → Nurture workflow continues lifecycle
```

### Three Separate Webhook Workflows

| Page | Fields Captured |
|---|---|
| `/take-quiz` | `first_name`, `last_name`, `email`, `phone`, `care_timeline`, `care_level`, `lead_score`, `lead_classification`, `source` |
| `/calculator` | `care_for`, `age_range`, `independence_level`, `level_of_care`, `care_timeline`, `care_payment_plan`, `budget_range`, `lead_score`, `lead_classification`, `source` |
| `/guide` | `first_name`, `last_name`, `email`, `phone`, `care_for`, `care_timeline`, `sms_consent`, `source` |

---

## Lead Scoring

Scores are calculated client-side in JavaScript at form submission and sent to GHL via webhook.

| Classification | Score Range |
|---|---|
| Cold | 0 – 39 |
| Warm | 40 – 70 |
| Hot | 71 – 100 |

Inputs that drive score: care timeline, independence level, age range, care type.

---

## Nurture Lifecycle

Leads age through a full ladder rather than dropping out at the end of each workflow:

```
nurture-hot → nurture-warm → nurture-cold → old-lead
```

Each stage removes the prior tag and adds the next, creating a clean lifecycle state at all times.

---

## Engagement Scoring

Separate from lead score. Measures behavioral momentum.

| Action | Points |
|---|---|
| Guide requested | +2 |
| Guide downloaded (email click) | +5 |
| Quiz submitted | +4 |
| Calculator submitted | +6 |
| Hot lead classification | +3 |
| Warm lead classification | +2 |
| Appointment booked | +15 |

### Engagement Tier Workflows

| Tag | Trigger |
|---|---|
| `engaged` | Engagement score > 10 |
| `high-engagement` | Engagement score > 20 |
| `sales-priority` | Engagement score > 30 |

When a contact reaches `sales-priority` **and** holds the `hot-lead` tag, an opportunity is created automatically.

---

## Contacts vs. Opportunities vs. Pipeline

- **Contact** — a person in the CRM database
- **Opportunity** — a lead actively being worked toward conversion
- **Pipeline** — the set of stages that shows where a deal is in the sales process

Guide downloads and cold leads do not automatically become opportunities. Only highly engaged, hot-tagged contacts are promoted into the sales pipeline.

---

## Email & Deliverability

- Sending domain: `mail.truenorthseniorcare.com` (authenticated)
- Sender identity: `winston@truenorthseniorcare.com`
- Reply/forward: `winston@truenorthmanor.com`
- Email copy rewritten across all sequences to be conversational and 1:1 in tone to improve inbox placement

---

## What's Still Pending

| Item | Status |
|---|---|
| Insurance CTA / referral connection | Awaiting client direction |
| Pipeline stage automation | Next major build item |
| Full system QA | After pipeline is complete |

---

*True North Senior Care · Atlanta, Georgia*
