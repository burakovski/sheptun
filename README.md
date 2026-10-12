# Sheptun · sheptun-stt

**Whisper it. I’ll write it down.**

Private, in-browser speech-to-text with a tavern fantasy UI. Audio never leaves your machine — Whisper and an optional local LLM run entirely in the browser.

**Use it:** [https://sheptun.vercel.app](https://sheptun.vercel.app)  
**Code:** [burakovski/sheptun](https://github.com/burakovski/sheptun)

[![License: MIT](https://img.shields.io/badge/License-MIT-burgundy.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> **Русский:** [Кратко по-русски](#русский) · полный UI на русском и английском.

---

## Share this

Give people the live link — not a downloaded HTML file:

```text
https://sheptun.vercel.app
```

Opening `index.html` from Telegram / `file://` breaks the app on phones. The Vercel URL is the product.

## Why this name?

**Sheptun** (Шептун) is a playful take on a “whisperer” — close to [OpenAI Whisper](https://openai.com/research/whisper), but as a friendly tavern character who *listens* and *writes*.  
GitHub: [burakovski/sheptun](https://github.com/burakovski/sheptun). Display name: **Sheptun**.

---

## Features

- **100% local STT** — Hugging Face Transformers.js + Whisper (`tiny` / `base` / `small`, auto-picked)
- **Optional local LLM** — WebLLM (WebGPU) for clean-up, business style, notes, protocol, letter
- **Translate to English** with CEFR level (A1–C2)
- **File upload or mic recording**
- **No account, no backend, no telemetry** from this app
- **RU / EN UI**
- Responsive layout (desktop · tablet · phone)

## Quick start

```bash
git clone https://github.com/burakovski/sheptun.git
cd sheptun
python3 -m http.server 8765
# open http://127.0.0.1:8765
```

Or open `index.html` via any static server.

**Share with users:** [https://sheptun.vercel.app](https://sheptun.vercel.app) (preferred). Local/`file://` HTML is for development only.

**Requirements**

| Need | Notes |
|------|--------|
| Modern Chromium / Firefox / Safari | Chrome/Edge recommended for WebGPU |
| WebGPU | Optional; needed for LLM styles / EN CEFR rewrite |
| Disk / RAM | First run downloads models into browser cache |

## Usage

1. Drop an audio file **or** record with the mic  
2. Pick language (or Auto) and style  
3. Hit **Mine the text** / **Добыть текст**  
4. Copy the result; optionally enable **Translate to English** + CEFR  

Styles: Clean · Business · Notes · Minutes · Letter.

## Privacy

- Audio is decoded and transcribed **in your browser**
- Models are fetched from public CDNs/Hugging Face on first use and cached by the browser
- This repository does not include a server that receives your audio

## Stack

| Piece | Tech |
|-------|------|
| UI | Single `index.html` + CSS + vanilla JS |
| STT | [`@huggingface/transformers`](https://github.com/huggingface/transformers.js) · Whisper |
| LLM | [`@mlc-ai/web-llm`](https://github.com/mlc-ai/web-llm) (optional) |
| Icons | [Lucide](https://lucide.dev) |

## Project layout

```
sheptun/
├── index.html          # app (UI + logic)
├── assets/             # bg, hero, frame, parchments, logo
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
└── .gitignore
```

## Browser support

- **STT:** Chromium, Firefox, Safari (WASM; WebGPU accelerates when available)
- **LLM rewrite / CEFR EN:** WebGPU required (Chrome/Edge best)

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Please follow the [Code of Conduct](CODE_OF_CONDUCT.md).

## Security

Please report vulnerabilities privately — see [SECURITY.md](SECURITY.md).

## License

[MIT](LICENSE) © Sheptun contributors.

Third-party models (Whisper, Qwen, Llama, Phi, etc.) remain under their own licenses — review upstream terms before redistribution or commercial use.

## Credits

- Character & tavern art — project assets in `assets/`
- Whisper — OpenAI; browser runtime via Transformers.js
- WebLLM — MLC

---

## Русский

**Sheptun (Шептун)** — локальный speech-to-text в браузере: прошептал — получил текст. Аудио не уходит на сервер.

**Пользоваться / шарить:** [https://sheptun.vercel.app](https://sheptun.vercel.app)

```bash
python3 -m http.server 8765   # локальная разработка
```

Репозиторий: [burakovski/sheptun](https://github.com/burakovski/sheptun).  
Стек: Transformers.js (Whisper) + опционально WebLLM для стилей и перевода на английский (CEFR).
