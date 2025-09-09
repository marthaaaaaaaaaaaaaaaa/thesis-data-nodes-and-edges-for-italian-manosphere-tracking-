# Italian Manosphere — Nodes & Edges (Thesis Dataset)

This repository contains the graph data behind my thesis on Italian manosphere ecosystems.  
It includes **nodes** (accounts, channels, communities) and **edges** (retweets, mentions, replies, quotes, hyperlinks, co-appearances), collected across **X/Twitter, Reddit,**, with community and emotion labels to support reproducible network analysis.

## What’s inside
- `data/nodes.csv` — one row per actor/community.
- `data/edges.csv` — one row per interaction/tie.
- `data/metadata.json` — collection windows, platform notes, preprocessing steps.
- `docs/codebook.md` — definitions for fields and labels.

## Schemas
**nodes.csv** (suggested columns)
- `id` (string, unique)  
- `handle` (string)  
- `platform` (x|reddit|youtube|telegram|other)  
- `type` (person|org|media|bot|community|unknown)  
- `bubble` (Far-Right|Neo-Fascist|Manosphere Practices|Self-Improvement|Other)  
- `lang` (ISO 639-1)  
- `followers_count` (int, optional)  
- `created_at` (ISO 8601, optional)  
- `notes` (string, optional)

**edges.csv** (suggested columns)
- `source` (string, node id)  
- `target` (string, node id)  
- `relation` (retweet|reply|mention|quote|hyperlink|coappearance|subscription)  
- `platform` (as above)  
- `weight` (int, e.g., frequency)  
- `first_seen` (ISO 8601)  
- `last_seen` (ISO 8601)  
- `post_id` (string, optional)

## Ethics & scope
This dataset is released **for academic research and documentation** only.  
It may include references to extremist or misogynistic content for contextual analysis; no endorsement is implied. Personally identifying information has been minimized/aggregated where feasible.

## License
Recommended: **CC BY-NC 4.0** (non-commercial, with attribution). Adjust as needed.

## Cite
If you use this data, please cite:  
Conterno, A.M. (2025). *Italian Manosphere — Nodes & Edges (Thesis Dataset).* GitHub repository.
