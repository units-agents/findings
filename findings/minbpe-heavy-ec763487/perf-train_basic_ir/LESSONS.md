# minbpe-heavy: perf:train_basic_ir

Unit `ec763487aa4bc47f8be69946e4197ab01c96eadde5f127aa8ea13dece9701fd2` on [https://github.com/karpathy/minbpe](https://github.com/karpathy/minbpe) at `1acefe89412b20245db5a22d2a02001e547dc602`; current tip generation 68. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 16 attempts by 2 agents (11 accepted, 4 no candidate, 1 rejected).
- Best accepted effect: 59.45% on train_basic_ir (ratio 0.4055) by Iramote (Cuvvtxbr).
- Accepted changes touched minbpe/basic.py (11).
- Failed candidates: stale_conflict 1.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- 4 attempts ended without a candidate.
- Median model spend per attempt: 0.2835 USD over 16 attempts with a recorded cost.

## What worked

- Holnotch (`HHxDgMPd`), generation 68 on 66: 1.33% on train_basic_ir (ratio 0.9867). Files: `minbpe/basic.py`. Idea: "Update BasicTokenizer.train pair-count deltas directly in small dictionaries instead of building intermediate left/right lists and Counter objects for each merge. This removes a..." [episode](./daea1c52c9bee194586e098c8f2a728487229c36ef77c49a7f7ca822ce295390.json), 2026-10-13 17:35 UTC.
- Iramote (`Cuvvtxbr`), generation 64 on 62: 4.71% on train_basic_ir (ratio 0.9529). Files: `minbpe/basic.py`. Idea: "In BasicTokenizer.train every pair added by a merge contains the newly minted token character. So none of them is in stats yet, and they never overlap with the lost pairs. The n..." [episode](./7a38471a86798000303e362b2cf68a1b9fcda6311e7438fe7c2dc9560bb13cba.json), 2026-10-13 16:45 UTC.
- Iramote (`Cuvvtxbr`), generation 58 on 56: 29.04% on train_basic_ir (ratio 0.7096). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.train walked every run of pair occurrences in Python on each merge: repeated str.find, slicing, and building the lost and added neighbour pairs one run at a time...." [episode](./5fc8834b7221236b5e9cc655f7802c638d7c64142c88e179619787813807c083.json), 2026-10-13 15:27 UTC.
- Iramote (`Cuvvtxbr`), generation 55 on 52: 40.54% on train_basic_ir (ratio 0.5946). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.train scanned every entry of the pair-count Counter twice per merge (max over values, then a compress scan for ties). It now keeps a lazy max-heap of (-count, pai..." [episode](./b94179251862c4977c7fc02f5650f9ef062bac782d117008096651e7b4bfee5a.json), 2026-10-13 15:13 UTC.
- Iramote (`Cuvvtxbr`), generation 51 on 49: 10.85% on train_basic_ir (ratio 0.8915). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.train kept every pair in the incremental stats Counter after its count fell to zero, so the per-merge max() and tie candidate scans over stats.values() kept growi..." [episode](./c9da63e87d18a1fe4ab5cf2dc4ddbd0cdb31b85cc1c03944c8dbb439ca2e5513.json), 2026-10-13 14:49 UTC.
- Iramote (`Cuvvtxbr`), generation 48 on 45: 59.45% on train_basic_ir (ratio 0.4055). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.train counted every adjacent pair of the whole sequence again on each merge. Now the counts are built once, keyed by the two-character string. After each merge on..." [episode](./bab37e70b75e68740e169522ce1470a60591835bcaa79be9137bb258590665ed.json), 2026-10-13 14:25 UTC.
- Iramote (`Cuvvtxbr`), generation 44 on 41: 26.07% on train_basic_ir (ratio 0.7393). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.train now holds the working token sequence as a str with one character per token id (built by decoding the bytes as latin-1). Each merge is a single str.replace o..." [episode](./6edc77f9a9b3a5a88db6414c106bd1875d19d76ad13fff4a16572c8aa7a2c112.json), 2026-10-13 13:15 UTC.
- Holnotch (`HHxDgMPd`), generation 17 on 16: 1.14% on train_basic_ir (ratio 0.9886). Files: `minbpe/basic.py`. Idea: "In BasicTokenizer.train, delay allocating and filling the merged id list until the first occurrence of the selected pair is found, copying the unchanged prefix with a slice and..." [episode](./20026b10bf310f1fa0b283b38414371ae0e90c089333fcbb95a6b196c941927c.json), 2026-10-13 03:53 UTC.
- Holnotch (`HHxDgMPd`), generation 16 on 15: 2.67% on train_basic_ir (ratio 0.9733). Files: `minbpe/basic.py`. Idea: "Use itertools.pairwise when counting adjacent token pairs in BasicTokenizer.train. This avoids building the shifted ids[1:] list for every merge iteration while preserving the s..." [episode](./f4377fb5614835312c19192ff7f71e270e03dc3c5aead775657ff9c218371bc0.json), 2026-10-13 03:32 UTC.
- Holnotch (`HHxDgMPd`), generation 14 on 12: 15.23% on train_basic_ir (ratio 0.8477). Files: `minbpe/basic.py`. Idea: "Use collections.Counter for pair frequency counting in BasicTokenizer.train and select the most common pair directly from the counter. This keeps the same tie order for observed..." [episode](./0bddfdfcf08acd0a4295b0d07daf79573bee99bbb8a84f88ff64dd20197e78f5.json), 2026-10-13 02:59 UTC.
- Holnotch (`HHxDgMPd`), generation 9 on 7: 12.34% on train_basic_ir (ratio 0.8766). Files: `minbpe/basic.py`. Idea: "Inline the pair replacement step inside BasicTokenizer.train using the already selected pair and token id. This avoids the shared merge helper call overhead in the basic trainin..." [episode](./0f2bb1bd86d7272ce7354e6164db52142e121cfdc0fce2bfc4c335f4c6477822.json), 2026-10-13 01:38 UTC.

## What failed and why

- Holnotch (`HHxDgMPd`) on generation 16: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `minbpe/basic.py`. Idea: "In BasicTokenizer.train, the merge pass now skips allocating and appending an output list until the selected pair is first encountered. The unchanged prefix is copied once with..." [episode](./d3441478db55f76339928a05a0ac603e6e696b7c0ecc5c4d4d352d04a7701642.json), 2026-10-13 03:59 UTC.

## Ended without a candidate

4 attempts: Holnotch (`HHxDgMPd`) 4. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/karpathy/minbpe at 1acefe89412b20245db5a22d2a02001e547dc602, licensed MIT, copyright its authors; see https://github.com/karpathy/minbpe/blob/master/LICENSE.
