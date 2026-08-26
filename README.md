<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0D1117,45:1F6FEB,100:BC8CFF&height=210&section=header&text=HASSAN%20ALI&fontSize=58&fontColor=FFFFFF&fontAlignY=34&desc=db%20schema%20to%20nginx%20config%20%E2%80%94%20same%20person&descAlignY=54&descSize=17&animation=fadeIn" width="100%" alt="Hassan Ali">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=17&duration=2000&pause=500&color=3FB950&background=0D1117&multiline=true&repeat=true&width=820&height=230&lines=%24+git+push+origin+main+--tags;BUILD++++++next.js+%C2%B7+nestjs+%C2%B7+rails+%C2%B7+flask;TEST+++++++214+passed+%C2%B7+0+flaky;ENCRYPT++++phi+columns+sealed+at+rest;DEPLOY+++++ec2+%C2%B7+nginx+%C2%B7+ubuntu+%C2%B7+redis;%E2%9C%93+live+in+42s+%C2%B7+p95+118ms+%C2%B7+i+own+the+pager" alt="deploy pipeline">

<br>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=19&duration=2800&pause=900&color=58A6FF&center=true&vCenter=true&repeat=true&width=820&lines=I+don't+hand+off+at+the+API+boundary.;Rails+%2B+NestJS+%2B+Python+%2B+Next.js+%E2%80%94+one+person%2C+whole+path.;Field-level+encryption+because+audits+are+real.;Offline-first+POS+that+works+with+the+internet+down." alt="what I do">

<br>

<a href="https://caffstack.com"><img src="https://img.shields.io/badge/caffstack.com-0D1117?style=for-the-badge&logo=googlechrome&logoColor=58A6FF&labelColor=0D1117" alt="Website"></a>
<a href="mailto:hassanali.naeem9811@gmail.com"><img src="https://img.shields.io/badge/say_hello-0D1117?style=for-the-badge&logo=gmail&logoColor=F778BA&labelColor=0D1117" alt="Email"></a>
<img src="https://img.shields.io/badge/open_to-full--stack_%2B_infra-0D1117?style=for-the-badge&labelColor=0D1117&color=3FB950" alt="Status">

</div>

<br>

```yaml
# whoami --verbose
role:      full-stack engineer · I write it, deploy it, and get paged for it
languages: [typescript, ruby, python, php]
scope:     schema → service → realtime channel → nginx → ec2 → on-call
bias:      right tool per service, not one stack forced everywhere
```

---

<table>
<tr><td width="50%" valign="top">

### What I own end to end

**Architecture.** Rails 7 API, NestJS services, a Python AI service, and a Next.js frontend — wired over WebSockets and ActionCable so state moves live instead of on refresh. Redis and Sidekiq behind it for anything that shouldn't block a request.

**Security.** RBAC, JWT, rate limiting, and field-level encryption at rest for PHI-grade data. Written to survive an audit, not to pass a demo.

**Infrastructure.** I deploy what I build — EC2, Nginx reverse proxy, Ubuntu, background queues. Nothing gets thrown over a wall.

</td><td width="50%" valign="top">

### What that has shipped

**Realtime platform** — multi-service system with live channels, encrypted columns, and job queues under load.

**Offline-first POS** — Laravel + Inertia + React with IndexedDB sync, barcode scan, thermal print. Keeps selling when the connection drops.

**Commerce** — Next.js 16 + Prisma + Postgres storefronts with NextAuth and Stripe.

**AI products** — OpenAI wired into Next.js and Flask services, not bolted on as a chat box.

</td></tr>
</table>

> Repos live under client and team NDA. I'll walk you through the architecture, the tradeoffs, and the things I'd do differently — on a call.

---

<div align="center">

### The stack, grouped by what it does

<table>
<tr>
<td align="center"><b>Write</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=ts,ruby,python,php&theme=dark"><img src="https://skillicons.dev/icons?i=ts,ruby,python,php&theme=light" alt="languages"></picture>
</td>
<td align="center"><b>Serve</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=nestjs,rails,laravel,flask&theme=dark"><img src="https://skillicons.dev/icons?i=nestjs,rails,laravel,flask&theme=light" alt="backend"></picture>
</td>
<td align="center"><b>Ship</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=nextjs,react,tailwind,vite&theme=dark"><img src="https://skillicons.dev/icons?i=nextjs,react,tailwind,vite&theme=light" alt="frontend"></picture>
</td>
</tr>
<tr>
<td align="center"><b>Store</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=postgres,mongodb,redis,prisma&theme=dark"><img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,prisma&theme=light" alt="data"></picture>
</td>
<td align="center"><b>Run</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=aws,nginx,ubuntu,git&theme=dark"><img src="https://skillicons.dev/icons?i=aws,nginx,ubuntu,git&theme=light" alt="infra"></picture>
</td>
<td align="center"><b>Integrate</b><br><br>
<picture><source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=openai,firebase,stripe,githubactions&theme=dark"><img src="https://skillicons.dev/icons?i=openai,firebase,stripe,githubactions&theme=light" alt="integrations"></picture>
</td>
</tr>
</table>

</div>

---

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=Hassan-html&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&theme=transparent&title_color=58A6FF&text_color=8B949E&icon_color=F778BA" alt="stats">
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Hassan-html&layout=compact&hide_border=true&langs_count=6&theme=transparent&title_color=58A6FF&text_color=8B949E" alt="languages">

<img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=Hassan-html&bg_color=0D1117&color=58A6FF&line=BC8CFF&point=F778BA&area=true&area_color=1F6FEB&hide_border=true&custom_title=Commit%20rhythm" alt="activity graph">

</div>

---

<div align="center">

**`db` → `api` → `edge` → `prod`** — one person, whole path.

Open to full-stack roles where I build the product *and* run the infrastructure.

<a href="mailto:hassanali.naeem9811@gmail.com"><img src="https://img.shields.io/badge/start_a_conversation-58A6FF?style=for-the-badge&logo=maildotru&logoColor=0D1117" alt="Contact"></a>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:BC8CFF,55:1F6FEB,100:0D1117&height=110&section=footer" width="100%" alt="">

</div>
