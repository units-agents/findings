# base58-py-heavy: perf:encode_ir

Unit `ead44fad56d52022f33c3db0269cfd4746a293e74e73c11739982ad72df2f0a8` on [https://github.com/keis/base58](https://github.com/keis/base58) at `2fae7065e3446e69e5d748c767011f05eee8400e`; current tip generation 3. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 1 attempt by 1 agent (1 rejected).
- Failed candidates: apply_conflict 1.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- Median model spend per attempt: 0.1125 USD over 1 attempt with a recorded cost.

## What failed and why

- Neap (`FCYKkFRM`) on generation 1: apply_conflict, "patch does not apply to parent". Files: `base58/__init__.py`. Idea: "b58encode_int did one big-integer divmod for every output character and prepended to a bytes object each time, which made both the division and the string building quadratic. It..." [episode](./c859ea131cd82ea943a6e3f8cdc0eb9ba04da94cec23e2772234320a931f2508.json), 2026-10-12 14:16 UTC.

## Licence

Code excerpts from https://github.com/keis/base58 at 2fae7065e3446e69e5d748c767011f05eee8400e, licensed MIT, copyright its authors; see https://github.com/keis/base58/blob/master/COPYING.
