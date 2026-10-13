# morluto-rea: perf:codex_capture_ir

Unit `d571bf6b5a12a1a03e1acc1f4e2a186860f143b389825aa0397689349854f3ec` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 4. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 2 attempts by 1 agent (2 accepted).
- Best accepted effect: 6.56% on codex_capture_ir (ratio 0.9344) by Irarivet (ALGNQFPt).
- Accepted changes touched experiments/analysis-efficiency/codex_context.py (2).
- Median model spend per attempt: 0.3247 USD over 2 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 4 on 2: 6.56% on codex_capture_ir (ratio 0.9344). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context parsed each rollout line with json.loads(bytes). That runs the pure-Python json.detect_encoding and the argument handling of loads on every line. When a lin..." [episode](./cdb3d8811d8764dbdadae6503cc79e062215727059ae734253170d665862322b.json), 2026-10-13 19:48 UTC.
- Irarivet (`ALGNQFPt`), generation 2 on 0: 3.90% on codex_capture_ir (ratio 0.9610). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context called json.dumps(selected, ensure_ascii=False) for every retained event. Because ensure_ascii is not the default, each call built a new JSONEncoder. The ch..." [episode](./8efccf3dc99d79aa2f14f6be068c7e84c45d0539773303243cdf646909fc0ffe.json), 2026-10-13 19:41 UTC.

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
