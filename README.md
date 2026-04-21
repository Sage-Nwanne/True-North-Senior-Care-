# True North Senior Care — Lead Qualification & Conversion System

## System Walkthrough Video

Watch the full walkthrough here: [System Walkthrough](https://youtu.be/Fw0Q3t7aUcs)

## Overview

This system is a fully automated lead intake, scoring, nurturing, and conversion engine built within GoHighLevel.

It is designed to:
- Identify high-intent leads immediately
- Continuously update lead priority based on behavior
- Route contacts into the correct follow-up experience
- Transition qualified leads into booked calls and pipeline opportunities
- Remove friction from both the customer journey and internal operations

This is not a collection of workflows — it is a **connected system** where each component contributes to a unified outcome: converting the right leads at the right time.

---

# System Architecture

The system is composed of five core layers:

1. Lead Intake (Quiz Submission)
2. Lead Scoring System
3. Engagement Tracking & Scoring
4. Nurture Workflows (Hot, Warm, Cold)
5. Booking & Pipeline Automation

Each layer feeds into the next while also dynamically updating previous states.

---

# 1. Lead Intake (Quiz Submission)

## Purpose
Capture user intent and classify leads immediately upon entry.

## Process
- User completes a quiz
- A contact is created in the CRM
- Data fields (quiz score, situation, timeline, etc.) are stored
- A lead classification is assigned based on quiz score:
  - Hot Lead
  - Warm Lead
  - Cold Lead

## Outcome
Every contact enters the system with:
- A defined starting intent level
- A corresponding classification tag
- A baseline engagement score (assigned in the next layer)

---

# 2. Lead Scoring System

## Purpose
Assign an initial engagement score based on intent.

## Logic

| Quiz Score | Classification | Engagement Score |
|------------|----------------|------------------|
| > 70       | Hot Lead       | +15              |
| 40–70      | Warm Lead      | +8               |
| < 39       | Cold Lead      | +3               |

## Additional Actions
- Tags are applied based on classification
- Previous conflicting tags are removed to maintain clean state

## Outcome
Every contact now has:
- A clear priority level
- A measurable engagement score
- A clean tag structure for routing

---

# 3. Engagement Tracking & Behavioral Scoring

## Purpose
Continuously update lead priority based on user behavior.

## Tracked Actions

### Email Engagement
- If a contact clicks a link in an email:
  → +5 engagement score

### Booking Action
- If a contact books a call:
  → +15 engagement score

## Implementation
- Link clicks are tracked via tags (e.g., `clicked-email-link`)
- Conditional checks inside workflows apply score increases
- These checks exist across all nurture paths

## Outcome
Lead scoring is no longer static — it evolves based on real behavior.

---

# 4. Engagement Routing System

## Purpose
Dynamically escalate leads based on engagement score.

## Thresholds

| Engagement Score | Routing Outcome |
|-----------------|----------------|
| 10+             | Engaged        |
| 20+             | High Engagement|
| 30+             | Sales Priority |

## Actions
- Tags are applied when thresholds are reached
- Higher-priority tags override lower ones
- These tags can trigger additional workflows or notifications

## Outcome
The system identifies:
- Who is warming up
- Who is highly interested
- Who is ready for sales interaction

---

# 5. Scored Email Generator

## Purpose
Deliver personalized communication based on lead classification.

## Logic
- If Hot Lead → send Hot Lead email
- If Warm Lead → send Warm Lead email
- If Cold Lead → send Cold Lead email

## Features
- Emails contain tracked links (for engagement scoring)
- Emails are aligned with urgency level and messaging tone
- Each email acts as both communication and a scoring trigger

## Outcome
Every contact receives messaging that matches their intent level while feeding behavioral data back into the system.

---

# 6. Nurture Workflows

There are three independent nurture paths:

- Nurture Hot
- Nurture Warm
- Nurture Cold

Each is triggered by its respective tag.

---

## Core Design Principles

All nurture workflows include:

### 1. Conditional Exit Logic
At multiple points in each workflow:

- If contact has "booked call" tag
  → Immediately removed from workflow

This ensures:
- No unnecessary follow-up after conversion
- No conflicting communication

---

### 2. Timed Follow-Ups
Each workflow includes delays:

- Hot → Short delays (faster follow-up)
- Warm → Moderate delays
- Cold → Longer delays

---

### 3. Engagement-Based Scoring
At each step:

- If email link clicked
  → +5 engagement score

---

### 4. Progressive Tagging
If engagement occurs:

- Hot → reinforced with nurture-hot
- Warm → may escalate
- Cold → may transition upward

---

### 5. Lifecycle Transitions
At the end of workflows:

- Tags are updated
- Contacts may move between nurture levels
- System maintains a clean state for re-entry or escalation

---

## Outcome

Each nurture workflow:
- Adapts to behavior
- Prevents redundant communication
- Keeps contacts moving toward conversion or reclassification

---

# 7. Booking & Pipeline Automation

## Trigger
- Appointment booked (calendar event)

## Actions

1. Add "booked call" tag
2. Increase engagement score (+15)
3. Remove conflicting tags if necessary
4. Send confirmation email
5. Create or update opportunity
6. Move opportunity into pipeline
7. Trigger internal notification

---

## Outcome

Once a lead books:
- They are removed from nurture workflows
- They are transitioned into the sales pipeline
- The system shifts from marketing → sales mode

---

# Complete Customer Experience

## Entry
- User completes quiz
- Receives immediate personalized email

---

## Path 1: High Intent (Hot Lead)
- Receives urgent messaging
- Clicks link → engagement score increases
- Books quickly → enters pipeline immediately

---

## Path 2: Medium Intent (Warm Lead)
- Receives educational messaging
- May click links → increases score
- May escalate into high engagement
- Eventually books or continues nurture

---

## Path 3: Low Intent (Cold Lead)
- Receives low-pressure messaging
- Longer delays between touches
- Engagement can gradually increase score
- May transition into warm or hot over time

---

## Dynamic Behavior

At any point:
- Clicking links increases score
- Booking removes them from nurture
- Tags update automatically
- Messaging adapts based on behavior

---

# Complete Admin Experience

## Lead Visibility
- Every contact has:
  - Classification (hot/warm/cold)
  - Engagement score
  - Behavior history

---

## Prioritization
- Admin can immediately identify:
  - Sales Priority leads
  - High engagement leads
  - Passive leads

---

## Pipeline Automation
- Opportunities are created automatically
- Contacts move into correct pipeline stages
- No manual data entry required

---

## Notifications
- Internal alerts for high-intent actions
- Immediate visibility into booked calls

---

## System Reliability
- No duplicate messaging
- No nurture overlap after booking
- Clean tag management
- Continuous scoring updates

---

# Final Outcome

This system transforms lead management into:

- A structured qualification process
- A behavior-driven prioritization engine
- A fully automated nurture system
- A seamless transition into sales execution

It ensures that:
- High-intent leads are acted on immediately
- Medium-intent leads are developed properly
- Low-intent leads are not ignored but handled efficiently

---

# Summary

This is a complete, production-ready CRM system that:

- Captures intent
- Measures engagement
- Adapts to behavior
- Automates follow-up
- Enables sales execution

All without manual intervention.
