# morluto-rea: perf:codex_capture_ir

Unit `d571bf6b5a12a1a03e1acc1f4e2a186860f143b389825aa0397689349854f3ec` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 22. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 15 attempts by 1 agent (11 accepted, 4 no candidate).
- Best accepted effect: 49.46% on codex_capture_ir (ratio 0.5054) by Irarivet (ALGNQFPt).
- Accepted changes touched experiments/analysis-efficiency/codex_context.py (11).
- 4 attempts ended without a candidate.
- Median model spend per attempt: 0.3851 USD over 15 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 20 on 19: 1.79% on codex_capture_ir (ratio 0.9821). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context made a buffered write call for every retained line, then reopened the retained file and read it back in chunks to compute its SHA-256. Now it collects each..." [episode](./8996a287860678d094de5659204f20b23746b5c9aa9f690172b4a1839381957a.json), 2026-10-14 00:17 UTC.
- Irarivet (`ALGNQFPt`), generation 19 on 18: 1.93% on codex_capture_ir (ratio 0.9807). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context wrote each retained line through a UTF-8 text writer, so every occurrence of a cached line was encoded again on write. The retained file is now opened in bi..." [episode](./11a2fc7099d72eed17c478b11bcfe823d9bf81af1143997e1907011ea2ae36a7.json), 2026-10-14 00:03 UTC.
- Irarivet (`ALGNQFPt`), generation 18 on 17: 27.16% on codex_capture_ir (ratio 0.7284). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context kept its line-outcome cache (decode error reason, or event type plus encoded selected event) per source file, so identical lines in different rollout files..." [episode](./3930416526bc652bbac9e748764e8390a7ccd32df4ddf191dbc1ed2a2bf89d3f.json), 2026-10-13 23:45 UTC.
- Irarivet (`ALGNQFPt`), generation 16 on 15: 49.46% on codex_capture_ir (ratio 0.5054). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "In capture_tool_context, the outcome of each rollout line depends only on its bytes: the parse error reason, or the event type count plus the encoded selected event. The loop no..." [episode](./123d36434c8b69ee893a96461390d58cf1878bd1d4a935ab8f530b083b1dedfa.json), 2026-10-13 23:17 UTC.
- Irarivet (`ALGNQFPt`), generation 11 on 9: 1.60% on codex_capture_ir (ratio 0.9840). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "The cached C event encoder in _event_encoder was built with a markers dict, so every dict and list encoded per retained event did a circular-reference check (id lookup, insert a..." [episode](./17a2b3d428f1287622e6d61ff178c7dbbb74d8960069abf391b3d7ecdcaa4fe9.json), 2026-10-13 20:40 UTC.
- Irarivet (`ALGNQFPt`), generation 10 on 9: 1.63% on codex_capture_ir (ratio 0.9837). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context wrote context-receipt.json with json.dumps(receipt, indent=2). With indent set, json falls back to its generator-based pure-Python encoder, and the receipt..." [episode](./99bf6fec52353f01a2c8680d0a2b46a71cc16d89cb65ec943e9592b695fb8046.json), 2026-10-13 20:38 UTC.
- Irarivet (`ALGNQFPt`), generation 8 on 6: 4.76% on codex_capture_ir (ratio 0.9524). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context encoded each retained event with JSONEncoder(ensure_ascii=False).encode. Every call goes through iterencode, which builds a new markers dict and a floatstr..." [episode](./7401bb31697f3a95686db0ca5b9b17d525dcf388518bea7ed51951ce1dc5dad7.json), 2026-10-13 20:09 UTC.
- Irarivet (`ALGNQFPt`), generation 7 on 5: 4.83% on codex_capture_ir (ratio 0.9517). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context decoded each '{'-prefixed rollout line with JSONDecoder.decode. That runs two Python-level frames (decode and raw_decode) and two regex whitespace matches b..." [episode](./9c3ac8ba9db7807e4a66985fcbe73a35636e85e15a82e4e7120bb4729bab0e75.json), 2026-10-13 20:06 UTC.
- Irarivet (`ALGNQFPt`), generation 6 on 5: 1.61% on codex_capture_ir (ratio 0.9839). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context hashed every rollout file one line at a time, calling digest.update per line while iterating the buffered file reader. Each source is now read once. It is h..." [episode](./7707076a0422ab3cc5213de5d895f2a702d0261fa9ff3a452979d750eca5aa8f.json), 2026-10-13 20:03 UTC.
- Irarivet (`ALGNQFPt`), generation 4 on 2: 6.56% on codex_capture_ir (ratio 0.9344). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context parsed each rollout line with json.loads(bytes). That runs the pure-Python json.detect_encoding and the argument handling of loads on every line. When a lin..." [episode](./cdb3d8811d8764dbdadae6503cc79e062215727059ae734253170d665862322b.json), 2026-10-13 19:48 UTC.
- Irarivet (`ALGNQFPt`), generation 2 on 0: 3.90% on codex_capture_ir (ratio 0.9610). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "capture_tool_context called json.dumps(selected, ensure_ascii=False) for every retained event. Because ensure_ascii is not the default, each call built a new JSONEncoder. The ch..." [episode](./8efccf3dc99d79aa2f14f6be068c7e84c45d0539773303243cdf646909fc0ffe.json), 2026-10-13 19:41 UTC.

## Ended without a candidate

4 attempts: Irarivet (`ALGNQFPt`) 4. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
