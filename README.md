<h1 align="center">Vlad Dogariu</h1>

<p align="center">
  <b>GenAI Solution Architect &amp; Front-End Engineer</b><br>
  I build AI systems that survive contact with production.
</p>

<p align="center">
  <a href="https://thevladdo.github.io/">Portfolio</a> ·
  <a href="https://www.linkedin.com/in/vlad-dogariu">LinkedIn</a> ·
  <a href="https://thevladdo.github.io/genui-framework/">Live demo</a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/thevladdo/thevladdo/main/genui-hero.svg" width="100%" alt="One GenUI zone declaration branching into three user segments, each assembling a different interface layout">
</p>

---

## GenUI Framework

Most GenAI demos die at the pilot. Impressive on a laptop, unshippable in front of a legal team. I wrote GenUI to find out what that gap actually consists of, and it comes down to 3 things. None of them is the model.

| The uncomfortable part                                                                                                                          | What I did about it                                                                                                                                                                                                                       |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| One LLM call per user, per request. That's a bill, not an architecture, and every AI-powered UI demo quietly assumes someone else is paying it. | **Segment cache.** Users collapse into deterministic segments, one generation per segment, stale-while-revalidate with single-flight. The LLM becomes an offline ranker instead of something sitting in the request path.                 |
| A prompt asking the model not to invent links is a hope with good grammar.                                                                      | **Output guarantees.** URL whitelist, numeric grounding, per-tenant content policy, pinned content checked against the real output. Enforced by the system and written up in a document a customer's legal team can attach to a contract. |
| "Does personalization work?" usually gets answered with a vibe.                                                                                 | **Holdout and z-test.** Control arm, CTR per arm, uplift with significance. Under 100 impressions per arm it calls the result preliminary noise instead of inventing a win.                                                               |

Built with React 18 + TypeScript, FastAPI, Qdrant, Redis. Provider-agnostic by design (OpenAI, Anthropic, Gemini, RunPod, any OpenAI-compatible endpoint): bring your own key, bring your own engine. Ships on-prem, one deployment per customer, multi-tenant.

<p align="center">
  <a href="https://doi.org/10.5281/zenodo.18237228"><img src="https://zenodo.org/badge/1133794652.svg" alt="DOI"></a>
  <a href="https://github.com/thevladdo/genui-framework/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-Apache%202.0-blue.svg" alt="License"></a>
  <a href="https://github.com/thevladdo/genui-framework/releases"><img src="https://img.shields.io/github/v/release/thevladdo/genui-framework?color=success" alt="Release"></a>
  <a href="https://github.com/thevladdo/genui-framework/stargazers"><img src="https://img.shields.io/github/stars/thevladdo/genui-framework?style=flat" alt="Stars"></a>
</p>

<p align="center">
  <a href="https://github.com/thevladdo/genui-framework"><b>Repository</b></a> ·
  <a href="https://thevladdo.github.io/genui-framework/"><b>Live demo</b></a> ·
  <a href="https://github.com/thevladdo/genui-framework/blob/main/deploy/OUTPUT-GUARANTEES.md"><b>Output guarantees</b></a>
</p>

---

## Other things I've built

[**rag-backend**](https://github.com/thevladdo/rag-backend) is a custom RAG pipeline on Pinecone and OpenAI, from before I got opinionated about vector stores.

[**AR Industrial Maintenance**](https://github.com/thevladdo/AR_Industrial_Maintenance) puts maintenance instructions in augmented reality, because reading a PDF manual with your hands inside a machine doesn't work.

[**Dev Portfolio**](https://thevladdo.github.io) is my corner of the web.

---

<details>
<summary><b>What I actually work with</b></summary>

<br>

**AI / GenAI**: RAG architectures (Qdrant, Pinecone, LlamaCloud) · multi-agent systems (Datapizza AI, Agno) · provider-agnostic LLM integration (RunPod, OpenAI, Anthropic, Gemini) · structured output and schema validation · regression testing on model output

**Backend**: Python, FastAPI · Redis · Docker · headless Drupal

**Frontend**: React, TypeScript, JavaScript · GSAP motion design · WCAG 2.2 / EN 301 549 accessibility · design systems and CSS-token theming

**Mobile**: React Native

</details>

<details>
<summary><b>The short version of me</b></summary>

<br>

I lead a tech team at [Kapusons](https://www.kapusons.it), taking GenAI from proof of concept to production for enterprise clients: insurance, corporate portals, document extraction. I teach AI at university on the side.

I care about accessibility more than most engineers do. And I think the interesting problems in AI right now sit on the boring side of the stack: what it costs, and how you prove it worked.

</details>

---

<p align="center">
  <sub>Open to conversations about Generative UI, RAG in production, and AI in regulated industries.</sub>
</p>
