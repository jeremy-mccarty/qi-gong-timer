# 氣功 Qi Gong Timer

A simple, offline-capable timer for 5-minute Qi Gong movement routines. Three interchangeable flows to keep things fresh — just pick one, press play, and move.

![Qi Gong Timer](screenshot.png)

## Routines

- **Shake & Swing** — fluid, flowy movements focused on arm swings and body waves
- **Loosen Up** — joint mobility and isolation work, from rag dolls to wrist rolls
- **Full Flow** — a complete full-body pass hitting everything head to toe

Each routine runs about 5 minutes. The timer chimes when it's time to switch movements and gives a countdown beep at 3 seconds.

## Use It

**The app is live at [`https://jeremy-mccarty.github.io/qi-gong-timer/`](https://jeremy-mccarty.github.io/qi-gong-timer/)**

### Add to Home Screen (iOS / Android)

1. Open the link above in Safari (iOS) or Chrome (Android)
2. Tap **Share → Add to Home Screen**
3. It launches fullscreen like a native app

### Run Locally

Download `index.html` and open it in any browser. That's it.

## Offline Support

The app uses a service worker to cache everything after the first load. Once cached, it works fully offline — no internet needed.

## Customizing

All three routines live in the `ROUTINES` object inside `index.html`. Each step has three fields:

```js
{ name: "Movement Name", duration: 30, desc: "Brief cue for the movement" }
```

Add, remove, or tweak steps as needed. If you change anything, bump the cache version in `sw.js` (e.g. `qigong-v1` → `qigong-v2`) so the service worker picks up the update.

## Built With

Vanilla HTML, CSS, and JavaScript. No frameworks, no build tools, no dependencies.
