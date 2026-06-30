# Dan Monahan

Engineering leader. Ex-Amazon Software Development Manager (10 years, up to 34 engineers across 3 teams), former VP of Engineering. I build AI-native engineering organizations, and I still ship.

My focus is AI on both sides: embedding it into products (RAG, agentic systems, voice agents) and using it to transform how engineering teams build software. The projects below are shipped end-to-end with AI-assisted development, spanning systems-level C, Go services, Python AI pipelines, and TypeScript front-ends, with a bias toward local-first tools that run on your own machine.

---

### Currently building: lens

**lens** is a multi-agent AI audit engine I founded and build solo. It runs one reasoning agent per dimension (security, performance, SEO, cost, accessibility), each grounded in deterministic scanners, and exposes its audits as tools through an MCP server, with SSRF and secret-redaction guardrails and Docker / CloudFormation deployment. Its web app, **lens-web**, is a React SPA on a FastAPI backend (AWS, DynamoDB) with Google OIDC/PKCE auth, per-account quotas, Stripe billing, and live progress over SSE.

**Live app:** [lens-web](https://838p8fjmcc.us-west-2.awsapprunner.com/)

*Proprietary, closed source (source not public).*

---

### Selected projects

| Project | What it is | Stack |
|---|---|---|
| **[corpus](https://github.com/monahand1023/corpus)** | Ask natural-language questions over your own notes, PDFs, and docs. Hybrid semantic + keyword search, multi-hop reference expansion, and a 7-tool MCP server for Claude Code. `pip install corpus-rag` | `Python` `RAG` `MCP` |
| **[claude-code-skills](https://github.com/monahand1023/claude-code-skills)** | 12 drop-in Claude Code skills for dev workflow and AWS ops. Auto-discover your AWS resources at runtime, no config files. | `Tooling` `AWS` `DX` |
| **[imageclust](https://github.com/monahand1023/imageclust)** | Clusters photos by *what they're about*, not just how they look. CLIP ViT-L/14 embeddings, Ward hierarchical clustering, and Ollama-generated labels. Entirely on-device. | `Go` `React` `CLIP` |
| **[cleancut](https://github.com/monahand1023/cleancut)** | Drop in a video, get back a cleaned `.mp4`: profanity muted, explicit scenes cut. Layered local AI stack (Whisper, Ollama, NudeNet + LLaVA, HF audio models). Every cut is auditable. | `Python` `Whisper` `Vision` |
| **[pdfcracker](https://github.com/monahand1023/pdfcracker)** | Recover passwords from encrypted PDFs on macOS. All encryption revisions (R2 to R6), 15+ attack modes, GPU acceleration via Metal, ARM NEON SIMD, distributed cracking. Zero dependencies. | `C` `Metal` `SIMD` |
| **[TPSGenerator](https://github.com/monahand1023/TPSGenerator)** | Java load tester for HTTP APIs: 12+ traffic patterns, lock-free HdrHistogram metrics, circuit breaker, real-time resource monitoring. Pairs with [TPSGenerator-Server](https://github.com/monahand1023/TPSGenerator-Server). | `Java` `Concurrency` |

---

### Background

Amazon (Software Development Manager, ~10 years) · LTK · Sigo Seguros (VP of Engineering). At Sigo I led the shift to an AI-native engineering org and shipped customer-facing AI products including Spanish-language voice agents, RAG systems, and a broker platform.

Trilingual: English, Spanish, and Japanese (JLPT N2). Speaking on production AI agents at ELC and SuperSmall in 2026.

### How I work

Engineering leadership, AI-native delivery, and cloud architecture (AWS) are genuinely hands-on. I ship production code across Go, C, Python, TypeScript, and Java through AI-assisted development. The projects here run mostly on-device: software people can own and audit.

---

<sub>Find me on [LinkedIn](https://www.linkedin.com/in/danielemonahan/).</sub>
