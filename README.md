# freelance-ops

A freelance back office that runs itself: pulls jobs from open job APIs, filters them with my own rules, stores them in SQLite, scores them with an LLM, drafts proposals, and pings me on Telegram.

## Pipeline

`APIs → rules → SQLite → LLM score → proposal draft → Telegram → weekly report`

## Stack

Python 3.12 · `httpx` · `sqlite3` · GitHub Actions · Telegram Bot API · Claude API. No framework.

Sources: Remotive, Arbeitnow (RemoteOK, Himalayas, Jobicy later).

## Run

    python -m venv .venv
    .venv\Scripts\activate
    pip install -r requirements.txt
    python -m src.main

## Roadmap

- [ ] 01 — Jobs from open APIs into one table
- [ ] 02 — Rules as code + SQLite (no duplicates)
- [ ] 03 — Telegram alerts + GitHub Actions schedule
- [ ] 04 — LLM scoring 0–10
- [ ] 05 — Proposal drafts (draft ≠ send)
- [ ] 06 — Tracker + weekly report → v1.0

Built in public — youtube.com/@waldowdev
