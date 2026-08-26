# Dan Monahan

Engineering leader. Ex-Amazon Software Development Manager (10 years, up to 34 engineers across 3 teams), most recently VP of Technology at Sigo Seguros. I build AI-native engineering organizations, and I still ship.

My focus is AI on both sides: embedding it into products (RAG, agentic systems, voice agents) and using it to transform how engineering teams build software. The projects below are shipped end-to-end with AI-assisted development, spanning systems-level C, Go services, Python AI pipelines, Swift/iOS apps, and TypeScript front-ends, with a bias toward local-first tools you can run and audit yourself.

---

### Shipped products

**[lens](https://lens.supersmall.ai)** is a multi-agent AI audit engine I founded and build solo, now live and taking paying customers. It runs 200+ in-house checks across 26 dimensions of a codebase and a live site (security, performance, reliability, supply chain, cloud cost, accessibility, SEO), with one reasoning agent per dimension grounded in deterministic scanners and every finding cross-verified by multiple frontier models to cut false positives. Output is two reports from one audit, plain-English for founders and engineer-grade for the team, plus a CycloneDX/SPDX SBOM and a prioritized fix-it roadmap.

It also ships as an MCP server, so the audit runs inline in Cursor, Claude Code, or Windsurf before the PR opens. Guardrails include SSRF protection and secret redaction before any report renders; repos are cloned to a temp directory, scanned, and deleted. Deployment is Docker / CloudFormation. The web app, **lens-web**, is a React SPA on a FastAPI backend (AWS, DynamoDB) with Google OIDC/PKCE auth, per-account quotas, Stripe billing, per-audit token metering, and live progress over SSE.

**Live:** [lens.supersmall.ai](https://lens.supersmall.ai) (see a [sample report](https://lens.supersmall.ai/sample))

**Panorama** turns an iPhone into a spherical-panorama camera — a modern, personal rebuild of the Photosynth experience. A guided ARKit sweep auto-captures frames, corrects for the phone's own tracking error, and stitches them into a seamless 360° image on-device with a custom Metal GPU stitcher. Fully local: no cloud, no accounts, no backend, nothing collected.

**App Store:** [Panorama: Spherical Camera](https://apps.apple.com/us/app/panorama-spherical-camera/id6786430972)

Two more, built and shipped solo end-to-end, from infrastructure through storefront:

- **[Kunkun](https://kunkun.io)** is a Japanese grammar and formality checker delivered as a Chrome extension and Google Docs add-on, running on AWS Bedrock. Real-time keigo, particle, and tense correction with explanations, aligned to JLPT N5 through N1.
- **[Gaijin Smash](https://gaijin-smash.net)** is a bilingual (EN/JA) direct-to-consumer streetwear brand: real Japanese cultural slogans with proper context, not Google Translate. Custom storefront, CloudFront-backed asset pipeline, full catalog and checkout.

*All four are proprietary, closed source (source not public).*

---

### Open-source projects

| Project | What it is | Stack |
|---|---|---|
| **[corpus](https://github.com/monahand1023/corpus)** | Ask natural-language questions over your own notes, PDFs, and docs. Hybrid semantic + keyword search with auto-tuned fusion, multi-hop reference expansion, a retrieval eval harness with a CI gate, and a 7-tool MCP server for Claude Code. Storage, index, search, and re-ranking are local; embeddings call your chosen provider. `pip install corpus-rag` | `Python` `RAG` `MCP` |
| **[pdfcracker](https://github.com/monahand1023/pdfcracker)** | Recover passwords from your own encrypted PDFs on macOS. All encryption revisions (R2 to R6), 15+ attack modes, GPU acceleration via Metal, ARM NEON SIMD, distributed cracking. Zero dependencies. | `C` `Metal` `SIMD` |
| **[imageclust](https://github.com/monahand1023/imageclust)** | Clusters photos by *what they're about*, not just how they look. CLIP ViT-L/14 embeddings, Ward hierarchical clustering, and Ollama-generated labels. Entirely on-device. | `Go` `React` `CLIP` |
| **[cleancut](https://github.com/monahand1023/cleancut)** | Drop in a video, get back a cleaned `.mp4`: profanity muted, explicit scenes cut. Layered local AI stack (Whisper, Ollama, NudeNet + LLaVA, HF audio models). Every cut is auditable. | `Python` `Whisper` `Vision` |
| **[claude-code-skills](https://github.com/monahand1023/claude-code-skills)** | 12 drop-in Claude Code skills for dev workflow and AWS ops. Auto-discover your AWS resources at runtime, no config files. | `Tooling` `AWS` `DX` |
| **[TPSGenerator](https://github.com/monahand1023/TPSGenerator)** | Java load tester for HTTP APIs: 12+ traffic patterns, lock-free HdrHistogram metrics, circuit breaker, real-time resource monitoring. Pairs with [TPSGenerator-Server](https://github.com/monahand1023/TPSGenerator-Server). | `Java` `Concurrency` |

---

### Background

Amazon (Software Development Manager, ~10 years), LTK, and Sigo Seguros (VP of Technology). At Sigo I led the shift to an AI-native engineering org, roughly 5x daily code output with median PR merge time down 77% and merge quality holding steady, and shipped 6 customer-facing products in 10 months on a 7-engineer team: three Spanish-language voice AI agents, WhatsApp quoting, a broker management platform connecting 15 carriers, and a customer block-list service. Conversion went from 3.5% to 12.9% and the business reached a $1M ARR run-rate.

Trilingual: English, Spanish, and Japanese (JLPT N2). Speaking on production AI agents at ELC and SuperSmall in 2026.

### How I work

Engineering leadership, AI-native delivery, and cloud architecture (AWS) are genuinely hands-on. I ship production code across Go, C, Python, TypeScript, and Java through AI-assisted development. The open-source projects here run mostly on-device: software people can own and audit.

---

Find me on [LinkedIn](https://www.linkedin.com/in/danielemonahan/).
