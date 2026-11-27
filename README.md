# PedalAI — Guitar Pedal Emulator

A browser-based guitar pedal emulator powered by Claude AI. Load real pedal specs by name, tweak knobs, hear the effect live, and train your ear with the built-in ear training mode.

## Features

- 🎸 **Karplus-Strong string synthesis** — physically modelled guitar sounds (chord, single note, palm mute, riff)
- 🔗 **Pedal chain** — stack up to 4 pedals in series
- 🎚 **Real pedal specs** via Claude AI — load any pedal by name
- 👂 **Ear training mode** — identify effects by ear
- 🌙 **Day / Night mode** — with font resizer

## Deploy to Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/pedalai)

1. Push this folder to a GitHub repository
2. Import the repo at [vercel.com/new](https://vercel.com/new)
3. No build settings needed — Vercel detects it as a static site automatically
4. Click **Deploy** — live in ~30 seconds

## API Key

Users supply their **own Anthropic API key** via the in-app panel:

1. Sign up free at [console.anthropic.com](https://console.anthropic.com)
2. Create an API key (API Keys → + Create Key)
3. Add a small credit — $5 covers hundreds of pedal lookups at < $0.01 each
4. Paste the key into the app — it's stored in the browser's localStorage only, never sent to any server

**All audio features and prebuilt pedals work without any API key.**  
The API key is only needed for custom pedal lookup by name.

## Privacy

- API keys are stored in the user's browser localStorage only
- Keys go directly from the browser to Anthropic's API — no backend, no server storage
- No analytics, no tracking

## Tech

Single-file HTML app — no build step, no npm, no frameworks.

- Web Audio API (Karplus-Strong, Schroeder reverb, ping-pong delay)
- Claude AI (`claude-sonnet-4-6`) for pedal spec lookup
- Pure CSS + vanilla JS
