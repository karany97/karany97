# Karan Yadav

Building local-first AI infrastructure and shipping it as open source.
Founder of [Nandai](https://nandai.store) (Indian luxury jewelry, live on Flipkart / Shopify / Amazon).

---

### What I'm building

I run a real e-commerce business and a research-grade AI stack out of the same garage. The infrastructure I had to invent to run my own company has become 6 open-source projects and counting. Everything here is **MIT or Apache 2.0**, runs on **consumer hardware** (2× RTX 3090, 187 GB DDR4), and is **production-validated** against my own workload before it goes public.

| Repo | What it solves | Lines | Status |
|---|---|---:|---|
| [**atelier-os**](https://github.com/karany97/atelier-os) | Multi-session AI desktop fleet — one container per employee, iframe-embeddable, Sway + Wayland + wayvnc + noVNC | ~3 k | MIT · 259/259 tests |
| [**destiny-computer**](https://github.com/karany97/destiny-computer) | Persistent Linux desktop an AI owns. You watch it work. You take the keyboard whenever you want. | ~2 k | MIT · Docker compose |
| [**nandai-atelier**](https://github.com/karany97/nandai-atelier) | Single-HTML-file local Claude/GPT alternative. Three brains vote on every answer. 108 MCP tools. | 540 KB | MIT · runs offline |
| [**moa-router**](https://github.com/karany97/moa-router) | Self-MoA (ICLR 2025) as a drop-in OpenAI-compatible proxy. +3.8 % – 6.6 % on reasoning. | 627 | MIT |
| [**tooltalk**](https://github.com/karany97/tooltalk) | Drop-in middleware translating Gemma 4 text-format tool calls into OpenAI structured `tool_calls`. Streaming-safe. | 972 | MIT |
| [**pingate**](https://github.com/karany97/pingate) | Simplest signed-cookie PIN gate for any local AI tool. HMAC-SHA256 + reverse proxy + WebSocket passthrough. | 544 | MIT |
| [**llamacpp-gemma4-mtp**](https://github.com/karany97/llamacpp-gemma4-mtp) | Reproducible Gemma 4 multi-token-prediction bench harness. **2.6 – 2.98× lossless speedup verified.** | — | Shell |

### Upstream contributions

- 🟢 **[ikawrakow/ik_llama.cpp #1744](https://github.com/ikawrakow/ik_llama.cpp/pull/1744)** — *Add MTP Support for Gemma 4* (+1 193 / −154, merged May 10 2026). The harness I built to measure the 2.98× speedup is open-sourced as `llamacpp-gemma4-mtp` above.

### Frontier-hardware moments

- Got **DeepSeek-R1-671B Q2_K_XL serving on 2× consumer RTX 3090** via KTransformers + flash-attn. Inference is functional end-to-end through an OpenAI-compatible endpoint and routed via LiteLLM as `nandai-r1-671b` and `nandai-longctx`. (211 GB GGUF, multi-GPU layer split, CPU-offloaded experts.)
- 6 MCP servers, ~100 tools, full multi-modal AI ops surface for Nandai — voice STT, embeddings, tool-calling, agentic browsing, the lot.

### What I want next

I'm looking for **staff / principal ML-infra roles at frontier-lab-adjacent companies** *or* **seed funding to turn this stack into a product**. If your team ships agentic systems that actually have to work in production and you've been wondering "could one person own that," yes — and the GitHub list above is the receipts.

📫 **Contact:** [karaan.yaadav@gmail.com](mailto:karaan.yaadav@gmail.com) · [LinkedIn](https://www.linkedin.com/in/karanyadav97/)

🏗️ **Currently:** building the next thing in the open. Investors / hiring managers — DMs open.

---

<sub>This page is generated from a Berserker-mode autonomous coding session. The infrastructure that built it is the infrastructure being described.</sub>
