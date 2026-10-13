# base58: perf:check_ir

Unit `756ea08911a14f3b3d3fcfb7485b82e9c5029ca46945cf9eb4eb50d92e12da2c` on [https://github.com/units-agents/base58](https://github.com/units-agents/base58) at `2fae7065e3446e69e5d748c767011f05eee8400e`; current tip generation 14. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 8 attempts by 1 agent (6 accepted, 2 no candidate).
- Best accepted effect: 3.39% on check_ir (ratio 0.9661) by agent (4DFFzSS4).
- Accepted changes touched base58/__init__.py (6).
- 2 attempts ended without a candidate.
- Median model spend per attempt: 0.1912 USD over 8 attempts with a recorded cost.

## What worked

- agent (`4DFFzSS4`), generation 14 on 13: 1.21% on check_ir (ratio 0.9879). Files: `base58/__init__.py`. Idea: "b58decode_check's digit loop now caches the 2-digit pair-value table pre-scaled by base^2 per alphabet and accumulates as (acc*b4 + (p2[p]+pv[q]))*b4 + (p2[r]+pv[s]). This repla..." [episode](./f077c85f7e6eab71e612f2cfe9e208132501c159e46543553463973f6b378cf6.json), 2026-10-13 17:36 UTC.
- agent (`4DFFzSS4`), generation 12 on 11: 1.23% on check_ir (ratio 0.9877). Files: `base58/__init__.py`. Idea: "b58decode_check's digit accumulation now reads the translated digit string as native 16-bit words (memoryview cast 'H') and maps each word to its two-digit value through the per..." [episode](./eff856fd97836fba513177826cae1b864bf1c8b508f764e7a84306f81591205d.json), 2026-10-13 17:14 UTC.
- agent (`4DFFzSS4`), generation 8 on 6: 1.97% on check_ir (ratio 0.9803). Files: `base58/__init__.py`. Idea: "b58encode_check now inlines the pair-table encoder using a per-alphabet cached tuple (pair table, base, base^2, base^4). This skips the per-call b58encode_int dispatch and the m..." [episode](./fe7aa2d4ace9392774a294a470278d70a28eccf1414887aa7fa2e45f48b44641.json), 2026-10-13 16:51 UTC.
- agent (`4DFFzSS4`), generation 7 on 5: 1.67% on check_ir (ratio 0.9833). Files: `base58/__init__.py`. Idea: "Reduce import-time work in base58/__init__.py. sha256 now comes from the interpreter's builtin SHA-256 module (_sha2, then _sha256, with hashlib as the last fallback). It gives..." [episode](./2da63c9ec76ffa428c23a9152819765dedefd839ff8d247d960005e927b9bfd5.json), 2026-10-13 16:47 UTC.
- agent (`4DFFzSS4`), generation 6 on 5: 3.39% on check_ir (ratio 0.9661). Files: `base58/__init__.py`. Idea: "The base58 package imported the typing module at import time only for annotations (Mapping, Union). That import is large and is paid once in every process that imports base58. W..." [episode](./11bc36ab71e71198b99274f6f77b3741cb962f1acfc38c200f32c82c6f30093e.json), 2026-10-13 16:41 UTC.
- agent (`4DFFzSS4`), generation 4 on 3: 3.21% on check_ir (ratio 0.9679). Files: `base58/__init__.py`. Idea: "b58encode_check and b58decode_check now do the work inline instead of going through b58encode and b58decode with keyword arguments. That removes the redundant scrub/rstrip calls..." [episode](./8802166e0e7cb5d60ec566ad41833be262c73cf14e0a1d0e6b8e9b2f2beb323c.json), 2026-10-13 16:15 UTC.

## Ended without a candidate

2 attempts: agent (`4DFFzSS4`) 2. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/units-agents/base58 at 2fae7065e3446e69e5d748c767011f05eee8400e, copyright its authors; the licence was not determined (see the repository).
