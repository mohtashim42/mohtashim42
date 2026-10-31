<!-- ============================================================
     GitHub Profile README — Muhammad Mohtashim
     Place this file in a public repo named exactly: mohtashim42
     ============================================================ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,14,18,20&height=230&section=header&text=Muhammad%20Mohtashim&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=36&desc=Software%20Engineer%20%E2%80%A2%20Full%20Stack%20%26%20AI%20Engineer&descAlignY=58&descSize=18" alt="Header" width="100%"/>

<a href="https://github.com/mohtashim42">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&duration=3200&pause=1000&color=58A6FF&center=true&vCenter=true&width=760&lines=Building+production-grade+web+platforms;Designing+multi-LLM+gateways+%26+AI+workflows;Shipping+enterprise+microservices+at+scale;15%2B+platforms+delivered+%7C+5%E2%98%85+Upwork+rating" alt="Typing animation" />
</a>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-themohtashimafzal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/themohtashimafzal)
[![Email](https://img.shields.io/badge/Email-Contact%20Me-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mohtashimbhatti425@gmail.com)
[![Upwork](https://img.shields.io/badge/Upwork-Top%20Rated-14A800?style=for-the-badge&logo=upwork&logoColor=white)](https://www.upwork.com)
[![Profile Views](https://komarev.com/ghpvc/?username=mohtashim42&label=Profile%20Views&color=7C3AED&style=for-the-badge)](https://github.com/mohtashim42)

</div>

---

## 👨‍💻 About Me

I am a **Software Engineer with 3+ years of experience** building web applications, enterprise microservices, and multi-model AI integrations. My work spans the JavaScript/TypeScript and Python ecosystems, and I have delivered **over 15 production e-commerce platforms and SaaS systems**, with a consistent focus on clean code, efficient database design, and high API performance.

```ts
const mohtashim = {
  role:      "Software Engineer — Full Stack & AI",
  currently: "Software Engineer @ Rajco Industries",
  location:  "Pakistan 🇵🇰",
  education: "BS Computer Science — University of Sialkot",
  focus:     ["Full Stack Systems", "LLM Orchestration", "Enterprise Microservices"],
  freelance: "Upwork Top-Rated • 5★ • 100% Client Satisfaction",
  openTo:    ["Remote roles", "Technical collaboration", "Freelance engagements"],
};
```

---

## 📊 At a Glance

<div align="center">

| 🚀 **15+** | ⏱️ **3+ Years** | ⚡ **< 200ms** | 🤖 **9 LLMs** | ⭐ **5.0** |
|:---:|:---:|:---:|:---:|:---:|
| Production platforms shipped | Professional experience | Response time on core endpoints | Orchestrated concurrently | Upwork rating |

</div>

---

## 🧰 Technology Stack

<div align="center">

**Languages & Backend**

<img src="https://skillicons.dev/icons?i=js,ts,python,nodejs,express,nestjs,fastapi,flask&perline=8" alt="Backend stack"/>

**Frontend & Mobile**

<img src="https://skillicons.dev/icons?i=react,nextjs,tailwind,redux,materialui,html,css&perline=8" alt="Frontend stack"/>

**Databases, Cloud & DevOps**

<img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,supabase,docker,aws,vercel,git,github&perline=9" alt="Infra stack"/>

</div>

<details>
<summary><b>📚 Full competency overview</b></summary>
<br/>

| Domain | Expertise |
|---|---|
| **Engineering** | System Design, REST APIs, Microservices, E-Commerce Systems |
| **AI & Integration** | LLM API Integration (OpenAI, Gemini, Claude), Multi-LLM Orchestration, SSE Streaming, Async Fan-out, RAG, LangChain, WhatsApp AI Integration |
| **Frontend & Mobile** | React.js, Next.js, React Native (Expo), Redux Toolkit, Zustand, Shadcn UI, Material-UI |
| **Data** | PostgreSQL, MongoDB, Oracle DB, SQL Server, Redis, Supabase |
| **Real-Time** | WebSockets (Socket.io), Redis Pub/Sub |
| **DevOps** | Docker, CI/CD, AWS (EC2, S3), Vercel, Render |

</details>

---

## 🚀 Featured Projects

### 🧠 Orchestrator AI — Multi-LLM Gateway & Evaluation System
> A high-throughput AI gateway that fans a single prompt out to **9 LLM providers concurrently** and uses a 10th model as an impartial judge.

`FastAPI` `Python` `asyncio` `SSE Streaming` `React`

- Dispatches prompts concurrently to GPT-4o, Claude, Gemini, Grok, DeepSeek, and other providers using `asyncio.gather`.
- Normalizes per-provider metrics (latency, token usage, cost) into a unified log.
- Employs a dedicated **Judge model** to score responses and synthesize a final answer, streamed live to a React dashboard via Server-Sent Events.

```mermaid
flowchart LR
    U([User Prompt]) --> G{{FastAPI Gateway}}
    G -->|asyncio.gather| L1[GPT-4o]
    G --> L2[Claude]
    G --> L3[Gemini]
    G --> L4[Grok]
    G --> L5[DeepSeek]
    G --> L6[+ 4 more]
    L1 & L2 & L3 & L4 & L5 & L6 --> N[Normalization Pipeline<br/>latency • tokens • cost]
    N --> J[[LLM Judge<br/>Score & Synthesize]]
    J -->|SSE Stream| D([React Dashboard])
```

📁 **Repository:** [`mohtashim42/orchestrator-ai`](https://github.com/mohtashim42/orchestrator-ai)

---

### 💬 Rajco AI Data Assistant — WhatsApp AI Bot & Enterprise BI System
> A conversational business-intelligence layer that allows internal teams to query live operational data in plain English through WhatsApp.

`FastAPI` `Node.js` `LangChain` `WhatsApp Business API` `Oracle DB` `MongoDB`

- Converts natural-language prompts into SQL and MongoDB aggregation queries through **secure, injection-resistant pipelines**.
- Delivers scheduled daily production summaries and critical inventory alerts to executives automatically.
- Uses asynchronous webhooks to return multi-format responses, including dynamic text reports and PDF exports.

```mermaid
sequenceDiagram
    participant U as Team Member
    participant W as WhatsApp Business API
    participant F as FastAPI Webhook
    participant A as LangChain Pipeline
    participant D as Oracle DB / MongoDB
    U->>W: "Show today's inventory status"
    W->>F: Async webhook event
    F->>A: Validate & transform to query
    A->>D: Parameterized SQL / Aggregation
    D-->>A: Result set
    A-->>F: Formatted report
    F-->>U: Text summary or PDF export
```

📁 **Repository:** [`mohtashim42/rajco-ai-assistant`](https://github.com/mohtashim42/rajco-ai-assistant)

---

### 🛒 Cerova — Kitchen & Home Accessories E-Commerce Platform
> A complete multi-interface commerce solution covering the storefront, administration, and client management.

`Next.js` `React` `TypeScript` `Node.js` `Express` `MongoDB` `Tailwind CSS` `Docker`

- Delivers three tailored interfaces: **Admin Dashboard**, **Customer Storefront**, and **Client Portal**.
- Implements product catalog management, order processing, inventory tracking, and payment gateway integration.

📁 **Repository:** [`mohtashim42/cerova`](https://github.com/mohtashim42/cerova)

---

### 📱 Enterprise Production Planning App — React Native
> A mobile application for order tracking and factory production planning with hands-free voice controls.

`React Native` `React Native Voice` `Node.js` `NestJS` `Oracle DB`

- Introduced voice-driven input, **reducing manual data-entry time by 35%**.
- Backed by secure services featuring JWT authentication and role-based access control.

> 🔒 *Developed for Rajco Industries; source code is proprietary.*

---

## 💼 Professional Experience

<table>
<tr>
<td width="140"><b>Aug 2025 — Present</b></td>
<td>

**Software Engineer** · *Rajco Industries*<br/>
Built Rajco AI (internal LLM system and WhatsApp bot), a voice-enabled React Native app, and full-stack services with NestJS and FastAPI. Authored optimized SQL and aggregation pipelines on Oracle DB for daily executive reporting.

</td>
</tr>
<tr>
<td><b>Jul 2023 — Sep 2025</b></td>
<td>

**MERN Stack Developer** · *SyncOps*<br/>
Developed REST APIs and microservices with sub-200ms core response times, real-time messaging with Socket.io and Redis, LLM-powered data extraction workflows, and Dockerized deployments on AWS, Vercel, and Render.

</td>
</tr>
<tr>
<td><b>Aug 2021 — Present</b></td>
<td>

**Software Engineer & Full Stack Developer** · *Upwork (Top-Rated)*<br/>
Delivered end-to-end web applications, e-commerce stores, and client portals while maintaining a 5-star rating and 100% client satisfaction.

</td>
</tr>
</table>

---

## 📈 GitHub Analytics

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=mohtashim42&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&rank_icon=github" alt="GitHub Stats"/>
<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=mohtashim42&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages"/>

<br/>

<img src="https://streak-stats.demolab.com/?user=mohtashim42&theme=tokyonight&hide_border=true" alt="GitHub Streak"/>

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=mohtashim42&theme=tokyo-night&hide_border=true&area=true" alt="Contribution Activity" width="95%"/>

</div>

---

## 🎯 Engineering Principles

- **Clean, maintainable code** — readable systems outlast clever ones.
- **Performance by design** — efficient schemas and lean APIs from the first commit.
- **Security first** — authentication, access control, and injection-safe data layers as defaults.
- **Production mindset** — containerized, deployed, and monitored, not merely demonstrated.

---

## 🤝 Let's Connect

I welcome conversations about full-stack engineering, AI integration, and impactful product development. Whether it is a full-time opportunity, a freelance engagement, or a technical collaboration, feel free to reach out.

<div align="center">

[![LinkedIn](https://img.shields.io/badge/Connect%20on-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/themohtashimafzal)
[![Email](https://img.shields.io/badge/Send-an%20Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mohtashimbhatti425@gmail.com)

<br/>

<i>“Engineering reliable systems, one commit at a time.”</i>

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=12,14,18,20&height=120&section=footer" alt="Footer" width="100%"/>

</div>
