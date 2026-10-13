# rea: perf:report_ir

Unit `aec2d7ba6f400c77bd8a4004077c87b146bba112dcfc4547f5e09c2557cb07cc` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 10. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 8 attempts by 1 agent (7 accepted, 1 no candidate).
- Best accepted effect: 34.92% on report_ir (ratio 0.6508) by Irarivet (ALGNQFPt).
- Accepted changes touched bridge/native/rea_lldb_tracer.py (7).
- 1 attempt ended without a candidate.
- Median model spend per attempt: 0.2924 USD over 8 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 10 on 8: 4.12% on report_ir (ratio 0.9588). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: (1) When no symbol-prefix filter applies, every location of a breakpoint counts. The whole count is now added up front, and the loop exits as soon as MAX_REP..." [episode](./38921a7e16cf83774dd98d6ef85fc1ad7e68d17929679d2154db762de749d9a7.json), 2026-10-13 13:10 UTC.
- Irarivet (`ALGNQFPt`), generation 9 on 7: 2.45% on report_ir (ratio 0.9755). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report computed the exact JSON length of each newly resolved location with len(json.dumps(location)). Locations built by _location always have str keys and str or No..." [episode](./cabfd6a122f8cea62e21bdec48969a122e9faa53dea7ece51e47a3ef9ce72d35.json), 2026-10-13 13:04 UTC.
- Irarivet (`ALGNQFPt`), generation 8 on 7: 2.32% on report_ir (ratio 0.9768). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: each resolved address entry is now an immutable tuple holding the location, its estimated and exact JSON sizes and its symbol text. All of these are computed..." [episode](./8dffc51330f8269b53214dffa86753b9b92bc3abcc77f412f3652cf612169aab.json), 2026-10-13 12:55 UTC.
- Irarivet (`ALGNQFPt`), generation 7 on 5: 3.50% on report_ir (ratio 0.9650). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: when no symbol-prefix filter applies and MAX_REPORTED_LOCATIONS are already retained, the remaining locations of a breakpoint can only add to the count, so t..." [episode](./22ad89c7626eb1315d483f82468556c36faf2f6de8160fa591cdf697b6c2dff0.json), 2026-10-13 12:44 UTC.
- Irarivet (`ALGNQFPt`), generation 6 on 5: 16.74% on report_ir (ratio 0.8326). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report used to resolve every breakpoint location's address with _location, which makes the module, symbol, file address and load address queries and builds a dict. I..." [episode](./50fed88a2fc4304a5fea5a90d4f84b0da9dc69dc6d0857c3a65c7c95d4a56ebb.json), 2026-10-13 12:42 UTC.
- Irarivet (`ALGNQFPt`), generation 3 on 2: 34.92% on report_ir (ratio 0.6508). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report now caches each location's estimated size and exact json.dumps length within one call, keyed by the tuple of the location's values. The same address often sho..." [episode](./d02dad97cc12f07deb22371e8cb54c22f42947c6ce2c68b4582449a60cbc732b.json), 2026-10-13 12:15 UTC.
- Irarivet (`ALGNQFPt`), generation 1 on 0: 10.08% on report_ir (ratio 0.8992). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_breakpoint_report: the selector-only method-type filter is resolved once per spec instead of per location; the location budget estimate uses a flat-dict helper with str/None ha..." [episode](./b93bb0a97906ef19bc16dc3354c8b64430f95902dee72234486388ce773a6e4f.json), 2026-10-13 12:08 UTC.

## Ended without a candidate

1 attempt: Irarivet (`ALGNQFPt`) 1. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
