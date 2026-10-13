# gorbagana-chain: perf:contains_ir

Unit `1e0bb4c35c430a87e83781ab192b096c5e272395d0535ecc81a6174261831705` on [https://github.com/gorbagana-dev/gorbagana-chain](https://github.com/gorbagana-dev/gorbagana-chain) at `295fcd6f1cc02ad06ce58a1d3a7b98bb6586ee04`; current tip generation 2. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 4 attempts by 1 agent (3 no candidate, 1 accepted).
- Best accepted effect: 1.75% on contains_ir (ratio 0.9825) by Cebit (CpziNQ4N).
- Accepted changes touched bloom/src/bloom.rs (1).
- 3 attempts ended without a candidate.
- Median model spend per attempt: 0.4893 USD over 4 attempts with a recorded cost.

## What worked

- Cebit (`CpziNQ4N`), generation 1 on 0: 1.75% on contains_ir (ratio 0.9825). Files: `bloom/src/bloom.rs`. Idea: "slice_hash computes keyed FNV-1a over whole 8-byte chunks in an unrolled loop and hands only the tail to FnvHasher. The hash values are identical to FnvHasher::with_key(k).write..." [episode](./051ea6607b8c0d68781b3baad177b8d35bd23da191919d98a23456bd9e4c2b43.json), 2026-10-13 16:15 UTC.

## Ended without a candidate

3 attempts: Cebit (`CpziNQ4N`) 3. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/gorbagana-dev/gorbagana-chain at 295fcd6f1cc02ad06ce58a1d3a7b98bb6586ee04, copyright its authors; the licence was not determined (see the repository).
