<h1 align="center">Trần Thanh Bình</h1>
<p align="center">
  <em>Backend Engineer — I build systems that stay correct under pressure.</em>
</p>

<p align="center">
  <a href="https://tb-portfolio.bian.io.vn"><img src="https://img.shields.io/badge/Portfolio-ttb.dev-6366f1?style=flat-square&labelColor=0f0f1a" /></a>
  <a href="mailto:trbinh.dev@gmail.com"><img src="https://img.shields.io/badge/Email-trbinh.dev@gmail.com-818cf8?style=flat-square&labelColor=0f0f1a&logo=gmail&logoColor=818cf8" /></a>
  <img src="https://img.shields.io/badge/Hanoi-Vietnam-52526e?style=flat-square&labelColor=0f0f1a&logo=googlemaps&logoColor=52526e" />
  <img src="https://komarev.com/ghpvc/?username=TrBinhDev&style=flat-square&color=6366f1&label=views" />
</p>

---

### `01` — Who I am

| | |
|:--|:--|
| **Role** | Backend Engineer |
| **Education** | B.Eng. Information Technology, Hanoi University of Architecture · 2022–2027 |
| **Focus** | Distributed systems, event-driven architecture, API design |
| **Based in** | Hanoi, Vietnam |

---

### `02` — About

Backend engineer working in Node.js and TypeScript, focused on building
systems that stay correct under concurrent load.

Across my projects I've worked with:

- **Microservices** — service boundaries, database-per-service, API gateway
- **Idempotency** — duplicate request handling on retries and double-submits
- **Locking** — optimistic and pessimistic locking depending on write contention
- **Transactions** — atomic multi-step writes, event-driven compensation across services
- **Race conditions** — overselling prevention via atomic conditional updates
- **Kafka** — async workflows, decoupling services from blocking responses
- **Docker & CI/CD** — containerized services, automated build and image publishing

---

### `03` — Tech Stack

**Core**

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white&labelColor=0f0f1a)
![Node.js](https://img.shields.io/badge/Node.js-5FA04E?style=flat-square&logo=nodedotjs&logoColor=white&labelColor=0f0f1a)
![Express](https://img.shields.io/badge/Express-eeeeff?style=flat-square&logo=express&logoColor=eeeeff&labelColor=0f0f1a)
![REST APIs](https://img.shields.io/badge/REST_APIs-818cf8?style=flat-square&logo=fastapi&logoColor=818cf8&labelColor=0f0f1a)

**Data & Messaging**

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white&labelColor=0f0f1a)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white&labelColor=0f0f1a)
![Kafka](https://img.shields.io/badge/Apache_Kafka-eeeeff?style=flat-square&logo=apachekafka&logoColor=eeeeff&labelColor=0f0f1a)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white&labelColor=0f0f1a)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white&labelColor=0f0f1a)

**Infrastructure**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white&labelColor=0f0f1a)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white&labelColor=0f0f1a)
![Cloudflare](https://img.shields.io/badge/Cloudflare_R2-F38020?style=flat-square&logo=cloudflare&logoColor=white&labelColor=0f0f1a)
![Socket.io](https://img.shields.io/badge/Socket.io-eeeeff?style=flat-square&logo=socketdotio&logoColor=eeeeff&labelColor=0f0f1a)

**Supporting**

![Next.js](https://img.shields.io/badge/Next.js-eeeeff?style=flat-square&logo=nextdotjs&logoColor=eeeeff&labelColor=0f0f1a)
![React Native](https://img.shields.io/badge/React_Native-61DAFB?style=flat-square&logo=react&logoColor=61DAFB&labelColor=0f0f1a)
![Tailwind](https://img.shields.io/badge/Tailwind-06B6D4?style=flat-square&logo=tailwindcss&logoColor=06B6D4&labelColor=0f0f1a)

---

### `04` — Activity

<div align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=TrBinhDev&show_icons=true&hide_border=true&bg_color=0f0f1a&title_color=6366f1&text_color=a8a8c0&icon_color=818cf8&rank_icon=github&include_all_commits=true&count_private=true" />
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=TrBinhDev&layout=compact&hide_border=true&bg_color=0f0f1a&title_color=6366f1&text_color=a8a8c0&langs_count=6&hide=html,css,scss" />
</div>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=TrBinhDev&bg_color=0f0f1a&color=a8a8c0&title_color=6366f1&line=6366f1&point=818cf8&area=true&hide_border=true&custom_title=Contribution%20Activity" />

---

### `05` — How I build

```mermaid
flowchart LR
    Client([Client]) --> GW[API Gateway]
    GW --> U[User<br/>Service]
    GW --> E[Event<br/>Service]
    GW --> B[Booking<br/>Service]
    U -.-> DB1[(db_users)]
    E -.-> DB2[(db_events)]
    B -.-> DB3[(db_bookings)]
    B --> K{{Apache Kafka}}
    E --> K
    K --> N[Notification<br/>Service]
    N --> Mail([Email])
    N --> WS([Socket.io])

    style GW fill:#6366f1,stroke:#818cf8,color:#fff
    style K fill:#17172a,stroke:#6366f1,color:#818cf8
    style N fill:#131320,stroke:#818cf8,color:#eeeeff
```

Database-per-service, a single gateway at the edge, and Kafka carrying
everything that shouldn't block a response — email, real-time push, and
cross-service rollbacks all happen off the request path.

<p align="center">
  <sub><code>ttb.dev</code> · Hanoi, Vietnam</sub>
</p>
