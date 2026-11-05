# AI API Engineering — API Key & Provider Guide

> A practical, research-oriented directory of AI API platforms, their use cases, integration approaches, and API-key security practices.

**Document type:** Personal Research & Technical Documentation  
**Research area:** AI API Engineering, LLM Integration & AI Development Platforms  
**Prepared and researched by:** MR. UNKNOWN, SACHITRA ROY  
**Role:** AI Engineering Researcher · Student · AI & Technology Enthusiast  
**Original research date:** November 2026

> [!IMPORTANT]
> This is an **informational reference**, not a collection of working API keys or a guarantee of free service. Free tiers, promotional credits, supported models, prices, regional eligibility and rate limits can change. Confirm details in each provider's official documentation before implementation.

## Table of Contents

- [1. Understanding AI API Keys](#1-understanding-ai-api-keys)
- [2. AI API Provider Directory](#2-ai-api-provider-directory)
- [3. Provider Profiles](#3-provider-profiles)
- [4. Getting an API Key](#4-getting-an-api-key)
- [5. API Key Security](#5-api-key-security)
- [6. Other APIs Used in AI Projects](#6-other-apis-used-in-ai-projects)
- [7. Search API Providers](#7-search-api-providers)
- [8. Choosing and Integrating Providers](#8-choosing-and-integrating-providers)
- [9. References and Verification](#9-references-and-verification)

## 1. Understanding AI API Keys

An **AI API key** is an authentication credential that lets an application access an AI provider's API. For example, a chatbot sends a prompt to a hosted model and displays its response.

```text
Your Application → API Request → AI Provider → AI Model
       ↑                                      |
       └──────────── API Response ───────────┘
```

### Are free AI APIs really free?

“Free” can mean different things:

- Free usage within a limited quota
- One-time trial or signup credits
- Monthly quotas or daily request limits
- Free access to selected models only
- Community/developer tiers or platform-specific free inference

**A free model or trial does not guarantee unlimited use or production availability.** Check model eligibility, billing rules, credit expiration, and rate limits.

## 2. AI API Provider Directory

These links are starting points for discovery; inclusion does not constitute an endorsement or verification of current offers.

| # | Platform | Website | General focus |
|---:|---|---|---|
| 1 | OpenRouter | https://openrouter.ai/ | Multi-model API gateway |
| 2 | OrcaRouter | https://www.orcarouter.ai/ | Multi-provider routing |
| 3 | TokenRouter | https://www.tokenrouter.com/ | Routing, budgets, BYOK management |
| 4 | TeamRouter | https://teamorouter.com/ | Centralized multi-provider access |
| 5 | Groq | https://console.groq.com/ | High-speed hosted inference |
| 6 | SambaNova AI | https://cloud.sambanova.ai | Hosted inference |
| 7 | Hugging Face | https://huggingface.co/ | Models and inference ecosystem |
| 8 | Mistral AI | https://mistral.ai/ | Language, coding, document AI |
| 9 | NVIDIA Build | https://build.nvidia.com/ | Hosted NIM model endpoints |
| 10 | Google Gemini | https://aistudio.google.com/ | Multimodal models and APIs |
| 11 | xKiro | https://xkiro.com/ | Unified multi-model API |
| 12 | GMI Cloud | https://console.gmicloud.ai/ | AI inference and GPU infrastructure |
| 13 | Ollama | https://ollama.com/ | Local model serving (no cloud key needed locally) |
| 14 | Cerebras | https://cloud.cerebras.ai/ | High-speed inference |
| 15 | Together AI | https://www.together.ai/ | Hosted open-model inference |
| 16 | Fireworks AI | https://fireworks.ai/ | Generative AI inference |
| 17 | Cloudflare Workers AI | https://www.cloudflare.com/products/workers-ai/ | Serverless/edge inference |
| 18 | Replicate | https://replicate.com/ | Specialized text, image, audio, video models |
| 19 | Cohere | https://cohere.com/ | Language, embeddings, retrieval |
| 20 | AI21 Labs | https://www.ai21.com/ | Language-model APIs |
| 21 | TabiAI | https://tabi.ai/ | Alternative third-party model access |
| 22 | JustWorker | Not specified in source document | Alternative model access; verify independently |
| 23 | B.ai | https://b.ai/ | Multi-model API options |

> **Source note:** The original directory lists 22 web entries, while the descriptive profiles also include **Ollama**. It is included here as entry 13 to make the directory consistent with all 23 profiles. Ollama is not a cloud API-key provider in the same sense as the others.

## 3. Provider Profiles

### 3.1 OpenRouter

**Best for:** Exploring many models through one API.

OpenRouter is a multi-model gateway with a unified, OpenAI-compatible interface. Its catalog covers various capabilities, prices and context lengths; some models or routing options may be free within limits. **Integration note:** Keep model IDs configurable. Individual models can differ in modality support, behavior, availability, context limits and cost, even when accessed through the same API.

### 3.2 OrcaRouter

**Best for:** Developers exploring unified multi-provider access.

The research describes an OpenAI-compatible gateway covering multiple model ecosystems and advertising routing and fallback options. **Integration note:** Test exact model IDs, request/response schemas, tool calling, error handling and fallback behavior. Do not assume every upstream model exposes the same features.

### 3.3 TokenRouter

**Best for:** Teams managing multiple providers and their consumption.

The research describes API routing with **bring your own key (BYOK)**, rate limits, budgets, analytics and team controls. **Integration note:** Protect both the router credential and upstream provider keys; configure budgets and monitor usage to reduce accidental overuse.

### 3.4 TeamRouter

**Best for:** Teams testing centralized access to multiple models.

A centralized routing layer may simplify model switching and shared access management. **Integration note:** Investigate API-key management, team permissions, routing and usage controls directly. The source does **not** establish detailed current plan limits or a verified complete feature set.

### 3.5 Groq

**Best for:** Interactive apps that prioritize inference speed.

GroqCloud serves supported models and is especially associated with fast inference. Potential uses include chatbots, coding tools, agents and voice interfaces. **Integration note:** Compare real latency, model quality, context limits, features and rate limits; handle throttling and temporary unavailability gracefully.

### 3.6 SambaNova AI

**Best for:** Hosted, high-performance model inference.

SambaCloud provides access to supported hosted models without requiring local GPU infrastructure. **Integration note:** Check the current model catalog, authentication requirements and API behavior before choosing it as an application dependency.

### 3.7 Hugging Face

**Best for:** Open-source model discovery and diverse AI tasks.

The ecosystem covers text generation, speech, images, embeddings, classification, vision and retrieval-augmented generation (RAG). Its Inference Providers system can offer hosted access to supported models. **Integration note:** A model's listing does not guarantee access through every provider. Check its license, supported tasks, inference availability, hardware needs and pricing.

### 3.8 Mistral AI

**Best for:** Language, coding, reasoning and document-AI apps.

Mistral offers models and developer services for multiple language-oriented workflows, including document processing. **Integration note:** Test with representative project prompts and verify model-specific limits. Access to a playground does not necessarily imply the same API entitlement.

### 3.9 NVIDIA Build

**Best for:** Experimenting with NVIDIA-hosted model endpoints.

NVIDIA Build provides access to supported NIM-based endpoints and a developer testing environment. **Integration note:** Check input/output schemas, model availability, authentication, usage limits and endpoint-specific compatibility. Playground access is not unlimited API access.

### 3.10 Google Gemini

**Best for:** General-purpose and multimodal AI applications.

Google AI Studio lets developers explore Gemini models and create API credentials. Supported features may include text, image understanding and long-context work, depending on the model. **Integration note:** Verify exact model input/output capabilities, rate limits, regional availability and current free-tier conditions.

### 3.11 xKiro

**Best for:** Using a familiar API format across multiple model families.

The research describes support for OpenAI Chat Completions and Anthropic Messages formats, plus text, speech, image and streaming capabilities. **Integration note:** Compatibility does not imply identical behavior for all parameters. Validate a basic call first, then streaming, errors and required modalities; make model IDs configurable.

### 3.12 GMI Cloud

**Best for:** Exploring hosted inference and AI/GPU infrastructure.

GMI Cloud offers AI-related cloud infrastructure and inference services. **Integration note:** An API key authenticates a request but does not automatically grant access to every model or compute resource. Confirm permissions, endpoint schemas, pricing and available models.

### 3.13 Ollama

**Best for:** Running models locally and experimenting offline.

Ollama serves models on your computer and commonly exposes a local API at `http://localhost:11434/api`. Local inference typically does **not** require a traditional cloud API key. **Integration note:** Performance depends on RAM, CPU/GPU and model size. Avoid exposing the local endpoint to the public internet without appropriate access controls.

### 3.14 Cerebras

**Best for:** Speed-sensitive hosted LLM applications.

Cerebras provides inference for supported models and emphasizes fast generation. **Integration note:** Measure end-to-end response time, including network, queueing and prompt/output length. Verify current trial terms and any expiration conditions.

### 3.15 Together AI

**Best for:** Hosted open-model access without self-managed GPUs.

Together AI serves a broad range of open-source models. The source describes this as paid access rather than a permanently free API offering. **Integration note:** Estimate realistic token consumption and operating costs before production deployment.

### 3.16 Fireworks AI

**Best for:** Trying hosted generative AI inference for agents, coding and text apps.

Fireworks provides a model-inference layer for generative applications, with usage-based pricing and potentially temporary introductory credits. **Integration note:** Account for model selection, input/output validation, error handling and credit expiry. Check active billing terms.

### 3.17 Cloudflare Workers AI

**Best for:** Serverless and edge-based AI applications.

Cloudflare Workers AI provides supported models on Cloudflare infrastructure and can be combined with Workers, Pages, AI Gateway and Vectorize. **Integration note:** Verify compatible models, billing units, allocations and account requirements; separate application logic from provider-specific requests when practical.

### 3.18 Replicate

**Best for:** Specialized image, video, audio, text and vision models.

Replicate exposes hosted machine-learning models through APIs without requiring developers to host them. **Integration note:** Each model can have a different input schema, execution duration, hardware profile and price. Check its individual model page and account for processing/startup time.

### 3.19 Cohere

**Best for:** Search, embeddings, reranking and RAG experiments.

Cohere supports language and retrieval-oriented workflows. Embeddings and rerankers can help retrieve relevant document passages for grounded LLM answers. **Integration note:** Trial access may be rate-limited and restricted for production/commercial use; check the latest terms.

### 3.20 AI21 Labs

**Best for:** Language models, assistants and document-oriented development.

AI21 Labs provides generative language APIs and SDKs. **Integration note:** Treat introductory credits as temporary; confirm expiration, supported models, request limits and behavior after credits are exhausted.

### 3.21 TabiAI

**Best for:** Investigating alternative third-party hosted model APIs.

The source describes model access and potential promotional signup credits. **Integration note:** These are **unverified current offers**: validate the provider's official docs, available models, API compatibility, credit conditions, usage limits and billing before depending on the service.

### 3.22 JustWorker

**Best for:** Exploring alternative hosted model services.

The source mentions selected models and promotional signup/referral credit claims, but does not provide an official website. **Integration note:** Confirm the operator, official URL, authentication scheme, model availability, metering, support and credit validity before sharing credentials or project data.

### 3.23 B.ai

**Best for:** Exploring another multi-model API service.

The research describes access to several model families. **Integration note:** Verify the current catalog, interface compatibility, model IDs, billing and privacy/terms. Keep models in configuration rather than hard-coding them.

## 4. Getting an API Key

The precise interface varies by provider, but the usual process is:

1. Choose a platform based on the models and capabilities your project needs.
2. Register through the provider's **official** website.
3. Navigate to **API Keys**, **Credentials**, **Developer**, **API Access** or **Settings**.
4. Create a new key. Copy it to a secure location—some services show the full value only once.
5. Configure the key as an environment variable or in a secrets manager.
6. Make a small test request and review usage, rate-limit and billing information.

**Example `.env` (placeholder values only):**

```dotenv
OPENROUTER_API_KEY=replace_with_your_key
GROQ_API_KEY=replace_with_your_key
GEMINI_API_KEY=replace_with_your_key
```

> [!CAUTION]
> A `.env` file containing **real** credentials must not be committed to GitHub. This example is for illustration, not a working configuration for every provider.

## 5. API Key Security

Treat every API key as a password.

**Never expose private keys in:** public repositories, client-side JavaScript, websites, screenshots, videos, Discord/Telegram posts or published documentation.

For browser apps, use a backend that holds the private credential:

```text
Browser / Client
       |
       v
Your Backend (stores the private key)
       |
       v
AI Provider API
       |
       v
Your Backend → Browser / Client
```

Add the following to your project's `.gitignore`:

```gitignore
.env
.env.*
!.env.example
```

Use a secrets manager for deployed environments; restrict key permissions when supported; set usage alerts/budgets; rotate credentials when needed. **If a real key has already been committed or shared, revoke/rotate it immediately**—deleting a file in a later commit does not undo earlier exposure.

## 6. Other APIs Used in AI Projects

A complete AI product may use **separate services for separate capabilities**:

| Capability | Purpose | What to evaluate |
|---|---|---|
| **Voice APIs** | Speech-to-text, text-to-speech, live voice interactions | Languages, latency, audio formats, streaming, pricing |
| **Search / internet APIs** | Fetch current information and relevant web pages | Source quality, result format, pricing, rate limits |
| **Image APIs** | Image generation, editing or understanding | Supported tasks, input/output formats, resolution, latency, content policy, cost |
| **LLM APIs** | Reasoning, chat, text generation and synthesis | Model quality, context, features, reliability, cost |

**Example voice assistant:**

```text
Spoken Input → Speech-to-Text → LLM → Text-to-Speech → Spoken Output
```

**Example web-grounded assistant:**

```text
User Question → Search API → Relevant Results → LLM → Answer
```

Search results are external information, **not automatically verified facts**. Applications should evaluate source credibility before using retrieved material.

### A note on Hugging Face

Hugging Face can be a useful place to explore models and inference across tasks. However, one Hugging Face account or key should **not** be assumed to unlock every voice, search and image service. Confirm each model's provider, access requirements and terms.

## 7. Search API Providers

| Provider | Focus | Integration role |
|---|---|---|
| **Tavily API** | Search and retrieval designed for AI/agent workflows | Returns research material for LLM processing |
| **Serper API** | Programmatic Google Search results | Returns structured search-result data |
| **SerpAPI** | Search-engine result data across supported engines/features | Returns structured search information |

These APIs **retrieve** information; they do not ordinarily replace the LLM that synthesizes the final conversational answer.

A modular research assistant might use **a search API** for up-to-date pages, **an LLM API** to synthesize findings, **a voice API** to read answers aloud, and optionally **an image API** for visual tasks. This is an architectural example, not a claim that any one provider includes all four features.

## 8. Choosing and Integrating Providers

A practical evaluation checklist derived from the guide:

- [ ] Identify the task: text, coding, reasoning, vision, speech, search or a combination.
- [ ] Confirm the exact model, endpoint and supported input/output formats.
- [ ] Verify whether an account offers trial credits, a recurring free quota or paid usage only.
- [ ] Check rate limits, context limits, regions, allowed use and pricing.
- [ ] Test latency, accuracy, streaming, tool calls and error handling on **your** use case.
- [ ] Keep provider names, model IDs and API keys in configuration.
- [ ] Build sensible fallback and throttling behavior if availability matters.
- [ ] Keep private keys server-side and monitor usage.

The guide distinguishes **model hosts**, **multi-provider gateways**, **local runtimes** and **special-purpose APIs**. They solve different problems; a gateway is not necessarily the underlying model, and a local model server is not a free hosted cloud service.

## 9. References and Verification

**Additional reading included in the original document:** [Best Websites to Get Free AI API Keys](https://akashsingh.net/best-websites-to-get-free-ai-api-keys/).

For the most reliable current information, use each provider's official website in the [directory](#2-ai-api-provider-directory) and check its API docs, pricing, supported models and terms of service.

**Research and verification note:** The profiles explain provider roles and general integration concepts from the November 2026 source document. They are **not** live audits of service capabilities. Briefly documented providers receive cautious descriptions rather than invented specifications; promotional claims require independent verification.

---

*Based on the supplied document: **AI API Engineering (API Key) — Developer Documentation**, November 2026. Reformatted as a navigable GitHub README while preserving its educational purpose and provider coverage.*
