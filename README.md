# Video Stream &#127909;

Bare-bones video streaming web app.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Setup](#setup)
- [Usage](#usage)
- [License](#license)

## Introduction

This is a bare-bones prototype video-streaming web app. 

## Main Features

- Streams video files from anywhere accessible by the host machine, including mounted network and USB drives.
- Subtitles automatically play if they are included alongside the video.
- The position within each video is saved, and the video will resume from that point automatically.

## Installation

Step-by-step instructions on how to get the development environment running.

```bash
git clone https://github.com/yarrumevets/videostream.git
cd videostream
yarn
```

## Setup

You'll need to have a folder accessible by the host machine to use as the root folder, where your videos will be stored.
This can be a local folder, or one on a mounted network or USB drive.

Edit config.json setting the rootPath to the absolute path, ex: "rootPath": "/Volumes/ExternalHD/Movies".

There is a specific folder structure and format that needs to be followed within the root folder:
- Each video must be in its own subfolder, and this folder must be in the 'root' folder, the rootPath specified above.
- The name of the folder will be the video's title displayed on the page
- You can have 1 subtitle file that must be in .vtt format and in the same folder as the video, and must named subtitles.vtt
- The cover image must be named cover.jpg in the same folder as the video. It will look better if it is roughly 2:3 aspect ratio. This will be the display image on the index page.
- Videos must be in a compatible format such as .mp4 (https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs)
- Set the server `port` in config.js

## Usage
```bash
node server.js
```
Go to http://localhost:`port` in your browser.

## License

Distributed under the MIT License. See the LICENSE file for more information.

## Media Sources
The example videos used in this project are sourced from [Pexels](https://www.pexels.com/) and are used in compliance with their [license](https://www.pexels.com/license/).