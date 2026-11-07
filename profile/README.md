<div align="center">

<img
  src="https://raw.githubusercontent.com/Arynwood-Technology/.github/main/assets/logo.png"
  alt="Arynwood Technology"
  width="240"
/>

# Arynwood Technology

### Open Source · Local-First Software · Independent Infrastructure

**Community software and creative tools on hardware you control.**

We build self-hosted community platforms, personal AI workspaces,
creative applications, and practical tools for independent computing.

Our work focuses on software ownership, open standards,
transparent development, and infrastructure you can operate yourself.

[Website](https://arynwood.com/) ·
[Setup Services](https://arynwood.com/#services) ·
[Developer](https://dev.arynwood.com/)

</div>

---

## Featured Projects

### [Arynwood Grove](https://github.com/Arynwood-Technology/arynwood-community)

**Self-hosted community software.**

Grove brings a group's calendars, conversations, files, plans,
and websites together on its own server.

Members access their community through a browser, while owners
manage membership, spaces, and appearance.

**Latest release: v0.7.4**

- Self-hosted community infrastructure
- Browser-based collaboration
- Configurable membership and community spaces
- Verified release delivery and build-provenance attestations
- Open source under AGPL-3.0

Formerly Arynwood Community. Existing Community 0.3
installations can upgrade in place.

[Source](https://github.com/Arynwood-Technology/arynwood-community) ·
[Downloads](https://github.com/Arynwood-Technology/arynwood-community/releases/latest) ·
[Manual](https://github.com/Arynwood-Technology/arynwood-community/blob/main/docs/MANUAL.md) ·
[Community](https://community.arynwood.com/)

---

### [Arynwood MCP](https://github.com/Arynwood-Technology/ArynwoodMCP)

**A personal AI and creative workspace for your desktop.**

Arynwood MCP brings local AI models, documents, design,
audio, video, and supervised tools into a unified desktop environment.

Available for Linux and Windows, with Grove accessible
through its integrated Community page.

**Latest release: v0.5.4 — Alpha**

- Local AI model integration
- Document and creative workflows
- Supervised tool execution
- Linux and Windows desktop packages
- Signed checksums and verified build provenance
- Open source under AGPL-3.0-only

Version 0.5.4 includes security and recording fixes,
hashed build dependencies, and property-based fuzz testing.

The main branch requires pull requests and passing backend,
frontend, API-reference, and Windows checks.

Official package verification and owner signing passed
before publication.

**Current limitations:** Desktop packages remain alpha.
Models and supporting services must be installed separately.

[Source](https://github.com/Arynwood-Technology/ArynwoodMCP) ·
[Downloads](https://github.com/Arynwood-Technology/ArynwoodMCP/releases/latest) ·
[Browser Demo](https://arynwood-technology.github.io/ArynwoodMCP/) ·
[Security](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/SECURITY.md)

---

## Software in Development

Projects at different stages of development, from early
prototypes to downloadable prereleases.

| Project | Description | Status | License |
|:---|:---|:---|:---|
| [Cutroom](https://github.com/Arynwood-Technology/Cutroom) | Kdenlive-based video editor | v0.1.0 prerelease | GPL-3.0 |
| [Chat Window](https://github.com/Arynwood-Technology/arynwood-chat-window) | Website chat grounded in public pages using a self-hosted model | v0.2.0 alpha | AGPL-3.0 |
| [Open Knowledge](https://github.com/Arynwood-Technology/arynwood-open-knowledge) | Educational research and inclusive-learning prototype | Prototype | MIT |

### Development Notes

**Cutroom**

A Kdenlive-based video editor with a Linux Flatpak
prerelease available.

The separate assistant tool server has not yet been published.
The editor download does not include that service.

**Chat Window**

An experimental website chat application that uses a model
you operate to answer questions grounded in public website content.

Version 0.2.0 is tagged, but no GitHub release has been published.

**Open Knowledge**

An educational research prototype exploring inclusive learning,
browser-local records, and public metadata search.

No published release is currently available.

---

## Research & Technical Guides

Research, benchmarks, and practical documentation
for open-source development and local computing.

### Research Repositories

**[SDXL LoRA Portability Study](https://github.com/Arynwood-Technology/arynwood-lora-training)**

Research into subject-identity transfer between SDXL derivatives.

Includes reproducible scripts, methodology, and trained checkpoints.
Personal training images are not publicly distributed.

License: CC BY 4.0

[Research Repository](https://github.com/Arynwood-Technology/arynwood-lora-training) ·
[DOI: 10.5281/zenodo.21282393](https://doi.org/10.5281/zenodo.21282393)

**[Local AI Benchmarks](https://github.com/Arynwood-Technology/local-ai-benchmarks)**

CPU and GPU inference performance measurements,
with scripts for benchmarking local AI models
on your own hardware.

License: MIT

[Benchmark Repository](https://github.com/Arynwood-Technology/local-ai-benchmarks)

### Technical Guides

- [Running Local AI Without a GPU](https://arynwood.com/local-ai-cpu-only.html)
- [Running Local AI on Linux](https://arynwood.com/local-ai-linux.html)

---

## Engineering & Release Practices

Arynwood Technology develops and maintains its software
using documented engineering, testing, and release processes.

### Security & Quality

Grove and MCP include:

- Automated test suites
- CodeQL static analysis
- Public OpenSSF Scorecard results
- Documented release verification
- OpenSSF Best Practices Passing badges

Both projects have earned the OpenSSF Best Practices
**Passing** badge through public project self-assessments.

These badges represent standing against published
best-practice criteria. They are not security certifications.

Dependency and maintenance findings are tracked separately.

### Release Verification

| Project | Release | Verification |
|:---|:---|:---|
| Arynwood Grove | v0.7.4 | Verified checksums and tagged-build attestations |
| Arynwood MCP | v0.5.4 | Verified Linux/Windows artifacts and owner-signed checksums |

**Important:** The MCP Windows installer does not currently
have Windows code signing.

Each repository documents its own security policy,
supported functionality, and known limitations.

---

## Development & Maintenance

Arynwood Technology is independently developed and maintained.

A single maintainer oversees:

- Software architecture and implementation
- Code review and automated testing
- Release preparation and verification
- Infrastructure and server operations
- Security reporting and maintenance

Our development process, contribution expectations,
and reporting routes are documented here:

**[How We Build](https://github.com/Arynwood-Technology/.github/blob/main/HOW-WE-BUILD.md)**

Security vulnerabilities should be reported privately
through the affected repository's **Security** tab.

### Project Maturity

Arynwood MCP is a single-owner desktop application in alpha.

Arynwood Grove is independently operated community software.

Other repositories have their own prototype, alpha,
or prerelease limitations.

Refer to individual project documentation before deployment.

---

<div align="center">

## Independent Software. Your Infrastructure.

We believe people should be able to understand,
modify, maintain, and operate the software they depend on.

**Your projects and data belong on hardware you control.**

Local-first does not mean every feature operates offline.
Network functionality may contact configured services when used.

---

[Website](https://arynwood.com/) ·
[GitHub](https://github.com/Arynwood-Technology) ·
[Developer](https://dev.arynwood.com/)

<sub>Built and maintained by Arynwood Technology.</sub>

</div>
