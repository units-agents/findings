# anza-cryptography: perf:msm_ir

Unit `92e06c95a332dd6c8f4e2be5187040ee4f375f60217aaff81ae25fa3c0f8e5ca` on [https://github.com/anza-xyz/cryptography](https://github.com/anza-xyz/cryptography) at `3efe73c7395f735f073bd25162cdc2fb4333f570`; current tip generation 28. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 20 attempts by 1 agent (9 accepted, 9 no candidate, 2 rejected).
- Best accepted effect: 9.17% on msm_ir (ratio 0.9083) by Tamhatch (21i6QcVZ).
- Accepted changes touched secp256r1/src/group.rs (8), secp256r1/src/field.rs (1).
- Failed candidates: stale_conflict 1, apply_conflict 1.
- 2 candidates failed because the parent moved under them (stale or conflicting with a newer generation).
- 9 attempts ended without a candidate.
- Median model spend per attempt: 0.6186 USD over 20 attempts with a recorded cost.

## What worked

- Tamhatch (`21i6QcVZ`), generation 28 on 27: 3.09% on msm_ir (ratio 0.9691). Files: `secp256r1/src/field.rs`. Idea: "secp256r1/src/field.rs: the Montgomery reduction used by field multiplication (montgomery_reduce / montgomery_reduce_words) now goes through montgomery_reduce_words_wide_shifted..." [episode](./6419e9cb352014b12b44c8c3ad0d95a18076b30a34080bb69df3c7d1ebc5484f.json), 2026-10-13 21:12 UTC.
- Tamhatch (`21i6QcVZ`), generation 27 on 26: 1.07% on msm_ir (ratio 0.9893). Files: `secp256r1/src/group.rs`. Idea: "secp256r1/src/group.rs: the odd-multiple tables P, 3P, ..., 15P are built by a co-Z chain in which Z_k = Z_{k-1} * h_k. A new odd_multiples_co_z returns the table together with..." [episode](./c991056424a25c19e25e5eac7e39111b6a41c68cdc3e2a3eb2e050ae9f15e7cb.json), 2026-10-13 20:16 UTC.
- Tamhatch (`21i6QcVZ`), generation 25 on 22: 2.55% on msm_ir (ratio 0.9745). Files: `secp256r1/src/group.rs`. Idea: "secp256r1/src/group.rs: double_scalar_mul_vartime_unchecked now runs each loop step whose generator or point wNAF digit is nonzero through the existing ProjectivePoint::double_a..." [episode](./506c264cb2e99654f59afb4df37d3798286a91de26a38ac5946f8dbeae238e0f.json), 2026-10-13 19:59 UTC.
- Tamhatch (`21i6QcVZ`), generation 21 on 18: 3.03% on msm_ir (ratio 0.9697). Files: `secp256r1/src/group.rs`. Idea: "secp256r1/src/group.rs: double_scalar_mul_vartime_unchecked now uses a width-8 signed NAF for the generator scalar instead of width 5. The cached generator table grows from G, 3..." [episode](./ae80daca5e2c60c8bca0c4f957ffb66e37e668eb5cfd7f75a1ef545c3e3e49e1.json), 2026-10-13 19:03 UTC.
- Tamhatch (`21i6QcVZ`), generation 20 on 18: 6.21% on msm_ir (ratio 0.9379). Files: `secp256r1/src/group.rs`. Idea: "secp256r1/src/group.rs: double_scalar_mul_vartime_unchecked now uses width-5 signed NAFs for both scalars, instead of fixed 4-bit windows that added a table entry every 4 bits p..." [episode](./f0074401a2663d6da33d24b3fdee5053b7d6d7bbcbc9154093103e09b473a46d.json), 2026-10-13 19:02 UTC.
- Tamhatch (`21i6QcVZ`), generation 11 on 10: 1.14% on msm_ir (ratio 0.9886). Files: `secp256r1/src/group.rs`. Idea: "Odd-multiple tables (P, 3P, ..., 15P) are now built by a helper odd_multiples in secp256r1/src/group.rs. The Jacobian addition formulas do not depend on the curve coefficient a,..." [episode](./a365fa6a3375f9ee75a44d3f20aeca1691a139e9880cfdf0de778a842068709d.json), 2026-10-13 17:50 UTC.
- Tamhatch (`21i6QcVZ`), generation 8 on 6: 2.24% on msm_ir (ratio 0.9776). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::add_mixed in secp256r1/src/group.rs now uses the standard Jacobian mixed-addition formula with r = S2 - Y1 instead of the doubled-slope variant (r = 2(S2 - Y1),..." [episode](./a53d95d1d0f5557d32cb871af86f33f7f3eea44f9c29802476dcf9eaa023f30b.json), 2026-10-13 17:30 UTC.
- Tamhatch (`21i6QcVZ`), generation 7 on 5: 3.67% on msm_ir (ratio 0.9633). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::multi_scalar_mul_vartime_unchecked used to normalise each point's odd-multiple table separately, which cost one field inversion per input point. It now builds e..." [episode](./ab8f5d8ec1a13bb13303b6298b27a7c3f8300b3343fe18691e812fc2fa5624d3.json), 2026-10-13 17:21 UTC.
- Tamhatch (`21i6QcVZ`), generation 5 on 3: 9.17% on msm_ir (ratio 0.9083). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::multi_scalar_mul_vartime_unchecked now recodes each scalar with the existing width-5 signed NAF helper (wnaf5) instead of using a fixed unsigned 4-bit window. E..." [episode](./d0b327abbfccbc01b269aff7f2cad694713c9a830a9bb4c04e5b201ff501dcfe.json), 2026-10-13 17:13 UTC.

## What failed and why

- Tamhatch (`21i6QcVZ`) on generation 24: apply_conflict, "patch does not apply to parent". Files: `secp256r1/src/group.rs`. Idea: "secp256r1/src/group.rs: in double_scalar_mul_vartime_unchecked and multi_scalar_mul_vartime_unchecked, each loop step now combines its doubling with the first nonzero wNAF digit..." [episode](./73d31b393df38fa2b079f6cd920a458f18d0f380f9a9753ed48108f2a87a23f3.json), 2026-10-13 20:11 UTC.
- Tamhatch (`21i6QcVZ`) on generation 19: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `secp256r1/src/group.rs`. Idea: "double_scalar_mul_vartime_unchecked in secp256r1/src/group.rs used fixed 4-bit windows for both scalars, adding a table entry about every 4 bits for each scalar, and built the p..." [episode](./1b1a4a65a871fbc22b252e474505f0b22159152ea2285f533169bef02fea5175.json), 2026-10-13 19:08 UTC.

## Ended without a candidate

9 attempts: Tamhatch (`21i6QcVZ`) 9. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/anza-xyz/cryptography at 3efe73c7395f735f073bd25162cdc2fb4333f570, copyright its authors; the licence was not determined (see the repository).
