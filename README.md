# Hi, I'm Dan Monahan 👋

Engineering leader and hands-on builder. I ship production software across the stack — systems-level C, Go services, Python AI pipelines, and TypeScript front-ends — with a bias for **local-first, no-SaaS** tools that run on your own machine.

Most of what's below is built end-to-end: the hard backend, the GPU kernel, *and* the README.

---

### 🛠️ Selected projects

| Project | What it is | Stack |
|---|---|---|
| **[pdfcracker](https://github.com/monahand1023/pdfcracker)** | Recover passwords from encrypted PDFs on macOS — all encryption revisions (R2–R6), 15+ attack modes, GPU acceleration via Metal, ARM NEON SIMD, distributed cracking. Zero dependencies. | `C` `Metal` `SIMD` |
| **[imageclust](https://github.com/monahand1023/imageclust)** | Clusters photos by *what they're about*, not just how they look — CLIP ViT-L/14 embeddings + Ward hierarchical clustering + Ollama-generated labels. Entirely on-device. | `Go` `React` `CLIP` |
| **[corpus](https://github.com/monahand1023/corpus)** | Ask natural-language questions over your own notes, PDFs, and docs. Hybrid semantic+keyword search, multi-hop reference expansion, 7-tool MCP server for Claude Code. `pip install corpus-rag` | `Python` `RAG` `MCP` |
| **[cleancut](https://github.com/monahand1023/cleancut)** | Drop in a video, get back a cleaned `.mp4` — profanity muted, explicit scenes cut. Layered local AI stack: Whisper, Ollama, NudeNet + LLaVA, HF audio models. Every cut is auditable. | `Python` `Whisper` `Vision` |
| **[TPSGenerator](https://github.com/monahand1023/TPSGenerator)** | Java load tester for HTTP APIs — 12+ traffic patterns, lock-free HdrHistogram metrics, circuit breaker, real-time resource monitoring. Pairs with [TPSGenerator-Server](https://github.com/monahand1023/TPSGenerator-Server). | `Java` `Concurrency` |
| **[claude-code-skills](https://github.com/monahand1023/claude-code-skills)** | 12 drop-in Claude Code skills for dev workflow and AWS ops — auto-discover your AWS resources at runtime, no config files. | `Tooling` `AWS` `DX` |

---

### 🧰 What I work with

**Languages** &nbsp;`Go` · `C` · `Python` · `TypeScript` · `Java`
**AI / ML** &nbsp;Local-first inference · CLIP · Whisper · Ollama · LLaVA · RAG · MCP · Amazon Bedrock
**Cloud** &nbsp;AWS Lambda · SAM · CloudFormation · DynamoDB · ECS Fargate · Amplify
**Systems** &nbsp;Metal GPU compute · ARM NEON SIMD · lock-free concurrency · serverless

---

<sub>Most projects run entirely on-device — no cloud APIs, no data leaving your machine. I care about software people can actually own and audit.</sub>
