Project summary: day zero to now
1. Original objective

The goal was to build a lead capture and nurture system inside GHL for True North Senior Care / True North Memory Manor that would:

capture leads from multiple entry points on the website
qualify those leads based on readiness and urgency
route them into the right nurture path
track engagement over time
create sales visibility for serious leads
support booking and eventual conversion

The core public-facing pages involved were:

/take-quiz
/calculator
/guide
/booking
2. Initial build direction

At the beginning, the site and CRM strategy leaned heavily on native GHL forms, surveys, and quiz-style logic.

The early workflow structure was built around:

form submitted triggers
survey submitted triggers
tag-based lead routing
separate nurture workflows for hot, warm, and cold leads

The initial workflow system included:

quiz intake / lead scoring
calculator intake
guide intake
scored lead email generator
nurture hot
nurture warm
nurture cold
booking confirmation / notify
3. Early workflow architecture

The first version of the logic was:

user submits quiz / calc / guide
workflow adds tags
logic determines hot / warm / cold
scored lead email generator sends first-stage email
corresponding nurture tag is added
contact enters nurture workflow

There was also an early attempt to simulate range-based quiz scoring through workflow conditions using individual answer fields such as:

care timeline
care level
urgency
independence level

This worked functionally for internal routing, but it was not truly using GHL’s native dynamic score-tier result experience.

4. First major obstacle: quiz scoring vs forms

A major issue surfaced around the assessment experience.

Problem

The client wanted:

exact range-based scoring behavior
dynamic result pages
CRM storage of answers
polished front-end experience

But native GHL forms:

could calculate values
could save fields
could submit data

However, they did not provide the same dynamic results-page experience as native GHL quizzes.

Pivot

A native GHL quiz was created and configured to test:

score tiers
dynamic result messaging
custom field generation
score-tier routing

This helped prove out the scoring logic, but it created a new conflict.

New issue

The native GHL quiz experience did not match the exact visual/spec copy and page design the client wanted. The client later requested the front-end pages match the custom HTML pages exactly, which led to the next major pivot.

5. Client-requested pivot: keep exact custom HTML pages

In the demo/review stage, the client requested that the website pages match the original HTML pages exactly, including:

exact copy
exact visual structure
exact front-end layout

That meant the project had to move away from relying on native GHL forms/quizzes for the primary public user experience.

Strategic pivot

The front-end pages were rebuilt as:

pure custom HTML
embedded into GHL pages
connected to GHL using webhook-based submission

This was a major architectural shift.

6. Second major obstacle: webhook integration and CRM mapping

Once the client requested the custom HTML pages remain intact, the challenge became:

how to keep custom front-end pages
while still storing all answers in GHL CRM
while still scoring and routing contacts automatically
Solution

Inbound webhook workflows were created for:

quiz page
calculator page
guide page

The process became:

custom HTML page submits JSON payload
payload hits GHL inbound webhook
webhook workflow maps fields into contact record
tags are added
downstream workflows route / score / nurture
Pages reconfigured to use webhooks

The following pages were fully reworked to function through webhook submission:

/take-quiz
/calculator
/guide
7. Webhook build details

Each webhook workflow was configured to:

create or update contact
map key fields into custom fields
apply source tags
trigger downstream scoring/routing behavior
Quiz webhook

Mapped fields like:

first name
last name
email
phone
care timeline
care level
source
lead score
lead classification
Calculator webhook

Mapped fields like:

care_for
age_range
independence_level
level_of_care
care_timeline
care_payment_method
budget_range
lead_score
lead_classification
source
Guide webhook

Mapped fields like:

first name
last name
email
phone
care_for
care_timeline
sms_consent
source
8. Third major obstacle: live site submissions not triggering

At one point, manual console tests worked but live page submissions did not.

Root issue

The embedded live page code was pointing to outdated or mismatched webhook URLs, while console tests were hitting the current live webhook.

Fix

The embedded page code was updated to use the exact current inbound webhook URL from the workflow trigger panel. After that:

live page submission
contact creation
workflow trigger
field mapping

all began working correctly.

9. Guide PDF and download logic

Initially the guide email used a placeholder link.

What changed
client later provided the actual guide PDF
the PDF was uploaded/hosted
the real media link replaced placeholder text in emails
Tracking issue

At first, a separate trigger-link-clicked workflow was considered for guide downloads, but it turned out to be redundant because:

GHL email click tracking was enabled
the guide email link could directly add the guide-downloaded tag on click
Result

The standalone download tracker workflow was no longer necessary as the click-to-tag behavior inside the email itself handled the desired tracking outcome.

10. Nurture workflow redesign

Originally, nurture workflows were distinct and ended independently.

The client later requested a more lifecycle-driven nurture sequence.

New requested behavior

Instead of dropping leads out at the end of each workflow:

hot nurture should roll into warm
warm nurture should roll into cold
cold nurture should end with old-lead
Final nurture ladder
nurture-hot runs → removed → adds nurture-warm
nurture-warm runs → removed → adds nurture-cold
nurture-cold runs → removed → adds old-lead

This created a full lead-aging lifecycle.

11. Email system and deliverability work
Early issue

Emails were sending, but placement varied:

some hit inbox
some landed only in All Mail / Promotions-like placement
Technical review

The sending domain mail.truenorthseniorcare.com was authenticated and verified. The issue was less about DNS and more about:

sender identity consistency
reply path setup
content style
domain reputation / warmup
Changes made
business email updated to winston@truenorthseniorcare.com
reply and forwarding configured to winston@truenorthmanor.com
sender identity aligned with verified sending domain
email copy rewritten to improve inbox placement
Email copy changes

Guide, hot, warm, and cold nurture emails were rewritten to:

feel more 1:1 and conversational
reduce sales/promotional tone
preserve required links
improve deliverability and trust
12. Opportunity and pipeline logic evolution

At first, opportunities were being created too broadly, including in the guide flow.

That raised a major strategic question:

should every contact become an opportunity?
Final understanding

No. Contacts and opportunities serve different purposes.

Contact = person in CRM
Opportunity = active sales conversation / deal
Pipeline = stages for managing that deal
Revised opportunity strategy

Guide leads should not automatically become opportunities.

Instead:

hot leads should be most likely to become opportunities
strong behavioral engagement should influence who gets promoted into sales priority
Client/business logic outcome

Opportunity creation was removed from the lead scoring workflow and centralized into engagement-based sales escalation.

13. Engagement score system added

A new layer was introduced using GHL’s engagement score.

Distinction created

Two separate systems now exist:

Lead score
comes from quiz/calculator answers
measures readiness / intent
drives hot / warm / cold
Engagement score
comes from behavioral actions
measures momentum / responsiveness
drives engaged / high-engagement / sales-priority
Workflow-based score modifications added

Examples:

guide request: +2
guide download: +5
quiz submitted: +4
calculator submitted: +6
hot lead classification: +3
warm lead classification: +2
appointment booked: +15
email link click boosts in scored lead generator
14. Engagement threshold workflows

Separate threshold workflows were built because GHL does not cleanly support branching by engagement trigger inside one workflow.

Final engagement workflows
Engaged
Trigger: Contact Engagement Score > 10
Add tag: engaged
Remove: high-engagement, sales-priority
High engagement
Trigger: Contact Engagement Score > 20
Add tag: high-engagement
Remove: engaged, sales-priority
Sales priority
Trigger: Contact Engagement Score > 30
Add tag: sales-priority
Remove: engaged, high-engagement
Internal notification
If contact has hot-lead tag → create/update opportunity

This gave the system clean engagement state transitions.

15. Current system architecture

At this point, the system now works like this:

Entry points
/take-quiz
/calculator
/guide
Submission method
custom HTML
webhook to GHL
CRM field mapping
Qualification
lead score from form answers
hot / warm / cold classification
Behavior tracking
engagement score via global rules + workflow modifications
guide download tracking via email click tag
booking engagement scoring
Nurture system
hot → warm → cold → old-lead
Sales escalation
only highly engaged, hot-tagged contacts become opportunities
What’s left to be done
1. Insurance CTA / insurance connection

This is still pending client direction and is the main unresolved external dependency.

2. Pipeline system

This is the next major build item:

establish opportunity stages clearly
automate movement between stages
connect behaviors to stage changes
create a usable sales process
3. Final polish / QA

Once the pipeline system is in place:

final full-system QA
confirm no duplicate opportunities
confirm stage progression works
confirm nurture removal on booking/conversion