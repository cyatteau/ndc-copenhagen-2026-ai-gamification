# AI-Powered Gamification for the Web

Demo repo for **AI-Powered Gamification for the Web**, a talk for **NDC Copenhagen 2026**.

This talk explores how AI can make gamified web experiences feel more responsive, more personal, and less gimmicky. The demos focus on small, practical loops: the app observes a signal, AI helps make a decision, and the UI responds in a way the user can actually feel.

## Talk theme

Good gamification is not just points, badges, or confetti. The useful version helps an app create:

- **Progress**: make momentum visible
- **Feedback**: respond in a way that feels relevant
- **Challenge**: adjust pacing so the experience stays balanced
- **Reward**: make unlocks feel connected to what the user actually did

The core pattern used throughout the talk is:

```txt
Signal -> AI decision -> UI response
```

## Repo contents

| File | Description |
| --- | --- |
| [`slides.pdf`](./slides.pdf) | Slide deck for the talk |
| [`demo-1`](./demo-1) | Dynamic Fact Finder: place-grounded AI facts and rewards |
| [`demo-2`](./demo-2) | Sentiment Snapshot: tone-aware feedback routes |
| [`demo-3`](./demo-3) | Adaptive Challenge Lab: browser-side difficulty tuning |
| [`demo-final`](./demo-final) | GeoExplorer: combined map, challenge, mood, reward, and recap experience |

## Demos

### Demo 1: Dynamic Fact Finder

A location-based demo that uses place context to generate fresh fact cards, progression, and a visual reward.

**Pattern:** dynamic content generation  
**Signal:** selected place, fact type, current location  
**AI decision:** generate a structured fact card  
**UI response:** render the fact, update progress, unlock a map snapshot and postcard reward

### Demo 2: Sentiment Snapshot

A feedback demo that analyzes a short player reflection and chooses a better response route.

**Pattern:** sentiment-aware feedback  
**Signal:** player reflection  
**AI decision:** classify sentiment and confidence scores  
**UI response:** adjust the feedback tone, support path, and recovery message

### Demo 3: Adaptive Challenge Lab

A small quiz experience where the browser watches performance signals and adjusts the next round.

**Pattern:** adaptive challenge tuning  
**Signal:** correctness, response time, current difficulty  
**AI decision:** predict the next difficulty level  
**UI response:** change the next question pace and show the prediction

### Final Demo: GeoExplorer

A combined map-based experience that brings the patterns together.

**OpenAI** generates location-based quiz content and session recaps.  
**TensorFlow.js** adapts challenge pacing in the browser.  
**Azure AI Language** reads mood from player reflections.  
**ArcGIS** grounds the experience in real places and interactive maps.

The goal is not to turn every app into a full game. The goal is to show how small AI-powered loops can make an experience feel more reactive, more personal, and more engaging.

## Tech used

- HTML, CSS, and JavaScript
- ArcGIS Maps SDK for JavaScript and ArcGIS location services
- OpenAI Responses API with structured outputs
- Azure AI Language sentiment analysis
- TensorFlow.js
- Canvas Confetti
- Browser local storage

## Running locally

These demos are designed as lightweight, presentation-friendly web demos.

Clone the repo:

```bash
git clone https://github.com/cyatteau/ndc-copenhagen-2026-ai-gamification.git
cd ndc-copenhagen-2026-ai-gamification
```

Start a local static server:

```bash
python -m http.server 5173
```

Then open:

```txt
http://localhost:5173
```

Depending on your browser and how the files are served, you may want to rename the demo files with `.html` extensions or place each demo in a folder with an `index.html` file.

## API keys and security

These demos use external services. For a real project, do **not** commit production API keys to GitHub.

Recommended setup:

- Keep OpenAI and Azure keys on a backend or serverless function
- Restrict ArcGIS API keys to the required services and allowed referrers
- Use environment variables for secrets
- Rotate any keys that were used during local prototyping
- Treat frontend-only API calls as demo-only unless the service and key restrictions are appropriate

## Presentation flow

Suggested talk order:

1. Why shallow gamification fails
2. What good gamification should do
3. Signal, decision, response framing
4. Demo 1: dynamic content
5. Demo 2: sentiment-aware feedback
6. Demo 3: adaptive challenge tuning
7. Final demo: GeoExplorer
8. Practical build takeaways

## Key takeaway

AI does not need to be the whole feature.

A useful AI-powered gamification loop can be small:

```txt
Notice one meaningful signal.
Make one focused decision.
Change one part of the experience.
```

That is often enough to make a web app feel more alive.
