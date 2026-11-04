<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=26&duration=3200&pause=900&color=2563EB&center=true&vCenter=true&width=720&lines=Hi%2C+I'm+Hassan+Ali;I+build+products+end+to+end;Next.js+%C2%B7+NestJS+%C2%B7+React+Native;From+the+database+to+the+App+Store" alt="Hi, I'm Hassan Ali" />

**Full-stack engineer from Sialkot, Pakistan.** I design it, build it, ship it and keep it running in production.

<a href="https://caffstack.com"><img src="https://img.shields.io/badge/caffstack.com-0A0A0A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website"></a>
<a href="https://talkwhy.com"><img src="https://img.shields.io/badge/talkwhy.com-2563EB?style=for-the-badge&logo=whatsapp&logoColor=white" alt="TalkWhy"></a>
<a href="https://www.upwork.com/freelancers/~01cfc6dacd367edf38"><img src="https://img.shields.io/badge/Upwork-14A800?style=for-the-badge&logo=upwork&logoColor=white" alt="Upwork"></a>
<a href="mailto:hassanali.naeem9811@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<!-- <a href="https://www.linkedin.com/in/hassan-ali-4abb39222/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a> -->

</div>

---

## Now shipping

### TalkWhy — the WhatsApp Business inbox for teams
**[talkwhy.com](https://talkwhy.com)** · web app + Android app (iOS coming) · live in production

One shared WhatsApp number, a whole team answering it, and an AI that handles the easy questions.

| | |
|---|---|
| **Shared team inbox** | Assignment, statuses, tags, contact lists, 24-hour-window aware composer, real-time sync across web and phone |
| **AI agent** | Assistant trained on each business's website and documents, auto-replies, translation both ways |
| **Templates & broadcasts** | Meta template builder with media headers, scheduled and recurring broadcasts, delivery tracking |
| **Mobile app** | React Native (Expo) with push notifications, voice notes, media, and the full inbox in your pocket |
| **Help desk** | Built-in support tickets with screenshots, SLA timers, internal notes and per-user blocking |
| **Platform** | Team roles and fine-grained permissions, public REST API with scoped keys, subscriptions and billing |

```mermaid
flowchart LR
    WA[WhatsApp Cloud API] -- webhooks --> API[Next.js 16 · server actions + REST]
    API --> DB[(PostgreSQL · Prisma)]
    API -- events --> WS[WebSocket server]
    WS --> WEB[Web inbox]
    WS --> APP[React Native app]
    API -- push --> PUSH[Expo · FCM / APNs] --> APP
    API <--> AI[OpenAI assistants + knowledge base]
    API -- send --> WA
```

### CaffStack
**[caffstack.com](https://caffstack.com)** · where I write about and teach the stack I use every day.

---

## How I work

- **Own the whole path.** Schema, API, UI, mobile, deploys, monitoring — one person, no hand-off gaps.
- **Run what I build.** Ubuntu + Nginx + PM2 clusters on AWS, zero-downtime reloads, live debugging from logs and the database.
- **Security is a feature.** RBAC, scoped API keys, rate limits, content-checked uploads, field-level encryption where data is sensitive.
- **Real-time by default.** WebSockets and push so screens never need a refresh.

---

## Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=ts,js,nextjs,react,nestjs,nodejs,express,prisma,postgres,mongodb,redis&perline=11" alt="Core stack" />
  <br/>
  <img src="https://skillicons.dev/icons?i=rails,ruby,laravel,php,python,flask,tailwind,vite,aws,nginx,ubuntu&perline=11" alt="More stack" />
</p>

| Area | Tools |
|---|---|
| **Web** | Next.js · React · Tailwind · Zustand · Inertia · Livewire |
| **Mobile** | React Native · Expo · EAS · push notifications |
| **Backend** | NestJS · Node/Express · Ruby on Rails · Laravel · Flask |
| **Data** | PostgreSQL · Prisma · MongoDB · Redis · Sidekiq |
| **Real-time** | WebSockets · Socket.IO · ActionCable |
| **AI & APIs** | OpenAI · WhatsApp Cloud API · Firebase · Stripe · Paymob |
| **Infra** | AWS (EC2, S3) · Nginx · PM2 · Cloudflare · Ubuntu |

---

## Also built

- **Real-time microservices platform** — Rails API, NestJS services, a Python AI service and a Next.js front end over WebSockets, with RBAC, background jobs and encrypted sensitive fields.
- **Offline-first point of sale** — Laravel + Inertia + React with IndexedDB sync, barcode scanning and thermal printing.
- **E-commerce storefronts** — Next.js + Prisma + PostgreSQL with auth, admin panels and payments.
- **CMS, ERP and internal tools** — content platforms on Laravel + Livewire, accounting and admin systems.

<sub>Most client work lives in private repositories. Happy to walk through architecture and code on request.</sub>

---

<div align="center">

**Open to building products where I own the stack from database to production.**

<a href="mailto:hassanali.naeem9811@gmail.com">hassanali.naeem9811@gmail.com</a>

</div>
