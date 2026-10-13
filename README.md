# Open EML, MSG and MBOX files in the browser

Read saved emails and mail archives in a browser tab and save messages as PDF. The file is read locally and never uploaded.

**Live:** https://savemail.app/?utm_source=github&utm_medium=referral&utm_campaign=links-2026-10


## Formats

| File | Where it comes from |
|---|---|
| `.eml` | standard saved email (Gmail download, Apple Mail, Thunderbird) |
| `.msg` | Outlook for Windows |
| `.mbox` | Google Takeout and other mailbox exports |

## What it does

- Shows the message with headers and attachments.
- Saves a message as PDF through the browser's print dialog.
- Downloads attachments as the original files.
- For MBOX: lists every message so you can pick the ones you need.

One PDF per message. Files of a few hundred MB open fine; very large Takeout exports are easier to handle if you export a single label.

## Tip: count messages in a Takeout MBOX with Python

```python
import mailbox
box = mailbox.mbox("All mail Including Spam and Trash.mbox")
print(sum(1 for _ in box), "messages")
```

---

This repository holds documentation only. Feedback is welcome in Issues.
