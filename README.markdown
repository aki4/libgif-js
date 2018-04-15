# Overview

This is the fork of buzzfeed's libgif-js https://github.com/buzzfeed/libgif-js (that is fork of https://github.com/shachaf/jsgif with some changes).

This repository contains example of gif to canvas loading and canvas to gif export with custom delay for each frame support.
It works correctly only with one gif per canvas.

## Caveat: same-domain origin (important!)

The gif has to be on the same domain (and port and protocol) as the page you're loading.

The library works by parsing gif image data in js, extracting individual frames, and rendering them on a canvas element. There is no way to get the raw image data from a normal image load, so this library does an XHR request for the image and forces the MIME-type to "text/plain". Consequently, using this library is subject to all the same cross-domain restrictions as any other XHR request.

## Used libraries

1. jsgif (Gif encoder, LZW encoder, NeuQuant algorithm) - https://github.com/antimatter15/jsgif
2. lingif-js (gif import to canvas) - https://github.com/buzzfeed/libgif-js 
