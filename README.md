# email-classifier

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
