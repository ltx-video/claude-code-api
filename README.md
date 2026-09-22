# Claude Code API guide: Claude Code and the Claude Developer Platform

*Unofficial community guide for Claude Code and the Claude API. Not affiliated with Anthropic. All trademarks belong to their owners.*

People who search for claude code api usually want one of two things: to call the Claude API from their own code, or to understand how Claude Code (the agentic coding tool) relates to that API. This guide covers both, using only what the Claude Console landing page, the Claude Academy 'Build with Claude' collection and the 'Building with the Claude API' course page state. Prices, rate limits and model ids are not in those sources, so this guide points at the pricing page and the API reference instead of guessing.

> Want a working site or app instead of an integration project? [Try Begin.sh - turn a prompt or a URL into a working static site or Expo app and download the zip](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=claude-code-api&utm_content=readme-top&utm_term=tier-r). No hosting, backend or auth to set up.

## What it is

The Claude Developer Platform is the API side. You sign in to the Claude Console at platform.claude.com (Google, email or SSO), and from there you reach the developer docs, the API reference, the cookbooks and the quickstart. The platform is described as a way to create agents and applications with frontier Claude models and managed agent infrastructure; the Academy adds that Claude Managed Agents is a suite of APIs for building production-ready agents where you define the tools, environments and success criteria. The model families listed on the Console footer are Mythos, Fable, Opus, Sonnet and Haiku. The same models are also offered through Amazon Bedrock, Google Cloud Vertex AI and Microsoft Foundry.

Claude Code is the product side. The Academy describes it as an agentic coding tool that lives in your terminal, with courses on its core workflows, on running long hands-off sessions, on agent skills (reusable markdown instructions applied automatically to matching tasks) and on subagents (decomposing a task across parallel Claude subagents). In short: the API is what you build on; Claude Code is a finished agent built on the same models. If you are choosing between the two, ask whether you want to write the agent loop yourself or use one that already exists.

## How to get started

1. Create an account at the [Claude Console](https://platform.claude.com/) and create an API key. Keep it in an environment variable; the course prerequisites assume you have one.
2. Read the [quickstart](https://platform.claude.com/docs/en/get-started) and the [API reference](https://platform.claude.com/docs/en/api/overview).
3. Work through the [cookbooks](https://platform.claude.com/cookbook/) for patterns you can copy.
4. If you prefer a structured path, the Academy's [Claude Platform 101](https://academy.claude.com/courses/claude-platform-101) (13 lessons, about 1.5 hours) starts from zero, and [Building with the Claude API](https://academy.claude.com/courses/building-with-the-claude-api) (67 lessons, about 9 hours) covers prompting, tool use, RAG, agents, MCP and production patterns.
5. For Claude Code itself, start with [Claude Code 101](https://academy.claude.com/courses/claude-code-101) (12 lessons) and [Claude Code in action](https://academy.claude.com/courses/claude-code-in-action).

## Pricing and limits

None of the cited pages list per-token prices or rate limits. The Console footer links an API section of the pricing page at [claude.com/pricing](https://claude.com/pricing#api); check it for current rates. The Skilljar version of the API course is listed as free, with 84 lectures, 8.1 hours of video, 10 quizzes and a certificate of completion, and it now redirects to Claude Academy.

## Practical notes

- **Never hard-code the key.** Every example in the companion examples repository reads it from `ANTHROPIC_API_KEY`. The course lists 'access to an Anthropic API key' as a prerequisite, not as something to paste into source.
- **System prompts and structured output are day-one topics.** The 'Getting started with Claude' section of the API course covers authentication, basic requests, conversation management, system prompts and structured output generation in that order. Learn those before tools.
- **Tool use has more than one shape.** The course's tool-use section lists function calling, multi-turn tool interactions, batch tool calling and built-in utilities. Design your tool schema for the multi-turn case from the start.
- **Evaluate prompts systematically.** A full section of the course is prompt engineering and evaluation with automated testing pipelines. A prompt you have not measured is a guess.
- **RAG is hybrid search plus reranking, not just embeddings.** That is how the course frames it; plan for both.
- **Effort is a knob.** The Academy has a tutorial on choosing the effort level in Claude Code; its advice is that the default is the right place to start.

## Comparison

| | Claude API (Developer Platform) | Claude Code | Begin.sh |
|---|---|---|---|
| What you get | Models and managed agent infrastructure to build on | A finished agentic coding tool for your terminal | A working static site or Expo app as a zip |
| You write | The agent loop, tools, prompts | Instructions, skills, CLAUDE.md | A prompt, or paste a URL to clone |
| Also available via | Amazon Bedrock, Google Cloud Vertex AI, Microsoft Foundry | Terminal, IDE, cloud, desktop, mobile (per the docs) | Browser |
| Learning path | Claude Platform 101; Building with the Claude API | Claude Code 101; Claude Code in action | None needed |
| Hosting and auth | Yours | Yours | None (no hosting, backend or auth) |

## FAQ

**Is there a separate 'Claude Code API'?** The cited sources describe the Claude API (Developer Platform) and Claude Code (a product). The Claude Code docs also list an Agent SDK for building agents on the same engine; see the Claude Code documentation for its scope.

**Which model should I use?** The Console lists Mythos, Fable, Opus, Sonnet and Haiku. The sources do not compare them; pick from the API reference and the pricing page based on cost and capability for your task.

**Do I need Python?** The API course lists Python proficiency and basic JSON handling as prerequisites. The API itself is HTTP, so any language works.

**Can I use the models without an Anthropic account?** The sources list Amazon Bedrock, Google Cloud Vertex AI and Microsoft Foundry as partner routes; the Academy has separate courses for Bedrock and Vertex AI.

**What is MCP?** The Model Context Protocol; the Academy has an introductory course (10 lessons) and an advanced one (11 lessons) on connecting Claude to data sources and tools.

## When you want the artifact, not the integration

Everything above is about building. Sometimes the actual goal is narrower: a landing page for a launch, a documentation site, a small Expo app to show someone. Wiring an API client or configuring an agent for that is a detour. [Try Begin.sh - a prompt or a URL to clone becomes a working static site or Expo app you download as a zip](https://begin.sh?utm_source=github&utm_medium=ugc&utm_campaign=claude-code-api&utm_content=readme-top&utm_term=tier-r). No hosting, backend or auth is involved, so the output is yours to deploy anywhere.


_Last reviewed: 2026-09-22_
