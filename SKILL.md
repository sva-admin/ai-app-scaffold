---
name: ai-app-scaffold
description: >
  Scaffold a working AI application from a one-line idea: RAG pipelines,
  agents, tool-using workflows, chatbots. Chooses a sensible stack, wires the
  pieces, and writes real (not placeholder) code. Trigger on "build an AI
  app", "RAG app", "make a chatbot that", "agent that does X", "AI workflow for",
  "scaffold an LLM app", "build a tool that uses an LLM to", or when the user
  wants a runnable starting point for an AI feature. Inspired by patterns in
  awesome-ai-apps and public-api-lists.
---

# AI App Scaffold

Go from idea to a runnable AI-app skeleton with the right architecture and no
TODO placeholders.

## Step 1: Classify the app
Pick the pattern (this drives everything else):
- **RAG**: answer over the user's documents/data. Needs: loader, chunker,
  embeddings, vector store, retriever, LLM answer with citations.
- **Agent**: LLM that plans and calls tools in a loop. Needs: tool definitions,
  an agent loop, stopping/verification, memory.
- **Workflow / chain**: fixed multi-step LLM pipeline (extract, transform,
  format). Deterministic order, each step typed.
- **Chatbot / assistant**: conversational UI plus one of the above behind it.

## Step 2: Choose the stack (state assumptions, don't over-ask)
Default to what's proven and minimal:
- Language: Python (LangChain/LlamaIndex) or TS (Vercel AI SDK). Match the
  user's ecosystem if known.
- Vector store: start with a local one (Chroma/FAISS) unless scale demands more.
- Model: provider-agnostic via an abstraction; read keys from env, never hardcode.
- External data: check public-api-lists for a free API before building a scraper.

## Step 3: Scaffold real code
Create a runnable project, not a sketch:
- `README.md` with run steps and required env vars.
- `.env.example` (never real keys).
- Working entry point plus the core pipeline implemented with real logic.
- One small example/sample input so `run` produces output immediately.
- Minimal test or a `make demo` / `npm run demo` that proves it works.

No `# TODO: implement` in the critical path. If something genuinely can't be
finished, isolate it behind a clearly-named stub and tell the user.

## Step 4: Verify
Run the demo path (with a dummy/test key or a mock if no key is available) to
confirm it imports and the pipeline executes end to end. Report what ran and
what needs a real API key.

## Guardrails
- Never put secrets in code or URLs; use env vars.
- Keep the first version small and working over feature-complete and broken.
- Save the project to the working folder and present the entry files.
