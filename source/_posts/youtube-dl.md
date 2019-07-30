---
title: youtube-dl
date: 2019-07-29 22:45:35
tags:
---

### Playlist download - general

```bash
#+BEGIN_SRC bash
youtube-dl \
--ignore-errors \
--hls-prefer-ffmpeg \
--output '%(title)s.%(ext)s' \
--restrict-filenames \
--continue \
--format 'bestaudio/best' \
--extract-audio \
--audio-format 'mp3' \
--audio-quality 0 \
--embed-thumbnail \
--prefer-ffmpeg \
https://www.youtube.com/playlist?list=IDSTRING1-IDSTRING2
```

### Playlist download - for caustic

Playlist subset with wave format, and playlist index in the title.
Cannot embed thumbnail into wave formats.

```bash
youtube-dl \
--ignore-errors \
--continue \
--playlist-start 151 \
--playlist-end 200 \
--output '%(playlist_index)s-%(title)s.%(ext)s' \
--restrict-filenames \
--extract-audio \
--format 'bestaudio/best' \
--audio-quality 0 \
--audio-format 'wav' \
--hls-prefer-ffmpeg \
--prefer-ffmpeg \
https://www.youtube.com/playlist?list=IDSTRING1-IDSTRING2
```

