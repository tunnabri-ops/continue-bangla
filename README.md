# Continue Bangla — VS Code-এ বাংলায় AI কোডিং সহকারী

Bangla-ready Continue config, built on **continuedev/continue**.

- **Original repo:** https://github.com/continuedev/continue (open-source coding agent — chat, edit and autocomplete inside VS Code and JetBrains, with any LLM)

## কী আছে / What is inside

- `config.yaml` — Continue config (new YAML format): chat + edit use local `qwen2.5-coder:7b` via Ollama, autocomplete uses `starcoder2:3b`. No API key needed.
- `rules-bangla.md` — project rules: explain code in Bangla, keep code and comments in English, never invent library APIs.

## যা ঠিক করা হয়েছে / What was fixed

- Upstream ships with no config at all — a new user must pick a provider, a model and write the YAML by hand. This config is ready to drop in: local Ollama models, Bangla-first behaviour.
- Model choice: `qwen2.5-coder:7b` — strong at code and understands Bangla instructions; `starcoder2:3b` is small and fast enough for autocomplete on a normal laptop.
- The rules file stops the agent from answering in English by default and from inventing APIs — the two most common annoyances with a fresh Continue install.

## ব্যবহার / How to use

```bash
# 1. Install Ollama and pull the models
ollama pull qwen2.5-coder:7b
ollama pull starcoder2:3b

# 2. Install the Continue extension in VS Code, then copy the config
cp config.yaml ~/.continue/config.yaml
cp rules-bangla.md ~/.continue/rules/bangla.md

# 3. Open VS Code, press Ctrl+Shift+L and chat in Bangla
```

Everything runs locally — no key, no account, no code leaves your computer.
