# SD SAT-2 — Lumen

A learning management system website demo for the **Round 2 low-level design challenge**.

The project is in [`lumen-demo`](lumen-demo). See its [README](lumen-demo/README.md) for the requested features, API-design coverage, and demo limitations.

## Run

```sh
cd lumen-demo
python3 -m http.server 4173 --bind 127.0.0.1 --directory dist
```

Open http://127.0.0.1:4173.

This is a frontend demo: REST calls and payment are simulated, and demo progress is saved in the browser.
