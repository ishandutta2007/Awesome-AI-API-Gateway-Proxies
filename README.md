# Awesome-AI-API-Gateway-Proxies

## Top AI API Gateway & Proxies Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on LLM Gateways, Unified API Proxies, Routing, Load Balancing, Observability & Cost Control*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **AI API Gateway & Proxies**. These systems sit in front of LLM and AI APIs to provide a unified interface, routing, retries, fallbacks, rate limiting, observability, caching, and cost tracking across multiple model providers.



**Examples** include Kong (AI Gateway), Portkey, Cloudflare AI Gateway, Apigee, Tyk Gateway, MuleSoft, AWS API Gateway, Azure API Management, Gravitee.io, and Traefik Enterprise (the category leaders).



**Open-source emphasis**: The AI gateway layer has excellent open options. **LiteLLM**, **Kong**, **Tyk**, **Traefik**, **Apache APISIX**, **KrakenD**, and related projects enable fully self-hosted, provider-agnostic AI API gateways. This section is heavily expanded.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms

- **[Kong AI Gateway](https://konghq.com/products/kong-ai-gateway)**  

  Enterprise API gateway with dedicated AI/LLM capabilities for routing, security, observability, and governance of generative AI traffic.



- **[Portkey](https://portkey.ai/)**  

  AI gateway and control plane for LLMs offering unified APIs, fallbacks, caching, observability, and guardrails across providers.



- **[Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/)**  

  Cloudflare’s managed gateway for AI requests providing analytics, caching, rate limiting, and routing in front of model providers.



- **[Apigee (Google Cloud)](https://cloud.google.com/apigee)**  

  Enterprise API management platform from Google that can front AI and LLM services with full lifecycle management and security.



- **[Tyk Gateway (Enterprise / Cloud)](https://tyk.io/)**  

  API gateway platform with open-source core and commercial offerings; used for traditional and AI/LLM traffic management.



- **[MuleSoft Anypoint](https://www.mulesoft.com/)**  

  Integration and API management platform that can serve as an enterprise gateway and orchestration layer for AI services.



- **[AWS API Gateway](https://aws.amazon.com/api-gateway/)**  

  Fully managed API gateway service frequently used to expose and protect backend and AI/LLM endpoints on AWS.



- **[Azure API Management](https://azure.microsoft.com/en-us/products/api-management)**  

  Microsoft’s managed API gateway and management service for securing, publishing, and monitoring APIs including AI workloads.



- **[Gravitee.io (Enterprise)](https://www.gravitee.io/)**  

  API management and event-native platform with open-source roots and commercial editions suitable for AI traffic control.



- **[Traefik Enterprise](https://traefik.io/traefik-enterprise/)**  

  Commercial distribution of Traefik focused on enterprise ingress, API gateway features, and observability.



## Open-Source GitHub Projects

- **[LiteLLM](https://github.com/BerriAI/litellm)**  

  Open-source library and proxy to call 100+ LLM APIs using the exact same OpenAI format — supports routing, load balancing, fallbacks, spend tracking, and a self-hosted proxy server.



- **[Kong](https://github.com/Kong/kong)**  

  Open-source API gateway (Lua/OpenResty) with a rich plugin ecosystem; widely extended for AI and LLM traffic management.



- **[Tyk](https://github.com/TykTechnologies/tyk)**  

  Open-source API gateway written in Go with strong performance, authentication, rate limiting, and analytics features.



- **[Traefik](https://github.com/traefik/traefik)**  

  Open-source cloud-native application proxy and ingress controller frequently used as an API gateway in Kubernetes environments.



- **[Apache APISIX](https://github.com/apache/apisix)**  

  High-performance open-source API gateway with dynamic routing, plugins, and growing AI/LLM-oriented capabilities.



- **[KrakenD](https://github.com/krakend/krakend-ce)**  

  Open-source ultra-high-performance API gateway focused on aggregation, security, and linear scalability.



- **[Gravitee API Management (Community)](https://github.com/gravitee-io/gravitee-api-management)**  

  Open-source API management platform covering gateway, portal, and policy enforcement.



- **[Envoy AI Gateway / Envoy](https://github.com/envoyproxy/envoy)**  

  High-performance open-source proxy that underpins many AI gateway solutions and can be extended for LLM traffic.



- **[OpenAI-compatible proxies & routers](https://github.com/BerriAI/litellm)**  

  Community projects and LiteLLM-based deployments that present a single OpenAI-compatible endpoint in front of many providers.



- **[Documentation and gateway pattern guides](https://docs.litellm.ai/)**  

  Official docs and community resources for deploying unified LLM gateways with open-source tools.



### Additional Strong Open-Source Options

- Deploying **LiteLLM Proxy** as a drop-in OpenAI-compatible gateway across dozens of providers.

- Using **Kong**, **Tyk**, **Traefik**, or **Apache APISIX** as the general-purpose API gateway layer with AI plugins.

- Combining open gateways with observability (Langfuse, Phoenix, OpenTelemetry) for full request visibility.

- Adding caching, rate limits, and spend controls at the gateway to reduce cost and risk.

- Accepting that managed AI gateways (Portkey, Cloudflare AI Gateway, Kong AI Gateway, cloud provider API Management) still lead in turnkey analytics, enterprise support, and global edge presence.



**Frameworks for building custom systems**: Put **LiteLLM Proxy** (or Kong/Tyk/APISIX) in front of all model providers → enforce auth, rate limits, and fallbacks → emit traces to open observability tools. Suitable for teams that want provider independence and full control. Many organizations still choose commercial AI gateways for managed operations and compliance features.



## How to Contribute

1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.

- API gateways handle authentication, keys, and potentially sensitive prompts/responses. Secure them properly and follow provider terms of service. This list is not security or architecture advice.



---

**Made for AI platform engineers, API architects, and open-gateway advocates.**

Let's keep AI API access unified, observable, and as open as practical.
