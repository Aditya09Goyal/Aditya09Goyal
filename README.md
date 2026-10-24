<!-- ============================================================
     TEMPLATE 4 · BLUEPRINT ARCHITECT  (system-design showcase)
     Mermaid diagrams render natively on GitHub.
     ============================================================ -->

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:0b1e3f,100:10274f&height=150&section=header&text=Aditya%20Goyal&fontSize=52&fontColor=4fc3f7&fontAlignY=42&desc=Systems%2C%20sketched%20before%20they%27re%20shipped&descAlignY=72&descSize=17&animation=fadeIn" width="100%" alt="header"/>
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Space+Mono&weight=700&size=20&duration=2800&pause=900&color=4FC3F7&center=true&vCenter=true&width=660&lines=Sketch+the+system.+Then+ship+it.;Backend+%2B+AI+%E2%80%A2+APIs+that+think;APIs+%E2%80%A2+Data+models+%E2%80%A2+Service+boundaries;Low-level+design+%E2%80%A2+High-level+design;Learning+to+scale%2C+one+bottleneck+at+a+time" alt="typing"/>
</p>

## 📐 Spec sheet

| Field | Value |
|:--|:--|
| **Engineer** | Aditya Goyal |
| **Program** | B.Tech Electronics & Communication Engineering, BIT Mesra (2023–2027) |
| **Focus** | Backend + AI, system design, distributed systems |
| **Strengths** | Data structures & algorithms, low-level design, full-stack web, data analytics |
| **Status** | 🟢 Open to SDE internships and full-time roles |

I care about designs that are simple to reason about, measurable under load and honest about their trade-offs. Coming from ECE, I think about latency, bandwidth and noise by default, and I bring that lens to how services talk to each other.

## 🧰 Materials

<p align="center">
  <img src="https://skillicons.dev/icons?i=cpp,py,js,ts,nodejs,express,fastapi,react,postgres,mongodb,git,vercel,postman,linux&perline=7&theme=dark" alt="skills"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Socket.io-0b1e3f?style=flat-square&logo=socketdotio&logoColor=4fc3f7"/>
  <img src="https://img.shields.io/badge/WebRTC-0b1e3f?style=flat-square&logo=webrtc&logoColor=4fc3f7"/>
  <img src="https://img.shields.io/badge/LangChain-0b1e3f?style=flat-square&logo=langchain&logoColor=4fc3f7"/>
  <img src="https://img.shields.io/badge/pgvector-0b1e3f?style=flat-square&logo=postgresql&logoColor=4fc3f7"/>
  <img src="https://img.shields.io/badge/React_Native-0b1e3f?style=flat-square&logo=react&logoColor=4fc3f7"/>
</p>

## 🗂️ Architecture notebook

How I think about systems: the building blocks I design with and keep studying.

### Sheet 01 · A scalable web service

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#10274f','primaryTextColor':'#e3f2fd','primaryBorderColor':'#4fc3f7','lineColor':'#4fc3f7','secondaryColor':'#0b1e3f','tertiaryColor':'#0b1e3f','background':'#0b1e3f'}}}%%
flowchart LR
  C[Clients] --> LB[Load balancer]
  LB --> A1[App server 1]
  LB --> A2[App server 2]
  LB --> A3[App server N]
  A1 & A2 & A3 --> R[(Cache)]
  A1 & A2 & A3 --> P[(Primary DB)]
  P -->|replication| RR[(Read replicas)]
  A1 & A2 & A3 -->|events| Q[[Message queue]]
  Q --> W[Background workers]
```

### Sheet 02 · Partitioning data with consistent hashing

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#10274f','primaryTextColor':'#e3f2fd','primaryBorderColor':'#4fc3f7','lineColor':'#4fc3f7','secondaryColor':'#0b1e3f','tertiaryColor':'#0b1e3f','background':'#0b1e3f'}}}%%
flowchart LR
  K[Request key] --> H[Hash function]
  H --> RING((Hash ring))
  RING --> N1[(Shard A)]
  RING --> N2[(Shard B)]
  RING --> N3[(Shard C)]
```

### Sheet 03 · A backend with AI inside (RAG)

```mermaid
%%{init: {'theme':'base','themeVariables':{'primaryColor':'#10274f','primaryTextColor':'#e3f2fd','primaryBorderColor':'#4fc3f7','lineColor':'#4fc3f7','background':'#0b1e3f'}}}%%
flowchart LR
  D[Documents] -->|chunk + embed| V[(Vector DB)]
  U[Client] --> API[API service]
  API -->|retrieve context| V
  API -->|prompt + context| L[LLM]
  L -->|grounded answer| U
```

## 📏 On the drafting table

What I already use, and what I'm working through for distributed systems.

- [x] Data structures & algorithms in C++
- [x] Low-level design: OOP, SOLID, design patterns
- [x] REST APIs and real-time communication (WebSockets)
- [x] Relational, document and vector databases
- [x] LLM apps with LangChain, RAG and embeddings
- [ ] Caching strategies and cache invalidation (Redis)
- [ ] Message queues and event-driven architecture (Kafka)
- [ ] Sharding, replication and consistent hashing
- [ ] CAP theorem, consistency models and consensus (Raft)
- [ ] Containerisation and deployment (Docker)
- [ ] AI agents, tool use and LLM evaluation

## 🧮 Load tests

<p align="center">
  <a href="https://leetcode.com/u/goyal_additya/"><img src="https://leetcard.jacoblin.cool/goyal_additya?theme=dark&font=Space%20Mono&ext=heatmap" alt="LeetCode"/></a>
</p>

<p align="center">
  <a href="https://leetcode.com/u/goyal_additya/"><img src="https://img.shields.io/badge/LeetCode-0b1e3f?style=for-the-badge&logo=leetcode&logoColor=4fc3f7"/></a>
  <a href="https://codeforces.com/profile/cp.adi.709"><img src="https://img.shields.io/badge/Codeforces-0b1e3f?style=for-the-badge&logo=codeforces&logoColor=4fc3f7"/></a>
  <a href="https://www.geeksforgeeks.org/profile/goyal_adi"><img src="https://img.shields.io/badge/GeeksforGeeks-0b1e3f?style=for-the-badge&logo=geeksforgeeks&logoColor=4fc3f7"/></a>
</p>

<p align="center">
  <img height="165" src="https://github-readme-stats.shion.dev/api?username=Aditya09Goyal&show_icons=true&hide_border=true&bg_color=0b1e3f&title_color=4fc3f7&text_color=b3e5fc&icon_color=4fc3f7&ring_color=4fc3f7" alt="stats"/>
  <img height="165" src="https://github-readme-stats.shion.dev/api/top-langs/?username=Aditya09Goyal&layout=compact&hide_border=true&bg_color=0b1e3f&title_color=4fc3f7&text_color=b3e5fc&langs_count=8" alt="langs"/>
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com/?user=Aditya09Goyal&hide_border=true&background=0B1E3F&ring=4FC3F7&fire=4FC3F7&currStreakNum=E3F2FD&currStreakLabel=4FC3F7&sideNums=E3F2FD&sideLabels=B3E5FC&dates=6A8BB0&stroke=1E4A7A" alt="streak"/>
</p>

<p align="center">
  <img width="100%" src="https://github-readme-activity-graph.vercel.app/graph?username=Aditya09Goyal&bg_color=0b1e3f&color=b3e5fc&line=4fc3f7&point=e3f2fd&area=true&area_color=4fc3f7&hide_border=true&custom_title=Throughput%20over%20time" alt="activity"/>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/Aditya09Goyal/Aditya09Goyal/output/snake-blueprint.svg" alt="snake"/>
</p>

## 🔌 Interfaces

<p align="center">
  <a href="https://linkedin.com/in/goyaladitya09"><img src="https://img.shields.io/badge/LinkedIn-0b1e3f?style=for-the-badge&logo=linkedin&logoColor=4fc3f7"/></a>
  <a href="mailto:goyaladi0911@gmail.com"><img src="https://img.shields.io/badge/Email-0b1e3f?style=for-the-badge&logo=gmail&logoColor=4fc3f7"/></a>
  <a href="https://instagram.com/goyal_additya"><img src="https://img.shields.io/badge/Instagram-0b1e3f?style=for-the-badge&logo=instagram&logoColor=4fc3f7"/></a>
  <img src="https://komarev.com/ghpvc/?username=Aditya09Goyal&label=Requests%20served&color=4fc3f7&style=for-the-badge" alt="views"/>
</p>

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=rect&color=0:10274f,100:0b1e3f&height=60&section=footer" width="100%" alt="footer"/>
</p>
