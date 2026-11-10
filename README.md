<div align="center">

# Datababy

**360-degree behavioral assessment platform for leadership and professional development, built for enterprise HR and L&D teams.**

[![Live](https://img.shields.io/badge/Live-datababy.io-0d1117?style=for-the-badge&logo=vercel&logoColor=white)](https://datababy.io)
![Client project](https://img.shields.io/badge/Client%20project-built%20end%20to%20end-0d1117?style=for-the-badge)

![Datababy product screens](screenshots/cover.png)

</div>

> This is a showcase repo. Datababy is a client product and its source code is private, so this page covers what it does, how it's built and what it looks like. Happy to walk through the work on a call.

## The problem

Traditional personality frameworks like DISC or Myers-Briggs box people into fixed types. Leadership and L&D teams get a static label instead of a real picture of how someone behaves under pressure, on a team or across contexts, and no clear way to act on it.

## What I built

I built Datababy end to end for the client, from the data model to the UI, payments and AI features.

- **Flexible behavioral polarities** (e.g. Experimental vs Traditional, Candid vs Diplomatic) instead of fixed types
- **360-degree assessments** gathered from peers, managers and teams through shareable survey links
- **Personal reports** mapping each person's pattern across self, leadership, team and cross-functional contexts
- **Rigidity flags** that highlight patterns likely to cause friction or burnout, plus complementary team pairings
- **AI coach**: chat with an AI version of yourself, role-play training scenarios and relationship chats, grounded in the person's own results
- **Subscriptions and payments** with Stripe, transactional email with Resend
- **An Assess, Train, Re-measure cycle** delivered through team cohorts, 1:1 coaching and AI simulation training

## Screenshots

| Report | Profile |
| --- | --- |
| ![Report](screenshots/report.png) | ![Profile](screenshots/profile.png) |

| Aura breakdown | AI coach |
| --- | --- |
| ![Aura](screenshots/aura.png) | ![AI coach](screenshots/ai-coach.png) |

## Architecture

```mermaid
flowchart LR
    U[Employees, managers<br/>and peers] --> W[Next.js app<br/>TypeScript + shadcn/ui]
    W --> DB[(Supabase<br/>Postgres + Auth)]
    W --> AI[OpenAI API<br/>insights and AI coach]
    W --> S[Stripe<br/>subscriptions]
    W --> E[Resend<br/>email]
    S -. webhooks .-> W
```

## Tech stack

![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![shadcn/ui](https://img.shields.io/badge/shadcn%2Fui-000000?style=flat-square&logo=shadcnui&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-635BFF?style=flat-square&logo=stripe&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white)
![Resend](https://img.shields.io/badge/Resend-000000?style=flat-square&logo=resend&logoColor=white)

React Hook Form for the multi-step assessment flows.

## Contact

**Muhammad Izhar** · [izhar.dev](https://izhar.dev) · [LinkedIn](https://linkedin.com/in/izharrr99) · muhammad.izhar11@gmail.com
