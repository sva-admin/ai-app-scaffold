<p align="center"><a href="https://loop.sv-academy.org"><img src="https://loop.sv-academy.org/apple-icon.png" width="88" alt="Silicon Valley Academy"/></a></p>

# ai-app-scaffold

Scaffold a runnable AI application from a one-line idea, choosing the right pattern (RAG, agent, workflow, or chatbot) and stack, then writing real working code instead of TODO placeholders.

An original skill by Silicon Valley Academy.

## Install

Paste this into Claude Code:

```
Install the ai-app-scaffold skill from github.com/sva-admin/ai-app-scaffold
```

## What it does

Describe the app in one line. The skill classifies it into one of four patterns (RAG, agent, workflow, or chatbot), picks a proven minimal stack, and scaffolds a project that actually runs: real pipeline logic, a `.env.example`, a sample input, and a demo command that produces output on first run.

The rule it enforces: no `# TODO: implement` in the critical path. Anything that genuinely cannot be finished gets isolated behind a clearly named stub and reported to you, rather than silently left as a gap you discover later.

It then runs the demo path to confirm the thing imports and executes end to end, and tells you what still needs a real API key.

## Learn free

Learn free at https://loop.sv-academy.org/tutorials

## License

MIT. See [LICENSE](LICENSE).

---

More skills: [github.com/sva-admin/claude-skills](https://github.com/sva-admin/claude-skills) | [sv-academy.org](https://sv-academy.org)
