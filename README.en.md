# amber-deepseek

Public periodic [AMBER](https://github.com/getaskclaw/amber) benchmark results of models on the official DeepSeek API (api.deepseek.com) — stable releases, preview builds, across reasoning-effort bands. **Cases stay private; results are public.** 中文说明：[README.md](README.md)

## What this is

- One `results/YYYY-Www.md` per issue: same cases, same harness, full library per model; same-family versions and providers side by side.
- Each issue pins: library size and hashes, per-case d2 score and pass/fail, terminal states, token usage (when the lane reports it) and latency, environment fingerprint, and a qualitative verdict written under evidence discipline.
- Cases, oracles, transcripts and intermediates are **never published**.
- Sister repos: [amber-gpt](https://github.com/getaskclaw/amber-gpt), [amber-crof](https://github.com/getaskclaw/amber-crof), [amber-ollama](https://github.com/getaskclaw/amber-ollama), [amber-devin](https://github.com/getaskclaw/amber-devin), [amber-opencode](https://github.com/getaskclaw/amber-opencode) (OpenCode Go lane), [amber-commandcode](https://github.com/getaskclaw/amber-commandcode) (CommandCode lane). Third-party-vendor scores for the same deepseek-v4 family live in those repos; **same-name cross-vendor duels** (official API / OpenCode Go / CommandCode — the same name may not be the same endpoint) live in the latter two. This repo's comparison axis is **cross-version on the official lane**, and every cross-repo citation carries an explicit date and band declaration.

## Publication red lines

1. Publish only: scores and aggregates, token usage (when reported), speed, qualitative verdicts.
2. Never publish: case content, oracles/graders, transcripts, candidate workspaces, anything that could reconstruct a case.
3. Every issue pins: model ID, effort band, date (UTC), harness version, per-case bundle hash — verifiable against the public hash index in [amber](https://github.com/getaskclaw/amber).
4. Case numbering is private: public matrices use stable aliases (A-xxxxxxxx, hash-derived) plus bundle hashes only.
5. Tone: community measurement, not vendor attacks.

## A methodological premise

Same model name, same provider, two runs can still score differently — inference parameters, load, and server-side versions drift. Preview/experimental models also carry lifecycle risk (they can vanish overnight). Every conclusion here is dated and banded, and we re-test periodically. A single day's number is a snapshot, not a law.

## Results index

| Issue | Content | Headline |
|---|---|---|
| [2026-W37](results/2026-W37.md) | deepseek-v4.1-flash-expires-on-0910 (preview) full-library debut (23 cases) | 14/23 (12/21 public subset); zero invalid scored papers; ~1/30 the input tokens of its 0731 sibling on third-party lanes; strong build/ops, clear regressions on adversarial review and delivery form; vision case first mis-judged capability-skip, retaken after a raw-API probe and scored a fail (see Errata); 2026-09-10 addendum: preview retired on schedule, GA `deepseek-flash` identity verification green on a 3-case signature; **Addendum 2 (same day): GA full-library debut 16/23 (14/21 public subset)** — blank-paper disease and clean-review regression both fixed, same band as [amber-opencode](https://github.com/getaskclaw/amber-opencode) (16/23) / [amber-commandcode](https://github.com/getaskclaw/amber-commandcode) (17/23), deferred-exam list closed |

## Disclaimer

Not affiliated with or sponsored by DeepSeek. Scores are dated, band-specific snapshots, not purchasing advice.
