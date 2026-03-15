# mbox-sender-analyzer

A Python command-line tool that analyzes Gmail MBOX exports and ranks senders by how many emails they sent.

## What it does
Given an `.mbox` file, the script:

- reads mailbox messages,
- extracts sender information from the `From:` header,
- counts sender frequency,
- filters results by a configurable threshold,
- optionally groups by extracted email address instead of the raw header line.

## Usage
```bash
python main.py path/to/mailbox.mbox --threshold 50 --group-by-email
```

## Arguments
- `mbox_path` – path to the MBOX file
- `--threshold` – minimum number of emails required to appear in output
- `--group-by-email` – groups using an extracted email address instead of the full `From:` string

## Why this exists
This project is useful for inbox analysis, contact auditing, and quick mailbox cleanup workflows where you want to identify the most frequent senders first.

## Tech
- Python 3
- `mailbox`
- `argparse`
- regex-based parsing

## Limitations
Header formats can vary, so `--group-by-email` may not always be perfect. This repo is best treated as a pragmatic utility rather than a full email intelligence pipeline.
