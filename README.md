# Control Box Project

This repository contains a Rust workspace for simulating and visualizing control systems, featuring a reusable signal library and a Yew-based web application.

## Workspace Structure

- [`control-box`](control-box/Cargo.toml): Core library for control system modeling, including signal traits, PT1 elements, and hysteresis. See [`README`](control-box/README.md)
- [`simulator`](simulator/Cargo.toml): Web application built with [Yew](https://yew.rs/) for interactive signal creation, editing, and visualization.
See [`README of simulator`](simulator/README.md)


## Features

- Modular signal types: step, impulse, superposition, and more ([see signal module](control-box/src/signal/mod.rs))
- Time range configuration and signal composition
- Plotly-based interactive visualizations ([see simulator components](simulator/src/components/))
- Git commit/tag/version info embedded at build time ([see build.rs](simulator/build.rs))
- Modern frontend styling with Tailwind CSS

## Getting Started (for Simulator web-frontend)

### Prerequisites

- [Rust](https://rust-lang.org/)
- [Trunk](https://trunkrs.dev/) (for WASM builds)
- [Node.js](https://nodejs.org/) (for frontend CSS tooling)

### Build & Run

```sh
cd simulator
trunk serve --open
```

Open [http://localhost:8080/control-box](http://localhost:8080/control-box) in your browser.

## Development

- Core signal logic: [`control-box/src/signal/`](control-box/src/signal/)
- Web frontend: [`simulator/src/`](simulator/src/)
- Add new signal types in [`control-box`](control-box/src/signal/)
- Use Trunk for hot-reload and WASM builds

## License

MIT — see [`LICENSE.md`](LICENSE.md)

---

