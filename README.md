# VayuGuard – Parametric Income Protection for Gig Workers

VayuGaurd is a parametric micro-insurance platform designed for gig delivery workers whose income depends on daily activity and weekly incentives.  
During floods, cyclones, extreme heat, protests, or traffic shutdowns, workers may be unable to complete deliveries and lose a significant portion of their weekly earnings.

Traditional insurance cannot verify this type of loss automatically and often requires manual claims, making it slow, expensive, and vulnerable to fraud.  
RouteShield solves this problem using **multi-signal parametric triggers, behavioral validation, and fraud-resistant trust scoring**, allowing payouts to be processed automatically while protecting the risk pool from coordinated spoofing attacks.

This project was built for the **Guidewire DEVTrails Hackathon** and demonstrates how modern insurance platforms can support real-time, API-driven, gig-economy-ready products.

---

## Problem Statement

Gig delivery workers earn based on completed orders and incentive slabs rather than fixed salaries.  
A short disruption — such as heavy rain, flooding, or a protest — can prevent them from working long enough to miss their weekly targets.

This leads to:

- Loss of income despite being available to work
- No simple way to prove the loss
- High risk of fraud if payouts are automated
- Difficulty for insurers to maintain pool solvency

The challenge is to design an insurance system that is:

- Automatic
- Fraud-resistant
- Scalable
- Compatible with real insurance workflows

---

## Persona – The 10-Minute Stakeholder

Arpit is a 23-year-old delivery partner working for a quick-commerce platform.  
He operates within a small delivery radius and earns weekly incentives based on completed orders.

If heavy rain stops work for a few hours, he may fail to reach his incentive slab and lose a large part of his weekly income.

Arpit needs:

- No paperwork
- Weekly coverage
- Fast payouts
- No manual claims
- Low premium

RouteShield provides a **zero-click income protection system aligned with gig-worker cash flow.**

---

## System Architecture

The platform follows a modular design similar to real insurance core systems.

### Engines

- **Policy Engine**  
  Manages weekly coverage cycles, renewals, and worker enrollment.

- **Risk Engine**  
  Calculates premium using zone risk, worker history, and disruption probability.

- **Event Engine**  
  Monitors parametric signals such as weather alerts and delivery activity.

- **Fraud Engine**  
  Validates claims using multi-signal trust scoring.

- **Claims Engine**  
  Processes automated payouts when trigger conditions are met.

- **Dashboard**  
  Shows analytics for workers, platforms, and insurers.

### Flow

Worker → Policy → Event Detection → Fraud Check → Claim → Payout

This modular architecture allows easy integration with real insurance systems.

---

## Guidewire Alignment

The design follows Guidewire-style insurance architecture.

| RouteShield Component | Guidewire Equivalent |
|-----------------------|----------------------|
| Policy Engine | PolicyCenter |
| Claims Engine | ClaimCenter |
| Risk Engine | Rating / Underwriting |
| Event Engine | External Oracle Integration |
| Fraud Engine | SIU / Rules Engine |
| Dashboard | Portal / Analytics |

This makes the system compatible with real insurer workflows.

---

## Financial Model

RouteShield uses a semi-dynamic parametric pricing model.

Base premium: ₹50 per week  
AI-adjusted range: ₹40 – ₹65 per week

Split model:

- Worker contribution: ₹35
- Platform subsidy: ₹5 – ₹30
- Risk pool: remaining amount

Expected loss formula:

Expected payout = Weekly income × disruption probability × loss percentage

Example:

₹5000 × 0.10 × 0.40 = ₹200 expected loss

This allows sustainable payouts while keeping premiums affordable.

---

## Multi-Signal Parametric Trigger

A payout is triggered only when all conditions are true.

1. Weather severity threshold crossed  
   Example: heavy rain, cyclone, extreme heat

2. Delivery activity drop in the zone  
   Example: ≥30% drop in successful orders

3. Worker inactivity anomaly  
   Worker is usually active but unable to work during event

This prevents payouts for:

- Normal slow days
- Personal breaks
- Fake location claims

---

## Adversarial Defense & Anti-Spoofing

GPS spoofing can be used to fake presence in disaster zones.  
To prevent fraud, RouteShield uses a multi-layer trust system.

### Layer 1 — Motion Validation

Accelerometer / gyroscope data confirms real movement.

### Layer 2 — Hyperlocal Consensus

Compare signals with nearby workers.

Fake clusters are detected.

### Layer 3 — Behavioral Intelligence

Check order history, activity pattern, and timing.

### Layer 4 — Economic Consistency

Claim must match historical earnings.

### Trust Score

High score → instant payout  
Medium score → verification  
Low score → manual review

Goal:

Make fraud economically impossible at scale.

---

## Liquidity Protection

To prevent mass fraud draining the pool:

- Zone payout limit
- Circuit breaker on high claim rate
- Cluster detection
- Blacklist memory for fraud devices

These ensure the system remains solvent.

---

## Demo Flow (Hackathon Prototype)

1. Worker buys weekly policy
2. Weather event triggered
3. Delivery activity drops
4. Fraud engine checks signals
5. Trust score calculated
6. Claim approved automatically
7. Payout generated

Prototype uses mock APIs for weather and delivery data.

---

## Why This Works

- Matches gig-worker income pattern
- No manual claims
- Fraud resistant
- Realistic insurance architecture
- Compatible with Guidewire
- Scalable to real deployment

RouteShield shows how insurance can become:

Real-time  
Parametric  
Fraud-resistant  
API-driven  
Gig-economy ready

---

## Future Scope

- Real platform API integration
- Reinsurance support
- Federated trust scoring
- DigiLocker identity link
- Full Guidewire integration
