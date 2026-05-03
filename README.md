# AgriBot — AI Agriculture Assistant

A single-page AI chatbot built for agriculture queries. Supports text, image uploads, and voice messages — all processed through an n8n automation backend.

## Features

- **Text chat** — Ask anything about crops, soil, weather, pests, or farming practices
- **Image input** — Upload a photo of a plant/crop and get AI analysis
- **Voice messages** — Record audio queries; transcribed and answered automatically
- **Markdown responses** — Bot replies render with formatted text, lists, and code blocks

## Tech Stack

| Layer | Tech |
|-------|------|
| Frontend | Vanilla HTML + Tailwind CSS |
| AI Orchestration | n8n (webhook-based) |
| Voice Processing | Web Audio API + MediaRecorder |
| Deployment | GitHub Pages |

## How to Use

1. Open `index.html` in a browser (or visit the GitHub Pages URL)
2. Type a question and press Enter, or click the microphone to record
3. Attach an image using the paperclip icon for visual crop analysis

## Self-Hosting / Configuration

To connect your own n8n instance, update these two constants at the top of the `<script>` block in `index.html`:

```js
const CHAT_WEBHOOK_URL = "https://your-n8n-instance.com/webhook/...";
const AUDIO_WEBHOOK_URL = "https://your-n8n-instance.com/webhook/...";
```

## Project Structure

```
agribot/
├── index.html    # Full app — UI + logic in one file
└── style.css     # Additional styles
```