---
layout: default
title: Annotation
permalink: /annotation
---

## Dataset Directory Structure

* `color_image`: Continuous RGB frames as png format, frame rate 60fps
* `depth_raw`: Continuous Depth frames as numpy format, each frame corresponds to the same name RGB frame, frame rate 60fps
* `event_image`: Continuous Event frames as png format, images generated using aggregation events into frames, frame rate 120fps, the corresponding relationship with RGB and Depth images needs to be obtained from label
* `event_raw`: Raw event camera output file, We have temporarily retained this file and NOT released yet
* `color_label`: Annotation files for RGB and Depth images of the same name
* `event_label`: Annotation files for Event images of the same name

```
CDEHP
├── outdoor                             # Part of Dataset taken outdoors
│   ├── train                           # Train set
│   │   ├── A0001P0001S00               # A0001 -> Action 1, P0001 -> Person 1, S00 -> First Shot
│   │   │   ├── color_image             # RGB images
│   │   │   │   ├── 000000.png
│   │   │   │   ├── 000001.png
│   │   │   │   └── ******.png
│   │   │   ├── depth_raw               # Depth images
│   │   │   │   ├── 000000.npy
│   │   │   │   ├── 000001.npy
│   │   │   │   └── ******.npy
│   │   │   ├── event_image             # Event images
│   │   │   │   ├── 000000.png
│   │   │   │   ├── 000001.png
│   │   │   │   └── ******.png
│   │   │   ├── event_raw               # Raw event camera output bin file, NOT released yet
│   │   │   │   └── A0001P0001S00.bin
│   │   │   ├── color_label             # Label for RGB images
│   │   │   │   ├── 000000.txt
│   │   │   │   ├── 000001.txt
│   │   │   │   └── ******.txt
│   │   │   └── event_label             # Label for Event images
│   │   │       ├── 000000.txt
│   │   │       ├── 000001.txt
│   │   │       └── ******.txt
│   │   └── A0001P0002S00
│   └── valid                           # Validate set
│       └── ******
└── indoor                              # Part of Dataset taken indoors
    ├── train
    │   ├── A0001P0001S00
    │   └── ******
    └── valid
```

## Definition of Key Points

All annotations use a unified number of key points. We use 13 key points to label parts of the human body.

1. Head
2. Left Shoulder
3. Right Shoulder
4. Left Elbow
5. Right Elbow
6. Left Hand
7. Right Hand
8. Left Buttock
9. Right Buttock
10. Left Knee
11. Right Knee
12. Left Foot
13. Right Foot

## Annotation File Format

All annotation files use a unified format, however, there are some differences between the annotation formats of RGB images and Events. Keypoints are annotated as a percentage relative to the image resolution (x y). Please remember that the resolution of RGB images and Event images are not same, RGB and Depth image use a resolution of `848 x 480`, Event image use a resolution of `1280 x 800`.

### Label of RGB and Depth Image

```
13                                      # Number of key points, fixed at 13
event_name:000001                       # Corresponding event frame file name
0.7016509433962265 0.41458333333333336  # Percent coordinates relative to the image
0.7158018867924528 0.4375
0.7099056603773585 0.4479166666666667
0.7264150943396226 0.5166666666666667
0.7169811320754716 0.5166666666666667
0.7252358490566038 0.5583333333333333
0.7075471698113207 0.5791666666666667
0.7122641509433962 0.5666666666666667
0.7287735849056604 0.5708333333333333
0.7087264150943396 0.6333333333333333
0.7488207547169812 0.6479166666666667
0.6886792452830188 0.7083333333333334
0.7594339622641509 0.71875
```

### Label of Event

```
13                                      # Number of key points, fixed at 13
color_name:000000                       # Corresponding RGb and Depth frame file name
0.82513311428125 0.3706991523125        # Percent coordinates relative to the image
0.8501153806093751 0.4064099953625
0.839520654015625 0.4227385711125
0.8702200228593749 0.53560962
0.8532573636249999 0.5353109638375
0.8686109479765625 0.6034388406375
0.8375879402109374 0.6384934238375
0.84581029965625 0.6178776785375
0.875207627203125 0.624133925625
0.840438244625 0.7273246002875
0.9124168345546876 0.7509422192875
0.8057340086406249 0.8516001396125
0.932000952484375 0.86591200105
```
