# GigSafe — RainReady
### AI-Powered Parametric Income Protection for Food Delivery Partners
*Built for Guidewire DEVTrails 2026 — University Hackathon*

Before You Read

A Short introduction on
what are solving and for whom are we solving it ? short answer to this is income loss the food delivery segment faces during heavy rain, cyclones, extreme heat, and citywide strikes . why just food delivery segment and not the e-commerce or the q-commerce ? lets say i order cold coffee and fries. And then rain hits , my order is delayed . I dont want watery coffee and soggy fries delivered to me so, i cancel my order . The rider loses that income permanently. It greatly affects the daily income of gig workers in this segment whereas in the e-commerce segment ,the income opportunity is just deferred, not destroyed. The order i made in amazon remains assigned and is fulfilled the following day. And Q-commerce like blinkit and zepto cafes were introduced in idea with the catchy concept of same hour delivery so , Behaviorally identical to food delivery and are affected likely in the same level. 

time-criticality is one of main reasons that led us taking focus in food delivery segment . They are greatly affected and require a safety net and So , We provide them a AI-Powered Parametric Income Protection 

Three main features 1.Risk profiling 2. Fraud detection 3.Parametric Automation of Claim and Instant payout

---

## Table of Contents

1. [Persona Segment — Who We're Building For](#1-persona-segment)
2. [The Problem We're Solving](#2-the-problem)
3. [Customer Persona — Rajan Kumar](#3-customer-persona)
4. [Requirements and Scenarios](#4-requirements-and-scenarios)
5. [Application Workflow](#5-application-workflow)
6. [Weekly Premium Model, Parametric Triggers, and Platform Choice](#6-weekly-premium-model)
7. [AI/ML Integration Plan](#7-aiml-integration)
8. [Tech Stack and Development Plan](#8-tech-stack)
9. [Adversarial Defense and Anti-Spoofing Strategy](#9-adversarial-defense)

---

## 1. Persona Segment

We chose **food delivery partners** — specifically riders on Swiggy, Zomato, and Q-commerce food verticals like Zepto Café and Blinkit Kitchen.

We deliberately excluded e-commerce delivery (Amazon, Flipkart, Shadowfax). Here's why that distinction matters.

When it rains and a food delivery is delayed, the order is ruined. A cold coffee is watery. Soggy fries are inedible. The customer cancels. The rider loses that delivery permanently. That income is gone.

With e-commerce, if it rains and a package can't be delivered today, the rider delivers it tomorrow. The job didn't disappear — the income opportunity was deferred, not destroyed. There's no meaningful income loss to insure against.

Q-commerce food (Zepto Café, Blinkit Kitchen) is included because it behaves identically to Swiggy or Zomato. The order is time-critical, the food is perishable, and any delay means cancellation. The disruption profile is the same.

**Our scope:** any platform-based delivery partner where the goods must arrive quickly or the order is permanently lost.

---

## 2. The Problem

India has over 5 million food delivery partners. They earn somewhere between ₹3,500 and ₹4,500 in a good week. When heavy rain hits, or a cyclone warning is issued, or a city-wide bandh is called — they can lose 60 to 80 percent of their daily income. Overnight. No warning. No compensation.

A single bad rain day in Chennai drops a rider's earnings from ₹700 to ₹150. He still has rent. EMI on his bike. Groceries for five people. School fees. None of that pauses because it rained.

These workers have almost no savings. One bad week means borrowing from colleagues. A monsoon season in Chennai — 3 to 4 weeks of heavy disruption every October and November — means ₹8,000 to ₹12,000 of annual income erased by weather alone.

No existing insurance product covers this. Health insurance covers the body. Vehicle insurance covers the bike. Nothing covers income lost when it rains too hard to deliver food.

**GigSafe (RainReady) fixes this.** Automatic payouts triggered by real weather and disruption data, straight to UPI. No claim forms. No phone calls. No waiting. When the trigger fires, the money moves.

---

## 3. Customer Persona

### Who Rajan is

**Rajan Kumar, 27. Velachery, Chennai.**

Swiggy delivery partner, 3 years on the platform. Rides a Honda Activa. Covers Velachery, Pallikaranai, and Medavakkam. Lives with his wife, one child, and parents — five people depending on his income. Sends ₹3,000 a month to his parents in Villupuram. Uses Google Pay every day. Speaks Tamil. Has a Redmi phone.

### The 13 persona dimensions

| Dimension | Rajan's profile |
|---|---|
| **Income pattern** | Per order, daily cashout via Swiggy wallet. Earns and spends same day. |
| **Peak hours** | 12–2pm (lunch) and 7–9pm (dinner). Rain during these windows causes the most damage. |
| **Zone type** | 3–5 km radius, flood-prone (Pallikaranai low-lying areas). High disruption zone. |
| **Vehicle type** | Honda Activa (petrol, owned, no EMI). Cannot ride safely above 25mm/hr rainfall. |
| **Disruption sensitivity** | Very high. Food orders cancel instantly when rain hits. 60–80% income drop on heavy rain days. |
| **App dependency** | Single platform (Swiggy only). All activity tracked — clean behavioral baseline for fraud detection. |
| **Digital literacy** | Low-medium. Tamil UI mandatory. GPay is his comfort zone. Abandons unfamiliar flows in 2 minutes. |
| **Avg weekly earnings** | ₹4,200 good week. ₹1,600 heavy rain week. |
| **Income volatility** | Very high. NE monsoon = 3–4 weeks of half-income per year. |
| **Savings buffer** | Near zero. Borrows from colleagues during bad weeks. |
| **UPI usage** | Google Pay, checked constantly between deliveries. A payout in GPay is the strongest trust signal we can send. |
| **Language preference** | Tamil for all financial decisions. English notifications get ignored. |
| **Claim behaviour** | Fully passive. Will not self-initiate anything. If any step is required, he forgets within 24 hours. |

### Disruption triggers (Chennai-specific)

| Disruption | When | Income loss |
|---|---|---|
| Heavy rain — NE monsoon | October–November, 3–5 days/week at peak | 70–80% |
| Cyclone alert | November–December | 100% — platform suspends ops |
| Extreme heat | April–June, 40–44°C | 35–45% |
| Severe AQI (>300) | Winter months | 40–55% |
| Bandh / political strike | 4–6 times a year statewide | 90–100% |

### Behaviour

Rajan's decision-making follows six patterns that we designed the entire product around.

**He trusts peers above everything.** If three Swiggy colleagues say it works, he'll try it without another question. His WhatsApp delivery group is our distribution channel — not ads, not influencers. One successful payout witnessed by peers converts better than any marketing spend.

**He abandons anything requiring forms.** Skeptical of long sign-up flows or document uploads. Leaves within 2 minutes if it feels complicated. Our onboarding is Aadhaar OTP only, Tamil UI, under 4 minutes total.

**He communicates in Tamil on WhatsApp.** Not English emails. Not in-app messages he hasn't noticed. Every payout alert, coverage confirmation, and support interaction goes through Tamil WhatsApp.

**He checks his phone at traffic lights.** That is the usage context. The home screen needs to show his coverage status in one glance. Nothing buried in menus. Under 30 seconds to do anything important.

**He'll switch mid-subscription if a friend shows him something better.** No brand loyalty — only outcome loyalty. The product has to earn its place every single week.

**The first payout is the entire product.** He needs to see money in GPay before he believes it works. First payout = lifetime loyalty. No first payout = he churns and tells ten friends it's a scam. We get one shot.

### Self-initiation likelihood

Near zero. He will not file a claim. He will not call support. He will not follow up. He will not remember he is insured during a rain event unless the app tells him first.

This means every payout must be fully automated. The system pays him before he even realizes the trigger fired. This is not a feature — it is the only viable product architecture for this persona.

### Willingness to pay (WTP)

Comfortable range: **₹39–79 per week.**

This is roughly 1–2% of a good week's income. The framing that works is not "1% of income" — Rajan thinks in deliveries, not percentages. The pitch is: *"Skip 2 deliveries this week. We cover 40 bad ones next monsoon."*

Above ₹99/week, he stops seeing it as a small safety bet and starts treating it as a real financial commitment. Without a track record of payouts he's witnessed personally, ₹99+ will not convert.

---

## 4. Requirements and Scenarios

### Must-have requirements

**R1 — Onboarding under 4 minutes.** Tamil/Hindi/Telugu UI. Aadhaar OTP only — no document uploads. UPI autopay mandate setup. Risk profiling runs silently at signup. Coverage active immediately after first payment.

**R2 — Dynamic weekly premium.** Recalculated every Monday 5am using XGBoost. Inputs: 7-day IMD rainfall forecast, zone flood risk, rider's 12-week claim history, AQI forecast, festival and strike calendar. Deducted automatically Monday 7am via UPI autopay.

**R3 — Parametric auto-trigger.** Real-time monitoring of IMD, CPCB AQI, and NDMA alerts. Dual-trigger AND gate — both weather API and order-volume proxy must confirm before payout fires. Zero action from rider required.

**R4 — Fraud detection (3-layer).** Behavioral baseline, anti-spoofing signals, and peer-cohort analysis. Graph Neural Network for coordinated ring detection. Combined fraud score 0–1 with graduated response tiers.

**R5 — Payout within 2 hours.** Razorpay UPI instant transfer. Tamil push notification on receipt. WhatsApp coverage certificate sent weekly.

**R6 — Analytics dashboard.** Admin view with active policies, payout volume, fraud flags, zone risk heatmap, and trigger event log.

### Non-functional requirements

- Payout SLA: under 2 hours from trigger confirmation to UPI credit
- Onboarding: under 4 minutes from first open to coverage active
- Languages: Tamil, Hindi, Telugu at MVP
- Fraud false positive rate: below 5%

### Persona-based scenarios

**Scenario 1 — NE monsoon rain, Velachery**

IMD issues a yellow alert at 11:30am — 18mm/hr rainfall in Velachery. Swiggy order volume in the zone drops 68% within 30 minutes. Both signals exceed threshold — the dual-trigger fires. Rajan was GPS-active and logged in at 11:15am, so he's eligible. Fraud check passes: normal GPS jitter, NavIC agrees with GPS, accelerometer shows movement, 44 of 50 nearby riders also inactive, inactivity timing spread over 22 minutes (no ring signature). By 12:45pm, ₹420 arrives in his GPay. Tamil push notification confirms it. That evening he shows the notification to his Swiggy group chat. Three colleagues sign up.

**Scenario 2 — Bandh day, complete shutdown**

Tamil Nadu bandh declared at 6am. NDMA civic alert fires. Swiggy suspends operations city-wide. Order volume = 0 — a single trigger is sufficient, no peer-cohort check needed. Full day payout fires for all active subscribers in affected zones. Rajan receives ₹700 (his declared daily average). The money arrived before he even asked about it.

**Scenario 3 — Coordinated fraud ring, 500 riders**

IMD yellow alert issued Thursday. A Telegram ring fires. 500 riders go inactive within 3 minutes of each other — temporal standard deviation = 2.4 minutes. Anomaly flag raised. Adjacency graph computed: 487 riders share the same IP subnet, identical GPS jitter score of 0.0, and inactivity onset within 90 seconds. Reference rider pool checked — 18 of 25 high-trust riders still active. Disruption not confirmed as real. Ring subgraph identified and blocked. The 13 honest riders not in the ring get paid normally. All blocked riders receive a Tamil WhatsApp message with a one-tap appeal. Human reviewer handles appeals within 4 hours.

---

## 5. Application Workflow

```
RIDER OPENS APP
      ↓
ONBOARDING (first time only)
  Language select → Aadhaar OTP → Rider profile (zone, platform, vehicle)
  → Tier selection → UPI autopay setup → Coverage active
      ↓
HOME SCREEN (every week)
  Coverage card · Rain radar widget · Pre-emptive alerts when IMD issues warnings
      ↓
EVERY MONDAY 5AM — PREMIUM ENGINE RUNS
  ML calculates personalised premium → UPI autopay deducts Monday 7am
  → WhatsApp certificate sent → Coverage live Mon–Sun
      ↓
DURING THE WEEK — REAL-TIME MONITORING
  IMD + CPCB + NDMA + order-volume proxy watched continuously
      ↓
DISRUPTION EVENT DETECTED
  Dual-trigger AND gate: both signals must confirm
  → Eligibility check (was rider active 30 min before?)
  → Fraud scoring (L1 behavioral + L2 anti-spoof + L3 graph)
  → Score below 0.40 → Instant payout → Tamil push + GPay credit
      ↓
NICE-TO-HAVE FEATURES
  Income dashboard · Streak rewards · Squad cover
  Income proof certificate · Community disruption map · Buddy check
      ↓
ADMIN DASHBOARD
  Active policies · Payout volume · Fraud queue · Zone risk heatmap
```

---

## 6. Weekly Premium Model, Parametric Triggers, and Platform Choice

### How the weekly premium model works

The premium is not flat. It reprices every Monday at 5am based on what's actually likely to happen that week.

The XGBoost model takes these inputs:
- 7-day IMD rainfall forecast for the rider's zone
- Historical disruption frequency for that zone and month
- CPCB AQI 7-day forecast
- Rider's own claim history over the last 12 weeks
- Festival and strike calendar for the coming week
- Zone risk index from NDMA flood hazard maps
- Peer group claim rate in the zone

It outputs a personalised weekly premium between ₹39 and ₹149. A rider in Velachery during October monsoon pays more than the same rider in February. A rider with a clean 12-week history pays less than someone with frequent claims.

Premium is deducted automatically via UPI autopay on Monday morning. Coverage runs Monday to Sunday. Each week is a fresh contract — no rollover, no annual lock-in.

**Payout formula:**

```
payout = avg_daily_earnings
         × (disruption_hours / working_day_hours)
         × severity_score
         × tier_multiplier
         × peak_hour_weight
         capped at: min(tier_daily_cap, 3 × weekly_premium)
```

The 3× cap prevents adverse selection — you can't buy a ₹39 policy Monday and claim ₹2,000 Tuesday when you see a storm coming.

### Parametric triggers

We use a dual-trigger AND gate. Both signals must confirm before any payout fires.

**Signal 1 — Weather API:** IMD rainfall ≥ 15mm/hr sustained for 30+ minutes in the rider's zone. OR CPCB AQI ≥ 300. OR NDMA/Sachet disaster alert issued.

**Signal 2 — Order-volume proxy:** 60%+ of GPS-active riders in the zone show zero delivery completions for 45 consecutive minutes. This is ground truth confirmation that income is actually being lost.

Why both? IMD can miss hyperlocal rain. The order proxy can miss platform outages. Each signal can be wrong individually. Both wrong simultaneously is extremely unlikely and nearly impossible to fake.

### Why mobile, not web

The choice is a product necessity, not a preference. Every critical feature requires native mobile capability:

- **Tamil push notifications** — when a payout fires, Rajan needs an immediate GPay-style alert. Web apps can't reliably push to a Redmi phone on BSNL prepaid.
- **Background GPS** — fraud detection requires continuous location monitoring. Browsers can't access GPS in the background.
- **Accelerometer** — a key anti-spoofing signal. Web apps can't reliably access device motion sensors.
- **Play Integrity API** — detecting GPS mock apps requires native Android integration.
- **NavIC cross-validation** — requires native GNSS access, unavailable in a browser.
- **UPI autopay** — requires deep Razorpay SDK integration for mandate creation.
- **Offline resilience** — Rajan is on BSNL prepaid with patchy data. A native app caches coverage status offline. A web app is dead without connection.

Beyond technical necessity, Rajan checks his phone at traffic lights. A native app is one tap. A web app requires browser, URL, login, wait. Nobody opens a browser at a red light.

---

## 7. AI/ML Integration

### M1 — Dynamic premium pricing (XGBoost Regression)

Runs every Monday 5am. Inputs: weather forecast, zone risk, claim history, AQI forecast, festival calendar, peer group risk index. Output: personalised weekly premium (₹39–₹149). Retrained monthly on new payout data.

**Training data:** IMD historical rainfall from data.gov.in and Kaggle India weather datasets. 10,000 synthetic rider profiles generated via Python Faker. Rule-based premium labels to train initial model.

### M2 — Rider risk profiling (Random Forest Classifier)

Runs once at onboarding, refreshes every 4 weeks. Inputs: city and zone, platform, vehicle type, declared working hours, zone flood risk score (NDMA maps), month of enrollment, declared daily earnings. Output: Base Risk Tier (Low / Medium / High) that anchors M1.

### M3 — Parametric trigger classifier (Rule engine + LSTM)

Runs continuously. Rule layer checks IMD threshold, AQI threshold, NDMA alerts. LSTM layer detects abnormal order-volume drops even when weather API lags, using historical baseline of normal order patterns per zone per hour.

### M4 — Fraud detection (3-layer)

**L1 — Isolation Forest (behavioral baseline).** 30-day GPS history, login patterns, movement speed, delivery frequency, claim rate. Flags deviations from personal baseline.

**L2 — Anti-spoofing rules.** GPS mock detection via Play Integrity API (free, passive). NavIC vs GPS disagreement score. GPS jitter analysis (real riders: ±3–8m variance; mock GPS: 0.0). Accelerometer stillness score. Home Wi-Fi SSID detection in beacon log. VPN detection via ip-api.com.

**L3 — Graph Neural Network (ring detection).** Builds adjacency graph using shared signals (device ID, IP subnet, GPS jitter score, inactivity onset timing). Louvain algorithm identifies dense fraud subgraph. Betweenness centrality finds ring coordinator nodes. Temporal clustering detects Telegram broadcast signature (σ < 4 minutes = ring flag).

Combined fraud score 0–1. Below 0.40 = instant payout. 0.40–0.70 = pay after 6 hours. 0.70–0.90 = hold 24 hours with notification. Above 0.90 = block with Tamil WhatsApp appeal channel.

### M5 — Payout calculator (Regression)

Runs per-event. Inputs: rider's 8-week average daily earnings, disruption duration and timing, coverage tier, disruption severity from M3, weekly premium paid. Output: exact ₹ payout, capped at 3× weekly premium.

---

## 8. Tech Stack and Development Plan

### Tech stack

| Layer | Technology |
|---|---|
| Mobile frontend | React Native (Android-first) |
| Backend API | Node.js |
| ML inference | Python + FastAPI |
| Primary database | PostgreSQL |
| Cache / real-time state | Redis |
| ML model storage | AWS S3 |
| Payments | Razorpay UPI (autopay + instant payout) |
| Push notifications | Firebase FCM |
| Communications | WhatsApp Business API |
| Weather | IMD API + OpenWeatherMap (free tier) |
| AQI | CPCB CAAQMS API + aqicn.org |
| Disaster alerts | NDMA RSS + Sachet portal |
| Device integrity | Google Play Integrity API (free) |
| VPN detection | ip-api.com (free) |
| Training data | Kaggle India weather datasets + Python Faker |

### 6-week development plan

**Week 1 (Seed) — Foundation**
Persona finalization, system architecture, database schema, API mock setup, synthetic dataset generation, ML scaffolding.

**Week 2 (Seed) — Core product**
Onboarding flow (Tamil UI + Aadhaar OTP + UPI autopay), M2 risk profiling, M1 premium engine (Monday recalculation), weekly policy generation, coverage card on home screen.
*Target: 4-star Seed submission.*

**Week 3 (Scale) — Trigger engine**
IMD + CPCB + NDMA API integration, dual-trigger AND gate logic, order-volume proxy computation, M3 LSTM anomaly detection, trigger event logging.

**Week 4 (Scale) — Fraud and payouts**
M4 L1 Isolation Forest + L2 anti-spoofing (NavIC, jitter, Play Integrity, accelerometer) + L3 adjacency graph and Louvain and betweenness centrality. M5 payout calculator. Razorpay UPI payout integration. Graduated fraud score response.
*Target: 5-star Scale submission.*

**Week 5 (Soar) — Polish and analytics**
Analytics dashboard, multilingual notifications, WhatsApp Business certificate, income dashboard, streak rewards, end-to-end testing.

**Week 6 (Soar) — Demo and pitch**
Live demo environment (rain trigger → fraud check → payout in 90 seconds), pitch deck, stress testing, DemoJam preparation.



---

## 9. Adversarial Defense and Anti-Spoofing Strategy

### The crisis

A syndicate of 500 delivery workers organized on Telegram. They downloaded a cheap GPS spoofing app. They faked their locations into a red-alert flood zone. They sat at home. The platform paid ₹420 × 500 = ₹2,10,000 in two hours. The liquidity pool was gone.

The attack didn't break the system. It used the system's own logic against it.

The peer-cohort model said: *500 out of 500 riders in the zone are inactive — that's a real disruption.* The logic was right. The ring knew the logic and built the attack around it.

Simple GPS verification is dead.

### What the data says

This is not hypothetical. India recorded **465+ GPS spoofing incidents between 2023 and 2025** (DGCA). Telegram-based fraud coordination grew **53% in 2024** (Kaspersky). Fraud ring activity more than doubled in the same period (Feedzai). GPS spoofing apps are commercial products selling for ₹100–200/month. Any rider with a smartphone can arm themselves for a ring.

Traditional anomaly detection (Isolation Forest) fails against coordinated rings because it looks at each person individually. A well-coached ring member looks completely normal alone. The fraud only appears in the connections between people. Graph Neural Networks outperform per-node models at AUC 0.961 vs 0.834 for ring detection — because fraud hides in the edges, not the nodes.

### 9.1 Differentiating a genuine rider from a faker

A single signal can't do it. The defense is making it impossible to fake everything simultaneously.

When Rajan is genuinely stranded in a Velachery flood:

- GPS says Velachery 
- NavIC satellite system also says Velachery 
- Cell tower triangulation puts him in the Velachery cluster 
- Wi-Fi beacon log shows no home router nearby 
- Accelerometer shows slight movement — fidgeting, not stone still 
- GPS path has natural jitter — ±4–6 metres per fix 
- He went inactive at 11:47am, about 20 minutes after rain started 

When a fraudster runs a GPS mock app from his living room:

- GPS says Velachery  (spoofed)
- NavIC says his actual home location — mismatch
- Cell towers say his home neighbourhood — mismatch
- His home Wi-Fi SSID appears in the beacon log — contradiction
- Accelerometer shows zero movement for 45 minutes — stationary
- GPS path has zero jitter — perfectly smooth, impossible for a real vehicle 
- He went inactive at exactly 11:43:09am, same second as 486 others  — impossible naturally

The genuine rider passes all seven checks. The spoofer fails four or five. All seven together make faking everything simultaneously nearly impossible.

**The NavIC advantage (India-specific).** NavIC (built by ISRO) runs on L5 and S-band frequencies — completely different from American GPS L1/L2. A ₹200 GPS mock app only spoofs GPS. It cannot spoof NavIC because doing so requires specialized hardware costing lakhs. Almost every Indian Android phone since 2019 has a NavIC receiver. We cross-check both signals silently in the background. If they disagree by more than 50 metres, we flag it. India's 465+ spoofing incidents were almost all GPS-layer attacks. NavIC catches them all.

**App Cloner detection.** Google Play Integrity API detects rooted devices, apps installed outside the Play Store, virtualization containers (how App Cloner works), and tampered APKs — for free, passively, with zero user action. The ₹200 GPS mock app the ring distributed is exactly the class of software this API was built to detect.

### 9.2 Data points that catch a coordinated ring

**GPS jitter score.** Real 2-wheeler movement produces ±3–8 metres of GPS variance per fix. A mock GPS app produces a mathematically perfect path with zero variance. Standard deviation near 0.0 = synthetic location. We also detect teleportation signatures — any GPS transition implying speed above 120 km/hr for a registered 2-wheeler.

**NavIC vs GPS disagreement score.** Distance in metres between what GPS claims and what NavIC claims. Above 50m = flag. Above 200m = strong fraud indicator.

**Temporal clustering — the Telegram signature.** Real disruptions spread organically. The standard deviation of inactivity onset times during a real disruption is 18–35 minutes. A Telegram broadcast makes everyone act at once. All 487 ring members went inactive within a 3-minute window. Standard deviation = 2.4 minutes.

Nature does not coordinate like that. Telegram does.

Rule: if cluster inactivity is above 60% AND standard deviation of onset times is below 4 minutes → coordinated ring flag, regardless of what the weather API says.

**The adjacency graph.** We build a graph where each rider is a node. Edges connect riders who share: same device ID, same IP subnet, same GPS jitter score within ±0.1, inactivity onset within 3 minutes, same GPS mock app detected via Play Integrity. An honest zone has a sparse graph — 1–2 connections per person. A fraud ring has a dense subgraph — almost everyone connected through multiple shared signals. The Louvain algorithm identifies this cluster automatically.

**Betweenness centrality — the ring leader.** The person who sent the Telegram broadcast has the highest betweenness centrality — they bridge the most sub-clusters. We don't need to ban 487 riders. We find 2–3 coordinator nodes. Remove them and the ring loses its broadcast channel.

**Reference rider pool.** 20–30 long-tenure clean-history riders per zone act as a control group. If the zone claims a disruption but 18 of 25 reference riders are still actively working, the disruption is suspicious regardless of what the rest of the zone shows.

**Adjacent zone comparison.** Real rain hitting Velachery affects neighbouring zones too. Disruption suspiciously contained to exactly one zone with no spillover is unnatural. A ring would need to coordinate across multiple zones simultaneously to beat this check — exponentially harder.

### 9.3 Handling flagged claims without punishing honest riders

Every payout event gets a combined fraud score 0.0–1.0. No auto-block based on a single signal.

| Score | Action | What Rajan sees |
|---|---|---|
| Below 0.40 | Instant payout | ₹420 in GPay within 2 hours. No friction. |
| 0.40 – 0.70 | Pay after 6 hours + passive logging | Payout arrives with slight delay. No message. |
| 0.70 – 0.90 | Hold 24 hours + notify | Tamil WhatsApp: "We're confirming your zone's disruption — your payment will arrive once verified." |
| Above 0.90 | Block + appeal channel | Tamil WhatsApp with one-tap appeal. Human reviewer within 4 hours. |

No silent denials. Ever.

**Ring exclusion, not zone exclusion.** When the GNN identifies a fraud ring of 487 riders within a zone of 500, we block only the 487 ring nodes. The 13 honest riders still get paid. We never block an entire zone because a ring operated there.

**The genuine network drop problem.** A rider with bad GPS signal in heavy rain will have higher jitter (looks MORE like a real rider), NavIC data that still roughly confirms their location, normal accelerometer movement, normal inactivity timing relative to peers, and no appearance in a dense subgraph with 486 others. A bad connection in rain creates none of the fraud signals. The fraud constellation — jitter = 0.0, NavIC mismatch, home Wi-Fi in beacon log, synchronized inactivity with hundreds — is too specific to appear from a dropped signal.

**Tenure-weighted trust.** A rider with 3 years on the platform and 150 clean payouts gets benefit of the doubt at moderate fraud scores. Long positive history counts.

**The human override.** ML is the first responder. A human is the court of appeal. Any payout held above 0.70 triggers a human review queue. The reviewer sees the full picture — rider history, signals that fired, reference pool status, NavIC score. For a rider like Rajan with 3 years of clean history, a human reviewer overrides a moderate ML flag in under 10 minutes. Ambiguity defaults to paying the rider.

This is not a weakness. It is the ethical firewall that prevents fraud detection from becoming an injustice machine.

---

The Seven Principles of Our Defense

1. **GPS is not ground truth.** Cross-validate with NavIC, cell towers, and Wi-Fi beacons. Any single signal is spoofable. All four simultaneously are not.

2. **The ring's tell is in the timing.** Real disruptions stagger (σ = 18–35 min). Telegram broadcasts synchronise (σ = 2–4 min). Low σ + high inactivity = ring investigation.

3. **The peer-cohort model can be weaponised.** 100% synchronised inactivity with a 3-minute standard deviation is statistically impossible in nature. Recalibrate: high inactivity + low timing variance = ring flag, not legitimacy confirmation.

4. **Fraud hides in edges, not nodes.** A dense subgraph of riders sharing device IDs, IP subnets, and GPS jitter scores of exactly 0.0 is the ring's fingerprint.

5. **Find three coordinators, not 487 riders.** Betweenness centrality identifies the ring leader. Remove the coordinator and the ring collapses.

6. **A false positive on an honest rider is a product failure.** Rajan losing ₹420 he deserved during a cyclone is not a fraud prevention success — it is a betrayal. Design to err toward paying honest riders.

7. **The human override is not optional.** ML is fast but fallible. Ambiguity defaults to paying the rider. The 4-hour human review SLA is a product commitment.

---

