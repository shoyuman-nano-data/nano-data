# NANO DATA

**Keep the source. Carry the purpose. Continue the work.**

A source-linked AI handoff prototype: keep the original, purpose, reason and next action; produce a compact CORE; explicitly request a receiver continuation; inspect saved results and references. Producer and receiver are separate requests to the same configured NVIDIA Nemotron model through Nebius Token Factory, not independent vendors.

## Current source and deployment boundary

This package matches the source bundle uploaded in the recorded 2026-10-28 15:47:57 UTC code-only deployment, version `175f72d3-802b-4172-ae74-ea228f778815`:

`2d05d6b09de7786877f09a302b216974aa02bc323b87c948e44938ba1de58853`

This is the local no-bundle upload identity from the operator receipt, not a newly extracted remote source hash. It supersedes public commit f3115ee9d1c8485b29e566cd12c2673b1b6c6ffd's worker8312 source. Runtime code, static assets, tests and migrations are included. No operational hosting configuration, databases, private grants or credentials are included.

**Final judging remains disabled.** At the recorded checkpoint the dedicated provider connection was not configured, final runtime/cost-policy settings were absent, and the expired pilot bridge remained. Code/schema deployment is not usable final access, a successful new AI journey, or submission. This package does not enable anything. Historical pilot dates and non-secret labels in executable code are retained for exact reproducibility, not permission to execute requests.

## Build and offline checks

### Verify the supplied source and bundle without installing packages

Use Node.js 24 or later and a POSIX shell (Linux/macOS). From the extracted `nano-data-source/` directory, run the four commands below. These checks use the supplied files and Node's built-in test runner; they do not require `npm ci`, an API key, an account, a database connection, or a running hosted app. Do not open a live app to run these checks.

```sh
# Source suite: expected 234 passing tests for this exact package.
node --import ./evidence/no-network.mjs --test evidence/*.test.mjs

# Supplied seed bundle: expected 37 passing tests.
SEED_APP_MODULE=../worker.mjs node --import ./evidence/no-network.mjs --test evidence/seed-chain.test.mjs

# Supplied judge bundle: expected 21 passing tests.
JUDGE_UI_APP_MODULE=../worker.mjs JUDGE_APP_MODULE=../worker.mjs JUDGE_ADVERSARIAL_MODULE=../worker.mjs JUDGE_FAULT_MODULE=../worker.mjs node --import ./evidence/no-network.mjs --test evidence/judge-trial.test.mjs evidence/judge-isolation-adversarial.test.mjs evidence/judge-bundle-fault.test.mjs evidence/judge-ui-handler.test.mjs

# Supplied final-mode bundle: expected 17 passing tests.
JUDGE_FINAL_APP_MODULE=../worker.mjs node --import ./evidence/no-network.mjs --test evidence/judge-final-route.test.mjs
```

Each command must exit with code 0 and report zero failed tests. The `no-network.mjs` preload rejects global `fetch`; provider transports and database fixtures in these tests are synthetic. Passing tests do not establish live provider connectivity, final judging availability, semantic accuracy or a real-user journey. These counts apply to the exact 2d05 package, not later UI or budget candidates.

On 29 October 2026, these commands were verified with Node.js 24.22.1 from a fresh extraction of this archive, without `node_modules` or package installation. This is an offline reproducibility check, not a deployment or fresh inference.

The `replacement-login.test.mjs` from the private candidate is intentionally excluded: it depends on an operational SQL file outside the source tree and wall-clock-sensitive history. No operational fixture was imported or fabricated. Therefore these commands validate the included suite, not every historical test.

To rebuild, `npm ci` installs lockfile-pinned esbuild0.28.2 and runs its install script (requires network on a fresh machine); then `npm run build`. The supplied worker runs on Cloudflare Workers, not a standalone Node HTTP server. MIT license and third-party notices are included. SHA256SUMS.json covers every archive payload except itself.

## Runtime setup and safe defaults

See JUDGE_TRIAL_SETUP.md and release/ for design/history. Historical documents, including README_BASELINE_HISTORY.md and BASE_PROVENANCE.json, are dated background, not current deployment state or authorization. This README and SOURCE_RELEASE.json define this package identity.

Provision owner and isolated judge databases separately. Do not blindly rerun migrations against existing databases. Migration0006 uses a local helper and is not a standalone production D1 script. The 0007 costguard schema was already applied to the live isolated judge database according to the deployment receipt; its PROPOSED filename is retained to preserve source identity, not an instruction to apply it again. Owner database was not changed. Deployments need separately authorized server settings and credentials; keys must never enter browser or source. Disabled JSON files are human-readable inventories, not ready-to-deploy configurations.

## Costguard and limitations

The final-mode path adds atomic lifetime monetary reservations immediately before model send, shared across sessions/grants, with no reservation refunds, resets or automatic retry after unknown outcomes. It validates model/price/context metadata and fails closed; legacy/final mixed configurations are rejected. These application reservations are **not an invoice hard cap**, proof of eligible free credits, or a guarantee against card charges. No unlimited judging availability, organizer exception, production concurrency benchmark or physical purge scheduler is claimed.

Receiver resource bounds do not prove semantic quality or absence of truncation. General lossless compression, superiority over other models and cost savings have not been established. A historical real synthetic Nemotron/Nebius handoff and saved-result playback exist separately; they must not be described as a successful final-judging journey. The video https://youtu.be/7pmSm6-GUSA is saved-work replay, not fresh live inference. Current playback was not checked by this packaging task.

## Testing the hosted app

The recorded app entry is https://nano-data-judge-test-20261025.shoyuman-official.workers.dev/judge . The URL alone does not establish usable access. Final private access provisioning and one authorized fictional-data producer → explicit receiver → save/reload journey remain separate prerequisites. Do not use historical pilot credentials, extend access, retry uncertain model calls, or assume this package grants spending authority. Final availability and formal submission remain incomplete at the recorded checkpoint.

## Source archive

Download and extract NANO_DATA_MATCHING_PILOT_SOURCE_20261027.zip (the established repository filename is retained). The code browser displays the archive rather than an expanded tree. Verify it with `sha256sum --check SOURCE_ARCHIVE_SHA256.txt`.

## This package verification

Packaging verification: included source tests234/234; existing bundle37/37; judge bundle21/21; final-mode bundle17/17 passed with global fetch blocked and synthetic transports. The pilot regression uses an explicit synthetic clock so the historical expiry does not invalidate its fixture; runtime code and cutoff are unchanged. Rebuild reproduced the exact worker SHA above. These are local checks, not real model calls or browser acceptance tests.
