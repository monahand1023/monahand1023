# Dan Monahan

Engineering leader. Ex-Amazon Software Development Manager (10 years, up to 34 engineers across 3 teams), most recently VP of Technology at Sigo Seguros. I build AI-native engineering organizations, and I still ship.

My focus is AI on both sides: embedding it into products (RAG, agentic systems, voice agents), and using it to change how engineering teams build software. I've taken a 7-engineer team through that shift, shipping 6 customer-facing products in 10 months — three Spanish-language voice AI agents, WhatsApp quoting, and a broker platform connecting 15 carriers.

The projects below are shipped end-to-end with AI-assisted development, across systems-level C, Go services, Python AI pipelines, Swift/iOS apps, and TypeScript front-ends. I lean toward local-first tools you can run and audit yourself.

---

### Shipped products

**[lens](https://lens.supersmall.ai)** — multi-agent AI audit engine, founded and built solo, live and taking paying customers.
- 200+ checks across 26 dimensions of a codebase and a live site (security, performance, reliability, supply chain, cloud cost, accessibility, SEO) — one reasoning agent per dimension, grounded in deterministic scanners, every finding cross-verified by multiple frontier models to cut false positives
- Also ships as an MCP server, so the audit runs inline in Cursor, Claude Code, or Windsurf before the PR opens
- One audit produces two reports (plain-English for founders, engineer-grade for the team), a full dependency and license inventory (SBOM, in CycloneDX or SPDX format), and a prioritized fix-it roadmap

**Live:** [lens.supersmall.ai](https://lens.supersmall.ai) · [sample report](https://lens.supersmall.ai/sample)

**Panorama** — turns an iPhone into a spherical-panorama camera, a modern rebuild of the Photosynth experience.
- Guided ARKit sweep auto-captures frames and corrects for the phone's own tracking error
- Stitches into a seamless 360° image on-device with a custom Metal GPU stitcher
- Fully local: no cloud, no accounts, no backend, nothing collected

**App Store:** [Panorama: Spherical Camera](https://apps.apple.com/us/app/panorama-spherical-camera/id6786430972)

**[Kunkun](https://kunkun.io)** — Japanese grammar-checking SaaS, built and run solo: Grammarly for Japanese.
- Context-aware corrections: politeness level, JLPT focus (N5–N1), and writer mode (learner vs. native) all shape the AI's response, with a plain-language explanation attached to every fix, not just the fix itself
- One backend, three surfaces — website, Chrome extension, Google Docs/Slides add-on — all reading live subscription state from the same API
- Go Lambda on AWS Bedrock (Claude/Nova) for inference, Firebase auth, Stripe subscriptions

**Live:** [kunkun.io](https://kunkun.io)

**[Gaijin Smash](https://gaijin-smash.net)** — bilingual (EN/JA) direct-to-consumer streetwear brand: real Japanese slogans with proper cultural context, not Google Translate.
- AI content pipeline (image generation, model photography, copy) with human review as the quality gate before anything goes live
- Built solo end-to-end: storefront, checkout, CloudFront-backed asset pipeline, admin dashboard

**Live:** [gaijin-smash.net](https://gaijin-smash.net)

*All four are proprietary — source not public.*

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

### Speaking

**[ELC: Production AI Agents, Beyond the Demo](https://elc.community/public/events/roundtable-production-ai-agents-beyond-the-demo-fzaux0ry1a)** — hosted, July 2026. Roundtable on the gap between AI agent demos and production-reliable systems: where agents actually run in production versus stay stuck in pilot, what breaks under real users, and how you monitor a system where there's no single correct output.

**[SuperSmall: Vibe-Code to Production](https://luma.com/qtfclu9a)** — featured speaker, June 2026. Workshop on taking AI-generated prototypes (Lovable, Cursor, Replit) to production: auth, databases, deployment, performance, with live Q&A on attendees' own projects.

---

Trilingual: English, Spanish, Japanese (JLPT N2). Find me on [LinkedIn](https://www.linkedin.com/in/danielemonahan/).
