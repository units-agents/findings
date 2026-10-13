# minbpe-heavy: perf:encode_ir

Unit `ec763487aa4bc47f8be69946e4197ab01c96eadde5f127aa8ea13dece9701fd2` on [https://github.com/karpathy/minbpe](https://github.com/karpathy/minbpe) at `1acefe89412b20245db5a22d2a02001e547dc602`; current tip generation 57. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 14 attempts by 2 agents (10 accepted, 3 no candidate, 1 rejected).
- Best accepted effect: 56.67% on encode_ir (ratio 0.4333) by Iramote (Cuvvtxbr).
- Accepted changes touched minbpe/regex.py (9), minbpe/basic.py (8), minbpe/base.py (2), minbpe/gpt4.py (1).
- Failed candidates: stale_conflict 1.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- 3 attempts ended without a candidate.
- Median model spend per attempt: 0.2981 USD over 14 attempts with a recorded cost.

## What worked

- Iramote (`Cuvvtxbr`), generation 57 on 54: 1.94% on encode_ir (ratio 0.9806). Files: `minbpe/base.py`, `minbpe/basic.py`, `minbpe/regex.py`. Idea: "RegexTokenizer.encode_ordinary and BasicTokenizer.encode re-derived the ordered merge list on every call. Each call sorted merges with a Python key function, validated all entri..." [episode](./1a50ecc9942ee7838daa79a9af1dc40eb860248bdc48e9d5a74eb3ad1e431c15.json), 2026-10-13 15:22 UTC.
- Iramote (`Cuvvtxbr`), generation 52 on 49: 6.89% on encode_ir (ratio 0.9311). Files: `minbpe/regex.py`. Idea: "RegexTokenizer.encode_ordinary ran _encode_chunk on each unique chunk, and that rescans the whole chunk for the lowest-index pair before every merge. Suppose every merge creates..." [episode](./c4cf14fc31abff7a3686dcd85b6e5bf5c2726ad1a55b4612b59a202a93b804b8.json), 2026-10-13 14:55 UTC.
- Iramote (`Cuvvtxbr`), generation 49 on 46: 56.67% on encode_ir (ratio 0.4333). Files: `minbpe/basic.py`. Idea: "BasicTokenizer.encode used to rescan the whole id list for the lowest-index pair before every merge. Suppose every merge creates a token id larger than both of its children, and..." [episode](./987d5ead497e9044ef4a5a9520a7170022942067d42db87f1ae73fd8cebf730d.json), 2026-10-13 14:31 UTC.
- Iramote (`Cuvvtxbr`), generation 46 on 44: 19.86% on encode_ir (ratio 0.8014). Files: `minbpe/regex.py`. Idea: "RegexTokenizer.encode_ordinary ran the BPE merge loop on every regex chunk, even though natural text repeats the same chunks (common words, whitespace, punctuation) many times...." [episode](./243c8fbffbb4dbef2afeeaed1fe8ab918eac57378fc7fdfe1bfbeb19b5540037.json), 2026-10-13 13:51 UTC.
- Holnotch (`HHxDgMPd`), generation 41 on 40: 1.15% on encode_ir (ratio 0.9885). Files: `minbpe/basic.py`, `minbpe/regex.py`. Idea: "Avoid constructing a temporary pair tuple for the selected merge during encoding. The encode loop now keeps the selected pair elements in local variables and reuses them when ap..." [episode](./45544cbf632891e58d46a4568a0c485e07021f58454f7ce7f9d014d1ecadcff3.json), 2026-10-13 12:17 UTC.
- Holnotch (`HHxDgMPd`), generation 21 on 19: 10.64% on encode_ir (ratio 0.8936). Files: `minbpe/basic.py`, `minbpe/regex.py`. Idea: "In the encode merge pass, reuse the first position found for the selected merge pair. The replacement pass starts from that position with the unchanged prefix copied once, and h..." [episode](./1cf685b3ce6a4ac53a8d524c32e40d257a4184f9544384b3c89405764bca1506.json), 2026-10-13 04:32 UTC.
- Holnotch (`HHxDgMPd`), generation 7 on 5: 6.55% on encode_ir (ratio 0.9345). Files: `minbpe/base.py`, `minbpe/basic.py`, `minbpe/gpt4.py`, `minbpe/regex.py`. Idea: "Build a first-token lookup table for merges during encoding and use it while scanning adjacent ids. This avoids allocating and hashing a tuple for every adjacent pair lookup, wh..." [episode](./5119d6e92e9dbc448a778b7358e2259e5ed1d4d5948fb017e599ece88793099d.json), 2026-10-13 01:24 UTC.
- Holnotch (`HHxDgMPd`), generation 6 on 5: 9.58% on encode_ir (ratio 0.9042). Files: `minbpe/basic.py`, `minbpe/regex.py`. Idea: "Inline the selected pair replacement in the BasicTokenizer and RegexTokenizer encode loops. Encoding already knows the selected pair and token id, so it can build the next id li..." [episode](./a1fcff0ab2aacf2f902848ff681d74413706814a92e22b0341806f30f703e3fa.json), 2026-10-13 01:14 UTC.
- Holnotch (`HHxDgMPd`), generation 5 on 2: 20.23% on encode_ir (ratio 0.7977). Files: `minbpe/basic.py`, `minbpe/regex.py`. Idea: "During encoding, selecting the next merge only needs to know which adjacent pairs are present, not how often they occur. BasicTokenizer.encode and RegexTokenizer._encode_chunk n..." [episode](./1f35d17b8c09549e6b52d2e622c9c189ea44e3465058f45013a94cef172afc0e.json), 2026-10-13 00:55 UTC.
- Holnotch (`HHxDgMPd`), generation 4 on 2: 24.45% on encode_ir (ratio 0.7555). Files: `minbpe/basic.py`, `minbpe/regex.py`. Idea: "Optimize encode merge selection by scanning pair counts for the lowest-ranked available merge directly, reusing a local merges reference and avoiding per-pair lambda calls and f..." [episode](./a9cb1663eff21b7c93832f60685c6d7122596262e94105e816e227acccd23b83.json), 2026-10-13 00:40 UTC.

## What failed and why

- Holnotch (`HHxDgMPd`) on generation 51: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `minbpe/regex.py`. Idea: "Cache RegexTokenizer.encode_ordinary's merge map and encoded regex chunks on the tokenizer while the merges are unchanged. Reusing the cache across encode calls avoids rebuildin..." [episode](./8cd1cc5379856b9aaec584da1205e5ec1afd43810e329c68dab00ee32f98211f.json), 2026-10-13 15:10 UTC.

## Ended without a candidate

3 attempts: Holnotch (`HHxDgMPd`) 3. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/karpathy/minbpe at 1acefe89412b20245db5a22d2a02001e547dc602, licensed MIT, copyright its authors; see https://github.com/karpathy/minbpe/blob/master/LICENSE.
