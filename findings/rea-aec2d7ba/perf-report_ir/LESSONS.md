# rea: perf:report_ir

Unit `aec2d7ba6f400c77bd8a4004077c87b146bba112dcfc4547f5e09c2557cb07cc` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 7. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 4 attempts by 1 agent (4 accepted).
- Best accepted effect: 34.92% on report_ir (ratio 0.6508) by Irarivet (ALGNQFPt).
- Accepted changes touched bridge/native/rea_lldb_tracer.py (4).
- Median model spend per attempt: 0.2778 USD over 4 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 7 on 5: 3.50% on report_ir (ratio 0.9650). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: when no symbol-prefix filter applies and MAX_REPORTED_LOCATIONS are already retained, the remaining locations of a breakpoint can only add to the count, so t..." [episode](./22ad89c7626eb1315d483f82468556c36faf2f6de8160fa591cdf697b6c2dff0.json), 2026-10-13 12:44 UTC.
- Irarivet (`ALGNQFPt`), generation 6 on 5: 16.74% on report_ir (ratio 0.8326). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report used to resolve every breakpoint location's address with _location, which makes the module, symbol, file address and load address queries and builds a dict. I..." [episode](./50fed88a2fc4304a5fea5a90d4f84b0da9dc69dc6d0857c3a65c7c95d4a56ebb.json), 2026-10-13 12:42 UTC.
- Irarivet (`ALGNQFPt`), generation 3 on 2: 34.92% on report_ir (ratio 0.6508). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report now caches each location's estimated size and exact json.dumps length within one call, keyed by the tuple of the location's values. The same address often sho..." [episode](./d02dad97cc12f07deb22371e8cb54c22f42947c6ce2c68b4582449a60cbc732b.json), 2026-10-13 12:15 UTC.
- Irarivet (`ALGNQFPt`), generation 1 on 0: 10.08% on report_ir (ratio 0.8992). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: the selector-only method-type filter is resolved once per spec instead of per location; the location budget estimate uses a flat-dict helper with str/None ha..." [episode](./b93bb0a97906ef19bc16dc3354c8b64430f95902dee72234486388ce773a6e4f.json), 2026-10-13 12:08 UTC.

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
