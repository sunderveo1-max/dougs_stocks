# Doug's semiconductor tracker

A static page with a daily snapshot of every US-listed stock in Morningstar's semiconductor industry group (chips, equipment & materials, solar).

- `index.html`: the page. It reads `semis.json` from the same folder.
- `semis.json`: the snapshot, rewritten after each trading day's close by a scheduled Claude task.

Snapshot format: `{"updated": ISO time, "rows": [{"symbol","name","seg","last","pct_change","market_cap","volume"}]}`, where `seg` is `chips`, `equipment` or `solar` and `pct_change` is a ratio (0.012 = +1.2%).

Data is delayed and for information only, not investment advice.
