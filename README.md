# NANO DATA

**Keep the source. Carry the purpose. Continue the work.**

NANO DATA is a source-linked AI handoff prototype. It retains the original record, purpose, reason and next action; produces a compact CORE; then lets a separately reviewed receiver request continue the task. Saved results and references remain available for human inspection.

## Official source distribution

The full source is distributed in **[NANO_DATA_MATCHING_PILOT_SOURCE_20261027.zip](NANO_DATA_MATCHING_PILOT_SOURCE_20261027.zip)** in this repository. GitHub's code browser shows this archive, not an expanded source tree. Download and extract it to inspect all source modules, frontend assets, tests, migrations, build files and setup instructions. It is source code, not only an executable binary. The root MIT license is an unchanged copy of the license inside the archive; its original copyright attribution is retained.

[Exact file map and checksum](SOURCE_ARCHIVE_SHA256.txt) · [MIT license](LICENSE)

### Download, verify and run offline tests

Download the source ZIP and `SOURCE_ARCHIVE_SHA256.txt` from this repository into the same directory. On a system with `sha256sum` and `unzip`:

```sh
sha256sum --check SOURCE_ARCHIVE_SHA256.txt
unzip NANO_DATA_MATCHING_PILOT_SOURCE_20261027.zip
cd nano-data-source
# Node.js 24 or later; these tests use local SQLite and mocked model transports.
npm test
npm run test:bundle
npm run test:judge-bundle
```

The archive has exactly one root directory, `nano-data-source/`. For rebuilding:

```sh
# Downloads the lockfile-pinned esbuild dependency and runs its install script.
npm ci
npm run build
```

The supplied generated worker is included. This packaging run reproduced its exact hash using esbuild 0.28.2. Offline verification passed 192 source tests, 37 owner-bundle tests and 20 judge-bundle tests. Those tests are not real inference or a measurement of model quality.

## NVIDIA and Nebius

The prototype uses `nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B` through Nebius Token Factory's server-side chat-completions API. Producer and receiver are separate requests to the configured model, not independent vendors. The frontend and database layer use Cloudflare Workers and D1. Provider keys belong only in server secret storage; none are included in this repository or sent to the browser.

See the extracted `README.md`, `.env.example`, `.env.judge-trial.example` and `JUDGE_TRIAL_DESIGN_HISTORY.md` for server bindings, disabled defaults and setup boundaries. These environment files are inventories, not automatic configuration. The runtime is a Cloudflare Worker, not a standalone Node HTTP server. Deployment requires separately provisioned databases, server settings and authorized credentials. The supplied test suite works offline without those operational resources. Do not reuse a historical policy label as permission to send requests.

## Source and deployment identity

Archive SHA-256:

```text
159b53e64199177abd937cb0536b2c86d7020423183aed3f7dd4771fd38f98a8
```

Bundled `nano-data-source/worker.mjs` SHA-256:

```text
b713c01d5da5e73507fe5a967c1f1b05894adff4d9943ca82da088b7a8e96421
```

This matches the local runtime bundle in the recorded 27 October 2026 15:46:49 UTC pilot deployment, version `55f4eab8-6e67-42bc-9b36-c47087755cbb`. This is a dated operator deployment record and reproducible source identity, not a fresh extraction from the host or a claim that no later deployment exists. The ZIP is unchanged from the verified source package. `SHA256SUMS.json` inside verifies 73 payload files; the archive contains 74 files including that manifest.

Nonsensitive pilot labels, public hostname and the 27 October 2026 18:00 UTC cutoff remain in executable code to preserve exact reproducibility. They are not credentials. The bridge is deliberately bounded and expires; do not broaden it for a new installation. Leave `JUDGE_TRIAL_PILOT_BRIDGE` unset and use separately reviewed isolated-judge provisioning for a new deployment. Operational hosting config, database/account identifiers, private access codes, grant hashes and authentication files are excluded.

## What has and has not been demonstrated

A historical real Nemotron-through-Nebius synthetic handoff produced a receiver preparation checklist, retained the listed resources and unknown outcomes, and was saved and reopened with its original reference. That useful result followed an explicitly approved additional receiver trial; it is not a first-attempt success-rate claim. The 150-second video is a replay of saved application work, not new live inference: https://youtu.be/7pmSm6-GUSA . Public visibility was reported by the operator on 27 October at approximately 09:26 UTC; this README does not independently establish current playback or visibility.

The later dated pilot deployment was recorded with **zero real pilot model calls** at the reviewed checkpoint. Historical real inference must not be attributed to that pilot as though it were a successful new run. Local tests, deployment and saved-result playback are different kinds of evidence.

General lossless compression, superiority over other models, cost savings, unrestricted autonomous execution and final judging readiness are not established. A finite, non-distributed two-call pilot ending at 18:00 UTC is not the final judging-period access contract. Public source publication does not resolve that contract. Session-bound storage has limitations; elapsed retention does not prove physical deletion, and no production purge scheduler is claimed. Cost guards are estimates, not billing hard caps. Final judge access, continued availability and final submission remain separate work.
