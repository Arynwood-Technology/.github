# How we build

I'm Lorelei. I've built Arynwood over about three years, designing, testing and running it
myself. I design the architecture, decide the scope, review changes, run the tests, ship
releases and operate the servers. This is a one-person project; I remain responsible for
what I ship.

Claude Code and Codex work with me as pair programmers. They help write and review code,
documentation and tests; I decide what belongs in the project. Some commits carry a
co-author trailer naming the assistant, and not every assisted commit does. Trailers are
not a complete record of assistance. TODO(Lorelei): trailer policy from now on.

The public [CLAUDE.md](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/CLAUDE.md)
and [AGENTS.md](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/AGENTS.md)
are the instructions I give assistants in that repository, kept public on purpose. They
record scope, architecture, protections and the mistakes I want the next session to avoid.
They describe my working process; they are not proof that every change is correct.

## What changes go through

These are the workflows on the default branches, checked on 2026-10-24:

- **Arynwood MCP:** `ci.yml` runs on pushes to main and pull requests. It runs pytest on
  Python 3.11, then frontend `npm ci`, `npm run build`, `npm run build:demo`, `npm test`
  and `node scripts/check-lint-baseline.mjs`. `release.yml` (Release (Linux)) runs on tags:
  it runs CI, freezes the backend with PyInstaller, smoke-tests it, stages GStreamer,
  builds the Tauri AppImage and .deb, writes SHA-256 checksums and attests provenance.
  `windows.yml` runs on PRs, tags and manual dispatch; it packages and smoke-tests the
  installer and attests it on tags. The manual `verify-release.yml` checks a draft's
  run against its tag, checksums, .deb version and `gh attestation verify`; it extracts
  the AppImage, checks for private configuration/database/memory files, smoke-tests the
  frozen backend, tests media in real WebKitGTK, and attaches the Windows installer.
  `deploy-demo.yml` deploys the demo to GitHub Pages. Attestations were added **after
  0.5.3**; **0.5.4 will be the first release with them**.
- **Arynwood Grove:** only `release.yml`, triggered by tags. It checks the version,
  backend unittests, frontend lint and tests, and installer syntax, then packages,
  attests and publishes. **There is no push or PR CI.**
  TODO(Lorelei): decide whether to add push/PR checks.
- **Chat Window:** `tests.yml` runs pytest on Python 3.10, 3.11 and 3.12 for main pushes
  and pull requests. It has a v0.2.0 tag, but no GitHub release.
- **Open Knowledge:** `ci.yml` (Validate) runs `npm test`, the build, `npm run evaluate`
  and `npm audit`.
- **Local AI benchmarks:** only `huggingface.yml`, mirroring the dataset to Hugging Face.
  There is no automated test suite; the mirror is not test CI.
- **LoRA study:** no workflows and no tests. The published scripts and methodology
  describe a pipeline; the personal photo dataset is not public.
- **Cutroom:** no Arynwood CI workflow on its default branch. Its v0.1.0 is a pre-release.
  A full Kdenlive build is substantial; a documentation-only change gets link checks
  and an explicit statement when that build wasn't run.

Passing checks say something about the cases they cover, not every use of an alpha.
Each PR should say exactly what ran, what passed and what wasn't run.

## Problems and security reports

For ordinary problems, open an issue in the project concerned with the version, platform,
steps and expected result. Remove private information. I review reports as time permits;
I cannot promise an immediate reply or a release date.

Don't post a vulnerability in a public issue. Read the repository's SECURITY.md first; it
says how to report privately:
[Arynwood MCP](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/SECURITY.md),
[Open Knowledge](https://github.com/Arynwood-Technology/arynwood-open-knowledge/blob/main/SECURITY.md)
and [Cutroom](https://github.com/Arynwood-Technology/Cutroom/blob/main/SECURITY.md).

Grove, Chat Window, the LoRA study and the benchmarks don't have a SECURITY.md yet. For those,
open an issue asking for a private contact, without exploit details or secrets.
TODO(Lorelei): publish Grove's security policy, and decide on one reporting channel for every repo.
