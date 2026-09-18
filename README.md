# MGRCM0065 Week 3 — AI for Finance

Data and pre-recorded model answers for the Week 3 Colab notebook.

The notebook carries its own embedded copy of everything here, so it works with no network at
all. On startup it checks this repo and, **only if every file downloads and the bundle is
internally consistent**, swaps in the newer one.

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
| `data/prices.csv` | Daily prices, 8 tickers, 2019– (yfinance, adjusted closes) |
| `data/headlines.csv` | The 8 Lab 1 headlines, with realised returns and labels |
| `data/headlines_fresh.csv` | The 4 recent headlines (the after-training-cutoff control group) |
| `cache/responses.json` | Recorded model answers, with the trading day they were built for |
| `cache/committee.md` | The Lab 4 investment-committee transcript |
| `VERSION.json` | Bundle version — the notebook only downloads when `data` differs |
