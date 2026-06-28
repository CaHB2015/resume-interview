<div align="center">

# 🎯 Project Positioning Agent

**Turn your code projects into interview-winning resume bullets & question banks**

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.0.0-green.svg)](CHANGELOG.md)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![GitHub Stars](https://img.shields.io/github/stars/CaHB2015/resume-interview?style=social)](https://github.com/CaHB2015/resume-interview)

</div>

---

## ✨ The Problem

Same project, two different descriptions — guess which one gets the interview:

```diff
- ❌ "Implemented CRUD for a library management system"
+ ✅ "Designed and built a high-concurrency library platform with Redis caching
+     reducing DB load by 60%, optimized queries via indexing for 300% faster
+     response, supporting 500+ concurrent users"
```

**Your code already does the hard part** — you just need to frame it right. That's what this Skill does.

---

## 🎬 Demo

Feed it your GitHub repo, get 5 outputs ready for interviews.

### Input: Your GitHub Repo

The Skill scans your codebase — tech stack, architecture, business logic.

### Output 1: Resume Bullets

| Before ❌ | After ✅ |
|----------|----------|
| Implemented user login | Built JWT dual-token auth (Access + Refresh), auth response < 30ms |
| Used Redis for caching | Two-level Redis + MySQL cache, hot query latency dropped from 120ms to 15ms |
| Added DB indexes | Optimized slow queries with Explain + composite/covering index design, 90% faster execution |

**Each bullet follows: `Business Scenario + Technical Solution + Engineering Action + Metric`**

```
> Optimized product search pipeline by building a Redis + MySQL data access
> architecture with cache preheating and dynamic updates.
> Search response time dropped from 120ms to 15ms (87% reduction),
> database QPS pressure decreased ~70%.
```

```
> Designed a unified auth & permission system using JWT + Spring Security
> for stateless authentication, with RBAC for fine-grained access control
> across 5 roles and 30+ endpoints.
```

### Output 2: Self-Introduction Scripts

| Version | Length | Use Case |
|---------|--------|----------|
| 🎤 30s | Quick overview | Group interview, intro round |
| 🎤 1min | Key technical points | First round, tech screen |
| 🎤 3min | Full story | Deep-dive rounds, system design |

### Output 3: Interview Question Bank ← The Killer Feature

The Skill predicts what interviewers will ask based on YOUR code — each with answer direction + follow-ups + difficulty:

| Question | Answer Direction | Follow-up | Difficulty |
|----------|-----------------|-----------|------------|
| Why Redis for caching? | Performance, data structures, persistence, clustering | Why not local cache (Caffeine)? | ⭐⭐ |
| How do you prevent cache penetration? | Bloom filter, empty-value cache | How does a Bloom filter work? False positive rate? | ⭐⭐⭐ |
| How do you prevent cache breakdown? | Mutex lock, logical expiration | Logical expiration implementation details? | ⭐⭐⭐ |
| How do you prevent cache avalanche? | Random TTL, multi-level cache, rate limiting | Multi-level cache architecture design? | ⭐⭐⭐ |
| How do you maintain cache consistency? | Cache Aside, delayed double-delete | Timing issues with delayed double-delete? | ⭐⭐⭐⭐ |

**Covers 8 domains**: Architecture · Caching · Database · Security · Concurrency · Message Queue · Performance · System Design

### Output 4: Follow-Up Tree (Interviewer's Thinking Chain)

```
Redis Cache Design
├── Why Redis?
│   ├── Why not local cache (Caffeine)?
│   │   ├── Data consistency issues
│   │   └── Distributed sync problems
│   └── Redis advantages?
│       ├── High performance (single-threaded + IO multiplexing)
│       └── Rich data structures
├── Cache penetration?
│   ├── Bloom filter principle?
│   └── Empty-value cache strategy?
└── Cache breakdown?
    ├── Mutex lock (SETNX + Lua)
    └── Logical expiration (async background refresh)
```

### Output 5: Upgrade Roadmap

Compare your project against real JD requirements to identify gaps:

| Technology | Market Demand | You Have It? | Priority |
|-----------|--------------|-------------|----------|
| RabbitMQ / Kafka | ⭐⭐⭐⭐ | ❌ | 🔴 High |
| Elasticsearch | ⭐⭐⭐ | ❌ | 🔴 High |
| Kubernetes | ⭐⭐ | ❌ | 🟡 Medium |
| CI/CD Pipeline | ⭐⭐⭐ | ❌ | 🟡 Medium |

---

## 🚀 Quick Start

### Installation

```bash
# Copy to Claude Code skills directory
cp -r resume-interview ~/.claude/skills/

# Or copy to Codex skills directory
cp -r resume-interview ~/.codex/skills/
```

### Usage

Just tell Claude:

```
Analyze my project and help me prepare interview-ready project experience.
```

Two modes:

| Mode | Trigger | Output | Best For |
|------|---------|--------|----------|
| ⚡ **Quick** | Default | Resume bullets + Self intro + Question bank | Applying now |
| 🔬 **Full** | "Do a complete project positioning analysis" | All 5 (incl. follow-up tree + roadmap) | Deep interview prep |

---

## 👤 Who Is This For?

| Audience | Why Use It |
|----------|-----------|
| 🎓 CS Students | Your class projects are better than you think — just needs the right framing |
| 📋 New Graduates | Getting no callbacks? Your resume likely sells your projects short |
| 💼 Internship Seekers | Nail the "tell me about your project" question every time |
| 🚀 Junior Devs | Level up your interview game even with limited professional experience |

---

## ⚙️ How It Works

```
Code → Analyze Tech Stack/Architecture → Map to Interview Capabilities → Generate Quantified Descriptions → Output Resume + Questions
```

Three steps:

1. **Reads your code**: scans project structure, identifies framework, database, caching, MQ, auth, deployment
2. **Maps to capabilities**: converts every tech choice into an interview-relevant competency (Redis → cache design, JWT → auth architecture)
3. **Generates output**: writes resume bullets, self-intros, question banks, follow-up trees, and upgrade roadmaps

---

## 📂 Project Structure

```
resume-interview/
├── SKILL.md                    # Core workflow (10 steps + rules)
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── LICENSE                     # MIT
├── agents/openai.yaml
├── references/
│   ├── capability-map.md       # Tech stack → interview capability mapping
│   ├── interview-topics.md     # Capability → interview topics (with follow-ups)
│   ├── jd-keywords.md          # JD keywords for 6 role types
│   └── output-templates.md     # Templates with good/bad examples
├── examples/sample-output.md   # Full output example
└── outputs/                    # Generated files (gitignored)
```

---

## 🧠 Design Principles

- **No fake claims**: everything comes from real code; distinguish "implemented" from "discussable"
- **Quantify everything**: every bullet includes metrics (latency, QPS, hit rate, % improvement)
- **Interview mindset**: don't say "what you did", say "what you achieved"
- **Anticipate follow-ups**: not just answers, but the interviewer's next 3 questions

---

## 🤝 Contributing

PRs and Issues welcome! Especially:

- 🌐 More tech stacks in capability-map (Rust, Kotlin, Swift, etc.)
- 📝 More role types in jd-keywords (Security Engineer, Game Dev, etc.)
- 🌍 More language support

See [CONTRIBUTING.md](CONTRIBUTING.md)

---

## 📄 License

[MIT](LICENSE) © 2026
