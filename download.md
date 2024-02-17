---
layout: default
title: Download
permalink: /download
---

## Download Link

| File Name | Google Drive | Baidu Disk | Github | sha256sum |
| :-------: | :----------: | :--------: | :----: | :-------: |
|   1.zip   |              |            |        |           |
|   2.zip   |              |            |        |           |

## Integrity Verification

After all chunks have been downloaded, it is strongly recommended that you perform a consistency check.

```shell
sha256sum 1.zip | sha256sum -c
```

## Unzip the Dataset

```shell
```

## Dataset Directory Structure

* `color`: Continuous RGB frames as png format
* `depth`: Continuous depth frames as numpy format, each frame corresponds to the same name RGB frame
* `event`: Raw event camera output file, We have temporarily retained this file and NOT released yet

```
CDEHP
├── outdoor
│   ├── train                           # Part of Dataset taken outdoors
│   │   ├── A0001P0001                  # A0001 -> Action 1, P0001 -> Person 1
│   │   │   └── S00                     # S00 -> First Shot
│   │   │       ├── color               # Continuous RGB frames as png format
│   │   │       │   ├── 000000.png
│   │   │       │   ├── 000001.png
│   │   │       │   └── ******.png
│   │   │       ├── depth               # Continuous depth frames as numpy format, each frame corresponds to the same name RGB frame
│   │   │       │   ├── 000000.npy
│   │   │       │   ├── 000001.npy
│   │   │       │   └── ******.npy
│   │   │       ├── event               # Raw event camera output file, We have temporarily retained this file and NOT released yet
│   │   │       │   └── A0001_P0001_S00.bin
└── indoor                              # Part of Dataset taken indoors
```
