# MGRCM0065 Week 3 — AI for Finance

**Students: [open the notebook in Colab](https://colab.research.google.com/github/thezeming/mgrcm0065-week3/blob/main/MGRCM0065_W3_AI_for_Finance.ipynb)**, then *File → Save a copy in Drive*.

Data and pre-recorded model answers for the Week 3 Colab notebook.

This repo publishes `w3_bundle.json.gz`, next to the notebook: a single file packaging the code
(`build/w3_core.py`), `data/`, `cache/` and `VERSION.json` together. The notebook downloads it from
here every time its first cell runs and uses it. If a copy of `w3_bundle.json.gz` has already been
placed in Colab's working folder by hand, the notebook uses that instead and does not download at
all — this is the instructor's fallback if GitHub can't be reached from the venue.

`data/prices.csv` and `cache/responses.json` are a **matched pair**. The cached answers are keyed
on prompts that contain the last trading day in the price file, so publishing prices without the
answers recorded against them would leave every Lab 3 and Lab 4 cell with no cached answer for any
student who has no API key or has run out of quota. Always publish the whole bundle in one commit,
via:

```bash
python build/refresh.py --publish ~/mgrcm0065-week3-repo
```

| Path | What it is |
|---|---|
| `w3_bundle.json.gz` | The single file the notebook downloads: code + `data/` + `cache/` + `VERSION.json` |
| `data/prices.csv` | Daily prices, 8 tickers, 2019– (yfinance, adjusted closes) |
| `data/headlines.csv` | The 8 Lab 1 headlines, with realised returns and labels |
| `data/headlines_fresh.csv` | The 4 recent headlines (the after-training-cutoff control group) |
| `cache/responses.json` | Recorded model answers, with the trading day they were built for |
| `cache/committee.md` | The Lab 4 investment-committee transcript |
| `VERSION.json` | Version info; the `notebook`/`code_fingerprint` field bumps only when the notebook's code cells change |
