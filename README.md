# Awesome AI API Gateway & Proxies [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of production-grade **AI API Gateways**, **LLM Proxies**, and **Unified Inference Routers** for Generative AI applications, Multi-Agent architectures, and enterprise API infrastructure.

[![GitHub stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-AI-API-Gateway-Proxies?style=social)](https://github.com/ishandutta2007/Awesome-AI-API-Gateway-Proxies/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/ishandutta2007/Awesome-AI-API-Gateway-Proxies/pulls)

*Focused on LLM Gateways, Unified Multi-Model API Proxies, Smart Semantic Caching, Dynamic Load Balancing, Guardrails, Observability & Token Cost Control.*

**Last updated:** October 2026

---

## Overview

Modern AI applications rarely rely on a single foundation model provider. An **AI API Gateway & LLM Proxy** acts as an intermediary orchestration, governance, and routing layer situated between client applications (frontends, backend services, autonomous agents) and upstream model providers (OpenAI, Anthropic, Google Vertex AI, AWS Bedrock, Azure OpenAI, Mistral, Ollama, self-hosted vLLM).

### Core Gateway Capabilities
- **Unified Interface:** Standardized OpenAI-compatible API schemas across hundreds of LLMs and embedding providers.
- **Dynamic Routing & Failover:** Automatic retries, load balancing, fallback routing across providers during outages or rate-limit events.
- **Cost & Token Governance:** Real-time token usage attribution, budget limits, virtual API keys, and rate limiting by user/team.
- **Semantic Caching:** Vector-based response caching to reduce inference latency and cut API expenses.
- **Security & Guardrails:** Prompt injection detection, PII masking, DLP filters, and secret scanning before requests reach providers.
- **End-to-End Observability:** Distributed request tracing, latency tracking, prompt/response logging, and evaluation pipelines.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Key Features Comparison Matrix](#key-features-comparison-matrix)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The global AI API and AI Inference Gateway market represents an explosive sub-segment of cloud networking and enterprise AI infrastructure, projected to scale from **$60B+ toward $250B+ by the early 2030s** at a compound annual growth rate (**CAGR of ~30–32%**). 

The market dynamics exhibit **moderate fragmentation with rapid enterprise consolidation**:
- **High startup innovation and fragmentation at the developer layer:** The rapid emergence of lightweight, developer-first proxies and open-source routers (such as LiteLLM, Bifrost, One API, and Portkey) fuels continuous tooling innovation around semantic caching, multi-agent MCP (Model Context Protocol) routing, and local inference bridging.
- **Cloud hyperscaler and incumbent concentration at the enterprise layer:** Trillion-dollar hyperscalers (Microsoft Azure, Google Cloud, AWS) and established enterprise API management leaders (Salesforce MuleSoft, Kong, Cloudflare) dominate mission-critical enterprise workloads through bundled infrastructure trust, compliance certifications (SOC2, HIPAA, FedRAMP), and private networking capabilities. Rather than a pure "winner-take-all" outcome, the market is crystallizing into a hybrid topology: centralized cloud gateways for enterprise governance paired with high-performance open-source sidecars and edge proxies for application-level routing.

---

## SaaS/Hosted Platforms

The following table benchmarks leading SaaS and fully managed AI API gateway platforms, sorted by **Company Size (Valuation / Market Cap / Revenue)** in descending order:

| Product | Description | Company Size (Valuation / Market Cap / Revenue) | Starting Paid Tier Pricing | Free Tier / Trial Limits |
| :--- | :--- | :--- | :--- | :--- |
| **[Azure API Management](https://azure.microsoft.com/en-us/products/api-management)** | Microsoft's enterprise-grade API management & serverless gateway with native GenAI gateway capabilities, token rate limiting, and Azure OpenAI multi-region load balancing. | **~$3.1 Trillion Market Cap** (Microsoft parent company) | **$0.0035 per 10,000 calls** on Consumption tier; Dedicated tiers start at **$48.04/month** (Developer) / **$147.17/month** (Basic v2) | **1,000,000 free API calls per subscription/month** forever on the Consumption tier (no SLA, up to 3,000 operations). |
| **[Apigee](https://cloud.google.com/apigee)** | Google Cloud's premier enterprise API management platform featuring generative AI policy enforcement, security, and lifecycle management. | **~$2.1 Trillion Market Cap** (Alphabet / Google parent company) | Pay-as-you-go: Base environment starts at **$0.50/hour/region** (~$365/month) + **$20 per 1M Standard calls** / **$100 per 1M Extensible calls** | **60-day free evaluation trial** with full access in evaluation environment; eligible for **$300 GCP new-account credits**. |
| **[AWS API Gateway](https://aws.amazon.com/api-gateway/)** | Fully managed AWS API gateway designed to create, secure, and monitor APIs at scale, widely used in front of AWS Bedrock, SageMaker, and Lambda LLM endpoints. | **~$1.9 Trillion Market Cap** (Amazon parent company) | **$1.00 per 1M calls** for HTTP APIs; **$3.50 per 1M calls** (first 333M) for REST APIs | **12-month free tier for new AWS accounts:** Includes **1,000,000 REST/HTTP API calls/month** and **1,000,000 WebSocket messages/month** (750,000 connection minutes/month). |
| **[MuleSoft Anypoint](https://www.mulesoft.com/)** | Salesforce's flagship enterprise integration & API platform featuring Anypoint AI Agent Fabric for managing, securing, and orchestrating enterprise AI services. | **~$300 Billion Market Cap** (Salesforce parent company; acquired MuleSoft for $6.5B) | Commercial packages typically start around **$2,000/month** (~$24,000–$50,000+/year contract minimum depending on Flow & Message consumption) | **30-day free trial** of Anypoint Platform control plane; Anypoint Studio & local community runtime are **free forever** for local dev/testing. |
| **[Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/)** | Global edge AI gateway delivering turnkey analytics, response caching, dynamic routing, rate limiting, and DLP guardrails in front of model providers. | **~$30 Billion Market Cap** (Cloudflare, NYSE: NET) | **Workers Paid starting at $5.00/month** (includes up to 1,000,000 logs/gateway, up to 20 gateways); Unified Billing adds 5% fee on prepaid credit purchases | **Free forever plan:** **100,000 total logs per account**, up to 10 gateways, 10 MB storage/gateway, free DLP scanning (BYOK without token markup). |
| **[Kong AI Gateway](https://konghq.com/products/kong-ai-gateway)** | Cloud control plane & enterprise data planes equipped with prompt decoration, multi-LLM semantic routing, credential virtualization, and AI analytics. | **$2.0 Billion Valuation** ($175M Series E; >$100M ARR) | **Konnect Plus starting at $25/month** (Serverless) / **$200/month** (Hybrid) / **$500/month** (Cloud dedicated), bundled with **1,000,000 API requests/month** ($0.20 per 1,000 additional calls) | **30-day free trial** of full Konnect Enterprise SaaS control plane; core open-source engine is **free forever** for self-hosting. |
| **[Portkey](https://portkey.ai/)** | Full-stack AI gateway and control plane offering unified model APIs, semantic caching, 50+ guardrails, load balancing, and tracing across 1,600+ models. | **$120 Million–$140 Million Valuation** (Acquired by Palo Alto Networks in 2026; $18.1M VC raised) | **Pro Plan starting at $49/month** (scales based on additional log volume, custom retention, and advanced SLAs) | **Free Dev Plan forever:** **10,000 logged requests/month**, 30-day log retention, unlimited gateway requests (routing never cuts off), access to 200+ LLMs. |
| **[Gravitee.io (Enterprise)](https://www.gravitee.io/)** | Event-native API management and AI control plane platform designed for synchronous and streaming API governance, secret protection, and model routing. | **$125+ Million VC Funding Raised** (Series C led by Sixth Street Growth; ~$15M ARR) | Commercial managed cloud deployments start at **~$2,500/month** (flat-rate or tiered multi-environment packaging) | **14-day to 30-day guided enterprise cloud trial** upon request; Community Edition (APACHE 2.0) is **free forever** for self-hosting. |
| **[Tyk Gateway (Cloud / Enterprise)](https://tyk.io/)** | High-performance Go-based API gateway and developer portal for unified API management, multi-protocol support, and LLM endpoint rate limiting. | **$40+ Million VC Funding Raised** (Valuation est. $100M–$250M; ~$18M ARR) | **Tyk Cloud Starter starting at ~$600/month** (packaged with ~5 APIs, ~10M API calls/month, and 100GB throughput) | **48-hour automated free cloud trial** (no credit card required) for full Tyk Cloud control plane; open-source gateway core is **free forever** (MPL-2.0). |
| **[Traefik Enterprise](https://traefik.io/traefik-enterprise/)** | Enterprise distributed ingress controller and API gateway with Raft consensus, automated WAF, distributed rate limiting, and native AI Gateway add-ons. | **$11 Million–$14 Million VC Funding Raised** (Series A led by Balderton Capital; ~$4M ARR) | Commercial tiers priced via custom annual enterprise agreements (historically starting from **~$2,000–$5,000/year** based on node count and support SLA) | **30-day free trial** with full enterprise feature unlock, distributed clustering, and AI/MCP gateway capabilities; OSS Traefik is **free forever** (MIT). |

---

## Open-Source GitHub Projects

The following list showcases open-source AI gateways, LLM proxies, reverse proxies, and inference orchestration layers, **sorted in descending order by GitHub Stars**:

1. **[Traefik](https://github.com/traefik/traefik)** [![GitHub stars](https://img.shields.io/github/stars/traefik/traefik?style=social&color=white)](https://github.com/traefik/traefik/stargazers)  
   Cloud-native modern HTTP reverse proxy and ingress controller written in Go. With automatic configuration discovery and dedicated AI gateway middleware plugins, it easily manages high-throughput microservices and LLM endpoint routing.

2. **[LiteLLM](https://github.com/BerriAI/litellm)** [![GitHub stars](https://img.shields.io/github/stars/BerriAI/litellm?style=social&color=white)](https://github.com/BerriAI/litellm/stargazers)  
   Lightweight, provider-agnostic proxy and Python SDK to call 100+ LLMs (OpenAI, Anthropic, Bedrock, Vertex AI, HuggingFace, Ollama) using the standard OpenAI input/output format. Features dynamic load balancing, cross-provider fallbacks, Redis-backed semantic caching, virtual key management, and detailed team spend tracking.

3. **[Kong](https://github.com/Kong/kong)** [![GitHub stars](https://img.shields.io/github/stars/Kong/kong?style=social&color=white)](https://github.com/Kong/kong/stargazers)  
   Ultra-fast, cloud-native API gateway built on OpenResty / NGINX and Lua. Its AI Gateway plugins support dynamic multi-LLM routing, semantic prompt decoration, credential virtualization, rate-limiting by token counts, and enterprise security guardrails.

4. **[One API](https://github.com/songquanpeng/one-api)** [![GitHub stars](https://img.shields.io/github/stars/songquanpeng/one-api?style=social&color=white)](https://github.com/songquanpeng/one-api/stargazers)  
   All-in-one OpenAI-compatible API aggregation and distribution gateway system written in Go. Supports unified redistribution, multi-key rotation, user quota management, and token conversion for major foundation models (OpenAI, Claude, Gemini, DeepSeek, Qwen, Baidu ERNIE). Packaged as a single binary and Docker container.

5. **[Langfuse](https://github.com/langfuse/langfuse)** [![GitHub stars](https://img.shields.io/github/stars/langfuse/langfuse?style=social&color=white)](https://github.com/langfuse/langfuse/stargazers)  
   Open-source LLM engineering platform and proxy companion offering comprehensive tracing, prompt management, model latency tracking, evals, and fine-grained token cost analysis for production agent applications.

6. **[Envoy](https://github.com/envoyproxy/envoy)** [![GitHub stars](https://img.shields.io/github/stars/envoyproxy/envoy?style=social&color=white)](https://github.com/envoyproxy/envoy/stargazers)  
   High-performance C++ distributed service proxy and communication bus. Powers enterprise service meshes and cloud-native gateways worldwide, and underpins high-speed LLM routing filters and agent communication networks.

7. **[Apache APISIX](https://github.com/apache/apisix)** [![GitHub stars](https://img.shields.io/github/stars/apache/apisix?style=social&color=white)](https://github.com/apache/apisix/stargazers)  
   High-performance dynamic, real-time API gateway based on NGINX and etcd. Delivers dynamic routing, hot-reloading plugins, rate limiting, and dedicated AI proxy plugins (`ai-proxy`) supporting multi-model upstream fallback, token billing, and load balancing.

8. **[Portkey Gateway](https://github.com/Portkey-AI/gateway)** [![GitHub stars](https://img.shields.io/github/stars/Portkey-AI/gateway?style=social&color=white)](https://github.com/Portkey-AI/gateway/stargazers)  
   Ultra-fast, production-ready AI gateway core written in TypeScript. Enables routing to 1,600+ LLMs with 50+ out-of-the-box guardrails, load balancing, automatic retries, semantic caching, and unified telemetry with a 9.9x lower latency footprint.

9. **[Phoenix (Arize AI)](https://github.com/Arize-ai/phoenix)** [![GitHub stars](https://img.shields.io/github/stars/Arize-ai/phoenix?style=social&color=white)](https://github.com/Arize-ai/phoenix/stargazers)  
   AI observability and evaluation gateway library providing OpenTelemetry-based LLM tracing, evaluation benchmarks, latency heatmaps, and prompt debugging for agent pipelines.

10. **[Triton Inference Server](https://github.com/triton-inference-server/server)** [![GitHub stars](https://img.shields.io/github/stars/triton-inference-server/server?style=social&color=white)](https://github.com/triton-inference-server/server/stargazers)  
    NVIDIA's open-source multi-framework inference serving proxy and gateway. Optimizes GPU/CPU resource utilization, dynamic batching, concurrent model execution, and hardware-accelerated endpoints for local model serving.

11. **[Tyk](https://github.com/TykTechnologies/tyk)** [![GitHub stars](https://img.shields.io/github/stars/TykTechnologies/tyk?style=social&color=white)](https://github.com/TykTechnologies/tyk/stargazers)  
    Open-source enterprise API gateway written in Go. Supports REST, GraphQL, and gRPC with zero third-party dependencies beyond Redis, featuring extensible middleware plugins for LLM rate limiting, auth, and analytics.

12. **[Higress](https://github.com/alibaba/higress)** [![GitHub stars](https://img.shields.io/github/stars/alibaba/higress?style=social&color=white)](https://github.com/alibaba/higress/stargazers)  
    Next-generation AI-native API gateway built on Envoy and Istio. Provides native OpenAI-compatible protocol conversion, multi-provider model routing, semantic caching, token rate limiting, and WebAssembly plugin extensibility.

13. **[BentoML](https://github.com/bentoml/BentoML)** [![GitHub stars](https://img.shields.io/github/stars/bentoml/BentoML?style=social&color=white)](https://github.com/bentoml/BentoML/stargazers)  
    Unified inference framework and model serving gateway for building distributed, production-grade AI services with auto-scaling, batching, multi-model pipelines, and OpenAI-compatible API endpoints.

14. **[Bifrost](https://github.com/maximhq/bifrost)** [![GitHub stars](https://img.shields.io/github/stars/maximhq/bifrost?style=social&color=white)](https://github.com/maximhq/bifrost/stargazers)  
    Ultra-low latency, high-performance AI and Model Context Protocol (MCP) gateway written in Go. Provides drop-in OpenAI compatibility across 20+ LLM providers, adaptive load balancing, semantic caching, virtual keys, and automated failover.

15. **[Envoy Gateway](https://github.com/envoyproxy/gateway)** [![GitHub stars](https://img.shields.io/github/stars/envoyproxy/gateway?style=social&color=white)](https://github.com/envoyproxy/gateway/stargazers)  
    Official Kubernetes Gateway API implementation managing Envoy Proxy as a standalone or Kubernetes-native ingress gateway, delivering advanced routing, traffic splitting, and AI workload governance.

16. **[KrakenD](https://github.com/krakend/krakend-ce)** [![GitHub stars](https://img.shields.io/github/stars/krakend/krakend-ce?style=social&color=white)](https://github.com/krakend/krakend-ce/stargazers)  
    Ultra-high performance, stateless open-source API gateway written in Go. Specializes in microservices aggregation, request transformation, and linear throughput scaling for backend AI microservices.

17. **[The Agent Router](https://github.com/theagentrouter/agent-router)** [![GitHub stars](https://img.shields.io/github/stars/theagentrouter/agent-router?style=social&color=white)](https://github.com/theagentrouter/agent-router/stargazers)  
    Unified access proxy and router for Generative AI and autonomous agent systems built on Envoy Gateway, implementing standard OpenAI-compatible routing and fine-grained agent policies.

18. **[Gravitee API Management](https://github.com/gravitee-io/gravitee-api-management)** [![GitHub stars](https://img.shields.io/github/stars/gravitee-io/gravitee-api-management?style=social&color=white)](https://github.com/gravitee-io/gravitee-api-management/stargazers)  
    Flexible, event-native open-source API management platform (Apache 2.0) covering gateway execution, developer portals, and policy design for streaming and RESTful AI services.

---

## Key Features Comparison Matrix

| Feature | LiteLLM | Portkey Gateway | Kong AI Gateway | Cloudflare AI Gateway | Higress | Bifrost |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Open Source Core** | Yes (MIT) | Yes (Apache 2.0) | Yes (Apache 2.0) | No (SaaS) | Yes (Apache 2.0) | Yes (Apache 2.0) |
| **Primary Language** | Python | TypeScript | Lua / C | Rust / Workers | Go / C++ (Envoy) | Go |
| **Supported LLM Providers** | 100+ | 1,600+ | 15+ | 20+ | 15+ | 25+ |
| **Drop-in OpenAI API** | Yes | Yes | Yes | Yes | Yes | Yes |
| **Semantic Vector Caching** | Yes (Redis) | Yes | Yes (Redis) | Yes (Cloudflare KV) | Yes (Redis) | Yes |
| **Dynamic Fallbacks / Retries**| Yes | Yes | Yes | Yes | Yes | Yes |
| **Spend & Token Tracking** | Yes | Yes | Yes | Yes | Yes | Yes |
| **Guardrails & Content Filter**| Yes | Yes (50+ built-in) | Yes | Yes (DLP) | Yes (WASM) | Yes |
| **MCP (Model Context Protocol)**| Yes | Yes | Yes | Roadmap | Yes | Yes |

---

## How to Contribute

We welcome community contributions! To suggest a new AI API gateway or update an existing entry:

1. **Fork the repository** to your GitHub account.
2. **Add or update entries** in [`README.md`](file:///README.md):
   - For **SaaS products**, populate the tabular format including company size/valuation, exact starting paid tier pricing, and specific free tier / trial limits.
   - For **Open-Source tools**, add the social white badge linking to `/stargazers` and maintain descending order by star count.
3. Verify that URLs, pricing documentation, and project links are active and factual.
4. **Submit a Pull Request** with a clear explanation of the addition or update.

---

## Disclaimer

This repository is a community-curated technical index and does not represent an endorsement of any commercial vendor or open-source software. AI API gateways handle sensitive credentials, authorization tokens, and user prompts; ensure you adhere to your organization's security standards and upstream provider terms of service.

---

<div align=\"center\">

**Maintained with ❤️ by the AI Platform Engineering Community.**  
*Keeping Generative AI API access unified, resilient, observable, and open.*

</div>
