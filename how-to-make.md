---
layout: default
title: How to Make CDEHP-Dataset
permalink: /how-to-make
---

## Introduction

We fixed a depth camera and an event camera on a simple tripod, took videos of multiple groups of volunteers and multiple groups of actions, and then used crowdsourcing and post-review methods to annotate the labels.

## Hardware Requirements

* A depth camera (We use `Intel® RealSense™ D435i`).
* An event-based camera/dynamic vision sensor (We use `CelePixel CeleX5`).
* An infrared filter, in order to avoid the infrared ranging module of the depth camera from affecting the event camera.

## Building Cameras Stand

We recommend using 3D printing technology to make a simple bracket to firmly fix two or more cameras to avoid deviation due to vibration after calibration.

![Cameras Stand](/assets/how-to-make_1.png)

## Camera calibration

We use `Zhang's method` for stereo camera calibration to obtain the parameters between the two cameras. Then we can use the homography transformation algorithm to convert the annotations of key points on the RGB image to the corresponding positions on the event frame.

1. Prepare a `Calibration Patterns Board(Checkerboards)`, the bigger the better, that can accurately calculate longer-distance movements.
2. Use [Shooting Tool](https://github.com/CDEHP-Dataset/Tools/tree/main/calibration) to take sets of photos at different angles, distances and locations. The more the better.
3. Detect key points of the chessboard on all photos, we use `Camera Calibrator` App in `MATLAB`.
4. Use [Calibration-Tool](https://github.com/CDEHP-Dataset/Calibration-Tool) calculate parameters between cameras.

## Recording Dataset

Use [Recording-Tool](https://github.com/CDEHP-Dataset/Recording-Tool) recording dataset.

## Label Dataset

Use [Annotation-Tool](https://github.com/CDEHP-Dataset/Annotation-Tool) label the dataset.
