# How we build

I'm Lorelei. I've built Arynwood since mid-2025, starting with ArynCore, designing, testing
and running it myself. I design the architecture, decide the scope, review changes, run the tests, ship
releases and operate the servers. This is a one-person project; I remain responsible for
what I ship.

Claude Code and Codex work with me as pair programmers. They help write and review code,
documentation and tests; I decide what belongs in the project. Earlier commits in some
repositories carry a co-author trailer naming the assistant; those stay in the history. From
October 24, 2026, commits carry no AI attribution trailers. This page is the disclosure instead:
treat any commit as possibly assisted, and as reviewed and shipped by me.

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
- **Arynwood Grove:** `ci.yml` runs on pushes to main and pull requests: backend
  unittests, frontend lint, tests and build, and an installer syntax check. `release.yml`
  runs the same checks on tags, checks the version, then packages, attests and publishes.
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

Arynwood MCP and Arynwood Grove also run **CodeQL** (security-extended queries) on every push
and pull request to main and weekly, and **OpenSSF Scorecard** weekly and on every push to main,
with its score public. **Dependabot** proposes dependency updates weekly; nothing merges by
itself. Every workflow action in those two repositories' security workflows is pinned to a
commit. All eight repositories have **secret scanning with push protection** turned on.

Passing checks say something about the cases they cover, not every use of an alpha.
Each PR should say exactly what ran, what passed and what wasn't run.

## Problems and security reports

For ordinary problems, open an issue in the project concerned with the version, platform,
steps and expected result. Remove private information. I review reports as time permits;
I cannot promise an immediate reply or a release date.

Don't post a vulnerability in a public issue. Every repository here has GitHub's private
vulnerability reporting turned on, and it is the one channel for all of them: open the
repository's **Security** tab and choose **Report a vulnerability**.

What to include is in each repository's SECURITY.md:
[Arynwood MCP](https://github.com/Arynwood-Technology/ArynwoodMCP/blob/main/SECURITY.md),
[Arynwood Grove](https://github.com/Arynwood-Technology/arynwood-community/blob/main/SECURITY.md),
[Open Knowledge](https://github.com/Arynwood-Technology/arynwood-open-knowledge/blob/main/SECURITY.md)
and [Cutroom](https://github.com/Arynwood-Technology/Cutroom/blob/main/SECURITY.md).
The rest follow the [organization's security policy](SECURITY.md).
