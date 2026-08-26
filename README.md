<div align="center">

```
 ███████╗████████╗ █████╗  ██████╗██╗  ██╗███████╗██████╗ 
 ██╔════╝╚══██╔══╝██╔══██╗██╔════╝██║  ██║██╔════╝██╔══██╗
 ███████╗   ██║   ███████║██║     ███████║█████╗  ██║  ██║
 ╚════██║   ██║   ██╔══██║██║     ██╔══██║██╔══╝  ██║  ██║
 ███████║   ██║   ██║  ██║╚██████╗██║  ██║███████╗██████╔╝
 ╚══════╝   ╚═╝   ╚═╝  ╚═╝ ╚═════╝╚═╝  ╚═╝╚══════╝╚═════╝ 
```

<svg width="100%" viewBox="0 0 800 200" xmlns="http://www.w3.org/2000/svg" style="max-width: 100%; height: auto; margin: 20px 0;">
  <defs>
    <style>
      @keyframes draw {
        from { stroke-dashoffset: 1000; }
        to { stroke-dashoffset: 0; }
      }
      @keyframes pulse {
        0%, 100% { opacity: 0.6; }
        50% { opacity: 1; }
      }
      @keyframes float {
        0%, 100% { transform: translateY(0px); }
        50% { transform: translateY(-8px); }
      }
      @keyframes scan {
        0% { x: -800; }
        100% { x: 800; }
      }
      
      .code-line { stroke-dasharray: 1000; animation: draw 2s ease-in-out forwards; }
      .line1 { animation-delay: 0s; }
      .line2 { animation-delay: 0.3s; }
      .line3 { animation-delay: 0.6s; }
      .line4 { animation-delay: 0.9s; }
      
      .tech-icon { animation: float 3s ease-in-out infinite; }
      .icon1 { animation-delay: 0s; }
      .icon2 { animation-delay: 0.3s; }
      .icon3 { animation-delay: 0.6s; }
      .icon4 { animation-delay: 0.9s; }
      
      .pulse-dot { animation: pulse 1.5s ease-in-out infinite; }
      .dot1 { animation-delay: 0s; }
      .dot2 { animation-delay: 0.2s; }
      .dot3 { animation-delay: 0.4s; }
      
      .scan-line { animation: scan 3s linear infinite; opacity: 0.3; }
    </style>
    
    <linearGradient id="gradBG" x1="0%" y1="0%" x2="100%" y2="100%">
      <stop offset="0%" style="stop-color:#0F172A;stop-opacity:1" />
      <stop offset="100%" style="stop-color:#1E293B;stop-opacity:1" />
    </linearGradient>
  </defs>
  
  <!-- Background -->
  <rect width="800" height="200" fill="url(#gradBG)"/>
  
  <!-- Grid background -->
  <defs>
    <pattern id="grid" width="40" height="40" patternUnits="userSpaceOnUse">
      <path d="M 40 0 L 0 0 0 40" fill="none" stroke="#64748B" stroke-width="0.5" opacity="0.1"/>
    </pattern>
  </defs>
  <rect width="800" height="200" fill="url(#grid)" />
  
  <!-- Scan line effect -->
  <rect class="scan-line" width="40" height="200" fill="url(#gradBG)" opacity="0.2"/>
  
  <!-- Code blocks (left) -->
  <text x="40" y="50" font-family="'Courier New', monospace" font-size="14" fill="#22C55E" font-weight="bold">const stack =</text>
  
  <path class="code-line line1" d="M 50 70 Q 100 70 150 70" stroke="#3B82F6" stroke-width="2" fill="none"/>
  <text x="50" y="68" font-family="'Courier New', monospace" font-size="12" fill="#94A3B8">{'{'}</text>
  
  <path class="code-line line2" d="M 60 90 Q 120 90 180 90" stroke="#8B5CF6" stroke-width="2" fill="none"/>
  <text x="60" y="88" font-family="'Courier New', monospace" font-size="11" fill="#CBD5E1">backend: NestJS, Rails</text>
  
  <path class="code-line line3" d="M 60 110 Q 140 110 200 110" stroke="#EC4899" stroke-width="2" fill="none"/>
  <text x="60" y="108" font-family="'Courier New', monospace" font-size="11" fill="#CBD5E1">frontend: Next.js, React</text>
  
  <path class="code-line line4" d="M 60 130 Q 130 130 190 130" stroke="#F59E0B" stroke-width="2" fill="none"/>
  <text x="60" y="128" font-family="'Courier New', monospace" font-size="11" fill="#CBD5E1">data: PostgreSQL, Redis</text>
  
  <text x="50" y="155" font-family="'Courier New', monospace" font-size="12" fill="#94A3B8">{'}'};</text>
  
  <!-- Tech stack icons (right) -->
  <g class="tech-icon icon1">
    <circle cx="520" cy="50" r="20" fill="#3B82F6" opacity="0.2"/>
    <text x="510" y="60" font-size="24">⚙️</text>
  </g>
  
  <g class="tech-icon icon2">
    <circle cx="600" cy="80" r="20" fill="#8B5CF6" opacity="0.2"/>
    <text x="590" y="90" font-size="24">🚀</text>
  </g>
  
  <g class="tech-icon icon3">
    <circle cx="680" cy="60" r="20" fill="#EC4899" opacity="0.2"/>
    <text x="670" y="70" font-size="24">💻</text>
  </g>
  
  <g class="tech-icon icon4">
    <circle cx="740" cy="110" r="20" fill="#F59E0B" opacity="0.2"/>
    <text x="730" y="120" font-size="24">🔒</text>
  </g>
  
  <!-- Status indicator -->
  <circle class="pulse-dot dot1" cx="580" cy="150" r="4" fill="#22C55E"/>
  <circle class="pulse-dot dot2" cx="600" cy="150" r="4" fill="#22C55E"/>
  <circle class="pulse-dot dot3" cx="620" cy="150" r="4" fill="#22C55E"/>
  <text x="500" y="175" font-family="'Courier New', monospace" font-size="12" fill="#22C55E">// production ready</text>
</svg>

# Hassan Ali

**Full-Stack Software Engineer** · Polyglot · Production Systems

<p>
  <a href="mailto:hassanali.naeem9811@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://caffstack.com"><img src="https://img.shields.io/badge/Website-0A0A0A?style=for-the-badge&logo=googlechrome&logoColor=white" alt="Website"></a>
</p>

</div>

---

## About me

I own features from database to production. Full-stack across **multiple languages and stacks** — TypeScript, Ruby, Python, PHP. I build and operate production systems on AWS, Nginx, Ubuntu.

### What I do

- **Microservice architectures** — Rails APIs + NestJS services + Python backends + Next.js frontends, wired with WebSockets and realtime channels
- **E-commerce & POS** — headless storefronts, offline-first systems, full-stack checkout flows
- **Security-first** — RBAC, JWT auth, rate limiting, field-level encryption (HIPAA-aware)
- **Owned infrastructure** — EC2, S3, Nginx, Redis, background jobs, CI/CD

---

## Tech Stack

### Languages
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Ruby](https://img.shields.io/badge/Ruby-CC342D?style=flat-square&logo=ruby&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=flat-square&logo=php&logoColor=white)

### Frontend
![Next.js](https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=next.js&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=black)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)

### Backend
![NestJS](https://img.shields.io/badge/Nest.js-E0234E?style=flat-square&logo=nestjs&logoColor=white)
![Rails](https://img.shields.io/badge/Ruby_on_Rails-CC0000?style=flat-square&logo=rubyonrails&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=flat-square&logo=express&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)

### Data & Infrastructure
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=white)

---

## What I've built

- **Realtime microservices** — Rails + NestJS + Python + Next.js with WebSockets, RBAC, field-level encryption
- **E-commerce platforms** — Next.js storefronts with offline-first POS (IndexedDB, barcode, thermal print)
- **AI integrations** — OpenAI-powered chat and automation in Next.js and Flask
- **Headless CMS & ERP** — Laravel + Livewire content systems and business tooling
- **Full-stack apps** — multi-language sites, NextAuth dashboards, Express + Prisma backends

*Repos private under client confidentiality. Architecture & code decisions on request.*

---

## At a glance

| Area | Stack |
|---|---|
| **Backend** | Rails · NestJS · Express · Flask · Laravel |
| **Frontend** | Next.js · React · React Native · Inertia · Livewire |
| **Data** | PostgreSQL · MongoDB · Redis · Sidekiq · Prisma |
| **Realtime** | WebSockets · Socket.IO · ActionCable |
| **AI & payments** | OpenAI API · Stripe · Firebase |
| **Cloud & infra** | AWS (EC2, S3) · Nginx · Ubuntu · Git |
| **Security** | RBAC · JWT · rate limiting · field encryption |

---

<div align="center">

**Full-stack engineer who builds the product and runs the infrastructure.**

</div>
