# Contributing to Sheptun

Thanks for helping improve a private, in-browser STT tool.

## Ways to contribute

- Bug reports and reproducible cases
- UI / a11y / i18n improvements
- Prompt and post-processing quality (without shipping secrets)
- Docs, translations, demos
- Performance (model load, WASM/WebGPU paths)

## Development

```bash
git clone https://github.com/burakovski/sheptun.git
cd sheptun
python3 -m http.server 8765
```

Open `http://127.0.0.1:8765` and hard-refresh after edits (`index.html` is the whole app).

### Conventions

- Keep the app **single-file friendly** unless a split clearly helps
- Prefer **local-first** behavior — no new network calls for user audio
- Match existing visual language (tavern / parchment / frame)
- Add both **RU and EN** strings when touching UI copy (`I18N` in `index.html`)
- Use conventional commits when possible: `feat:`, `fix:`, `docs:`, `refactor:`, `chore:`

## Pull requests

1. Fork and branch from `main`
2. Keep PRs focused and small
3. Describe **what** and **why**; attach screenshots for UI changes
4. Note browser + OS if relevant (especially WebGPU)

## Issues

- Use the bug / feature templates when available
- For STT quality issues, include language, style, model (tiny/base/small), and whether WebGPU/LLM was used — **not** private audio

## Code of Conduct

By participating, you agree to the [Code of Conduct](CODE_OF_CONDUCT.md).
