# rea: perf:hits_ir

Unit `aec2d7ba6f400c77bd8a4004077c87b146bba112dcfc4547f5e09c2557cb07cc` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 12. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 7 attempts by 1 agent (4 accepted, 1 rejected, 2 no candidate).
- Best accepted effect: 15.33% on hits_ir (ratio 0.8467) by Irarivet (ALGNQFPt).
- Accepted changes touched bridge/native/rea_lldb_tracer.py (4).
- Failed candidates: stale_conflict 1.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- 2 attempts ended without a candidate.
- Median model spend per attempt: 0.2671 USD over 7 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 11 on 9: 1.06% on hits_ir (ratio 0.9894). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_handle_breakpoint's backtrace loop looked up context["retained_trace_bytes"], context["target"], record["backtrace"] and thread.GetFrameAtIndex on every frame. These values do..." [episode](./d4087fe98d17978933cd4b0cd542e19243d1ce4d6e1bbf1bd70627d67d99a14a.json), 2026-10-13 13:46 UTC.
- Irarivet (`ALGNQFPt`), generation 5 on 3: 15.33% on hits_ir (ratio 0.8467). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In _handle_breakpoint's backtrace loop, each frame location's estimated JSON size and exact JSON length are now memoised in a small module-level cache keyed by tuple(location.it..." [episode](./8579b7963c0d1a0d106bb61734d82ec183e5e5ddf218791d8fbcb3b9e73de122.json), 2026-10-13 12:24 UTC.
- Irarivet (`ALGNQFPt`), generation 4 on 2: 6.92% on hits_ir (ratio 0.9308). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In the breakpoint hit path, the exact JSON length of each backtrace location was computed with len(json.dumps(location)). A new helper, _location_json_size, computes the same le..." [episode](./1f1ef56746be76603bf07e1f4ebab06c988588e6fd81d1ed7958fcdb55070561.json), 2026-10-13 12:17 UTC.
- Irarivet (`ALGNQFPt`), generation 2 on 0: 8.00% on hits_ir (ratio 0.9200). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In the breakpoint hit path, the dict and list branches of _estimated_json_size now loop explicitly and handle str, None and int values inline. They fall back to recursion for ev..." [episode](./2779233538b3d68fabf9f3a19f3c9d7e86ee9befd80ed5659df09074d792066c.json), 2026-10-13 12:10 UTC.

## What failed and why

- Irarivet (`ALGNQFPt`) on generation 1: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `bridge/native/rea_lldb_tracer.py`. Idea: "Breakpoint hit path in bridge/native/rea_lldb_tracer.py: the record, primary location and backtrace location size estimates use the flat-dict helper _estimated_location_size. It..." [episode](./753995c17d81cd9d031aa1e0dba0962697df2bdd565af5c8beb35ae3eb6573cc.json), 2026-10-13 12:13 UTC.

## Ended without a candidate

2 attempts: Irarivet (`ALGNQFPt`) 2. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
