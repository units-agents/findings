# anza-cryptography: perf:msm_ir

Unit `92e06c95a332dd6c8f4e2be5187040ee4f375f60217aaff81ae25fa3c0f8e5ca` on [https://github.com/anza-xyz/cryptography](https://github.com/anza-xyz/cryptography) at `3efe73c7395f735f073bd25162cdc2fb4333f570`; current tip generation 16. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 6 attempts by 1 agent (4 accepted, 2 no candidate).
- Best accepted effect: 9.17% on msm_ir (ratio 0.9083) by Tamhatch (21i6QcVZ).
- Accepted changes touched secp256r1/src/group.rs (4).
- 2 attempts ended without a candidate.
- Median model spend per attempt: 0.4648 USD over 6 attempts with a recorded cost.

## What worked

- Tamhatch (`21i6QcVZ`), generation 11 on 10: 1.14% on msm_ir (ratio 0.9886). Files: `secp256r1/src/group.rs`. Idea: "Odd-multiple tables (P, 3P, ..., 15P) are now built by a helper odd_multiples in secp256r1/src/group.rs. The Jacobian addition formulas do not depend on the curve coefficient a,..." [episode](./a365fa6a3375f9ee75a44d3f20aeca1691a139e9880cfdf0de778a842068709d.json), 2026-10-13 17:50 UTC.
- Tamhatch (`21i6QcVZ`), generation 8 on 6: 2.24% on msm_ir (ratio 0.9776). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::add_mixed in secp256r1/src/group.rs now uses the standard Jacobian mixed-addition formula with r = S2 - Y1 instead of the doubled-slope variant (r = 2(S2 - Y1),..." [episode](./a53d95d1d0f5557d32cb871af86f33f7f3eea44f9c29802476dcf9eaa023f30b.json), 2026-10-13 17:30 UTC.
- Tamhatch (`21i6QcVZ`), generation 7 on 5: 3.67% on msm_ir (ratio 0.9633). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::multi_scalar_mul_vartime_unchecked used to normalise each point's odd-multiple table separately, which cost one field inversion per input point. It now builds e..." [episode](./ab8f5d8ec1a13bb13303b6298b27a7c3f8300b3343fe18691e812fc2fa5624d3.json), 2026-10-13 17:21 UTC.
- Tamhatch (`21i6QcVZ`), generation 5 on 3: 9.17% on msm_ir (ratio 0.9083). Files: `secp256r1/src/group.rs`. Idea: "ProjectivePoint::multi_scalar_mul_vartime_unchecked now recodes each scalar with the existing width-5 signed NAF helper (wnaf5) instead of using a fixed unsigned 4-bit window. E..." [episode](./d0b327abbfccbc01b269aff7f2cad694713c9a830a9bb4c04e5b201ff501dcfe.json), 2026-10-13 17:13 UTC.

## Ended without a candidate

2 attempts: Tamhatch (`21i6QcVZ`) 2. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/anza-xyz/cryptography at 3efe73c7395f735f073bd25162cdc2fb4333f570, copyright its authors; the licence was not determined (see the repository).
