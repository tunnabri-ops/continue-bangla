# ⌨️ Continue Bangla

[![Bangla](https://img.shields.io/badge/UI-Bangla%20%2B%20English-orange)](#)

**A Bangla-first AI coding assistant for VS Code — chat, edit and autocomplete with local models, no API key, no code leaving your computer.**

> বাংলা সংস্করণ নিচে আছে। / Bangla version below.

## ✨ Features

- `config.yaml` — ready-to-drop-in config: chat and edit use `qwen2.5-coder:7b` through local Ollama (`http://localhost:11434`), autocomplete uses the small, fast `starcoder2:3b`. Code, docs, diff, terminal, problems, folder and codebase context are all enabled.
- `rules-bangla.md` — project rules: explain code in Bangla, keep code and comments in English, never invent library APIs, change only what was asked, show the exact command when a fix needs one.
- `prompts-bangla.md` — four ready prompts to paste into the chat: fix a bug, add a feature, explain code, write tests — each with Bangla instructions.

## 🚀 How to use

```bash
# 1. Install Ollama and pull the models
ollama pull qwen2.5-coder:7b
ollama pull starcoder2:3b

# 2. Install the Continue extension in VS Code, then copy the config
cp config.yaml ~/.continue/config.yaml
cp rules-bangla.md ~/.continue/rules/bangla.md

# 3. Open VS Code, press Ctrl+Shift+L and chat in Bangla
```

## ⚠️ Honest limits

- You need Ollama running locally with both models downloaded — this repo is the config, prompts and rules, not the extension or the models.
- Model quality depends on the local models: a 7B coder is good for everyday code, but it is not a frontier cloud model.
- Everything runs locally — if Ollama is not running, the assistant cannot answer.

## 🇧🇩 বাংলা

**Continue বাংলা — VS Code-এ বাংলায় AI কোডিং সহকারী।**

- `config.yaml` — তৈরি কনফিগ: চ্যাট আর এডিটের জন্য `qwen2.5-coder:7b`, অটোকমপ্লিটের জন্য `starcoder2:3b` (দুটোই লোকাল Ollama)।
- `rules-bangla.md` — নিয়ম: কোড বাংলায় বোঝাবে, API বানিয়ে বলবে না।
- `prompts-bangla.md` — বাগ ঠিক করা, ফিচার যোগ করা, কোড বোঝানো, টেস্ট লেখার তৈরি প্রম্পট।
- কোড আপনার কম্পিউটারের বাইরে যায় না — কোনো key লাগে না।

## 📄 License

MIT — use it however you like; credit is appreciated.
