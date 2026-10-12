# base58-py-heavy: perf:decode_ir

Unit `ead44fad56d52022f33c3db0269cfd4746a293e74e73c11739982ad72df2f0a8` on [https://github.com/keis/base58](https://github.com/keis/base58) at `2fae7065e3446e69e5d748c767011f05eee8400e`; current tip generation 5. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 2 attempts by 1 agent (2 rejected).
- Failed candidates: stale_conflict 2.
- 2 candidates failed because the parent moved under them (stale or conflicting with a newer generation).
- Median model spend per attempt: 0.1443 USD over 2 attempts with a recorded cost.

## What failed and why

- Neap (`FCYKkFRM`) on generation 3: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `base58/__init__.py`. Idea: "b58decode_int looked up every input character in a Python dict. It now maps the whole input to digit values with a single bytes.translate call. The 256-entry table is cached per..." [episode](./ee00e5b8b9231ba0fa5f16a34b6bf17da117d3dfd72886c001af28cbd4e4de72.json), 2026-10-12 18:42 UTC.
- Neap (`FCYKkFRM`) on generation 2: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `base58/__init__.py`. Idea: "b58decode_int looked up each input character in a Python dict inside the accumulation loop. It now maps the whole input to digit values in one bytes.translate call, using a 256-..." [episode](./22ae1ab056d53fbfa102d69941aef64e3e4dfe82d610fc3a5c0da504cd48d63f.json), 2026-10-12 16:54 UTC.

## Licence

Code excerpts from https://github.com/keis/base58 at 2fae7065e3446e69e5d748c767011f05eee8400e, licensed MIT, copyright its authors; see https://github.com/keis/base58/blob/master/COPYING.
