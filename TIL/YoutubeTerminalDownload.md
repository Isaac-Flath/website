---
title: "Download Youtube Videos with yt-dlp"
author: "Isaac Flath"
date: "2024-8-21"
description: "Download youtube videos with yt-dlp in the terminal"
categories: [terminal]
---

# Today I Learned

There's a magic terminal ccommand that can download youtube videos thanks to [Hamel's twitter post](https://x.com/HamelHusain/status/1825751477060522435)

[This](https://github.com/yt-dlp/yt-dlp) is the library it uses, which seems like it can do lots of stuff that may be useful some day.

```bash
yt-dlp -v -f mp4 --cookies-from-browser chrome "<url>"
```
