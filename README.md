# True North Senior Care — Lead Qualification & Conversion System

## Overview

This is a fully automated lead intake, scoring, nurturing, and conversion system built in GoHighLevel.

It captures leads, qualifies them based on intent, tracks their behavior over time, and transitions high-priority leads into booked calls and pipeline opportunities — all automatically.

---

## 🎥 System Walkthrough

[![Watch the walkthrough](https://img.youtube.com/vi/Fw0Q3t7aUcs/maxresdefault.jpg)](https://youtu.be/Fw0Q3t7aUcs)

---

## System Architecture

The system is composed of five connected layers:

1. Lead Intake (Quiz Submission)
2. Lead Scoring System
3. Engagement Tracking & Scoring
4. Nurture Workflows (Hot, Warm, Cold)
5. Booking & Pipeline Automation

Each layer feeds into the next while continuously updating lead priority.

---

## Lead Intake (Quiz)

- User completes quiz
- Contact is created in CRM
- Responses are stored
- Lead is classified as:
  - Hot
  - Warm
  - Cold

This immediately determines how the system treats the lead.

---

## Lead Scoring System

Initial engagement score is assigned based on quiz results:

| Classification | Engagement Score |
|----------------|------------------|
| Hot Lead       | +15              |
| Warm Lead      | +8               |
| Cold Lead      | +3               |

This establishes a baseline for prioritization.

---

## Engagement Tracking

The system continuously updates lead priority based on behavior.

### Actions tracked:
- Email link click → +5
- Booking a call → +15

This allows leads to move up in priority based on real engagement, not just initial input.

---

## Engagement Routing

Leads are automatically escalated based on score:

| Score | Status |
|------|--------|
| 10+  | Engaged |
| 20+  | High Engagement |
| 30+  | Sales Priority |

This determines who needs immediate attention.

---

## Scored Email System

Leads receive different emails based on classification:

- Hot → urgency-driven
- Warm → informational
- Cold → low-pressure

Each email includes tracked links that feed back into the engagement system.

---

## Nurture Workflows

Three independent nurture paths:

- Hot Nurture
- Warm Nurture
- Cold Nurture

### Features:
- Timed follow-ups
- Behavior-based scoring
- Progressive engagement tracking

---

## Critical Feature: Exit Logic

At multiple points in each workflow:

- If a contact books a call
  → They are immediately removed from nurture

This prevents:
- Over-messaging
- Conflicting communication
- Poor user experience

---

## Booking & Pipeline Automation

When a contact books:

- Engagement score increases (+15)
- Contact is removed from nurture
- Confirmation email is sent
- Opportunity is created
- Contact is moved into pipeline

---

## Customer Experience

### Hot Lead
- Receives urgent messaging
- Engages quickly
- Books call → enters pipeline

### Warm Lead
- Receives educational content
- Engagement increases over time
- May escalate into high priority

### Cold Lead
- Receives low-pressure follow-ups
- Can gradually increase engagement
- May transition upward over time

---

## Admin Experience

- See lead classification instantly
- Track engagement score in real time
- Identify priority leads immediately
- Manage opportunities in pipeline
- No manual follow-up required

---

## Outcome

This system provides:

- Structured lead qualification
- Behavior-driven prioritization
- Automated follow-up
- Clean transition into sales pipeline

---

## Tech Stack

- GoHighLevel (CRM & Automation)
- Workflow Builder
- Tag-based segmentation
- Event-driven triggers

---

## Status

System is fully built and tested.

Pending:
- Insurance CTA integration
- Optional future enhancements (SMS, reporting, etc.)
