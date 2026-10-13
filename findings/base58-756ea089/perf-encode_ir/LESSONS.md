# base58: perf:encode_ir

Unit `756ea08911a14f3b3d3fcfb7485b82e9c5029ca46945cf9eb4eb50d92e12da2c` on [https://github.com/units-agents/base58](https://github.com/units-agents/base58) at `2fae7065e3446e69e5d748c767011f05eee8400e`; current tip generation 17. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 12 attempts by 1 agent (5 accepted, 2 rejected, 5 no candidate).
- Best accepted effect: 34.32% on encode_ir (ratio 0.6568) by agent (4DFFzSS4).
- Accepted changes touched base58/__init__.py (5).
- Failed candidates: apply_conflict 1, stale_conflict 1.
- 2 candidates failed because the parent moved under them (stale or conflicting with a newer generation).
- 5 attempts ended without a candidate.
- Median model spend per attempt: 0.2801 USD over 12 attempts with a recorded cost.

## What worked

- agent (`4DFFzSS4`), generation 16 on 15: 1.00% on encode_ir (ratio 0.9900). Files: `base58/__init__.py`. Idea: "b58encode now has a per-alphabet fast path (pair table, base, base^2, base^4, base^8). It peels 8 base58 digits per loop iteration using two divmods by base^4, which keeps the d..." [episode](./3517cef42d51d8209665cbffb714f8ecd06ad84709ee634e0252381bd345f063.json), 2026-10-13 17:59 UTC.
- agent (`4DFFzSS4`), generation 11 on 8: 1.13% on encode_ir (ratio 0.9887). Files: `base58/__init__.py`. Idea: "The inlined pair-table encoding loops in b58encode and b58encode_check now call parts.append(...) directly instead of a cached bound method. That lets the interpreter use its sp..." [episode](./97bbbf145cd7ce8f6f7d75ecf4b2dd73fd3590a555293caae85fc4062d86335a.json), 2026-10-13 17:02 UTC.
- agent (`4DFFzSS4`), generation 10 on 8: 1.93% on encode_ir (ratio 0.9807). Files: `base58/__init__.py`. Idea: "b58encode now runs the pair-table encoding loop itself for bytes alphabets. It uses the per-alphabet cached tuple (_ENC_INFO: pair table, base, base^2, base^4) that b58encode_ch..." [episode](./483be72b80f421e0e46a5091f79cf31a9949cfbedeaeff4d604f4829816ffda4.json), 2026-10-13 17:00 UTC.
- agent (`4DFFzSS4`), generation 3 on 1: 5.79% on encode_ir (ratio 0.9421). Files: `base58/__init__.py`. Idea: "b58encode_int: each base**4 remainder is now split with % and // instead of a divmod call, which avoids building and unpacking a tuple. The top digits (fewer than four) are emit..." [episode](./8124b86a574719d78969a4156ba76d45b3d3041a0dc76ea8e67711d3a731bdce.json), 2026-10-13 16:12 UTC.
- agent (`4DFFzSS4`), generation 2 on 0: 34.32% on encode_ir (ratio 0.6568). Files: `base58/__init__.py`. Idea: "b58encode_int did one bigint divmod per output character and prepended to a bytes string (quadratic). It now divides by base**4 (fits a single 30-bit digit for base58), splits e..." [episode](./b5cc7b2983d01ed76eb3d7b72d5ec903cc92e61fa5f4491fa1d07b40ac65b5a2.json), 2026-10-13 16:01 UTC.

## What failed and why

- agent (`4DFFzSS4`) on generation 6: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `base58/__init__.py`. Idea: "b58encode now runs the pair-table encoding loop itself for bytes alphabets, using a per-alphabet cached tuple (pair table, base, base^2, base^4, zero char). This removes the b58..." [episode](./0075ad7d8289bea4cbefba698b3eab2465026b534c7f01b1f85760d2e0a26922.json), 2026-10-13 16:51 UTC.
- agent (`4DFFzSS4`) on generation 2: apply_conflict, "patch does not apply to parent". Files: `base58/__init__.py`. Idea: "b58encode now runs its own inlined fast path for bytes alphabets. A per-alphabet tuple (pair table, base^2, base^4, zero char, base) is cached in a plain dict, so there is no lr..." [episode](./300d9c29fbd0aa7432491251b4a40d845748cbf5891f75180e6289dbeeca714d.json), 2026-10-13 16:21 UTC.

## Ended without a candidate

5 attempts: agent (`4DFFzSS4`) 5. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/units-agents/base58 at 2fae7065e3446e69e5d748c767011f05eee8400e, copyright its authors; the licence was not determined (see the repository).
