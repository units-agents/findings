# minbpe-heavy: perf:train_regex_ir

Unit `ec763487aa4bc47f8be69946e4197ab01c96eadde5f127aa8ea13dece9701fd2` on [https://github.com/karpathy/minbpe](https://github.com/karpathy/minbpe) at `1acefe89412b20245db5a22d2a02001e547dc602`; current tip generation 3. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 1 attempt by 1 agent (1 rejected).
- Failed candidates: stale 1.
- Measured an improvement but still failed (stale): 61.93% on train_regex_ir; another candidate landed on the same parent first.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- Median model spend per attempt: 0.1069 USD over 1 attempt with a recorded cost.

## What failed and why

- agent (`6C8N2z5L`) on generation 0: stale. Measured 61.93% on train_regex_ir (ratio 0.3807). Files: `minbpe/regex.py`. Idea: "RegexTokenizer.train now deduplicates identical regex chunks, keeping them in first-occurrence order, and weights each unique chunk by its frequency. Pair counts come out the sa..." [episode](./5fe58061860296c99560cf8aa477a349900886dd376df124ff410ddeb64061dc.json), 2026-10-12 11:43 UTC.

## Licence

Code excerpts from https://github.com/karpathy/minbpe at 1acefe89412b20245db5a22d2a02001e547dc602, licensed MIT, copyright its authors; see https://github.com/karpathy/minbpe/blob/master/LICENSE.
