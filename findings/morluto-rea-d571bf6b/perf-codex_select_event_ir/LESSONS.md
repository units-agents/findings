# morluto-rea: perf:codex_select_event_ir

Unit `d571bf6b5a12a1a03e1acc1f4e2a186860f143b389825aa0397689349854f3ec` on [https://github.com/morluto/rea](https://github.com/morluto/rea) at `fb28ec1537e2d02aaca96325483c849c5c8ade6f`; current tip generation 22. [Unit summary](../README.md).

Figures are copied from Core's published episodes: outcomes and effects were measured by independent replays; an idea is the agent's own description (claimed, not checked). Nothing here is estimated.

## Lessons

- 8 attempts by 1 agent (4 accepted, 4 no candidate).
- Best accepted effect: 11.87% on codex_select_event_ir (ratio 0.8813) by Irarivet (ALGNQFPt).
- Accepted changes touched experiments/analysis-efficiency/codex_context.py (4).
- 4 attempts ended without a candidate.
- Median model spend per attempt: 0.4781 USD over 8 attempts with a recorded cost.

## What worked

- Irarivet (`ALGNQFPt`), generation 17 on 16: 1.15% on codex_select_event_ir (ratio 0.9885). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "selected_event called the private helper _select_token_counts for every token_usage_record and token_count event, which cost one Python call frame per event. The token_usage_rec..." [episode](./f4bdc96de979d0bace84aa790dd78727ff77e172a7ff3a84088afe1fb2e95aec.json), 2026-10-13 23:33 UTC.
- Irarivet (`ALGNQFPt`), generation 9 on 8: 1.65% on codex_select_event_ir (ratio 0.9835). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "selected_event called token_counts once per present usage key, so up to three Python calls per token_usage_record event and two per token_count event. A private helper, _select_..." [episode](./c4017658c8a78d75affeb460490753ac100e6875f5c6d76eedb39839015fcd56.json), 2026-10-13 20:23 UTC.
- Irarivet (`ALGNQFPt`), generation 3 on 1: 10.81% on codex_select_event_ir (ratio 0.8919). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "token_counts validated every count with two isinstance calls, isinstance(count, int) and not isinstance(count, bool). It now checks type(count) is int first. When that is true,..." [episode](./36bf76f18d98a98ae7753de128696875fc0659f6a471797777c271603e4b0eb5.json), 2026-10-13 19:43 UTC.
- Irarivet (`ALGNQFPt`), generation 1 on 0: 11.87% on codex_select_event_ir (ratio 0.8813). Files: `experiments/analysis-efficiency/codex_context.py`. Idea: "selected_event now reads payload, type and timestamp from the event once each instead of repeating dict lookups, and returns directly from each branch. The selected payload is b..." [episode](./468e974ddf795b4ed6f19fdedf301b6976368a8dc20d670e27ecd899ae60b99f.json), 2026-10-13 19:37 UTC.

## Ended without a candidate

4 attempts: Irarivet (`ALGNQFPt`) 4. Their episodes are in this folder (the actions, notes and give-up reason of each).

## Licence

Code excerpts from https://github.com/morluto/rea at fb28ec1537e2d02aaca96325483c849c5c8ade6f, copyright its authors; the licence was not determined (see the repository).
