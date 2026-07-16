# Awesome Safe-RL-QP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of robots, controllers, and projects built on **Acc-CBF-QP**, an mc_rtc-based safety filter framework that enforces Control Barrier Function constraints on Reinforcement Learning policies at runtime.

Acc-CBF-QP was introduced in:

> **Safe Execution of RL Policies via Acceleration-based CBF-QP Constraint Enforcement for Real-World Robotic Deployments**
> Bastien Muraccioli*, Alice Cariou*, Pierre-Alexandre Leziart, Mathieu Celerier, Arnaud Demont, Gentiane Venture, Mehdi Benallegue
> IROS 2026 — [Paper](https://hal.science/hal-05362571) · [Project page](https://safe-rl-qp.github.io/)

This list tracks the ecosystem around the framework: the core implementation, install tooling, a starting template for new robots/policies, and community-built controllers. If you've built something on top of Acc-CBF-QP, please [add it](CONTRIBUTING.md)!

## Contents

- [Core Framework](#core-framework)
- [Getting Started](#getting-started)
- [Community Controllers](#community-controllers)
- [Related Projects](#related-projects)
- [Contributing](#contributing)
- [License](#license)

## Core Framework

| Project | Description |
|---|---|
| [Acc-CBF-QP](TODO-core-framework-repo-url) | The core framework: acceleration-based CBF-QP safety filter for mc_rtc. Includes the version used in the IROS 2026 paper (see the `TODO-tag-name` tag). |

## Getting Started

| Project | Description |
|---|---|
| [Acc-CBF-QP Superbuild](TODO-superbuild-repo-url) | CMake superbuild that installs the full framework, dependencies, and a ready-to-run Unitree H1 policy example. Start here if you want to try it out. |
| [Acc-CBF-QP Template](TODO-template-repo-url) | Template controller for adapting the framework to a new robot or a new RL policy. Includes a roadmap of planned features. |

## Community Controllers

Controllers, robots, and RL policies built on top of the framework by the community.

<!--
Please keep this table sorted alphabetically by project name.
Format: | [Project Name](link) | Robot | Author/Org | One-line description |
-->

| Project | Robot | Author | Description |
|---|---|---|---|
| _Be the first to add yours!_ | | | |

## Related Projects

| Project | Description |
|---|---|
| [mc_rtc](https://github.com/jrl-umi3218/mc_rtc) | The robot control framework Acc-CBF-QP is built on. |

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for the submission guidelines before opening a PR.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

This list is released under [CC0](LICENSE) (public domain). Note this covers the *list* only — each linked project has its own license, and the Acc-CBF-QP framework itself is licensed separately (see its repository).
