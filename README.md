# SignalBridge

SignalBridge is a clean-room product prototype for helping people narrow down common home internet problems and prepare a concise support handoff.

## What works

- Four-step responsive flow: describe the issue, report safe checks, review a cautious rules-based suggestion, and prepare a support summary.
- Issue routing distinguishes a likely device or service issue, a possible Wi-Fi/router/provider connection issue, and cases with too little evidence.
- Copy and download actions generate a text handoff from the answers entered in the current browser tab.
- Reset clears the current flow. There is no account, backend, analytics, browser storage, router access, or network request in the prototype.
- Keyboard-friendly native controls, visible focus behavior, mobile layout, and reduced-motion support.

## Important limits

This is a reconstructed implementation based on the SignalBridge concept discussed in this project. It is not recovered original source code. The guided checks are self-reported; the app cannot inspect a router, measure speed, run a network probe, or confirm an ISP outage. The diagnosis is a transparent heuristic and must not be presented as a verified cause.

## Run locally

Serve `dist/` with any static HTTP server, then open its local URL. For example:

```sh
python3 -m http.server 8000 --directory dist
```

Open `http://localhost:8000`.

## Product documentation

See [PRODUCT_BRIEF.md](PRODUCT_BRIEF.md) for the problem hypothesis, MVP scope, discovery plan, proposed measures, experiment, risks, and roadmap. Proposed targets are hypotheses to validate, not achieved results.
