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

The supplied generated worker is included. This private candidate independently reproduces its exact hash using the existing pinned esbuild0.28.2 and passes10 focused synthetic bridge/postcommit/UI/replacement checks. The operator reports source197/197 and bundle21/21 at the applied checkpoint; this packaging task did not rerun those full suites. Tests are not real inference or a measurement of model quality.

## NVIDIA and Nebius

The prototype uses `nvidia/NVIDIA-Nemotron-3-Nano-30B-A3B` through Nebius Token Factory's server-side chat-completions API. Producer and receiver are separate requests to the configured model, not independent vendors. The frontend and database layer use Cloudflare Workers and D1. Provider keys belong only in server secret storage; none are included in this repository or sent to the browser.

See the extracted `README.md`, `.env.example`, `.env.judge-trial.example` and `JUDGE_TRIAL_DESIGN_HISTORY.md` for server bindings, disabled defaults and setup boundaries. These environment files are inventories, not automatic configuration. The runtime is a Cloudflare Worker, not a standalone Node HTTP server. Deployment requires separately provisioned databases, server settings and authorized credentials. The supplied test suite works offline without those operational resources. Do not reuse a historical policy label as permission to send requests.

## Source and deployment identity

Archive SHA-256:

```text
4921c70616b9f835bdd4630b67bb1f65b5ef13f884bec8f7c1a2d683749ba7b3
```

Bundled `nano-data-source/worker.mjs` SHA-256:

```text
8312a888670538ee5019752719259fb15f8abdc97d2bd0cc32aec1b02cbf5771
```

This matches the local runtime bundle in the recorded 28 October 2026 10:03:27 UTC pilot deployment, version `894a64e6-8834-4bcc-b8a5-be49d4704ef6`. This is a dated operator deployment record and reproducible source identity, not a fresh extraction from the host or a claim that no later deployment exists. This private postcommit-recovery candidate succeeds the d190 source at public commit a883475946e30b91a1719fa85becfd3820b35959; this task does not modify any public commit. Historical commit 4fd8f8d753578e59bacd779f580f15ce902dc146 preserves the original b713 package. `SHA256SUMS.json` inside verifies 76 payload files; the archive contains 77 files including that manifest.

Nonsensitive pilot labels, public hostname and the 28 October 2026 13:00 UTC cutoff remain in executable code to preserve exact reproducibility. They are not credentials. The bridge is deliberately bounded and expires; do not broaden it for a new installation. Leave `JUDGE_TRIAL_PILOT_BRIDGE` unset and use separately reviewed isolated-judge provisioning for a new deployment. Operational hosting config, database/account identifiers, private access codes, grant hashes and authentication files are excluded.

## What has and has not been demonstrated

A historical real Nemotron-through-Nebius synthetic handoff produced a receiver preparation checklist, retained the listed resources and unknown outcomes, and was saved and reopened with its original reference. That useful result followed an explicitly approved additional receiver trial; it is not a first-attempt success-rate claim. The 150-second video is a replay of saved application work, not new live inference: https://youtu.be/7pmSm6-GUSA . Public visibility was reported by the operator on 27 October at approximately 09:26 UTC; this README does not independently establish current playback or visibility.

The later dated pilot deployment was recorded with **zero real pilot model calls** at the reviewed checkpoint. Historical real inference must not be attributed to that pilot as though it were a successful new run. Local tests, deployment and saved-result playback are different kinds of evidence.

General lossless compression, superiority over other models, cost savings, unrestricted autonomous execution and final judging readiness are not established. A finite, non-distributed two-call pilot ending at 28 October 2026 13:00 UTC is not the final judging-period access contract. Public source publication does not resolve that contract. Session-bound storage has limitations; elapsed retention does not prove physical deletion, and no production purge scheduler is claimed. Cost guards are estimates, not billing hard caps. Final judge access, continued availability and final submission remain separate work.

## Postcommit login recovery — 28 October 2026

The operator recorded an explicitly approved postcommit login fix and one further replacement-login allowance. If usage or case-detail retrieval fails after a session is committed, the response retains that same session cookie and marks details pending; execution remains disabled until a GET refresh confirms details. The UI does not repeat login. This fixes the reproduced synthetic postcommit failure, not every possible production cause: transport loss, cookie refusal and uncertain commit state remain separate.

The cumulative max_sessions predicate is now3. The prior active session was revoked; sessions_issued2 and two revoked historical sessions were retained at the operator10:03 checkpoint. There was one remaining login issuance at that dated checkpoint, not three new sessions. No new grant/code, counter reset or extra inference allowance was created. Total model-call ceiling2 and estimated USD0.02 guard remain unchanged; the guard is not a billing cap. Pilot expiry remains13:00 UTC; owner expiry remains05:00 UTC and was not reactivated. The existing case-metadata capacity formula rises from4 to5; the authorized operational synthetic case remains one.

Operator receipt records deployment894a64e6-8834-4bcc-b8a5-be49d4704ef6 at10:03:27 UTC and zero runs at that checkpoint. Subsequent activity is not determined by this package. Operator-reported tests: source197/197 and bundle21/21; synthetic old-version postcommit regression1PASS2FAIL became3PASS. This packaging check independently rebuilds the worker and runs only focused synthetic tests. It does not rerun the full suites or call a real provider.

New regression tests and their synthetic fixture are included for offline reproducibility. Operational SQL, database snapshots, authentication state and private grants are not bundled. The portable replacement-login fixture uses a fixed synthetic clock rather than wall-clock time; it is not a production administration script.

This is a private publication candidate, not permission to publish, deploy, extend access, retry model calls or submit. Existing public commits are not modified. Finite pilot access remains distinct from final judging-period access.
