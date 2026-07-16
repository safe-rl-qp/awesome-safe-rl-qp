# Awesome Safe-RL-QP [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of robots, controllers, and projects built on **Acc-CBF-QP**, an mc_rtc-based safety filter framework that enforces Control Barrier Function constraints on Reinforcement Learning policies at runtime.

Acc-CBF-QP was introduced in:

> **Safe Execution of RL Policies via Acceleration-based CBF-QP Constraint Enforcement for Real-World Robotic Deployments**
> Bastien Muraccioli, Alice Cariou, Pierre-Alexandre Leziart, Mathieu Celerier, Arnaud Demont, Gentiane Venture, Mehdi Benallegue
> IROS 2026 — [Paper](https://hal.science/hal-05362571) · [Project page](https://safe-rl-qp.github.io/)

This list tracks the ecosystem around the framework: the core implementation, install tooling, a starting template for new robots/policies, and community-built controllers. If you've built something on top of Acc-CBF-QP, please [add it](CONTRIBUTING.md)!

## Contents

- [Paper Implementation](#paper-implementation)
- [Getting Started](#getting-started)
- [Community Controllers](#community-controllers)
- [Related Projects](#related-projects)
- [Contributing](#contributing)
- [License](#license)

## Paper Implementation

| Project | Description |
|---|---|
| [Acc-CBF-QP](https://github.com/safe-rl-qp/mc-safe-rl-qp) | Archived source code of the acceleration-based CBF-QP safety filter for mc_rtc, at the state used for the IROS 2026 paper's experiments. |

## Getting Started

| Project | Description |
|---|---|
| [Acc-CBF-QP Superbuild](https://github.com/safe-rl-qp/safe-rl-qp-mc-rtc-superbuild) | CMake superbuild that installs the full framework, dependencies, and a ready-to-run Unitree H1 policy example. Start here if you want to try it out. |
| [Acc-CBF-QP Template](https://github.com/bastien-muraccioli/new-rl-qp-controller) | Template controller for adapting the framework to a new robot or a new RL policy. Includes a roadmap of planned features. |

## Community Controllers

Controllers, robots, and RL policies built on top of the framework by the community.

<!--
Please keep this table sorted alphabetically by project name.
Format: | [Project Name](link) | Robot | Author/Org | One-line description | Last commit badge |
The "Last Updated" badge is a shields.io live badge — see CONTRIBUTING.md for the exact syntax.
-->

| Project | Robot | Author | Description | Last Updated |
|---|---|---|---|---|
| [hrp5p_rl_qp_controller](https://github.com/bastien-muraccioli/hrp5p_rl_qp_controller) | HRP5-p | Bastien Muraccioli, Hippolyte Leroy ([CNRS-AIST JRL](https://jrl-umi3218.github.io/)) | FSM walking policy | ![Last Commit](https://img.shields.io/github/last-commit/bastien-muraccioli/hrp5p_rl_qp_controller) |
| [rl_controller](https://github.com/isri-aist/rl_controller) | Unitree H1 | Alice Cariou, Bastien Muraccioli, Pierre-Alexandre Leziart ([CNRS-AIST JRL](https://jrl-umi3218.github.io/)) | Gamepad-controllable walking policy | ![Last Commit](https://img.shields.io/github/last-commit/isri-aist/rl_controller) |
| [rl_kinova_ball_balancing](https://github.com/bastien-muraccioli/rl_kinova_ball_balancing_mc_controller) | Kinova Gen 3 | Bastien Muraccioli, Mathieu Celerier ([CNRS-AIST JRL](https://jrl-umi3218.github.io/)) | F/T sensor-based ball balancing policy | ![Last Commit](https://img.shields.io/github/last-commit/bastien-muraccioli/rl_kinova_ball_balancing_mc_controller) |

## Related Projects

| Project | Description |
|---|---|
| [mc_rtc](https://github.com/jrl-umi3218/mc_rtc) | The robot control framework Acc-CBF-QP is built on. |

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for the submission guidelines before opening a PR.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

This list is released under [CC0](LICENSE) (public domain). Note this covers the *list* only — each linked project has its own license, and the Acc-CBF-QP framework itself is licensed separately (see its repository).