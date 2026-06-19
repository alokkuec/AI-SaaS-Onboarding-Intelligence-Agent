Problem:

B2B SaaS companies lose users during onboarding.
This AI-powered onboarding intelligence agent identifies at-risk users, classifies onboarding health, and automatically generates personalized engagement actions.

Architecture Diagram:
<img width="1372" height="891" alt="image" src="https://github.com/user-attachments/assets/43e1f729-8ef8-4552-a32b-ce221bda92f2" />

User Journey:
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

Product Decisions:
1. Why Rule Engine Instead of AI Scoring?
Scoring is deterministic and business-critical. Using a rule engine improves explainability, reduces hallucination risk, and keeps customer segmentation consistent.

2. Why Use AI?
AI is used for personalized engagement messaging, not for critical business decisions.
