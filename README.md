# Capture Engine (OSS)

A local, open-source arbitrage monitor for Solana with a terminal‑style UI.

## Features
- Real‑time opportunity detection (simulated multi‑DEX quotes around Jupiter reference)
- Live feed with profit, bps, TTL and basic stats
- Non‑custodial, read‑only (no wallet required)

## Requirements
- Python 3.10+

## Installation
```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## Run
```bash
python capture.py
```
Then open `http://localhost:8080`.

## Notes
- SSE/WebSocket handled via Flask‑SocketIO; UI updates are pushed in real‑time.
- Data-plane in this open package simulates cross‑venue price variations around Jupiter quotes.
- Intended for local use and educational/demo purposes.

## Project layout
```
capture.py              # Flask + Socket.IO server and arbitrage monitor
templates/          # Jinja templates (dashboard + sections)
static/             # CSS/JS assets
requirements.txt    # Python deps
README.md           # This file
```
