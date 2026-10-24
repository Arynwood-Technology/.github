# Arynwood Technology

Arynwood builds software for people who want their own community spaces, desktop AI and creative tools on hardware they control.

<img src="https://raw.githubusercontent.com/Arynwood-Technology/.github/main/assets/logo.png" alt="Arynwood Technology" width="120" height="120">

I'm Lorelei, the developer behind Arynwood.
I've built it over about three years, designing, testing and running it myself.
I use AI assistants as pair programmers, and I decide the scope, review the work and ship the releases.
I also operate the servers these projects run on.

[Website](https://arynwood.com/) · [Setup services](https://arynwood.com/#services) · [Lorelei Noble](https://dev.arynwood.com/)

## What we build

**[Arynwood Grove](https://github.com/Arynwood-Technology/arynwood-community)** — private community software
for families, friends and teams: calendars, plans, boards, chat, tasks, lists and notes on a server you control.
**v0.7.3** (2026-10-23), AGPL-3.0. Formerly Arynwood Community; Community 0.3 installs upgrade in place.
[Visit Arynwood's Grove](https://community.arynwood.com/).

**[Arynwood MCP](https://github.com/Arynwood-Technology/ArynwoodMCP)** — a local-first AI and creative workspace
for one person's desktop. **v0.5.3** (2026-10-23): Linux x86_64 AppImage/.deb and Windows x64 installer,
all alpha. Models and supporting services are separate.
[Try the browser demo](https://arynwood-technology.github.io/ArynwoodMCP/).

**[Cutroom](https://github.com/Arynwood-Technology/Cutroom)** — an AI-assisted video editor built on Kdenlive.
**v0.1.0 pre-release** (2026-10-12), Linux Flatpak, GPL-3.0. The assistant's separate tool server
is not published yet, so the downloaded editor cannot run that assistant on its own.

**[Chat Window](https://github.com/Arynwood-Technology/arynwood-chat-window)** — a website chat window
that answers from your public pages through a model you run. Alpha; tagged v0.2.0, no GitHub release,
and not yet used with real visitors. AGPL-3.0.

**[Open Knowledge](https://github.com/Arynwood-Technology/arynwood-open-knowledge)** — a local-first educational
research and inclusive learning prototype. Browser-local records, public metadata search and documented
limitations; no GitHub release. MIT.

## Research

**[SDXL LoRA portability study](https://github.com/Arynwood-Technology/arynwood-lora-training)** — scripts and
methodology for subject-identity LoRA transfer across SDXL checkpoints. Personal training images are not public.
GitHub's latest release is **0.1.1**; the README's v0.2.0 DOI label is unresolved.
TODO(Lorelei): reconcile these versions. Declared CC BY 4.0; GitHub detects Other.

**[Local AI benchmarks](https://github.com/Arynwood-Technology/local-ai-benchmarks)** — measured local model
speeds, tool behavior and scripts for checking ordinary hardware. MIT; no releases or test suite.
[CPU guide](https://arynwood.com/local-ai-cpu-only.html).

## How we build

One developer, with Claude Code and Codex as pair programmers. [How we build](https://github.com/Arynwood-Technology/.github/blob/main/HOW-WE-BUILD.md)
describes responsibility, assistant credit, checks and reporting problems.

## Why local-first

Your projects and data belong on hardware you control. Network features still contact outside
services when used; local-first does not mean an enforced offline mode.
