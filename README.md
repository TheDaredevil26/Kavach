# Kavach 🛡️
### *कवच — Your Shield Against Income Loss*
### AI-Powered Parametric Income Insurance for India's Q-Commerce Gig Workers

> **Guidewire DEVTrails 2026 — University Hackathon Submission**
> Phase 1: Ideation & Foundation

---

## Table of Contents

1. [The Problem](#1-the-problem)
2. [Our Persona](#2-our-persona)
3. [Solution Overview](#3-solution-overview)
4. [Why Kavach is Different](#4-why-kavach-is-different)
5. [Parametric Triggers](#5-parametric-triggers)
6. [Weekly Premium Model](#6-weekly-premium-model)
7. [Predictive Pre-Alert System](#7-predictive-pre-alert-system)
8. [Fraud Detection Architecture](#8-fraud-detection-architecture)
9. [AI/ML Integration Plan](#9-aiml-integration-plan)
10. [Application Flow & Personas](#10-application-flow--personas)
11. [Platform Strategy](#11-platform-strategy)
12. [Tech Stack](#12-tech-stack)
13. [Database Justification](#13-database-justification)
14. [System Architecture](#14-system-architecture)
15. [Development Plan](#15-development-plan)
16. [Business Viability](#16-business-viability)

---

## 1. The Problem

India's Q-Commerce sector (Zepto, Blinkit, Swiggy Instamart) has grown at **80% YoY** since 2022, creating an estimated **1.2 million active delivery riders** as of 2025. These workers operate in a uniquely fragile financial environment:

- Average Q-Commerce rider earns approximately **₹750–800/day** (14–16 deliveries combining normal and peak hour rates)
- Weekly earnings cycle: **₹4,500–4,800/week** (~₹2.5–3.2 LPA annually)
- External disruptions reduce monthly earnings by **20–30%** on average
- **Zero income protection** exists for weather, infrastructure, or social disruptions

### Earnings Structure (Ground Reality)

| Hour Type | Deliveries | Per Order | Daily Contribution |
|---|---|---|---|
| Normal hours (~8 deliveries) | 8 | ₹40–60 (avg ₹50) | ₹400 |
| Peak hours (~6 deliveries) | 6 | ₹70–100 (avg ₹85) | ₹510 |
| **Total daily** | **~14** | — | **~₹750–800** |
| Weekly (6 days) | ~84 | — | **~₹4,500–4,800** |
| Annually | — | — | **~₹2.5–3.2 LPA** |

> Source: Industry reports on gig worker earnings in India (2024–25). The 3.2 LPA figure represents top-end earners in high-density metro zones; 2.5 LPA is more representative of average full-time Q-Commerce riders.

### The Disruption Reality (India-Specific Data)

| Disruption Type | Frequency (Annual) | Avg. Income Loss Per Event |
|---|---|---|
| Heavy rainfall (>30mm/hr) | 18–25 days/year in metro cities | ₹350–600/day |
| Extreme heat (>43°C feels-like) | 30–45 days/year (April–June) | ₹250–450/day |
| Hazardous AQI (>300) | 20–40 days/year (Oct–Jan, North India) | ₹200–400/day |
| Local curfews / Section 144 | 4–8 events/year per city | ₹500–800/day |
| Dark store / platform outage | 6–12 events/year per dark store | ₹150–350/event |

> **Combined impact**: A typical Zepto/Blinkit rider in a metro city loses approximately **₹7,000–12,000/year** to uncontrollable external disruptions with zero recourse.

### What Currently Exists

- **Health insurance**: Covers medical expenses. Does NOT cover income loss.
- **Vehicle insurance**: Covers repair costs. Does NOT cover income loss.
- **Platform incentives**: Sporadic bonuses. Not guaranteed, not disruption-specific.
- **Government schemes (PM-SYM, e-Shram)**: Pension-focused, not income replacement.

**There is no product today that covers a Q-Commerce rider's lost wages during an external disruption. Kavach builds exactly that.**

---

## 2. Our Persona

### Chosen Segment: Quick Commerce (Q-Commerce) Delivery Riders
**Platforms covered:** Zepto, Blinkit, Swiggy Instamart, Dunzo Daily

### Why Q-Commerce Specifically?

Q-Commerce riders have a fundamentally different risk profile compared to food delivery (Zomato/Swiggy) or e-commerce (Amazon/Flipkart):

| Factor | Food Delivery | E-Commerce | **Q-Commerce** |
|---|---|---|---|
| Delivery radius | 5–8 km | 10–30 km | **2–4 km (dark store radius)** |
| Deliveries/day | 8–12 | 4–6 | **12–16** |
| Single point of failure | Distributed | Distributed | **Dark store health** |
| Weather sensitivity | High | Medium | **Very High** |
| Shift pattern | Evening-heavy | Daytime | **Multi-shift, 6am–midnight** |
| Income per disruption hour | ₹40–60 | ₹30–50 | **₹70–100 (peak)** |

The critical insight: **Q-Commerce riders are tethered to a single dark store**. If that dark store goes down — power outage, flooding, sudden closure — every rider assigned to it loses income simultaneously. No other delivery segment has this single infrastructure dependency.

### Worker Profile: Meet Rajan

> **Rajan, 27** — Blinkit delivery partner, Koramangala, Bengaluru
> Works 2 shifts daily (8am–1pm, 5pm–10pm), 6 days/week
> Normal hours: 8 deliveries × ₹50 = ₹400
> Peak hours: 6 deliveries × ₹85 = ₹510
> **Daily earnings: ~₹770 | Weekly: ~₹4,620 | Annual: ~₹2.75 LPA**
> Lost income last monsoon season (June–September): ~**₹9,500**
> Current safety net: **None**

---

## 3. Solution Overview

**Kavach** is an AI-enabled parametric income insurance platform built exclusively for Q-Commerce delivery riders. It provides:

- **Automatic, zero-touch income protection** against 5 categories of external disruptions
- **Three transparent weekly plan tiers** with AI-calibrated dynamic coverage
- **Instant payouts** directly to the worker's bank account — no claims to file, no paperwork
- **Predictive pre-alerts** notifying active policyholders 36–48 hours before a predicted disruption
- **Dark store network triggers** — a Q-Commerce-exclusive coverage mechanism unique to Kavach

### What Kavach Covers

✅ Income lost due to extreme weather (rain, heat, AQI)
✅ Income lost due to social disruptions (curfews, local strikes, zone closures)
✅ Income lost due to dark store / platform outage during peak hours

### What Kavach Explicitly Does NOT Cover

❌ Health, medical, or accident expenses
❌ Vehicle repair or maintenance costs
❌ Fuel or operational expenses
❌ Income lost due to worker's own choice to not work
❌ Pre-existing disruptions (72-hour waiting period on all new policies)

---

## 4. Why Kavach is Different

### Differentiator 1: Dark Store Network Triggers (Q-Commerce Exclusive)

Every other insurance product treats weather as the only trigger. Kavach introduces **dark store health monitoring** — a trigger that literally cannot exist for any other delivery segment.

**How it works:**
- Each Zepto/Blinkit dark store has a simulated health score derived from order volume
- If order volume from a dark store drops >75% for 90+ consecutive minutes → trigger fires
- All riders registered to that dark store are automatically compensated for lost peak hours
- Captures outages, power failures, flooding of the store itself, and staff strikes

This trigger is **architecturally impossible to replicate for food delivery or e-commerce** — those segments don't operate on a dark store model. It is Kavach's most defensible product feature.

### Differentiator 2: Predictive Pre-Alert (Proactive, Not Reactive)

Every other parametric platform waits for a disruption, then pays. Kavach's AI monitors 36–48 hour weather forecasts and **warns active policyholders before the event hits.**

> *"Heavy rainfall forecast in your zone tomorrow 4pm–9pm. You're covered. Estimated protection: ₹280–380."*

This transforms Kavach from an insurance product into a **financial safety partner**. Pre-alerts are exclusively for existing active policyholders — new signups during a prediction window receive a 72-hour waiting period with the predicted event excluded, preventing adverse selection.

### Differentiator 3: Three Transparent Tiers, AI-Calibrated Coverage

Workers choose a plan that matches their income and risk appetite. The AI dynamically calibrates the **coverage ceiling and trigger-day limits** within each tier based on zone risk — keeping the pool financially sustainable without changing the price the worker pays.

---

## 5. Parametric Triggers

Kavach monitors 5 parametric triggers. All thresholds are objective, verifiable, and API-driven. No worker needs to file a claim — the system initiates and processes everything automatically.

### Trigger 1: Heavy Rainfall

| Parameter | Value |
|---|---|
| Data source | OpenWeatherMap API (free tier) |
| Geographic scope | Pin-code level (rider's registered zone) |
| Threshold | Rainfall intensity > 30mm/hour for 45+ consecutive minutes |
| Peak hour multiplier | 1.5× payout if trigger fires between 12–2pm or 6–10pm |
| Payout logic | (Daily income baseline ÷ 8 hrs) × hours trigger active × plan coverage % |
| Typical payout | ₹130–380 per event |

**Why 30mm/hour:** IMD classifies rainfall above 15mm/hr as "heavy." 30mm/hr is the empirically observed threshold at which Q-Commerce platforms begin experiencing order volume drops of 40%+ in Bengaluru and Mumbai (2023 urban mobility data).

---

### Trigger 2: Extreme Heat Index

| Parameter | Value |
|---|---|
| Data source | OpenWeatherMap API — feels-like temperature endpoint |
| Geographic scope | City-level (heat is uniform within a metro) |
| Threshold | Feels-like temperature > 45°C for 3+ consecutive hours |
| Active months | April, May, June (North & Central India primarily) |
| Payout logic | Half-day compensation if 3–5 hours; full-day if 5+ hours |
| Typical payout | ₹180–450 per event |

**Why feels-like temperature:** At 42°C actual with 50% humidity, the feels-like temperature reaches 55°C+. The heat index — combining temperature and humidity — determines whether outdoor work is physiologically possible, not the thermometer reading alone.

---

### Trigger 3: Severe Air Quality Index (AQI)

| Parameter | Value |
|---|---|
| Data source | OpenAQ API (free, open-source) / AQICN API |
| Geographic scope | City zone level (nearest AQI monitoring station to rider's pin code) |
| Threshold | AQI > 300 (Hazardous category, CPCB scale) for 4+ consecutive hours |
| Active period | October–January (North India smog season primarily) |
| Payout logic | Full-day compensation per day AQI remains in hazardous range |
| Typical payout | ₹250–550 per event |

**Supporting data:** Delhi AQI exceeded 300 on **42 days** in winter 2024–25 (CPCB data). At AQI >300, outdoor delivery worker productivity drops 60–80% due to government advisories and platform-level restrictions.

---

### Trigger 4: Hyperlocal Curfew / Section 144

| Parameter | Value |
|---|---|
| Data source | Simulated government alert API (mock for hackathon) |
| Geographic scope | Zone/ward level — only riders in the declared area covered |
| Threshold | Government-declared Section 144 or curfew in rider's registered pin code |
| Verification | Cross-referenced with platform order volume drop (dual verification) |
| Payout logic | Full working-hour compensation for declared curfew duration |
| Typical payout | ₹350–800 per event |

**Design note:** Dual verification — official curfew declaration AND corresponding platform order drop — prevents fraudulent claims based on spoofed news alerts.

---

### Trigger 5: Dark Store / Platform Outage *(Kavach Exclusive)*

| Parameter | Value |
|---|---|
| Data source | Simulated Zepto/Blinkit platform health API (mock) |
| Geographic scope | Per dark store — only riders registered to affected store |
| Threshold | Order volume drops >75% for 90+ consecutive minutes during operational hours |
| Peak hour condition | Trigger only eligible during 10am–10pm (active delivery window) |
| Fraud protection | Requires matching GPS activity drop from registered riders in zone |
| Payout logic | (Hourly income baseline) × hours of outage × plan coverage % |
| Typical payout | ₹150–350 per event |

**Why this matters:** Individual dark stores in Indian metros experienced an average of 8–12 significant outage events per year lasting 90+ minutes (2024 Q-Commerce reliability analysis). At ₹70–100/hour average peak earnings, this represents ₹1,500–4,000 in annual uncompensated losses per rider purely from infrastructure failures.

### Trigger Summary Table

| # | Trigger | API Source | Threshold | Max Weekly Fires |
|---|---|---|---|---|
| 1 | Heavy Rainfall | OpenWeatherMap | >30mm/hr, 45+ min | 3 days |
| 2 | Extreme Heat | OpenWeatherMap | Feels-like >45°C, 3+ hrs | 2 days |
| 3 | Hazardous AQI | OpenAQ / AQICN | AQI >300, 4+ hrs | 4 days |
| 4 | Curfew / Section 144 | Mock govt. API | Active in rider's pin code | 2 days |
| 5 | Dark Store Outage | Mock platform API | Vol. drop >75%, 90+ min | 3 events |

### Compound Trigger Logic

```
If (Rain > threshold) AND (Peak hours active):
  → Payout = base payout × 1.5

If (AQI > threshold) AND (Temp > 42°C):
  → Dual environmental trigger: payout = base payout × 1.3

If (Curfew active) AND (Dark store down):
  → Maximum of the two triggers applies (no stacking)
  → Prevents over-payout while remaining fair to the worker
```

---

## 6. Weekly Premium Model

### Three Transparent Plan Tiers

Workers choose their plan at onboarding. Plans can be changed once per billing cycle (on Sunday before renewal).

| Plan | Weekly Premium | Coverage | Max Weekly Payout | Trigger Days/Week |
|---|---|---|---|---|
| **Basic** | ₹49/week | 50% of income lost | ₹1,200 | 3 days |
| **Standard** | ₹89/week | 75% of income lost | ₹2,200 | 4 days |
| **Pro** | ₹129/week | 100% of income lost | ₹3,200 | 5 days |

### Affordability Check (Against 3.2 LPA Benchmark)

| Plan | Weekly Premium | % of Weekly Earnings (₹4,620) | Verdict |
|---|---|---|---|
| Basic ₹49 | ₹49 | **1.06%** | ✅ Well within 3% benchmark |
| Standard ₹89 | ₹89 | **1.93%** | ✅ Within 3% benchmark |
| Pro ₹129 | ₹129 | **2.79%** | ✅ Just under 3% benchmark |

All three tiers sit comfortably within the Swiss Re Institute micro-insurance affordability benchmark of 3% of income — making Kavach genuinely accessible to full-time Q-Commerce riders at every level.

### Dynamic Coverage Calibration (AI Layer)

Within each tier, the AI Risk Engine **calibrates the worker's effective coverage ceiling** each week based on their zone risk score. The worker's price never changes — the system ensures pool sustainability by adjusting max payouts for high-risk zones.

```
Risk Score = (0.40 × Zone Risk Index)
           + (0.35 × Weather Forecast Score)
           + (0.25 × Worker Profile Score)

Zone Risk Index:
  → Historical disruption frequency in pin code (last 24 months)
  → Zone Order Density Score (dark store activity level)
  → Flood/waterlogging zone classification (NDMA data)

Weather Forecast Score:
  → 7-day forecast probability of threshold-exceeding events
  → Seasonal adjustment (monsoon / AQI season)

Worker Profile Score:
  → Claim history relative to zone peers
  → Policy tenure (loyalty reward after 8 continuous weeks)
  → Average active shift hours per week
```

**Calibration output (example — Standard tier, ₹89/week):**

| Zone Risk Band | Effective Payout Ceiling | Trigger Days | Loyalty Bonus (8+ weeks) |
|---|---|---|---|
| Low (0.0–0.35) | ₹2,200 (full) | 4 days | +1 trigger day free |
| Medium (0.36–0.65) | ₹1,900 | 4 days | ₹10 discount next week |
| High (0.66–1.0) | ₹1,500 | 3 days | ₹5 discount next week |

The ceiling reduction for high-risk zones is **transparent and disclosed** — workers see it in their dashboard at the start of each week. It is not a hidden penalty.

### Payout Calculation Formula

```
Step 1 — Income Baseline:
  Daily Baseline = Worker's average daily earnings over last 28 days
  (from mock platform data; default ₹750/day if unavailable)

Step 2 — Hours Lost:
  Hours Lost = Duration trigger was continuously active (API timestamp)
  Capped at 8 hours per trigger event

Step 3 — Gross Income Lost:
  Gross Lost = (Daily Baseline ÷ 8) × Hours Lost

Step 4 — Plan Payout:
  Basic:    Gross Lost × 50%
  Standard: Gross Lost × 75%
  Pro:      Gross Lost × 100%
  → Capped at plan's effective weekly ceiling

Step 5 — Compound Multiplier (if applicable):
  Final Payout = Step 4 × compound trigger multiplier (1.3× or 1.5×)
```

### Worked Example: Rajan (Standard Plan, Medium Risk Zone)

> **Daily baseline:** ₹770 | **Plan:** Standard ₹89/week | **Ceiling:** ₹1,900
>
> **Monday:** Heavy rain trigger fires 6pm–9pm (3 hours, peak window)
> Gross lost = (₹770 ÷ 8) × 3 = ₹289
> Payout = ₹289 × 75% × 1.5 (peak multiplier) = **₹325**
>
> **Thursday:** AQI hits 315 from 10am–5pm (7 hours)
> Gross lost = (₹770 ÷ 8) × 7 = ₹674
> Payout = ₹674 × 75% = **₹506**
>
> **Week total payout: ₹831 | Premium paid: ₹89 | Net benefit: ₹742**

### Weekly Renewal Cycle

```
Monday 12:00am  → New weekly policy activates automatically
Friday 6:00pm   → Pre-alert push (if disruption forecast for coming week)
                   "Coverage renews Sunday. Your ceiling next week: ₹1,900"
Sunday 11:00pm  → ₹89 deducted via UPI auto-debit
                   New risk score calculated; new week begins
```

---

## 7. Predictive Pre-Alert System

### How It Works

Every day at 6:00am, Kavach's Prediction Engine pulls **7-day weather forecasts** and **historical disruption patterns** for all active pin codes. When it detects >65% probability of a threshold-exceeding event in the next 36–48 hours, it sends a pre-alert to all active policyholders in that zone.

```
Prediction Pipeline:
  1. Pull 7-day forecast from OpenWeatherMap (hourly granularity)
  2. Calculate P(trigger threshold exceeded) per trigger type per zone
  3. Cross-reference with historical patterns for pin code and month
  4. If P(trigger) > 65% in next 36–48 hrs → generate pre-alert
  5. Personalize with worker's estimated payout range (by plan tier)
  6. Deliver via mobile push notification + SMS fallback
```

### Pre-Alert Message (Worker's Phone)

```
🌧️ Kavach Alert — Rajan

Heavy rain forecast in Koramangala tomorrow
4pm – 9pm (78% probability)

You're covered under Standard Plan.
Estimated protection: ₹280–380

Stay safe. Your earnings are protected.

[View My Coverage]  [View Forecast]
```

### Adverse Selection Prevention

| Scenario | Rule |
|---|---|
| New signup during 48hr pre-alert window | 72-hour waiting period; predicted event excluded from first coverage window |
| Worker upgrades plan after pre-alert sent | Upgrade valid for all future events; specific predicted trigger excluded |
| Claim for pre-alert event within waiting period | Automatic fraud flag; full hold for manual review |

---

## 8. Fraud Detection Architecture

Since all claims are automatic, fraud detection operates across three layers **before any payout is processed**.

### Layer 1: Pre-Payout Gates (Runs in <2 seconds)

```
Gate 1 — Policy Age Check
  Policy must be active 72+ hours before any claim is eligible
  → Prevents last-minute signups ahead of known storm events

Gate 2 — Location Continuity Score
  Worker's last 3 recorded app-open GPS locations must be within
  or adjacent to the triggered pin code
  Worker appearing in zone ONLY after trigger fired → GPS spoof flag

Gate 3 — Claim Deduplication
  One payout per trigger event per worker per day
  Compound triggers → highest applicable payout only, not additive
```

### Layer 2: ML Anomaly Scoring

Produces a **Fraud Risk Score (0–1)** for each pending payout:

```
Fraud Risk Score = weighted model:

  Activity Pattern Score      (weight: 0.35)
  → Normal: app-active before disruption, offline during
  → Suspicious: offline all day, active only when trigger fires

  Claim Frequency Score       (weight: 0.30)
  → Worker claiming 3× more than zone median = anomaly flag

  Earnings Baseline Drift     (weight: 0.20)
  → Sudden earnings spike 2 weeks before monsoon = flag

  Device & Identity Score     (weight: 0.15)
  → Multiple accounts on one device ID → immediate block
  → SIM/phone change within 7 days of first claim → flag
```

| Fraud Score | Action |
|---|---|
| 0.0 – 0.49 | Auto-approve → instant payout |
| 0.50 – 0.74 | Pay 50% immediately; hold 50% pending 24hr review |
| 0.75 – 1.00 | Full hold → admin review queue → worker notified |

### Layer 3: Post-Payout Audit (Background)

```
Zone Correlation Check
  35%+ of zone workers claiming same event → expected, no flag
  <5% claiming for an event affecting the whole zone → investigate

Platform Activity Reconciliation (Mock)
  Claimed "lost hours" cross-checked against platform delivery logs
  Completed deliveries during trigger window → fraud flag

Historical Pattern Audit
  6+ weeks no claims → sudden weekly max payout claims → flag
```

---

## 9. AI/ML Integration Plan

### Model 1: Dynamic Risk Engine

- **Type:** Weighted scoring model — explainable by design (critical for insurance)
- **Inputs:** Zone disruption history, 7-day forecast probability, worker profile, seasonal index
- **Output:** Risk Score (0–1) → maps to coverage calibration within chosen plan tier
- **Stack:** Python (scikit-learn), served via FastAPI microservice
- **Refresh:** Every Sunday night for the upcoming week

### Model 2: Fraud Anomaly Detector

- **Type:** Isolation Forest (unsupervised anomaly detection) for V1
- **Inputs:** GPS continuity, claim frequency, baseline drift, device fingerprint
- **Output:** Fraud Risk Score (0–1)
- **Stack:** Python (scikit-learn), served via FastAPI
- **Latency target:** <500ms per request (runs synchronously before every payout)

### Model 3: Disruption Prediction Engine

- **Type:** Time-series threshold probability model
- **Inputs:** OpenWeatherMap 7-day hourly forecast, historical trigger frequency by pin code and month
- **Output:** P(trigger fires in next 48 hours) per zone per trigger type
- **Stack:** Python (pandas + probability functions)
- **Run schedule:** Daily at 6:00am

### Node.js ↔ Python Integration

```
Node.js Risk Engine    → POST /ml/risk-score    → Python FastAPI
Node.js Fraud Engine   → POST /ml/fraud-score   → Python FastAPI
Node.js Prediction Job → POST /ml/predict-zone  → Python FastAPI

All ML services return JSON within 500ms
Node.js owns all business logic; Python owns only model inference
```

---

## 10. Application Flow & Personas

### Flow A: Worker Onboarding

```
1. Download Kavach app (Android primary)
2. Mobile number → OTP verification
3. Select platform (Zepto / Blinkit / Swiggy Instamart)
4. Enter registered pin code + dark store zone
5. Platform ID verification (mock API call)
6. Enter bank account details (for direct transfer payouts)
7. AI Risk Engine calculates zone risk score
8. Worker selects plan: Basic ₹49 / Standard ₹89 / Pro ₹129
9. Coverage ceiling displayed: "Your weekly protection: up to ₹2,200"
10. UPI auto-debit setup → policy activates (72-hour waiting period)
```

### Flow B: Disruption → Auto Payout (Zero Touch)

```
1. Trigger Engine (cron, every 10 mins) polls all 5 data sources
2. Threshold exceeded in Zone X → trigger event created
3. System fetches all active policyholders in Zone X
4. For each worker:
   a. Layer 1 fraud gates run (<2 seconds)
   b. ML fraud score calculated (<500ms)
   c. Payout amount calculated per plan tier
5. If approved → Razorpay test API → bank transfer initiated
6. Worker push notification:
   "Heavy rain trigger fired. ₹325 transferred to your bank.
    Ref: GS-2026-03-21-4821"
7. Entire process under 90 seconds. Worker does nothing.
```

### Flow C: Pre-Alert Notification

```
1. Daily prediction job runs at 6:00am
2. Zone X: P(rain > threshold tomorrow 4–9pm) = 78%
3. Push notification sent to all active policyholders in Zone X
4. Worker opens Forecast tab:
   - Disruption type + probability
   - Estimated payout range for their plan tier
   - Current coverage status and ceiling
5. No action needed — system handles everything automatically
```

### Flow D: Admin / Insurer Dashboard

```
Real-time view:
  → Active triggers right now (zone, type, affected worker count)
  → Payouts processed today (count + total value)
  → Fraud holds pending review (count + held value)
  → Live loss ratio (rolling 30-day)

Predictive analytics:
  → Next 7 days: zones with >60% disruption probability
  → Estimated payout exposure by plan tier
  → Pool health (reserves vs projected claims)

Worker management:
  → Fraud review queue with worker details
  → Zone-level claim pattern heatmap
  → Dark store health status per store
  → Plan distribution (Basic / Standard / Pro split)
```

---

## 11. Platform Strategy

### Primary: Mobile Application (Android)

**Why mobile-first:**
- 97% of Q-Commerce delivery riders use Android smartphones (IAMAI 2024)
- Core worker experience is notification-driven — alerts, payout confirmations, forecast
- Policy management and claim history are inherently mobile-native interactions
- WhatsApp integration (Phase 3 bonus): key alerts via WhatsApp for zero-app-open experience

**Framework:** React Native (Expo) — cross-platform, team's React expertise transfers directly

### Secondary: Web Application

**Why web is still needed:**
- Admin/insurer dashboard is data-heavy — better suited to desktop
- Worker fallback access for low-storage devices
- API demonstration layer for judges

**Framework:** React.js (shared design system and component logic with React Native)

### Notification Strategy

| Event | Channel | Timing |
|---|---|---|
| Pre-alert (disruption forecast) | Push + SMS | 36–48 hrs before predicted event |
| Trigger fired | Push notification | Within 2 minutes of threshold breach |
| Payout processed | Push + SMS + in-app | Within 90 seconds of trigger |
| Weekly renewal reminder | Push | Friday 6pm + Sunday 9pm |
| Coverage ceiling update | In-app | Sunday night with new week activation |

---

## 12. Tech Stack

### Frontend

| Layer | Technology | Justification |
|---|---|---|
| Mobile app | React Native (Expo) | Cross-platform; team's React expertise transfers directly |
| Web dashboard | React.js + Vite | Fast build, component reuse from mobile |
| Styling | TailwindCSS + NativeWind | Consistent design system across web and mobile |
| Charts | Recharts (web), Victory Native (mobile) | Lightweight, well-documented |
| State management | Zustand | Simpler than Redux, sufficient for this scale |

### Backend

| Layer | Technology | Justification |
|---|---|---|
| API server | Node.js + Express | Team's primary strength |
| Authentication | JWT + bcrypt | Stateless, mobile-friendly |
| Cron jobs | node-cron | Native Node scheduling, no extra infrastructure |
| ORM | Prisma | Type-safe, seamless PostgreSQL integration |

### Database & Infrastructure

| Layer | Technology |
|---|---|
| Primary database | PostgreSQL (self-hosted) |
| Cache | Redis |
| ML microservice | Python + FastAPI |
| ML models | scikit-learn |

### External APIs

| API | Purpose | Tier |
|---|---|---|
| OpenWeatherMap | Rain, heat, 7-day forecast | Free tier |
| OpenAQ | AQI monitoring | Free, open-source |
| Razorpay | Simulated bank payouts | Test/sandbox mode |
| Twilio (Phase 3) | WhatsApp + SMS alerts | Trial tier |
| Mock APIs (custom) | Zepto/Blinkit platform, dark store health, curfew alerts | Self-built JSON mocks |

---

## 13. Database Justification

### Why PostgreSQL Over the Alternatives

The database choice for Kavach is a deliberate architectural decision. Insurance and financial data has specific requirements that rule out several popular options. Here is an honest comparison:

---

### PostgreSQL vs MongoDB

MongoDB is a document database — it stores flexible JSON-like documents without an enforced schema. This makes it excellent for unstructured or rapidly evolving data. However, Kavach's data is fundamentally **relational and structured**:

```
Worker → has many → Policies
Policy → has many → Claims
Claim  → has one  → Payout
Payout → has one  → Audit Log
```

Every one of these relationships requires **joins**, and every financial transaction requires **ACID compliance** — Atomicity, Consistency, Isolation, Durability:

- A premium deduction and policy activation must succeed or fail **together** — never one without the other
- A payout and its audit log entry must be written **atomically** — partial writes are unacceptable in financial systems
- Two simultaneous claims for the same trigger event must not produce double payouts — **isolation** prevents this

MongoDB's flexible schema is actually a **liability** here. In insurance you want a rigid, enforced schema — a claim record must always have a worker ID, policy ID, trigger type, and timestamp. A schema-less database makes it possible to write incomplete records, which in a financial context is a compliance and audit failure.

**PostgreSQL handles all of this natively** with its relational model, foreign key enforcement, and full ACID transaction support.

---

### PostgreSQL vs Supabase

This is a common misconception worth addressing directly: **Supabase is not a different database. Supabase is PostgreSQL.**

Supabase is an open-source Backend-as-a-Service platform that runs PostgreSQL under the hood and layers a UI, authentication system, real-time subscriptions, and auto-generated REST APIs on top of it. The actual database engine is identical.

So why not use Supabase then?

| Factor | Self-Hosted PostgreSQL | Supabase |
|---|---|---|
| Database engine | PostgreSQL | PostgreSQL (identical) |
| Control | Full | Partial (Supabase manages infra) |
| Cost at scale | Predictable server cost | Scales with row count and bandwidth |
| Custom ML integration | Direct DB connection | Works but adds a managed layer |
| Hackathon visibility | Full stack visible to judges | DB layer abstracted away |
| Vendor dependency | None | Supabase platform dependency |

For this hackathon specifically, self-hosted PostgreSQL gives the team **full visibility over every layer** — important when demonstrating architecture to judges. Supabase abstracts the database behind a managed service, which reduces the technical depth judges can evaluate.

In a production scenario, Supabase would be a perfectly reasonable choice since it is the same database with reduced operational overhead.

---

### PostgreSQL vs Firebase / Firestore

Firebase/Firestore is a NoSQL real-time document database optimized for mobile apps. It has the same fundamental problems as MongoDB for financial data — no ACID transactions across documents, no relational joins — with the added constraint of **vendor lock-in to Google Cloud**.

For Kavach's real-time needs (live trigger state, instant payout notifications), **Redis handles the real-time layer** while PostgreSQL handles all persistent data. This is a cleaner, more scalable separation of concerns than pushing everything into Firestore.

---

### Why Redis Alongside PostgreSQL

Redis is an in-memory key-value store used specifically for:

- **Live trigger state:** Which pin codes are currently under an active trigger — needs to be read in under 10ms across concurrent requests
- **Fraud score cache:** ML fraud scores cached for 5 minutes to avoid redundant inference calls on the same worker
- **Session tokens:** JWT blacklist for logged-out sessions

Redis does not replace PostgreSQL — it handles data that is **temporary, high-frequency, and latency-sensitive**. Everything that must persist long-term lives in PostgreSQL.

---

### Summary

| Database | Verdict for Kavach |
|---|---|
| **PostgreSQL** | ✅ Primary — relational, ACID, perfect fit for financial/insurance data |
| **Redis** | ✅ Cache layer — live trigger state, session data, ML score cache |
| **Supabase** | ⚠️ Same engine as PostgreSQL; fine for production, unnecessary abstraction for hackathon |
| **MongoDB** | ❌ NoSQL, no enforced schema, weaker transactions — wrong fit for financial data |
| **Firebase/Firestore** | ❌ NoSQL + Google vendor lock-in; real-time needs handled by Redis instead |

---

## 14. System Architecture

```
┌──────────────────────────────────────────────────────────────────┐
│                          FRONTEND LAYER                          │
│    React Native / Expo (Mobile)     React.js (Web Dashboard)     │
└─────────────────────────┬────────────────────────────────────────┘
                          │ HTTPS / REST
┌─────────────────────────▼────────────────────────────────────────┐
│                Node.js API Gateway (Express)                      │
│            JWT Auth · Rate Limiting · Route Dispatch             │
└──────┬───────────────┬──────────────┬───────────────┬────────────┘
       │               │              │               │
  ┌────▼────┐    ┌──────▼─────┐  ┌────▼────┐    ┌────▼────┐
  │  Risk   │    │  Trigger   │  │  Fraud  │    │ Payout  │
  │ Engine  │    │  Engine    │  │ Engine  │    │ Engine  │
  │         │    │ (cron/10m) │  │(pre-pay)│    │         │
  └────┬────┘    └──────┬─────┘  └────┬────┘    └────┬────┘
       │                │              │               │
       └────────────────┴──────────────┴───────────────┘
                                │
              ┌─────────────────┼────────────────┐
              │                 │                │
        ┌─────▼──────┐  ┌───────▼────┐  ┌────────▼───┐
        │ PostgreSQL │  │   Redis    │  │ Python ML  │
        │ (primary)  │  │  (cache)   │  │ (FastAPI)  │
        └────────────┘  └────────────┘  └────────────┘
                                │
              ┌─────────────────┼────────────────┐
              │                 │                │
        ┌─────▼──────┐  ┌───────▼────┐  ┌────────▼───┐
        │  Weather   │  │ Mock APIs  │  │  Payment   │
        │   APIs     │  │(Platform,  │  │ (Razorpay  │
        │(OWM, AQICN)│  │Dark Store, │  │  sandbox)  │
        └────────────┘  │  Curfew)   │  └────────────┘
                        └────────────┘
```

### Repository Structure

```
kavach/
├── mobile/                     ← React Native (Expo) — worker app
│   ├── screens/
│   │   ├── Onboarding/
│   │   ├── Dashboard/
│   │   ├── Policy/
│   │   ├── Payouts/
│   │   └── Forecast/
│   └── components/
├── web/                        ← React.js — admin dashboard
│   ├── pages/
│   │   ├── Overview/
│   │   ├── Triggers/
│   │   ├── FraudReview/
│   │   └── Analytics/
│   └── components/
├── server/                     ← Node.js + Express API
│   ├── routes/
│   ├── engines/
│   │   ├── triggerEngine.js
│   │   ├── riskEngine.js
│   │   ├── fraudEngine.js
│   │   └── payoutEngine.js
│   ├── jobs/
│   │   ├── triggerMonitor.js   ← cron, every 10 minutes
│   │   └── predictionJob.js    ← cron, daily 6:00am
│   └── db/                     ← Prisma schema + migrations
├── ml-service/                 ← Python FastAPI
│   ├── models/
│   │   ├── risk_model.py
│   │   ├── fraud_model.py
│   │   └── prediction_model.py
│   ├── data/                   ← Mock training datasets
│   └── main.py
└── mock-apis/                  ← Simulated external APIs
    ├── zepto_platform.js
    ├── dark_store_health.js
    └── curfew_alerts.js
```

---

## 15. Development Plan

### Phase 1 (March 4–20): Ideation & Foundation ✅
- [x] Persona selection and Q-Commerce research
- [x] Parametric trigger design (5 triggers including dark store)
- [x] 3-tier premium model (₹49 / ₹89 / ₹129) with AI coverage calibration
- [x] Predictive pre-alert system design with adverse selection rules
- [x] Fraud detection framework (3-layer architecture)
- [x] Tech stack and database justification
- [x] System architecture design
- [x] README documentation
- [ ] Project scaffolding (repo setup, folder structure)
- [ ] Mock API stubs for all 5 data sources

### Phase 2 (March 21–April 4): Core Build

**Week 3:**
- [ ] Worker onboarding flow (mobile) — registration, plan selection, zone setup
- [ ] PostgreSQL schema + Prisma models (workers, policies, claims, payouts, audit)
- [ ] Node.js API core routes (auth, workers, policies)
- [ ] OpenWeatherMap + OpenAQ integration (Triggers 1, 2, 3)
- [ ] Trigger Engine v1 — Rain and AQI triggers first

**Week 4:**
- [ ] All 5 triggers live in Trigger Engine
- [ ] Dark store mock API + dark store trigger logic
- [ ] Risk Engine + Python ML service (weighted scoring, coverage calibration)
- [ ] Dynamic coverage ceiling per plan tier and zone
- [ ] Payout Engine — calculation + Razorpay sandbox integration
- [ ] Worker dashboard (policy status, coverage ceiling, payout history)
- [ ] Layer 1 fraud gates

### Phase 3 (April 5–17): Polish & Scale

**Week 5:**
- [ ] ML Fraud Anomaly Model (Isolation Forest)
- [ ] Predictive Pre-Alert Engine (daily cron + push notifications)
- [ ] Admin dashboard (triggers, fraud queue, loss ratio, zone analytics)
- [ ] Full automated end-to-end demo flow (trigger → payout in <90s)
- [ ] WhatsApp alert integration via Twilio trial (bonus)

**Week 6:**
- [ ] End-to-end testing with simulated disruption scenarios
- [ ] 5-minute demo video (screen capture walkthrough)
- [ ] Final pitch deck (PDF)
- [ ] Performance optimization + code cleanup
- [ ] Final README update

---

## 16. Business Viability

### Market Sizing

| Metric | Value |
|---|---|
| Q-Commerce active riders in India (2025) | ~1.2 million |
| Target cities Phase 1 | 6 metros (Delhi, Mumbai, Bengaluru, Hyderabad, Chennai, Pune) |
| Addressable riders (6 metros) | ~600,000 |
| Target adoption Year 1 | 5% → 30,000 riders |
| Assumed plan distribution | 40% Basic / 40% Standard / 20% Pro |
| Blended weekly premium | ~₹81/week |
| Annual revenue per rider | ₹81 × 52 = ₹4,212 |
| **Year 1 ARR (5% adoption)** | **~₹12.6 Crore** |

### Loss Ratio Sustainability

```
Annual disruption exposure per rider: ~22 trigger events/year
Average payout per event (Standard plan, ₹89/week): ~₹280
Annual gross payout per rider: ₹280 × 22 = ₹6,160
Annual premium per rider (Standard): ₹89 × 52 = ₹4,628

Raw loss ratio: ₹6,160 ÷ ₹4,628 = 133% → requires adjustment

Sustainability mechanisms:
1. Plan tier payout ceilings (Basic ₹1,200 / Standard ₹2,200 / Pro ₹3,200 per week)
2. 72-hour waiting period + adverse selection prevention
3. AI coverage calibration (high-risk zones get lower effective ceilings)
4. Fraud detection (estimated 8–12% reduction in fraudulent payouts)
5. Zone-level risk pooling across all plan tiers

Target adjusted loss ratio: 65–75% (industry standard for parametric micro-insurance)
```

### Platform Partnership Opportunity

Zepto and Blinkit have strong financial incentives to subsidize rider insurance — it directly improves retention and reduces churn during adverse weather events. A platform subsidy of even ₹20–30/week per rider would meaningfully improve both affordability and Kavach's loss ratio simultaneously, creating a win-win for the platform, the insurer, and the worker.

---

## 17. Adversarial Defense & Anti-Spoofing Strategy

> *500 delivery partners. Fake GPS. Real payouts. A coordinated fraud ring just drained a platform's liquidity pool. This section describes exactly how Kavach detects, isolates, and neutralizes it — without punishing a single honest worker.*

---

### Understanding the Attack Surface

Individual fraud (one person spoofing GPS) is solved by basic location checks. **Coordinated ring fraud is categorically different.** A well-organized ring of 500 actors can defeat every naive defense:

- They register weeks in advance → defeats the 72-hour policy age gate
- They all spoof GPS correctly to the triggered pin code → defeats simple location checks
- They all claim simultaneously → looks like a real mass disruption event
- They use different devices → defeats simple device fingerprinting

The only way to catch a fraud ring is to find signals that **500 people cannot collectively fake** — because coordination itself leaves traces, and because genuine disruption behavior has physical properties that spoofed behavior cannot replicate.

---

### The Fundamental Insight: Activity Before the Trigger

The single most powerful signal in Kavach's arsenal is deceptively simple:

**A genuinely stranded worker was actively delivering immediately before the disruption hit. A fraudster was not.**

```
Genuine worker:   [delivering] → [delivering] → [rain starts] → [goes offline]
Fraud ring actor: [offline]    → [offline]    → [rain starts] → [suddenly "in zone"]
```

This pre-trigger activity window — the 60–90 minutes before a trigger fires — is the cleanest discriminator between a real claim and a fake one. Kavach passively logs app-open events and last-known GPS pings continuously. When a trigger fires, it looks backward, not just at the current moment.

A fraudster can spoof where they are *now*. They cannot retroactively spoof where they were *before they knew the trigger would fire*.

---

### The 6-Layer Anti-Spoofing Architecture

#### Layer A: GPS Physics Validation

Real GPS signals have physical properties that spoof tools routinely fail to replicate:

```
Signal Jitter Check:
  Real GPS:   ±5–15 meter variance between consecutive pings (atmospheric noise)
  Spoofed GPS: Suspiciously perfect coordinates — same exact lat/long repeatedly
               OR teleportation jumps (15km movement in 2 minutes)

Velocity Plausibility Check:
  Worker's last known location + time elapsed → maximum possible displacement
  If current claimed location is physically unreachable in the elapsed time → flag

  Example: Worker's last ping was 18km away, 8 minutes ago
  Maximum motorcycle speed in urban traffic: ~40km/h
  Maximum reachable distance: ~5.3km
  Claimed zone: 18km away → IMPOSSIBLE → GPS spoof flag

Altitude Consistency Check:
  Delivery riders on roads have consistent altitude profiles
  A spoofed location set to a pin code centroid often places the worker
  on a rooftop or inside a building at altitude Z — impossible for a rider
```

#### Layer B: Pre-Trigger Behavioral History

Kavach's passive activity logging creates a **72-hour behavioral fingerprint** for every active worker. This fingerprint cannot be faked retroactively.

```
Pre-Trigger Activity Score (calculated at trigger fire time):

  HIGH activity (genuine signal):
  → Worker had app-open events in the 90 mins before trigger
  → Worker's GPS trail shows movement consistent with deliveries
  → Worker's last known location was within or adjacent to triggered zone
  → Worker has order completions logged in the platform mock API in last 2 hours

  LOW activity (fraud signal):
  → Worker was app-closed for 4+ hours before trigger
  → Worker's last GPS ping was in a completely different zone
  → Zero order activity in the platform log today
  → Worker suddenly "appears" in triggered zone within 5 minutes of trigger firing

Pre-Trigger Activity Score below 0.3 → claim held regardless of current GPS
```

#### Layer C: Network Graph Analysis (Ring Detection)

Individual actors look innocent in isolation. A ring reveals itself through its **social and registration graph**. Kavach builds a lightweight network graph of all registered workers and runs anomaly detection on it weekly.

```
Registration Clustering:
  Flag workers who registered within the same 4-hour window
  AND share any two of: same IP range, same device model,
  same bank branch (IFSC prefix), same referral chain

  500 people registering from 12 IP addresses in one evening
  is not organic adoption — it is coordinated onboarding

Account Velocity:
  Normal organic registration: 10–50 new users/day per city
  Ring registration: 100–500 new users in a single session
  → Automatic elevated-monitoring flag on all accounts in the spike

Payout Destination Clustering:
  Real workers have diverse bank accounts across many branches
  Fraud rings often funnel payouts to accounts at the same bank branch
  or to accounts with sequential account number patterns
  → If 30+ workers in a zone share the same IFSC code → investigation flag

Claim Synchronization Score:
  Real disruption: Workers claim over a 15–40 minute window
  (people notice the rain, stop working, open app at different times)
  Fraud ring: All 500 claims arrive within a 90-second window
  → Burst claim detection: if >50 claims arrive from one zone in <3 minutes
     → automatic hold on ALL claims from that zone pending cross-validation
```

#### Layer D: Zone Claim Rate Anomaly

Real disruptions have a **predictable and measurable claim participation rate** based on historical data. Fraud rings break this pattern dramatically.

```
Historical Zone Claim Rate (from training data):
  Heavy rain event in Zone X → typically 35–55% of registered workers claim
  (The rest were already done for the day, were indoors, chose to continue, etc.)

Fraud Ring Signature:
  A coordinated ring will attempt to maximize payouts → 80–95% claim rate
  500 out of 520 registered workers claiming the exact same event
  is statistically near-impossible in organic behavior

Anomaly Threshold:
  If zone claim rate > 70% for any single trigger event → freeze zone payouts
  Cross-validate against:
    1. Pre-trigger activity scores of claimants
    2. Platform order volume data for that zone
    3. GPS physics validation scores
  
  Release payouts only to workers who pass all three cross-validation checks
  Workers who fail cross-validation are held for manual review — not denied
```

#### Layer E: Platform Activity Reconciliation

The mock platform API provides Kavach with a critical ground truth signal that fraudsters cannot manipulate — the actual delivery log.

```
For every claim, Kavach queries the platform mock API:

  "Did worker [ID] complete any deliveries in the 2 hours
   before trigger [ID] fired in Zone [X]?"

Genuine worker:   YES → last delivery completed at 6:12pm, trigger fired at 6:34pm
Fraud ring actor: NO  → zero deliveries today, account dormant

This single check eliminates the majority of fraud ring actors
because they have no delivery history — they registered to claim,
not to deliver.

For workers with no delivery history today but legitimate reasons
(day off, late shift start), the system cross-validates against
pre-trigger GPS and app-open history before making a decision.
```

#### Layer F: Temporal Decoupling (The Ring's Achilles Heel)

This is Kavach's most sophisticated defense and the one a fraud ring cannot easily defeat.

The insight: a fraud ring coordinates in real time. They need to know **when** a trigger fires to spoof their GPS to the right location at the right time. This coordination signal is itself detectable.

```
Trigger Announcement Delay:
  When a trigger threshold is crossed, Kavach does NOT immediately
  announce it to all clients. Instead:
  
  1. Trigger is detected internally at T=0
  2. System silently snapshots GPS and activity data for all zone workers at T=0
  3. Trigger is announced to app clients at T=0 + 8 minutes
  4. Claims window opens at T=0 + 8 minutes

  A fraud ring monitoring the app for trigger announcements will spoof
  their GPS AFTER the announcement (T=8min). But Kavach already
  captured their true location at T=0.

  Genuine workers were already in the zone at T=0 (they were delivering).
  Fraud ring actors were not in the zone at T=0 — they spoofed after announcement.

  The 8-minute snapshot window makes retroactive spoofing impossible.
  The ring cannot fake where they were before they knew the trigger fired.
```

---

### How Kavach Distinguishes the Genuinely Stranded Worker

The hardest problem is not catching obvious fraudsters — it is ensuring that **a legitimate worker is never denied a valid payout** because they happened to score poorly on one signal.

Kavach uses a **weighted evidence model**, not a binary pass/fail system:

```
Claim Confidence Score = weighted combination of all signals:

  Pre-trigger activity history    (weight: 0.30)  ← strongest signal
  GPS physics validation          (weight: 0.25)
  Platform delivery reconciliation(weight: 0.20)
  Network graph isolation         (weight: 0.15)  ← is worker part of flagged ring?
  Zone claim rate context         (weight: 0.10)

Score ≥ 0.65:  Full auto-approve → instant payout
Score 0.40–0.64: Partial payout (60%) now + 40% held 24hrs pending review
Score < 0.40:  Full hold → admin review → worker notified with reason
```

**Protecting honest workers in a ring-affected zone:**

When a fraud ring is detected in a zone, Kavach does not freeze ALL payouts — it freezes payouts for accounts with low Claim Confidence Scores while processing high-confidence claims normally. A genuine worker with strong pre-trigger activity and GPS history gets paid on time even if 400 fraudsters in their zone are being held.

```
Zone Fraud Ring Detected Protocol:
  1. Identify accounts with Claim Confidence Score < 0.40 → hold
  2. Accounts with Score ≥ 0.65 → process immediately (these are real workers)
  3. Accounts with Score 0.40–0.64 → partial payout + 24hr review
  4. Admin notified of ring detection with network graph visualization
  5. Law enforcement referral threshold: coordinated ring > 50 accounts
```

---

### What a Fraud Ring Cannot Fake (Summary)

| Signal | Why It Cannot Be Faked |
|---|---|
| Pre-trigger GPS history | Captured before trigger announcement — retroactive spoofing impossible |
| Platform delivery log | Real order completions exist in the platform's own system |
| GPS jitter pattern | Physical property of real GPS hardware — perfect coordinates are suspicious |
| Velocity plausibility | Physics — cannot teleport 18km in 8 minutes |
| Registration network graph | 500 people registering from 12 IPs in one evening is structurally visible |
| Payout destination clustering | Bank account patterns across a ring are statistically anomalous |
| Claim burst timing | 500 simultaneous claims in 90 seconds is not human behavior |
| Trigger announcement delay | 8-minute snapshot window captures true location before ring can react |

---

### False Positive Protection (The Honest Worker Guarantee)

Kavach's adversarial defense is explicitly designed to **never sacrifice honest workers to catch fraudsters**. Every hold triggers a notification to the worker explaining which signal caused the review — not a denial, a delay with a reason.

```
Worker notification on hold:
  "Your claim is under review (Ref: GS-HOLD-2026-03-21-8821).
   This happens automatically when our system detects unusual
   patterns in your area. We'll complete the review within 24 hours.
   If approved, your full payout will be processed immediately.
   Questions? Contact support."

SLA: All held claims reviewed within 24 hours
Appeals: Worker can submit GPS screenshot + platform activity proof
Outcome: If approved after review, payout processed with no deduction
```

No honest worker is permanently denied. The system delays, investigates, and pays — it does not silently reject.

---

## Coverage Constraints (Mandatory Compliance)

Per Guidewire DEVTrails 2026 requirements:

| Constraint | Status |
|---|---|
| Health / medical insurance | ❌ Explicitly excluded |
| Accident coverage | ❌ Explicitly excluded |
| Vehicle repair | ❌ Explicitly excluded |
| Life insurance | ❌ Explicitly excluded |
| Weekly pricing model | ✅ Three weekly tiers: ₹49 / ₹89 / ₹129 |
| Income loss only | ✅ All payouts are income replacement only |
| Parametric triggers | ✅ 5 objective, API-verified triggers |
| AI/ML integration | ✅ Risk scoring, fraud detection, prediction engine |

---

*Kavach — Built for the workers who power India's 10-minute economy.*

*Guidewire DEVTrails 2026 | Phase 1 Submission | March 20, 2026*
