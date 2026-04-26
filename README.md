# SubSignal

> Churn early-warning for SaaS founders. A weekly email digest — no dashboard, no complexity.

🌐 **Live:** [sub-signal.com](https://sub-signal.com)

---

## The problem

Most SaaS founders discover churn after it happens — a cancellation email, a failed renewal, a card decline. By then it's too late. The signals were there weeks earlier: a user who stopped logging in, a team that quietly dropped a core feature, an account that hasn't touched the product in 21 days.

SubSignal catches those signals and sends you a plain weekly email listing exactly which customers are at risk, why, and what to do next. You don't check a dashboard. It comes to you.

---

## Who it's for

SaaS founders at £1k–20k MRR who are close enough to their customers to act on early warnings, but too busy to monitor usage data manually.

---

## How it works

1. Drop one JavaScript snippet into your app
2. Connect your Stripe account
3. Set your own thresholds (login frequency, feature usage, days inactive)
4. Receive a weekly email digest every Monday morning

No dashboards. No AI-generated summaries. No complex scoring models. Just specific, actionable signals from your own data.

---

## Tech stack

| Layer | Technology |
|---|---|
| Frontend | React |
| Backend | Node.js / Express |
| Database | PostgreSQL |
| Payments | Stripe (webhooks + subscription events) |
| Tracking | Custom JS snippet (login frequency, feature usage) |
| Email | Weekly digest via transactional email |
| Auth | Clerk |

---

## Key technical decisions

**No dashboard by design.** The product sends email rather than requiring log-in. This isn't a limitation — it's the core product decision. Founders already have too many tools to check. SubSignal works invisibly in the background and interrupts only when something needs attention.

**Customer-defined thresholds.** Rather than a proprietary churn score, founders set their own rules: "alert me if a customer hasn't logged in for 14 days" or "flag if core feature usage drops below 3 times a week." This makes alerts meaningful rather than algorithmic noise.

**Stripe + behaviour signals combined.** Payment events alone are lagging indicators. Combining Stripe webhook data with in-app behaviour gives a 2–4 week earlier warning window before financial churn occurs.

**Free tier up to 10 customers.** No credit card required for the free tier. Conversion happens naturally when the product is genuinely useful and the customer count grows past the free limit.

---

## Pricing

| Plan | Price | Limit |
|---|---|---|
| Free | £0 | Up to 10 customers |
| Founding | £29/mo | First 50 subscribers — locked forever |
| Standard | £49/mo | Unlimited |

---

## Status

Live since April 2026. Actively developed.
