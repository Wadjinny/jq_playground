# jq playground

In-browser [jq](https://jqlang.org/) playground. JSON and filters run entirely in the browser via WASM (jq 1.7); nothing is sent to a server.

**Live:** [jq-playground.w-ilyas.site](https://jq-playground.w-ilyas.site)

## Features

- Full jq 1.7 in the browser (biowasm / Aioli)
- Monaco editors for input, filter, and output
- Common jq flags (compact, sort-keys, raw-in/out, slurp, …)
- Shareable URL query params; dark/light theme

## Run locally

Static site — no build step:

```bash
# from repo root, e.g.
python3 -m http.server -d frontend 8080
```

Then open http://localhost:8080.

## Deploy

Push to `main` rsyncs `frontend/` over SSH and updates the Caddy site config.
