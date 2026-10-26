# Arynwood Technology

**Community software and creative tools on hardware you control.** Arynwood builds
shared spaces for people, a personal desktop workspace, and tools for making and
organizing creative work.

<img src="https://raw.githubusercontent.com/Arynwood-Technology/.github/main/assets/logo.png" alt="Arynwood Technology" width="120" height="120">

[Website](https://arynwood.com/) · [Setup services](https://arynwood.com/#services) · [Lorelei Noble](https://dev.arynwood.com/)

## The projects

### [Arynwood Grove](https://github.com/Arynwood-Technology/arynwood-community)

A place for a group's calendars, conversations, files, plans and websites, on its
own server. Members use their browsers; owners choose the people, spaces and look.
**0.7.4 is published**, with verified release delivery and build-provenance
attestations. Open source under the AGPL-3.0. Formerly Arynwood Community;
Community 0.3 installations can upgrade in place.

[Downloads](https://github.com/Arynwood-Technology/arynwood-community/releases/latest) · [Manual](https://github.com/Arynwood-Technology/arynwood-community/blob/main/docs/MANUAL.md) · [Visit Arynwood's Grove](https://community.arynwood.com/)

### [Arynwood MCP](https://github.com/Arynwood-Technology/ArynwoodMCP)

A personal AI and creative workspace for Linux and Windows desktops: local models,
your documents, design, audio, video and supervised tools, with your Grove inside
the Community page. Open source under AGPL-3.0-only; desktop packages remain alpha.
Models and supporting services are installed separately.

**0.5.4 is published with signed checksums and verified provenance.** It adds security
and recording fixes, hashed build dependencies and property fuzzing. Main now
requires pull requests and passing backend, frontend, API-reference and Windows
checks. Official package verification and owner signing passed before publication.

[Downloads](https://github.com/Arynwood-Technology/ArynwoodMCP/releases/latest) · [Browser demo](https://arynwood-technology.github.io/ArynwoodMCP/) · [Security and limitations](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/SECURITY.md)

### More work in progress

- **[Cutroom](https://github.com/Arynwood-Technology/Cutroom):** a Kdenlive-based video editor,
  with a Linux Flatpak **0.1.0 prerelease**, GPL-3.0. The separate assistant tool
  server is not yet published; the editor download does not supply that service.
- **[Chat Window](https://github.com/Arynwood-Technology/arynwood-chat-window):** website chat
  grounded in public pages through a model you run. Alpha, tagged 0.2.0; no published
  GitHub release. AGPL-3.0.
- **[Open Knowledge](https://github.com/Arynwood-Technology/arynwood-open-knowledge):** an
  educational research and inclusive-learning prototype with browser-local records
  and public metadata search. No published release. MIT.

## Where the projects stand

Grove and MCP have automated tests, CodeQL analysis, public OpenSSF Scorecard
results and documented release checks. Their best-practices badges are still in
progress. Some dependency and maintenance findings remain open; these are tracked,
not hidden or presented as completed certification.

Grove's 0.7.4 downloads have verified checksums and tagged-build attestations. MCP 0.5.4
adds verified Linux/Windows artifacts and owner-signed checksums. The Windows
installer remains without Windows code signing.

Each project's README and security policy describe its own scope. MCP is a
single-owner desktop alpha, Grove is separately operated community software, and
the other projects have their own prototype or prerelease limits.

## Research and guides

- **[SDXL LoRA portability study](https://github.com/Arynwood-Technology/arynwood-lora-training):**
  subject-identity transfer between SDXL derivatives, with scripts, methodology and
  trained checkpoints. Personal training images are not public. CC BY 4.0;
  [DOI 10.5281/zenodo.21282393](https://doi.org/10.5281/zenodo.21282393).
- **[Local AI benchmarks](https://github.com/Arynwood-Technology/local-ai-benchmarks):** measured
  CPU and GPU generation speeds, with scripts to test your own machine. MIT.
- [Local AI without a GPU](https://arynwood.com/local-ai-cpu-only.html).
- [Run local AI on Linux](https://arynwood.com/local-ai-linux.html).

## Maintenance and ownership

One maintainer handles scope, architecture, review, tests, releases and server
operation. [How we build](https://github.com/Arynwood-Technology/.github/blob/main/HOW-WE-BUILD.md)
describes the process and reporting routes. Report vulnerabilities privately using
the affected repository's Security tab.

Your projects and data belong on hardware you control. Network features still
contact their configured services when used; local-first does not imply an
enforced offline mode.
