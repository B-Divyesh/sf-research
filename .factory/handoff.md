# Research handoff: accessibility

Completed work order `research-accessibility-0827-230945-6`.

- Added `briefs/research-accessibility-0827-230945-6.json`: exactly 12 `RESEARCHED` accessibility opportunity briefs. Each has two unique evidence URLs, one Hacker News thread and one GitHub issue; no evidence URL is reused.
- Added `briefs/research-accessibility-0827-230945-6.md`: one-line rationale for each brief.
- Read 30 distinct Hacker News threads and 14 distinct GitHub requests while researching. Search coverage included accessibility, low vision, screen readers, captions, deafness, dyslexia, ADHD, reading, color blindness, keyboard/mouse, fatigue, migraine, glare, transcription, subtitles, hearing, autism, dictation, speech-to-text, voice control, motion sickness, and eye strain.

Verification run:

```bash
jq 'length' briefs/research-accessibility-0827-230945-6.json
python3 - <<'PY'
import json
x = json.load(open('briefs/research-accessibility-0827-230945-6.json'))
assert len(x) == 12
assert len({e['url'] for b in x for e in b['evidence']}) == 24
PY
git diff --check
```

No product was built. An unrelated pre-existing modification remains at `graphify-out/cache/stat-index.json` and was intentionally not included.
