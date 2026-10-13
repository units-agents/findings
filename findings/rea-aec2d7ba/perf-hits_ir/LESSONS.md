# rea: perf:hits_ir

Unit `aec2d7ba6f400c77bd8a4004077c87b146bba112dcfc4547f5e09c2557cb07cc` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 23. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 19 attempts by 1 agent (14 accepted, 2 rejected, 3 no candidate).
- Best accepted effect: 20.45% on hits_ir (ratio 0.7955) by Irarivet (ALGNQFPt).
- Accepted changes touched bridge/native/rea_lldb_tracer.py (14).
- Failed candidates: stale_conflict 1, no_improvement 1.
- Measured but below the minimum effect: 0.93% on hits_ir.
- 1 candidate failed because the parent moved under them (stale or conflicting with a newer generation).
- 3 attempts ended without a candidate.
- Median model spend per attempt: 0.3684 USD over 19 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 23 on 22: 1.68% on hits_ir (ratio 0.9832). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "On each breakpoint hit, _record_json looped over the record's register dicts a second time to encode them. That meant dict lookups, type checks, a cache lookup and an encode_bas..." [episode](./ed2003809d62b3b14ac825e8f2f882fc29c22f3f09a5c085c28624c84c6a7e39.json), 2026-10-13 18:06 UTC.
- Irarivet (`ALGNQFPt`), generation 22 on 21: 1.91% on hits_ir (ratio 0.9809). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "Per-hit work in bridge/native/rea_lldb_tracer.py. _record_estimate now reads argument registers inline, in one loop with one shared SBError, instead of calling _read_register fo..." [episode](./68b80abc03b44542fd362c4da620e89a841ccb669b86e9b322b6af8a64570d6f.json), 2026-10-13 17:23 UTC.
- Irarivet (`ALGNQFPt`), generation 21 on 20: 6.81% on hits_ir (ratio 0.9319). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "On every breakpoint hit, _handle_breakpoint ran _encode_json over the whole record. That included the five location keys, even though the encoded location text is already cached..." [episode](./2f9abce93645750c7b09a3f13d218c9242f3c11832873deff93e90dd138e9e1c.json), 2026-10-13 16:35 UTC.
- Irarivet (`ALGNQFPt`), generation 20 on 19: 1.19% on hits_ir (ratio 0.9881). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_handle_breakpoint already filters unwanted symbols with _wanted before calling _record_estimate, which repeated the same check on every hit. The check now lives in _record, the..." [episode](./8fea2998249b2373bbfe28ea7b385bb7d86efedf951b8bf5ddf2f4264bbf4464.json), 2026-10-13 16:13 UTC.
- Irarivet (`ALGNQFPt`), generation 19 on 18: 2.20% on hits_ir (ratio 0.9780). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "Per-hit backtrace path in bridge/native/rea_lldb_tracer.py. _frame_location now caches each module's filename and path keyed by id(module) in a bounded _FRAME_MODULES dict, with..." [episode](./49a78338255d780d9b5dae1a624dc3e1453a29077d043c80a685cc84ad02e055.json), 2026-10-13 15:59 UTC.
- Irarivet (`ALGNQFPt`), generation 17 on 16: 9.30% on hits_ir (ratio 0.9070). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_record_estimate computed the record's estimated size by calling _estimated_json_size on the whole record dict for every breakpoint hit. That walked all eight keys and recursed..." [episode](./bd144566d6c6b427d18d17c9c7856aeb1ce4c4ad92f932979d62f83147cf7caa.json), 2026-10-13 15:14 UTC.
- Irarivet (`ALGNQFPt`), generation 16 on 15: 4.76% on hits_ir (ratio 0.9524). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_handle_breakpoint built the stopped PC's location with the uncached _location, then re-estimated it in _record, then ran _estimated_json_size over the whole record (base fields..." [episode](./c0a57942ce619304a73f739945c0fac3705356e94c0d6290fe00e3571cf30126.json), 2026-10-13 14:56 UTC.
- Irarivet (`ALGNQFPt`), generation 15 on 14: 6.70% on hits_ir (ratio 0.9330). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_frame_location now memoises the whole backtrace frame entry (location dict, estimated size, lazily filled json text) keyed by the raw LLDB values (load address int, file addres..." [episode](./4e46d287f4621c305a8243387d43b1478bd6b202731113a127e84bfe7896b86d.json), 2026-10-13 14:39 UTC.
- Irarivet (`ALGNQFPt`), generation 14 on 12: 3.24% on hits_ir (ratio 0.9676). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In _handle_breakpoint's backtrace loop, each frame previously built its location dict with _location and then passed it to _location_sizes, which built a memo key from tuple(loc..." [episode](./7c3b002016a7efe3d3db6f6d8d209bd222a8cae502e7ea68081035f1081b690f.json), 2026-10-13 14:30 UTC.
- Irarivet (`ALGNQFPt`), generation 13 on 12: 20.45% on hits_ir (ratio 0.7955). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_handle_breakpoint serialized each event twice: json.dumps(record) for the exact budget check, then json.dumps again on the whole journal row with the filled backtrace. Now the..." [episode](./0542a96fab94ad4c4e38e3e866eb7980fbf50490e05a6b7c333ca3c5d113a84e.json), 2026-10-13 14:20 UTC.
- Irarivet (`ALGNQFPt`), generation 11 on 9: 1.06% on hits_ir (ratio 0.9894). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "_handle_breakpoint's backtrace loop looked up context["retained_trace_bytes"], context["target"], record["backtrace"] and thread.GetFrameAtIndex on every frame. These values do..." [episode](./d4087fe98d17978933cd4b0cd542e19243d1ce4d6e1bbf1bd70627d67d99a14a.json), 2026-10-13 13:46 UTC.
- Irarivet (`ALGNQFPt`), generation 5 on 3: 15.33% on hits_ir (ratio 0.8467). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In _handle_breakpoint's backtrace loop, each frame location's estimated JSON size and exact JSON length are now memoised in a small module-level cache keyed by tuple(location.it..." [episode](./8579b7963c0d1a0d106bb61734d82ec183e5e5ddf218791d8fbcb3b9e73de122.json), 2026-10-13 12:24 UTC.
- Irarivet (`ALGNQFPt`), generation 4 on 2: 6.92% on hits_ir (ratio 0.9308). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In the breakpoint hit path, the exact JSON length of each backtrace location was computed with len(json.dumps(location)). A new helper, _location_json_size, computes the same le..." [episode](./1f1ef56746be76603bf07e1f4ebab06c988588e6fd81d1ed7958fcdb55070561.json), 2026-10-13 12:17 UTC.
- Irarivet (`ALGNQFPt`), generation 2 on 0: 8.00% on hits_ir (ratio 0.9200). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "In the breakpoint hit path, the dict and list branches of _estimated_json_size now loop explicitly and handle str, None and int values inline. They fall back to recursion for ev..." [episode](./2779233538b3d68fabf9f3a19f3c9d7e86ee9befd80ed5659df09074d792066c.json), 2026-10-13 12:10 UTC.

## What failed and why

- Irarivet (`ALGNQFPt`) on generation 21: no_improvement, "worst ratio 0.9907 vs required 0.9900". Measured 0.93% on hits_ir (ratio 0.9907). Files: `bridge/native/rea_lldb_tracer.py`. Idea: "Per-hit register handling in bridge/native/rea_lldb_tracer.py. _record_estimate called _read_register once per argument register, and each call built a new lldb.SBError. The rea..." [episode](./a93f42a33100ea69154cf4261e26577e8d8606de5fdbb339ef35668a76e725f3.json), 2026-10-13 16:52 UTC.
- Irarivet (`ALGNQFPt`) on generation 1: stale_conflict (verdict: apply_conflict), "patch does not apply to parent". Files: `bridge/native/rea_lldb_tracer.py`. Idea: "Breakpoint hit path in bridge/native/rea_lldb_tracer.py: the record, primary location and backtrace location size estimates use the flat-dict helper _estimated_location_size. It..." [episode](./753995c17d81cd9d031aa1e0dba0962697df2bdd565af5c8beb35ae3eb6573cc.json), 2026-10-13 12:13 UTC.

## Ended without a candidate

3 attempts: Irarivet (`ALGNQFPt`) 3. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
