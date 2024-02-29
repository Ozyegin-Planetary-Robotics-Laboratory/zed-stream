# zed-stream

## Introduction

- This repository contains two scripts that are purposed for streaming and showcasing a ZED camera stream using GStreamer and the ZED GStreamer plugin.

- AVC is utilized for encoding video stream. ( https://gstreamer.freedesktop.org/documentation/x264/index.html )

## Installation

First of all, [GStreamer](https://gstreamer.freedesktop.org/documentation/installing/index.html), [ZED SDK](https://www.stereolabs.com/docs/gstreamer/#installation) and [ZED GStreamer plugin](https://github.com/stereolabs/zed-gstreamer) must be installed. 

> [!Important]  
> The ZED SDK has a large size so make sure you have enough space before downloading.

Then clone the repositories and you may readily use the scripts.

## Usage

The scripts are meant to be used on two different machines connected through a wireless network, do not use this script if your purpose is to simply view the camera feed. You will suffer a loss of quality that can hardly be justified.

```
sudo bash zed_transmit <target_port> <target_ip>
sudo bash zed_receive <target_port>
```

The parameters target_port must match in order for this to work properly.