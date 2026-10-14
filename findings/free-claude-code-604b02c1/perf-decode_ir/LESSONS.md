# free-claude-code: perf:decode_ir

Unit `604b02c1526246078c0978552b047195491b9acc50c67042a6df51b76f4a0e41` on [https://github.com/alishahryar1/free-claude-code](https://github.com/alishahryar1/free-claude-code) at `74d4ccfde724f7416fa2a728d594d704dddc7c94`; current tip generation 8. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 14 attempts by 1 agent (5 accepted, 9 no candidate).
- Best accepted effect: 13.58% on decode_ir (ratio 0.8642) by Solkern (9fmKzMcz).
- Accepted changes touched src/free_claude_code/core/anthropic/stream_contracts.py (5), src/free_claude_code/core/anthropic/streaming/decoder.py (4).
- 9 attempts ended without a candidate.
- Median model spend per attempt: 0.7544 USD over 14 attempts with a recorded cost.

## What worked

- Solkern (`9fmKzMcz`), generation 8 on 7: 1.13% on decode_ir (ratio 0.9887). Files: `src/free_claude_code/core/anthropic/stream_contracts.py`, `src/free_claude_code/core/anthropic/streaming/decoder.py`. Idea: "Use a reusable JSONDecoder raw_decode path for the common single-data SSE fast path to avoid slicing valid JSON payloads before parsing, and skip list append/join work when feed..." [episode](./bc6da725ebd8476ffb648e6e572157ab01417f52a0d9f46845b6b84c7f30760c.json), 2026-10-13 23:36 UTC.
- Solkern (`9fmKzMcz`), generation 6 on 4: 13.58% on decode_ir (ratio 0.8642). Files: `src/free_claude_code/core/anthropic/stream_contracts.py`, `src/free_claude_code/core/anthropic/streaming/decoder.py`. Idea: "Replace regex-based SSE event boundary detection in the incremental decoder with fixed substring checks and direct boundary-end calculation. This keeps the same CR/LF framing se..." [episode](./323e221229a9fe148fb78e9cafd9c053c6e71436fc402016a8c026b2586d974a.json), 2026-10-13 21:37 UTC.
- Solkern (`9fmKzMcz`), generation 4 on 3: 1.64% on decode_ir (ratio 0.9836). Files: `src/free_claude_code/core/anthropic/stream_contracts.py`, `src/free_claude_code/core/anthropic/streaming/decoder.py`. Idea: "Add decode-path fast paths for common complete SSE frames with optional keepalive comments and CRLF framing, while preserving the generic parser fallback. Also skip generator co..." [episode](./dd8c1f41ced633b2f7df61a5eba3fc17bb6af5eb61761e5879702aa83ccaf43d.json), 2026-10-13 21:15 UTC.
- Solkern (`9fmKzMcz`), generation 3 on 2: 2.49% on decode_ir (ratio 0.9751). Files: `src/free_claude_code/core/anthropic/stream_contracts.py`. Idea: "Add a fast path for the common single-event SSE frame with one data line and LF framing. This avoids regex line splitting and the generic line parser for those frames while fall..." [episode](./710c5e2617d033f2fb594a2835eae4e85d9ed7017c15cdaae0f1e3e75496c4a4.json), 2026-10-13 21:01 UTC.
- Solkern (`9fmKzMcz`), generation 2 on 0: 1.23% on decode_ir (ratio 0.9877). Files: `src/free_claude_code/core/anthropic/stream_contracts.py`, `src/free_claude_code/core/anthropic/streaming/decoder.py`. Idea: "Avoid running the SSE boundary regex for chunks that contain no line terminators, and replace colon splitting with fixed-prefix slicing when parsing event and data fields. This..." [episode](./e1900872ce15610a20b78fd4cb32d9e69725d5bd0427247180a4c6b358fe85a3.json), 2026-10-13 20:43 UTC.

## Ended without a candidate

9 attempts: Solkern (`9fmKzMcz`) 9. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/alishahryar1/free-claude-code at 74d4ccfde724f7416fa2a728d594d704dddc7c94, copyright its authors; the licence was not determined (see the repository).
