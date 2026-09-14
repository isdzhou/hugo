---
title: "Rime"
date: 2026-09-14T19:59:37+08:00
slug: "b5183379"
draft: false
tags: ["rime", "输入法"]
categories: ["输入法"]
description: ""
---

[RIME | 中州韻輸入法引擎](https://rime.im/)

## [白霜词库](https://github.com/zjralhf/rime--)

```shell
# rime 用户文件夹
git clone --depth 1 https://github.com/gaboolic/rime-frost
# 更新
git pull
```

## 不同软件默认中英文

```yaml
# weasel.custom.yaml
patch:
  # 针对特定应用程序单独定制输入状态
  app_options:
    # 终端 / 编辑器：切换进入时默认进入英文（ascii_mode）
    Code.exe:
      ascii_mode: true
    WindowsTerminal.exe:
      ascii_mode: true
    cmd.exe:
      ascii_mode: true
    powershell.exe:
      ascii_mode: true
    idea64.exe:
      ascii_mode: true

    # 办公 / 聊天软件：切换进入时保持默认中文
    WINWORD.EXE:
      ascii_mode: false
    WeChat.exe:
      ascii_mode: false
```
