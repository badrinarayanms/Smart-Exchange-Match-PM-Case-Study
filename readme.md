# 🔄 Smart Exchange Match — PM Case Study
Enabling successful exchanges even when inventory is unavailable.

# Notion Link:
https://app.notion.com/p/Smart-Exchange-Match-PM-Case-Study-38a7a999c0a5816db672d29566e09404?source=copy_link

# 

**Enabling successful exchanges even when inventory is unavailable.**

> 💡 **Status:** Portfolio Case Study | **Role:** Product Manager | **Domain:** Fashion E-Commerce | **Date:** June 2026
> 

---

## 📋 Table of Contents

1. Executive Summary
2. Problem Discovery
3. User Research
4. Market Research
5. Competitive Analysis
6. User Personas
7. User Journey Mapping
8. Root Cause Analysis
9. Product Vision
10. Solution Design
11. MVP Definition
12. User Stories
13. Feature Prioritization (RICE)
14. Wireframe Planning
15. Product Requirements Document (PRD)
16. Success Metrics
17. Product Roadmap
18. Risks and Tradeoffs
19. Future Scope
20. PM Reflection


## 1. 📌 Executive Summary
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/e1b2eee4-0f85-49ea-ab1f-2d396609d26e" />

### Problem

Fashion e-commerce platforms lose significant revenue and customer goodwill when customers request a size exchange but the desired size is out of stock. The only resolution today is a full refund — which means lost revenue, higher return logistics costs, and a frustrated customer who may not return.

### Proposed Solution

**Smart Exchange Match** is an internal platform feature that detects complementary exchange requests between customers — for example, Customer A wants to exchange XL → L, and Customer B wants to exchange L → XL — and facilitates an official, brand-mediated swap between them.

This is **not** a peer-to-peer marketplace or swap community. It is a native e-commerce feature integrated within the platform's existing exchange workflow.

### Target Users

- **Primary:** Fashion shoppers who have received a wrong-fit item and want a size exchange
- **Secondary:** E-commerce Operations Managers responsible for reducing return rates and managing inventory

### Expected Business Impact

| Metric | Baseline | Target (12 months post-launch) |
| --- | --- | --- |
| Exchange Success Rate | ~40% (inventory-limited) | 65–70% |
| Return Rate (size-related) | ~28% of all returns | Reduce by 15–20% |
| Revenue Retained per Exchange | ₹0 (full refund issued) | ₹800–₹2,000 per matched pair |
| Customer Satisfaction (CSAT) | 3.2/5 post-exchange | 4.2/5 |

> 🏆 **North Star Metric:** Exchange Success Rate — the % of size-exchange requests that result in a completed exchange (vs. a refund)
> 

---

## 2. 🔍 Problem Discovery

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/512aa77b-55a2-491c-9d21-af8a5ae7c1ea" />


### Personal Observation

The idea for Smart Exchange Match originated from a real shopping experience. A customer ordered a clothing item in **XL** but upon delivery realized they needed **L**. When they initiated an exchange on the platform, the system responded: *"L is currently out of stock. We can only process a refund."*

Here's what made this frustrating: another customer had ordered the same item in **L** and needed **XL**. Both customers wanted the exact opposite size of what they had. Yet the platform had no mechanism to connect these two complementary needs. Both customers ended up with refunds — the platform lost two revenue events, and both customers left dissatisfied.

### Why This Matters

| Pain Point | Impact |
| --- | --- |
| Customer forced into refund | Lost sale, no re-engagement |
| Complementary requests undetected | Missed matching opportunity |
| Return logistics cost | ₹80–₹200 per item in reverse logistics |
| Refund processing cost | ~2–5% transaction fee loss |
| Customer churn post-bad exchange | LTV drop; acquisition cost wasted |
| Poor NPS from exchange failures | Brand perception damage |

### Problem Statement

> *"Fashion e-commerce customers frequently request size exchanges for items where the desired size is unavailable in inventory. Platforms default to refunds, resulting in revenue loss, high logistics costs, and frustrated customers — even when complementary exchange requests exist within the same customer base that could satisfy each other's needs."*
>

## 3. 🧪 User Research

### Survey Methodology

- **Method:** Online survey via Google Forms + informal user interviews
- **Sample Size:** 25 respondents
- **Recruitment:** Fashion app users aged 18–38, across Tier 1 and Tier 2 cities in India
- **Duration:** ~10-minute survey

> ⚠️ **Assumption:** Survey data is simulated for portfolio purposes. Findings are grounded in real e-commerce behavior patterns.
> 

### Respondent Profile

| Attribute | Segment | % of Respondents |
| --- | --- | --- |
| Age | 18–24 | 36% |
| Age | 25–34 | 48% |
| Age | 35–45 | 16% |
| Shopping Frequency | Weekly | 24% |
| Shopping Frequency | Monthly | 56% |
| Shopping Frequency | Occasionally | 20% |
| Platforms Used | Myntra | 80% |
| Platforms Used | Amazon Fashion | 68% |
| Platforms Used | Ajio | 52% |
| Platforms Used | Meesho | 44% |

### Survey Questions & Key Findings

**Q1: Have you ever ordered a clothing item that didn't fit correctly?**

| Response | % |
| --- | --- |
| Yes, multiple times | 72% |
| Yes, once or twice | 20% |
| No | 8% |

**Q2: What did you do when a size exchange was unavailable?**

| Action Taken | % |
| --- | --- |
| Accepted refund (didn't reorder) | 48% |
| Accepted refund and reordered different item | 28% |
| Kept the wrong-fit item | 16% |
| Contacted customer support | 8% |

**Q3: Would you wait 3–5 days for a matched exchange if it meant keeping your order?**

| Response | % |
| --- | --- |
| Yes, definitely | 56% |
| Yes, if given status updates | 28% |
| No, I'd prefer an immediate refund | 16% |

**Q4: How important is it to you that the exchange process is managed by the official brand?**

| Importance Level | % |
| --- | --- |
| Very important (trust matters a lot) | 68% |
| Somewhat important | 24% |
| Not important | 8% |

**Q5: What would most increase your confidence in a customer-matched exchange?**

| Feature | % Selecting |
| --- | --- |
| Official brand quality check before shipment | 74% |
| Real-time tracking of exchange shipment | 64% |
| Rating/trust score of the exchange partner | 52% |
| Money-back guarantee if exchange fails | 80% |

### Key Insights

> 💡 **Insight 1:** 84% of users have experienced a sizing issue — this is not a niche problem, it's a mainstream one.
> 

> 💡 **Insight 2:** 48% of customers who can't exchange simply leave without reordering. This represents pure churn.
> 

> 💡 **Insight 3:** 84% of users would wait for a matched exchange — indicating high willingness to adopt if the feature is trustworthy and well-communicated.
> 

> 💡 **Insight 4:** Trust is the #1 concern. Brand mediation and a money-back guarantee are the most critical enablers of adoption.
> 

---

## 4. 📊 Market Research

### Fashion E-Commerce Return Rates

Industry data consistently shows fashion has one of the highest return rates of any e-commerce vertical — often cited between **25–40%** of all orders. In India specifically, fashion returns hover around **20–30%** depending on the platform and category.

### Common Reasons for Returns

| Return Reason | Estimated % of Returns |
| --- | --- |
| Size doesn't fit | 38% |
| Item looks different from images | 22% |
| Quality not as expected | 18% |
| Wrong item delivered | 12% |
| Changed mind | 10% |

### Why Size Returns Are the Hardest to Solve

- **Inconsistent sizing standards** across brands and countries
- **Absence of standardized fit data** on product pages
- **Impulse purchases** where customers guess their size
- **Limited try-before-you-buy options** in online fashion

### Industry Trends

- Platforms like ASOS and Zalando in Europe have invested in **size recommendation engines** — but these are preventive, not curative. They help customers pick the right size but don't solve the problem once a wrong-size item has arrived.
- **Reverse logistics** is estimated to cost Indian fashion platforms ₹80–₹250 per return shipment.
- A **15% reduction in size-related returns** on a platform processing 1 million monthly orders could save ₹12–₹37 crore annually in logistics alone.

### Why This Is a Market-Wide Problem

Every major fashion platform faces this exact challenge. No current Indian platform has a customer-matching exchange mechanism. This is a **systemic gap** in the post-purchase experience, not an edge case.

---

## 5. 🏆 Competitive Analysis
## 3. 🧪 User Research

### Survey Methodology

- **Method:** Online survey via Google Forms + informal user interviews
- **Sample Size:** 25 respondents
- **Recruitment:** Fashion app users aged 18–38, across Tier 1 and Tier 2 cities in India
- **Duration:** ~10-minute survey

> ⚠️ **Assumption:** Survey data is simulated for portfolio purposes. Findings are grounded in real e-commerce behavior patterns.
> 

### Respondent Profile

| Attribute | Segment | % of Respondents |
| --- | --- | --- |
| Age | 18–24 | 36% |
| Age | 25–34 | 48% |
| Age | 35–45 | 16% |
| Shopping Frequency | Weekly | 24% |
| Shopping Frequency | Monthly | 56% |
| Shopping Frequency | Occasionally | 20% |
| Platforms Used | Myntra | 80% |
| Platforms Used | Amazon Fashion | 68% |
| Platforms Used | Ajio | 52% |
| Platforms Used | Meesho | 44% |

### Survey Questions & Key Findings

**Q1: Have you ever ordered a clothing item that didn't fit correctly?**

| Response | % |
| --- | --- |
| Yes, multiple times | 72% |
| Yes, once or twice | 20% |
| No | 8% |

**Q2: What did you do when a size exchange was unavailable?**

| Action Taken | % |
| --- | --- |
| Accepted refund (didn't reorder) | 48% |
| Accepted refund and reordered different item | 28% |
| Kept the wrong-fit item | 16% |
| Contacted customer support | 8% |

**Q3: Would you wait 3–5 days for a matched exchange if it meant keeping your order?**

| Response | % |
| --- | --- |
| Yes, definitely | 56% |
| Yes, if given status updates | 28% |
| No, I'd prefer an immediate refund | 16% |

**Q4: How important is it to you that the exchange process is managed by the official brand?**

| Importance Level | % |
| --- | --- |
| Very important (trust matters a lot) | 68% |
| Somewhat important | 24% |
| Not important | 8% |

**Q5: What would most increase your confidence in a customer-matched exchange?**

| Feature | % Selecting |
| --- | --- |
| Official brand quality check before shipment | 74% |
| Real-time tracking of exchange shipment | 64% |
| Rating/trust score of the exchange partner | 52% |
| Money-back guarantee if exchange fails | 80% |

### Key Insights

> 💡 **Insight 1:** 84% of users have experienced a sizing issue — this is not a niche problem, it's a mainstream one.
> 

> 💡 **Insight 2:** 48% of customers who can't exchange simply leave without reordering. This represents pure churn.
> 

> 💡 **Insight 3:** 84% of users would wait for a matched exchange — indicating high willingness to adopt if the feature is trustworthy and well-communicated.
> 

> 💡 **Insight 4:** Trust is the #1 concern. Brand mediation and a money-back guarantee are the most critical enablers of adoption.
> 

---

## 4. 📊 Market Research

### Fashion E-Commerce Return Rates

Industry data consistently shows fashion has one of the highest return rates of any e-commerce vertical — often cited between **25–40%** of all orders. In India specifically, fashion returns hover around **20–30%** depending on the platform and category.

### Common Reasons for Returns

| Return Reason | Estimated % of Returns |
| --- | --- |
| Size doesn't fit | 38% |
| Item looks different from images | 22% |
| Quality not as expected | 18% |
| Wrong item delivered | 12% |
| Changed mind | 10% |

### Why Size Returns Are the Hardest to Solve

- **Inconsistent sizing standards** across brands and countries
- **Absence of standardized fit data** on product pages
- **Impulse purchases** where customers guess their size
- **Limited try-before-you-buy options** in online fashion

### Industry Trends

- Platforms like ASOS and Zalando in Europe have invested in **size recommendation engines** — but these are preventive, not curative. They help customers pick the right size but don't solve the problem once a wrong-size item has arrived.
- **Reverse logistics** is estimated to cost Indian fashion platforms ₹80–₹250 per return shipment.
- A **15% reduction in size-related returns** on a platform processing 1 million monthly orders could save ₹12–₹37 crore annually in logistics alone.

### Why This Is a Market-Wide Problem

Every major fashion platform faces this exact challenge. No current Indian platform has a customer-matching exchange mechanism. This is a **systemic gap** in the post-purchase experience, not an edge case.

---

## 5. 🏆 Competitive Analysis

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/2db6b3b2-2dd1-4fef-91c3-8b77faf3a8ac" />

### Exchange Capability Comparison

| Feature | Myntra | Ajio | Meesho | Amazon Fashion | Smart Exchange Match |
| --- | --- | --- | --- | --- | --- |
| Standard Size Exchange | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes |
| Out-of-Stock Exchange Handling | ❌ Refund only | ❌ Refund only | ❌ Refund only | ❌ Refund only | ✅ Smart Match |
| Customer-to-Customer Matching | ❌ No | ❌ No | ❌ No | ❌ No | ✅ Yes |
| Exchange Waitlist | ❌ No | ❌ No | ❌ No | ❌ No | ✅ Yes |
| Real-time Exchange Tracking | ✅ Yes | ✅ Yes | ⚠️ Partial | ✅ Yes | ✅ Yes |
| Exchange Time Window | 30 days | 15 days | 7 days | 30 days | 30 days |
| Refund Speed | 5–7 days | 7–10 days | 7 days | 3–5 days | 3–5 days (fallback if no match found) |
| Trust/Rating for Exchanges | ❌ No | ❌ No | ❌ No | ❌ No | ✅ Yes |

### Gap Analysis

> 🎯 **The gap is universal:** Not a single major Indian fashion platform has a mechanism to detect or facilitate complementary exchange requests. Every platform defaults to refunds when inventory is unavailable.
> 

### Smart Exchange Match's Differentiation

- First-mover advantage in customer-matched exchanges in Indian fashion e-commerce
- Retains revenue that would otherwise be lost to refunds
- Improves post-purchase NPS — a key competitive battleground
- Creates a new trust layer (brand-mediated quality checks) that peer-to-peer platforms cannot offer

---

## 6. 👤 User Personas

### Persona 1 — The Fashion-Forward Shopper

| Attribute | Detail |
| --- | --- |
| **Name** | Priya Sharma |
| **Age** | 26 |
| **Location** | Bengaluru, India |
| **Occupation** | UX Designer at a startup |
| **Shopping Frequency** | 2–3 times per month |
| **Platforms Used** | Myntra, Instagram Shopping, Ajio |
| **Tech Comfort** | High |

**Goals:**

- Get the best fit without visiting a store
- Resolve post-purchase issues quickly and with minimal friction
- Trust that the brand will handle problems professionally

**Behaviors:**

- Orders multiple sizes and returns the ones that don't fit
- Reads sizing charts but still gets it wrong ~30% of the time
- Checks exchange policies before purchasing from a new brand

**Frustrations:**

- *"Why can't the app just fix this? Someone else must have the same problem but in reverse."*
- Refunds take too long and break the shopping momentum
- Feels penalized for a problem that wasn't entirely her fault

**Motivations:**

- Keeping the item she wanted, just in the right size
- A seamless, fast resolution that respects her time
- Confidence that the exchange item will be in good condition

---

### Persona 2 — The E-Commerce Operations Manager

| Attribute | Detail |
| --- | --- |
| **Name** | Arjun Mehta |
| **Age** | 34 |
| **Location** | Mumbai, India |
| **Role** | Head of Post-Purchase Operations, Fashion Platform |
| **Team Size** | 20 (CS agents, logistics coordinators, ops analysts) |
| **Reporting To** | VP of Customer Experience |

**Responsibilities:**

- Owning return rate KPIs across fashion categories
- Managing reverse logistics vendor relationships
- Reducing WISMO (Where Is My Order) support tickets
- Improving post-purchase NPS

**KPIs He's Measured On:**

- Return rate < 22%
- Exchange success rate > 60%
- Post-purchase CSAT > 4.0/5
- Reverse logistics cost per unit < ₹150

**Challenges:**

- High refund volumes spike during sale seasons
- CS agents spend disproportionate time on size exchange failures
- No tooling to identify or act on complementary exchange patterns

**Goals:**

- Reduce refund volume without increasing friction for customers
- Find scalable solutions that don't require hiring more CS agents
- Build features that turn exchange failures into retention opportunities

---

## 7. 🗺️ User Journey Mapping

### Current User Journey (Without Smart Exchange Match)

| Stage | Customer Action | Platform Response | Pain Point |
| --- | --- | --- | --- |
| 1. Delivery | Receives item, wrong size | — | Disappointment, friction starts |
| 2. Initiates Exchange | Opens app → Orders → Exchange | Checks inventory | System is slow, UX is unclear |
| 3. Size Unavailable | Sees "L not available" message | Shows refund option only | **Dead end** — no alternatives offered |
| 4. Forced Refund | Accepts refund | Initiates pickup | Feels defeated; momentum lost |
| 5. Return Pickup | Waits 1–3 days for pickup | Schedules pickup | Inconvenient, time-consuming |
| 6. Refund Processing | Waits for refund | Processes refund (5–7 days) | Long wait, frustration compounds |
| 7. Post-Refund | Considers reordering | No proactive outreach | **Churn risk** — 48% don't reorder |

**Emotional Low Points:** Stage 3 (forced into refund) and Stage 7 (no follow-up) represent the biggest drops in customer sentiment.

---

### Proposed User Journey (With Smart Exchange Match)

| Stage | Customer Action | Platform Response | Improvement |
| --- | --- | --- | --- |
| 1. Delivery | Receives item, wrong size | — | Same baseline |
| 2. Initiates Exchange | Opens app → Exchange | Checks inventory | Same process |
| 3. Size Unavailable | Sees "L not available" | **Offers Smart Exchange Match option** | ✅ Alternative offered immediately |
| 4. Opts Into Match | Taps "Find Exchange Match" | Searches exchange pool | ✅ Customer has agency |
| 5. Match Found | Receives notification | Shows match details, trust score | ✅ Transparent, trustworthy |
| 6. Reviews & Approves | Reviews match, taps Approve | Confirms match with both parties | ✅ Customer in control |
| 7. Exchange Logistics | Awaits item | Brand coordinates pickup & delivery | ✅ Brand handles logistics |
| 8. Delivery & Confirmation | Receives correct size | Sends satisfaction survey | ✅ Positive closure |
| 9. Post-Exchange | Happy with outcome | Sends loyalty reward or coupon | ✅ Retention moment created |

**Experience Improvements:** Customer goes from a dead end to an active resolution pathway. Brand turns a potential churn moment into a loyalty opportunity.

---

## 8. 🐟 Root Cause Analysis

### 5 Whys Analysis

**Problem:** Customer cannot exchange to desired size when it's out of stock.

| Why # | Question | Answer |
| --- | --- | --- |
| Why 1 | Why can't the customer exchange? | Because the desired size is out of inventory |
| Why 2 | Why is the system limited to inventory? | Because the exchange engine only checks warehouse stock |
| Why 3 | Why doesn't it check other customer-held stock? | Because no mechanism exists to pool exchange requests |
| Why 4 | Why doesn't an exchange pool exist? | Because the platform was designed for inventory-out flows, not peer exchange |
| Why 5 | Why was peer exchange never designed? | Because the problem was seen as an inventory problem, not a matching opportunity |

**Root Cause:** The exchange system is architecturally limited to a one-directional inventory check, with no mechanism to identify or leverage complementary exchange requests among existing customers.

---

### Fishbone Diagram Analysis

**Problem Statement:** Failed exchanges leading to forced refunds

| Category | Contributing Causes |
| --- | --- |
| **Process** | Exchange workflow terminates at inventory check; no fallback path; no waitlist or queue mechanism |
| **Inventory** | Size stock depleted after sales events; no real-time pooling of customer-held stock |
| **Technology** | No matching algorithm; no exchange request database; no real-time notification system for matches |
| **Customer Behavior** | Customers order without checking size charts; high impulse purchase rates; multi-size ordering habits |
| **Operations** | CS teams have no tooling to identify match candidates; refund defaults are operationally easier to process |

---

## 9. 🔭 Product Vision

### Vision Statement

> *"A world where no customer is left without their perfect fit — where every exchange request finds its match, and no sale is lost to a sizing mismatch."*
> 

### Mission Statement

> *"Smart Exchange Match enables fashion e-commerce platforms to transform failed exchange requests into successful customer outcomes by intelligently connecting complementary size-exchange needs within their existing customer base."*
> 

### Short-Term Vision (0–12 months)

Deploy a functional matching engine that detects complementary size-exchange requests for the same SKU and facilitates brand-mediated exchanges, reducing refund rates by 15% and improving post-purchase CSAT by at least 1 point.

### Long-Term Vision (12–36 months)

Build the most intelligent post-purchase experience in Indian fashion e-commerce — one that proactively suggests the right size at purchase, recovers failed exchanges through smart matching, and uses behavioral data to eliminate sizing errors at the source.

### Strategic Value

- **For customers:** Agency and resolution instead of dead ends
- **For the platform:** Revenue retention, reduced logistics costs, improved NPS
- **For the brand ecosystem:** A post-purchase moat that competitors cannot easily replicate

---

## 10. 🛠️ Solution Design

### Feature Overview

Smart Exchange Match is a native module within the platform's exchange workflow. When inventory check fails, the system activates the matching layer — searching an internal pool of pending exchange requests for the reverse complement of the current request.

**Example:**

- Customer A: Has XL, wants L → Enters exchange pool
- Customer B: Has L, wants XL → Enters exchange pool
- System detects match → Notifies both → Both approve → Brand coordinates exchange

The feature operates **entirely within the platform** — no third-party marketplace, no public listing, no community features.

### User Flow

```
Customer initiates exchange request
        ↓
System checks warehouse inventory
        ↓
[Inventory Available] → Standard exchange process (unchanged)
        ↓
[Inventory NOT Available]
        ↓
System searches Exchange Request Pool
        ↓
[No Match Found] → Customer offered: Join Waitlist OR Accept Refund
        ↓
[Match Found] → Customer notified with match details
        ↓
Both customers review and approve the match
        ↓
Platform coordinates simultaneous pickup and delivery
        ↓
Both customers receive correct size
        ↓
Exchange confirmed → Satisfaction survey sent
```

### Core Product Logic

| Logic Component | Description |
| --- | --- |
| **Match Criteria** | Same SKU, same product condition, complementary sizes |
| **Match Expiry** | Match offer expires in 48 hours if not approved |
| **Fallback** | If no match, customer joins a 7-day waitlist before refund is forced |
| **Quality Assurance** | Platform performs condition verification at pickup before completing match |
| **Cancellation** | Either party can cancel before physical pickup is initiated |

---

## 11. 📦 MVP Definition

### MVP Scope

| Feature | Included in MVP | Rationale |
| --- | --- | --- |
| Exchange request creation & pool entry | ✅ Yes | Core to the feature |
| Matching engine (same SKU, complementary sizes) | ✅ Yes | Core logic |
| Match approval workflow (both parties) | ✅ Yes | Required for consent |
| Email/SMS/Push notifications | ✅ Yes | Users must know about the match |
| Exchange tracking (basic status) | ✅ Yes | Minimum trust requirement |
| 7-day waitlist with refund fallback | ✅ Yes | Manages expectations |

### Out of Scope (MVP)

| Feature | Excluded | Why Excluded |
| --- | --- | --- |
| AI-powered size recommendations | ❌ Out | High complexity; preventive not curative; separate roadmap item |
| Cross-brand exchanges | ❌ Out | Legal, quality, and brand complexity; not a P0 problem |
| Multi-way swap chains (A→B→C) | ❌ Out | Logistical complexity exponentially increases; failure rate too high for MVP |
| Dynamic pricing for exchanges | ❌ Out | Introduces perceived unfairness; trust risk |
| Trust/reputation scoring | ❌ Out | Requires historical data; added in Phase 3 |
| In-app chat between exchange partners | ❌ Out | Privacy risk; not necessary for brand-mediated exchange |

> 💡 **Prioritization Principle:** MVP must deliver the core matching value with maximum simplicity. Every excluded feature either adds disproportionate complexity or requires behavioral data that doesn't exist yet at launch.
> 

---

## 12. 📝 User Stories

### Customer Stories

1. **As a customer** who ordered XL but needs L, **I want** to see a "Find Exchange Match" option when my size is out of stock, **so that** I don't have to settle for a refund.
2. **As a customer** waiting for an exchange match, **I want** to receive a real-time notification when a match is found, **so that** I can review and approve it quickly.
3. **As a customer** reviewing a potential exchange match, **I want** to see the match details (size, condition, exchange partner's trust score), **so that** I can make an informed decision before approving.
4. **As a customer** who has approved an exchange match, **I want** to track the status of my incoming item, **so that** I know when to expect it.
5. **As a customer** who has been waiting 7 days without a match, **I want** to be automatically offered a refund with a clear explanation, **so that** I'm not left wondering what happens next.
6. **As a customer** who completed a successful exchange, **I want** to rate my experience, **so that** the platform can improve and future users can trust the system.
7. **As a customer** who is uncomfortable with a matched exchange, **I want** to decline the match and still receive a refund, **so that** I always feel in control of the outcome.

### Operations Team Stories

1. **As an operations manager**, **I want** a dashboard showing all pending exchange matches and their statuses, **so that** I can monitor the feature's performance and intervene if needed.
2. **As a logistics coordinator**, **I want** the system to auto-generate coordinated pickup schedules for both exchange parties, **so that** I don't have to manually coordinate two separate return/delivery flows.

### Customer Support Stories

1. **As a customer support agent**, **I want** to see a full timeline of a customer's exchange match request in my CRM, **so that** I can quickly resolve disputes or questions without asking the customer to repeat themselves.
2. **As a customer support agent**, **I want** the ability to manually override a match expiry on behalf of a customer, **so that** genuine edge cases (travel, illness) can be handled with empathy.

---

## 13. 📐 Feature Prioritization (RICE Framework)

### RICE Scoring

| Feature | Reach (1–10) | Impact (1–3) | Confidence (%) | Effort (weeks) | RICE Score | Priority |
| --- | --- | --- | --- | --- | --- | --- |
| Matching Engine (core logic) | 9 | 3 | 85% | 6 | **382.5** | 🔴 P0 |
| Push/Email/SMS Notifications | 9 | 2 | 90% | 3 | **540** | 🔴 P0 |
| Exchange Approval Workflow | 8 | 3 | 85% | 4 | **510** | 🔴 P0 |
| Exchange Status Tracking | 7 | 2 | 80% | 3 | **373** | 🟡 P1 |
| Trust/Reputation Scoring | 5 | 2 | 65% | 5 | **130** | 🟡 P1 |
| Multi-Way Swap Chains | 3 | 2 | 50% | 10 | **30** | 🟢 P2 |
| AI Size Recommendations | 4 | 3 | 60% | 14 | **51.4** | 🟢 P2 |

> **RICE Formula:** (Reach × Impact × Confidence) ÷ Effort
> 

### Prioritization Rationale

- **Notifications ranked highest** because even a perfect matching engine fails if users don't know a match was found. This is the trust delivery mechanism.
- **Approval Workflow** is core to user consent and legal compliance — cannot be skipped.
- **Trust Scoring** is deferred because it requires historical data that won't exist at launch.
- **Multi-way swaps** add exponential logistical complexity with marginal coverage gain — best post-MVP.

---

## 14. 🖼️ Wireframe Planning
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/f1b188b8-e6fd-48c8-ae0b-3e39b471c439" />

### Screen 1: Exchange Request Screen

- **Goal:** Allow customer to initiate an exchange and see the Smart Match option when inventory is unavailable
- **Key UI Components:**
    - Order card (product image, name, size ordered)
    - "Exchange for Size" size selector
    - Inventory status tag: *"L is currently out of stock"*
    - **Primary CTA:** "Find Exchange Match" (filled button)
    - **Secondary CTA:** "Get Refund Instead" (text link)
    - Info banner: *"We'll search for another customer who needs your size. This is managed by [Platform] and backed by our Exchange Guarantee."*
- **Expected User Actions:** Select size → Tap "Find Exchange Match" → Confirm entry into pool

---

### Screen 2: Match Found Screen

- **Goal:** Inform the customer that a compatible exchange partner has been found
- **Key UI Components:**
    - Celebratory illustration (two packages swapping)
    - Match card showing: Item name, size being received, match partner's trust badge
    - Estimated exchange completion timeline (e.g., "Expected by Jan 12")
    - Condition note: *"Item verified by [Platform] before dispatch"*
    - **Primary CTA:** "Approve Exchange" (filled button)
    - **Secondary CTA:** "Decline — Get Refund" (text link)
    - Countdown timer: *"Offer expires in 47:32"*
- **Expected User Actions:** Review details → Tap Approve or Decline

---

### Screen 3: Approval Confirmation Screen

- **Goal:** Confirm that both parties have approved and exchange is being coordinated
- **Key UI Components:**
    - Success state animation
    - Summary: "Your exchange is confirmed. We'll coordinate pickup and delivery."
    - Pickup date/time slot selector
    - Exchange tracking ID
    - **CTA:** "Track My Exchange"
- **Expected User Actions:** Select pickup slot → View tracking

---

### Screen 4: Exchange Tracking Screen

- **Goal:** Keep the customer informed throughout the exchange logistics
- **Key UI Components:**
    - Step-by-step progress bar: Pickup Scheduled → Item Verified → In Transit → Delivered
    - Current status highlighted in blue
    - Estimated delivery date
    - Support link: *"Need help? Contact us"*
    - Exchange ID visible for CS reference
- **Expected User Actions:** Monitor status passively; contact support if needed

---

### Screen 5: Exchange History Screen

- **Goal:** Provide a record of all past exchanges (standard and matched)
- **Key UI Components:**
    - List view of past exchanges with status tags: Completed / In Progress / Declined / Refunded
    - Each card: Product image, original size, received size, date
    - Tap to expand for full timeline
    - Rating prompt for completed exchanges not yet rated
- **Expected User Actions:** Review past exchanges; submit ratings

---

## 15. 📄 Product Requirements Document (PRD)

### Objective

Build and launch Smart Exchange Match as a native module within the platform's exchange workflow to reduce refund rates by 15%, improve exchange success rates to 65%, and increase post-purchase CSAT by 1 point within 12 months of launch.

### Scope

- **In Scope:** Exchange request ingestion, matching engine, approval workflow, notifications, basic tracking, ops dashboard
- **Out of Scope:** Cross-brand exchanges, AI recommendations, multi-way chains, dynamic pricing

### Functional Requirements

| ID | Requirement | Priority |
| --- | --- | --- |
| FR-01 | System shall detect when requested exchange size is out of warehouse inventory | P0 |
| FR-02 | System shall present Smart Exchange Match option as primary CTA when inventory is unavailable | P0 |
| FR-03 | System shall maintain a real-time exchange request pool indexed by SKU and size | P0 |
| FR-04 | Matching engine shall identify complementary requests (same SKU, reverse size pair) | P0 |
| FR-05 | System shall notify both matched parties via push, email, and SMS within 5 minutes of match | P0 |
| FR-06 | Each match offer shall expire after 48 hours if not approved by both parties | P0 |
| FR-07 | Both parties must explicitly approve before logistics are initiated | P0 |
| FR-08 | System shall coordinate simultaneous pickup scheduling for both parties | P1 |
| FR-09 | Customer shall be able to track exchange status in real time | P1 |
| FR-10 | If no match found within 7 days, system shall automatically offer refund | P1 |
| FR-11 | Ops dashboard shall display all active, pending, and completed matches | P1 |
| FR-12 | CS agents shall have full exchange timeline visible in CRM | P1 |

### Non-Functional Requirements

| ID | Requirement |
| --- | --- |
| NFR-01 | Match search must return results within 3 seconds |
| NFR-02 | Notification delivery success rate ≥ 98% |
| NFR-03 | System uptime ≥ 99.5% |
| NFR-04 | Exchange pool data must be encrypted at rest and in transit |
| NFR-05 | Platform must not expose personal details of exchange partners to each other |

### Assumptions

- At launch, match volume will be low; the system must handle zero-match scenarios gracefully
- Customers are willing to wait up to 7 days for a match before requesting a refund
- The platform's logistics partner can coordinate simultaneous pickups at no incremental cost
- Items are assumed to be in acceptable condition unless flagged at pickup verification

### Constraints

- Cannot modify the existing standard exchange flow
- Must comply with Consumer Protection Act 2019 (India) regarding refund timelines
- Must not require customers to create a new account or profile

### Dependencies

- Logistics API integration for coordinated pickup scheduling
- Notification service (push, email, SMS)
- CRM plugin for CS agent visibility
- Ops dashboard (internal tooling)

---

## 16. 📈 Success Metrics
<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/1eadf852-208a-408c-9683-a867a11d8362" />

### North Star Metric

> 🌟 **Exchange Success Rate** — The percentage of size-exchange requests that result in a completed exchange (vs. a refund)
> 

**Target:** 65% within 12 months (baseline: ~40%)

### Supporting Metrics

| Metric | Definition | Why It Matters | Target |
| --- | --- | --- | --- |
| **Return Reduction %** | % decrease in size-related returns post-launch | Validates that matches are converting what would have been returns | -15% within 12 months |
| **Match Acceptance Rate** | % of presented matches approved by both parties | Signals trust and UX quality of the match presentation | ≥ 70% |
| **Match Discovery Rate** | % of exchange requests that find at least one match | Measures the pool's density and coverage | ≥ 50% within 6 months |
| **Customer Satisfaction (CSAT)** | Post-exchange satisfaction score | Validates that the experience is better than a refund | ≥ 4.2/5 |
| **Revenue Retained per Exchange** | Avg. order value saved per matched pair | Business impact of avoided refunds | ₹1,200–₹2,000/pair |
| **Exchange Completion Rate** | % of approved matches that reach delivery | Operational efficiency metric | ≥ 90% |
| **Time to Match** | Avg. time between exchange request and match found | Speed signals system quality | < 48 hours |
| **Waitlist Conversion Rate** | % of waitlisted requests that eventually match | Tests the long-tail value of the pool | ≥ 25% |

---

## 17. 🗓️ Product Roadmap

### Phase 1 — Foundation & Basic Matching (Months 1–3)

**Objective:** Prove the core matching concept works at minimum viable scale

| Feature | Description |
| --- | --- |
| Exchange Request Pool | Database of pending exchange requests indexed by SKU + size |
| Basic Matching Engine | Rule-based: same SKU, complementary sizes, within 30-day window |
| Approval Workflow | Two-party consent flow (approve/decline) |
| Push + Email Notifications | Match found, approval reminder, expiry alert |
| Refund Fallback (7-day) | Auto-trigger refund if no match found in 7 days |

**Success Criteria:** 100+ matched pairs completed, match acceptance rate ≥ 60%, CSAT for matched exchanges ≥ 4.0

---

### Phase 2 — Notifications & Tracking (Months 4–6)

**Objective:** Improve transparency and trust through better communication

| Feature | Description |
| --- | --- |
| SMS Notifications | Expand notification channel for lower-smartphone segments |
| Real-Time Exchange Tracking | Step-by-step logistics status for both parties |
| Exchange History Screen | Full history with ratings |
| CS Dashboard | Agent visibility into exchange timelines |

**Success Criteria:** Exchange completion rate ≥ 88%, CSAT ≥ 4.2, CS handle time for exchange tickets -20%

---

### Phase 3 — Trust & Quality Layer (Months 7–9)

**Objective:** Increase confidence in matched exchanges through trust signals

| Feature | Description |
| --- | --- |
| Exchange Partner Trust Score | Score based on: delivery compliance, rating received, account age |
| Item Condition Verification | Logistics partner checks item at pickup; flags if condition unacceptable |
| Exchange Guarantee Badge | Display guarantee on match screen to increase approval rates |
| Ops Analytics Dashboard | Match rate trends, waitlist analytics, revenue retained reports |

**Success Criteria:** Match acceptance rate ≥ 72%, exchange success rate ≥ 65%, return reduction ≥ 15%

---

### Phase 4 — Advanced Matching & Intelligence (Months 10–12)

**Objective:** Expand matching coverage and improve system intelligence

| Feature | Description |
| --- | --- |
| Extended Match Window | Allow matches across 45-day exchange window (up from 30) |
| Multi-Category Expansion | Extend beyond apparel to footwear |
| Match Pool Density Reporting | Internal tool for category managers to see demand-supply gaps |
| A/B Test: Waitlist Incentives | Test offering discount coupons for customers who join waitlist |

**Success Criteria:** Exchange success rate ≥ 70%, revenue retained > ₹5 crore/month platform-wide

---

## 18. ⚠️ Risks and Tradeoffs

### Risk Register

| Risk | Impact | Probability | Mitigation |
| --- | --- | --- | --- |
| **Low match volume at launch** | High — feature appears broken if matches don't form | High | Soft launch in high-SKU categories (basic tees, jeans) where pool density is highest; set waitlist expectations clearly |
| **User trust concerns** | High — customers may distrust exchanging with a stranger | Medium | Brand mediation messaging; item condition check at pickup; Exchange Guarantee badge; money-back fallback |
| **Inventory conflict** | Medium — warehouse system might not properly exclude items in exchange pool | Medium | Build real-time lock on items in active exchange match; release lock if match expires or is declined |
| **Logistics coordination failure** | High — simultaneous pickup scheduling is complex | Medium | Start with same-city matches only in MVP; expand to inter-city in Phase 2 |
| **Regulatory risk** | Medium — consumer protection laws around exchange timelines | Low | Legal review before launch; ensure 7-day refund fallback complies with CCPA/Consumer Protection Act |
| **Abuse / gaming the system** | Medium — users might game the pool for early access to out-of-stock sizes | Low | Match only within verified purchase history; require original order ID validation |

---

### Tradeoffs

**Why Multi-Way Swap Chains Were Excluded from MVP**

> Multi-way chains (A needs B's size → B needs C's size → C needs A's size) theoretically maximize match coverage. However, each additional party in the chain exponentially increases failure probability. If any one party declines or goes unresponsive, the entire chain collapses. For MVP, the tradeoff is coverage vs. reliability — we chose reliability. Multi-way chains can be introduced in Phase 4 once two-party matching is stable.
> 

**Why AI Size Recommendations Were Postponed**

> AI recommendations require training data: purchase history, body measurements, return patterns. At launch, the platform has this data but the model hasn't been built or validated. Building the AI system in parallel with the exchange matching engine would delay launch by 3–5 months. The tradeoff is depth vs. speed. We chose to launch the curative feature (matching) first, and build the preventive layer (AI sizing) on Phase 3–4 data.
> 

**Why Cross-Brand Exchanges Were Excluded**

> Cross-brand exchanges introduce brand quality standards conflicts, legal liability questions, and customer confusion about who is responsible for the exchange guarantee. The tradeoff is coverage vs. complexity. A Nike XL for a Puma XL is not a reliable exchange — sizing standards differ. We excluded this to maintain quality integrity and brand trust.
> 

---

## 19. 🚀 Future Scope

| Future Feature | User Value | Business Value | Complexity |
| --- | --- | --- | --- |
| **AI Match Recommendations** | Proactively suggests size before purchase errors happen | Reduces return rate at source; fewer exchanges needed | High — requires ML pipeline, body data |
| **Multi-Way Exchange Chains** | Expands match availability; more users get resolved | Higher match rate → more revenue retained | High — complex orchestration, failure cascade risk |
| **Personalized Size Intelligence** | Platform learns your fit across brands over time | Increases conversion rate; reduces size-guessing | Medium — data collection + user consent needed |
| **Inventory Forecasting Integration** | Alerts buyers when a size is likely to run out, prompting restock | Reduces the frequency of out-of-stock exchanges at source | Medium — requires integration with demand planning |
| **Smart Recommendation Engine** | Recommends similar items in the right size if no match found | Converts failed exchange into new purchase | Low-Medium — catalog + filter logic, no ML needed initially |

---

## 20. 🪞 PM Reflection

### What Did We Learn?

The most important insight from this case study is that **the exchange problem is fundamentally a data problem dressed up as an inventory problem**. Platforms already have all the information they need — pending exchange requests — but they're not using it to create value. The PM lesson: look at data flows before assuming a problem requires new inventory.

### Why Is This Problem Worth Solving?

Because 48% of customers who can't exchange simply leave. That's not an acceptable customer experience, and it's not acceptable business math. Every refund represents a broken relationship, not just a lost transaction. This feature turns an exit into a retention moment.

### What Assumptions Still Need Validation?

| Assumption | How to Validate |
| --- | --- |
| Users will wait up to 7 days for a match | Run a 30-day waitlist beta with opt-in customers |
| 84% willingness-to-wait holds at scale | A/B test: show Smart Match option vs. refund-only; measure opt-in rate |
| Logistics can coordinate simultaneous pickups | Pilot with 1 logistics partner in 1 city before scaling |
| Trust score improves acceptance rates | A/B test: match card with vs. without trust badge |
| Same-city matches will form at sufficient density | Analyze exchange request heatmap by city and SKU before launch |

### What Would Be the Next PM Step Before Launch?

1. **Discovery validation:** Run 15 user interviews with the proposed match flow as a clickable prototype
2. **Logistics feasibility:** Workshop with logistics partners on simultaneous pickup feasibility and cost
3. **Legal review:** Confirm refund fallback timelines comply with Consumer Protection Act 2019
4. **Engineering scoping:** 2-week sprint 0 to assess matching engine complexity and data model design
5. **Pilot city selection:** Choose 2 cities (likely Mumbai + Bengaluru) with highest fashion order density for controlled launch

---

> 📬 **Case Study prepared by:** Badri Narayan M S | Product Management Portfolio 2026
> 

> 
> 

> *This case study was developed as a portfolio project demonstrating PM thinking across problem discovery, user research, solution design, and go-to-market planning. All survey data is simulated for illustration purposes.*
>









