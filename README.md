# Karan Yadav

Founder, [Nandai](https://nandai.store). Operating on-premise AI infrastructure that powers a production e-commerce business.

---

Nandai is a luxury Indian jewelry company shipping live orders across Flipkart, Shopify, and Amazon. To run it at the cost structure the category demands, I built the AI stack from scratch — on premise, open-sourced under MIT, benchmarked against my own workload before anything ships.

### Production stack (all MIT, all on GitHub)

| Repo | Function | LoC |
|---|---|---:|
| [**atelier-os**](https://github.com/karany97/atelier-os) | Multi-session AI desktop fleet — one container per teammate, iframe-embeddable. **259 / 259 tests passing.** | ~3 k |
| [**destiny-computer**](https://github.com/karany97/destiny-computer) | Persistent Linux desktop owned by an AI. Docker compose, single command. | ~2 k |
| [**nandai-atelier**](https://github.com/karany97/nandai-atelier) | Single-HTML-file local Claude / GPT alternative. Three brains vote on every answer. 108 MCP tools. | 540 KB |
| [**moa-router**](https://github.com/karany97/moa-router) | Self-MoA (ICLR 2025) as drop-in OpenAI-compatible proxy. Measured **+3.8 % – 6.6 %** on reasoning benchmarks. | 627 |
| [**tooltalk**](https://github.com/karany97/tooltalk) | Drop-in middleware translating Gemma 4 text-format tool calls into OpenAI structured `tool_calls`. Streaming-safe, quote-tolerant. | 972 |
| [**pingate**](https://github.com/karany97/pingate) | Signed-cookie PIN gate for any local AI tool. HMAC-SHA256 + reverse proxy + WebSocket passthrough + CSS theme injection. | 544 |

### Upstream merged contributions

- **[ikawrakow/ik_llama.cpp #1744](https://github.com/ikawrakow/ik_llama.cpp/pull/1744)** — *Add MTP Support for Gemma 4* (+1 193 / −154, merged May 2026). The reproducible benchmark harness that produced the **2.6 × – 2.98 × lossless speedup** is open-sourced as [`llamacpp-gemma4-mtp`](https://github.com/karany97/llamacpp-gemma4-mtp).

### Frontier-model serving on consumer hardware

- **DeepSeek-R1-671B Q2_K_XL** running end-to-end on 2× NVIDIA RTX 3090 via KTransformers + flash-attn. 211 GB weights, multi-GPU layer split, CPU-offloaded experts. Routed via OpenAI-compatible endpoint and LiteLLM as `nandai-r1-671b` and `nandai-longctx`. Every patch tested on premise before deploy.
- **6 production MCP servers, ~100 tools** — voice STT, embeddings, agentic browsing, e-commerce ops, structured tool-calling. All self-hosted.

### Operational footprint

- 2× NVIDIA RTX 3090 + 187 GB DDR4 — every model above runs here, full-time
- Cloudflare tunnels — no public IP exposure
- LiteLLM gateway routing 17 model aliases through one OpenAI-compatible endpoint
- On-premise observability + monitoring stack

---

> The thesis: production-grade agentic AI does not require a hyperscaler bill — it requires correct engineering. Nandai is the proof.

[karaan.yaadav@gmail.com](mailto:karaan.yaadav@gmail.com) · [linkedin.com/in/karanyadav97](https://www.linkedin.com/in/karanyadav97/) · [nandai.store](https://nandai.store)
