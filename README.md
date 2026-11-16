<p align="center">
  <img src="banner.png" alt="WhatsApp Pay: feature requirements, process maps and wireframes" width="100%">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Type-Course%20case%20study-8FA8FF?style=flat-square" alt="Course case study">
  <img src="https://img.shields.io/badge/Skill-Requirements-FFC79C?style=flat-square" alt="Requirements">
  <img src="https://img.shields.io/badge/Skill-Process%20mapping-B9C6FF?style=flat-square" alt="Process mapping">
  <img src="https://img.shields.io/badge/Skill-Wireframes-FFC79C?style=flat-square" alt="Wireframes">
</p>

> **Course project** (Simplilearn CBAP programme, Course-end Project 3). This is a case study. It is not a real client project and is not connected to Meta or WhatsApp.

## The question
How can people send money **inside a chat**, without switching to a separate banking app?

## At a glance

| | |
|---|---|
| **Stakeholders** | 17 (9 internal, 8 external) |
| **Features** | 10 |
| **Requirements** | 6 business, 12 functional, 8 non-functional |
| **Risks** | 10, each with likelihood, impact and a mitigation |
| **Diagrams** | As-Is flow, 2 future-state flows, context and use case diagram, SWOT, 2 wireframe sets |
| **Roll-out plan** | Brazil pilot, then India, then global |

## Business objectives

| Ref | Objective | Success measure | Timeline |
|---|---|---|---|
| BO-01 | 1 million active WhatsApp Pay users | Monthly active payment users of 1M or more | Within 3 months of launch |
| BO-02 | 30% of the WhatsApp user base using Pay | 600M+ users actively transacting | Within 12 months of launch |
| BO-03 | Phased rollout: Brazil, India, then global | India launch with a 400M user target | 6 to 18 months after launch |

## From As-Is to To-Be
**Today:** the user opens a separate banking or payment app, logs in again, types the recipient's account details by hand, and the confirmation arrives outside the conversation.

**With WhatsApp Pay (Method 1, payment from a chat):**

```mermaid
flowchart LR
    A["Open the chat"] --> B["Tap the payment icon"]
    B --> C{"Card linked?"}
    C -- No --> D["One-time card linking"]
    D --> E["Enter amount and note"]
    C -- Yes --> E
    E --> F["Enter 5-digit PIN"]
    F --> G["System processes payment"]
    G --> H["Reference number shown"]
    H --> I["Both users see the payment in the chat"]
```

## Diagrams

<table>
  <tr>
    <td width="50%"><b>As-Is: how people pay today</b><br><img src="01_AsIs_Current_State.png" alt="As-Is current state"></td>
    <td width="50%"><b>To-Be, Method 1: pay from a chat</b><br><img src="02_Future_State_Method1_Chat_Payment.png" alt="Future state, chat payment"></td>
  </tr>
  <tr>
    <td><b>To-Be, Method 2: pay by QR code</b><br><img src="03_Future_State_Method2_QR_Payment.png" alt="Future state, QR payment"></td>
    <td><b>Context and use case diagram</b><br><img src="04_Context_UseCase_Diagram.png" alt="Context and use case diagram"></td>
  </tr>
  <tr>
    <td><b>SWOT analysis</b><br><img src="05_SWOT_Analysis.png" alt="SWOT analysis"></td>
    <td><b>Wireframe: send money</b><br><img src="06_Wireframe_Send_Money.png" alt="Wireframe, send money"></td>
  </tr>
  <tr>
    <td colspan="2"><b>Wireframe: payments home and history</b><br><img src="07_Wireframe_Payments_Home_History.png" alt="Wireframe, payments home and history"></td>
  </tr>
</table>

## Risks (3 of 10)

| Ref | Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|---|
| R-01 | Regulatory rejection or delay (for example, India's regulator first blocked the launch) | High | Very high | Engage regulators 6+ months before launch |
| R-02 | Data breach or security compromise | Medium | Very high | PCI-DSS Level 1, end-to-end encryption, penetration testing |
| R-03 | Low adoption, because users do not want to link a bank card | Medium | High | Step-by-step onboarding, first-payment cashback, repeated privacy assurance |

## Requirements (examples)

| Ref | Requirement |
|---|---|
| BR-01 | Reach at least 1 million active users within 3 months of launch |
| BR-03 | The Brazil pilot must meet its KPIs before the India launch is approved |
| FR-01 | The user can link a debit or credit card, validated with the issuing bank using tokenisation |
| FR-02 | From any chat: tap the payment icon, choose the amount, add a note, enter the PIN, confirm |
| NFR-01 | Payment processing completes within 3 seconds under normal load |
| NFR-02 | 99.99% uptime (less than 52 minutes of downtime a year) |
| NFR-03 | End-to-end encryption for all transaction data, PCI-DSS Level 1 compliance |

The full list is in the Word document.

## Transition plan

| Phase | State | Timeline |
|---|---|---|
| 1 | Current state: separate banking and UPI apps, or cash | Before launch |
| 2 | Pilot in Brazil, monitor adoption, payment success and fraud | 0 to 6 months after launch |
| 3 | Available in all major markets, 30%+ of users | 12 to 24 months after launch |

## What this shows
Stakeholder analysis, risk identification, SWOT, transition state analysis, AS-IS and TO-BE process mapping, context and use case modelling, requirements writing (business, functional, non-functional) and wireframing.

## Files
- [`Amosh_Roopsingh_WhatsAppPay_CBAP.docx`](Amosh_Roopsingh_WhatsAppPay_CBAP.docx): the full business analysis document
- The `.png` files: all diagrams

---
<sub>Amosh Roopsingh, Birmingham, UK</sub>
