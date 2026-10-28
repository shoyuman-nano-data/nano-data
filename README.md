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

The supplied generated worker is included. The original package build used esbuild 0.28.2 and passed 192 source tests, 37 owner-bundle tests and 20 judge-bundle tests. For this deadline-only update, the operator reports focused source4/4, focused bundle4/4, owner bundle37/37 and deadline transition1/1 passing; the prior full suites were not rerun by this packaging check. Those tests are not real inference or a measurement of model quality.

## NVIDIA and Nebius

The prototype uses `nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B` through Nebius Token Factory's server-side chat-completions API. Producer and receiver are separate requests to the configured model, not independent vendors. The frontend and database layer use Cloudflare Workers and D1. Provider keys belong only in server secret storage; none are included in this repository or sent to the browser.

See the extracted `README.md`, `.env.example`, `.env.judge-trial.example` and `JUDGE_TRIAL_DESIGN_HISTORY.md` for server bindings, disabled defaults and setup boundaries. These environment files are inventories, not automatic configuration. The runtime is a Cloudflare Worker, not a standalone Node HTTP server. Deployment requires separately provisioned databases, server settings and authorized credentials. The supplied test suite works offline without those operational resources. Do not reuse a historical policy label as permission to send requests.

## Source and deployment identity

Archive SHA-256:

```text
09715bbd9ef2d757b4246504ad34e75fe0bd9338435161a8983468dd096475d6
```

Bundled `nano-data-source/worker.mjs` SHA-256:

```text
d190204be7b45305ac8fb1bdc3f08a7b193ec5b5dc25c830e029428d60886d87
```

This matches the local runtime bundle in the recorded 27 October 2026 17:51:36 UTC pilot deployment, version `978703fa-782f-4b9d-a33b-8f385f347c9e`. This is a dated operator deployment record and reproducible source identity, not a fresh extraction from the host or a claim that no later deployment exists. This deadline-extension ZIP supersedes the original b713 archive; historical commit 4fd8f8d753578e59bacd779f580f15ce902dc146 preserves that earlier package. `SHA256SUMS.json` inside verifies 73 payload files; the archive contains 74 files including that manifest.

Nonsensitive pilot labels, public hostname and the 28 October 2026 05:00 UTC cutoff remain in executable code to preserve exact reproducibility. They are not credentials. The bridge is deliberately bounded and expires; do not broaden it for a new installation. Leave `JUDGE_TRIAL_PILOT_BRIDGE` unset and use separately reviewed isolated-judge provisioning for a new deployment. Operational hosting config, database/account identifiers, private access codes, grant hashes and authentication files are excluded.

## What has and has not been demonstrated

A historical real Nemotron-through-Nebius synthetic handoff produced a receiver preparation checklist, retained the listed resources and unknown outcomes, and was saved and reopened with its original reference. That useful result followed an explicitly approved additional receiver trial; it is not a first-attempt success-rate claim. The 150-second video is a replay of saved application work, not new live inference: https://youtu.be/7pmSm6-GUSA . Public visibility was reported by the operator on 27 October at approximately 09:26 UTC; this README does not independently establish current playback or visibility.

The later dated pilot deployment was recorded with **zero real pilot model calls** at the reviewed checkpoint. Historical real inference must not be attributed to that pilot as though it were a successful new run. Local tests, deployment and saved-result playback are different kinds of evidence.

General lossless compression, superiority over other models, cost savings, unrestricted autonomous execution and final judging readiness are not established. A finite, non-distributed two-call pilot ending at 28 October 2026 05:00 UTC is not the final judging-period access contract. Public source publication does not resolve that contract. Session-bound storage has limitations; elapsed retention does not prove physical deletion, and no production purge scheduler is claimed. Cost guards are estimates, not billing hard caps. Final judge access, continued availability and final submission remain separate work.

## Deadline-only update

Approved at 17:45:56 UTC on 27 October: extend existing owner and pilot deadlines only to 28 October 2026 05:00 UTC. Runtime changes are limited to one pilot-bridge date literal and its rebuilt worker. Existing owner100/estimatedUSD0.06 and pilot2/estimatedUSD0.02 remain unchanged; no new grant, key, dataset or model invocation is claimed. The operator reports deployment at17:51:36 UTC; source identity does not by itself verify remote policy values. This finite extension is not unrestricted final judging access.
