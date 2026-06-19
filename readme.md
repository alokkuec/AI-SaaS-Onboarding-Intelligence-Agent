1. # AI SaaS Onboarding Intelligence Agent

An AI-powered onboarding automation system built using n8n, Claude, Gmail, Google Sheets and Telegram.

The workflow monitors onboarding activity, segments users based on activation signals, generates personalized engagement actions, updates CRM records, and delivers weekly onboarding insights.

Built as a portfolio project demonstrating AI workflow orchestration, product-led growth automation, and customer onboarding intelligence.

2. ## Demo

🎥 Loom Demo: [Add Link]

### Sample Flow

1. User onboarding activity captured
2. Rule engine calculates activation score
3. User classified as:
   - At Risk
   - On Track
   - Power User
4. AI generates personalized engagement content
5. CRM updated
6. Notifications delivered


3. # Architecture Diagram:
<img width="1372" height="891" alt="image" src="https://github.com/user-attachments/assets/43e1f729-8ef8-4552-a32b-ce221bda92f2" />

### Components

- Google Sheets (CRM)
- Rule Engine
- Claude AI Agents
- Gmail
- Telegram
- Weekly Analytics Workflow

# User Journey:
User Activity Data
       ↓
Rule Engine
       ↓
Segmentation
       ↓
At Risk / On Track / Power User
       ↓
AI Personalization
       ↓
Email + CRM Update

4. ## Business Problem

Many SaaS companies lose users during onboarding because customers fail to complete key activation milestones.

Typical challenges:

- API keys never created
- First workflow never configured
- Team members never invited

Without proactive intervention, these users often churn before experiencing product value.

5. ## Activation Framework
| Activity          | Points |
| ----------------- | ------ |
| API Key Created   | 40     |
| Workflow Created  | 40     |
| Teammates Invited | 20     |

| Score            | Segment    |
| ---------------- | ---------- |
| <40 after 3 days | At Risk    |
| 40-79            | On Track   |
| 80-100           | Power User |

6. # Product Decisions:
1. Why Rule Engine Instead of AI Scoring?
Scoring is deterministic and business-critical. Using a rule engine improves explainability, reduces hallucination risk, and keeps customer segmentation consistent. Customer segmentation impacts business actions.
Using deterministic rules improves:

- Explainability
- Reliability
- Auditability
- Consistency

AI is reserved for communication generation rather than critical business decisions.

2. Why Use AI?
AI is used for personalized engagement messaging, not for critical business decisions.

7. # Workflow Actions:
At Risk:
- Personalized recovery email
- Telegram alert to Customer Success
- CRM update

On Track:
- Encouragement email
- CRM update

Power User:
- Congratulation email
- Expansion opportunity identification
- CRM update

8. ## Weekly Onboarding Insights Workflow

Runs every Monday.

Aggregates:

- Total users
- At Risk users
- On Track users
- Power Users
- Activation rate

Claude generates executive summary and improvement recommendations.

Summary delivered to Telegram.

9. ## Future Roadmap

- Event-driven architecture using webhooks
- SplitInBatches for large-scale processing
- Slack integration
- HubSpot CRM integration
- Churn prediction model
- Product usage analytics integration
