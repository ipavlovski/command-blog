---
title: curl
date: 2019-07-29 23:16:31
tags:
---


### Download a binary into system bins dir

- `-L` - `--location`, redo the request on the new location
- `-o` - `--output` <file>, output to a file

```bash
sudo curl -L https://yt-dl.org/downloads/latest/youtube-dl -o /usr/local/bin/youtube-dl
```
