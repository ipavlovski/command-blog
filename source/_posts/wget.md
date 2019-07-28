---
title: wget
date: 2019-07-26 18:01:12
tags:
---

## Create a copy from remote repo locally

- `--cut-dirs=2` would strip auto-created greenpowerpbc.svn.cloudforge.com/pems dirs
- `-R "index.html*"` remove all auto-created html files
- `--user` and `--password` for credentials
- `mirror` - `-r` recursive, `-l inf`unlimited depth
- `np` - no parents. prevents wget from copying the entire root directory
- `nH`

```
wget --mirror -np -R "index.html*" -nH --cut-dirs=2 \
  --user user1 --password pass1 \
  https://greenpowerpbc.svn.cloudforge.com/pems/trunk
```