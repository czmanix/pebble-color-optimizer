# Pebble Photo Optimizer

## Overview
Pebble Photo Optimizer is a web-based tool designed to help developers and designers convert full-color images into optimized 64-color assets for Pebble Time smartwatches.

Developing for Pebble's e-paper display can be challenging. [cite_start]What looks great on a bright computer monitor in software colors often loses contrast or looks completely different on the actual watch under various lighting conditions (like direct sunlight or the blue backlight)[cite: 4]. [cite_start]Standard conversion tools mathematically map colors to the standard Pebble palette, but the physical reality of the e-paper display often washes out details and ruins the designer's original vision[cite: 31, 39].

This tool solves this problem by using **hardware simulation palettes** (Sun, Room, Backlight). [cite_start]It calculates the best color match based on how the colors *actually appear* in real life, and then reverse-maps them to generate the correct standard Pebble color code you need for your project[cite: 38, 41].



## Features
* [cite_start]**Live Environment Previews:** Instantly see how your image will look across different lighting conditions side-by-side: Direct Sunlight, Standard Room lighting, and the watch's built-in Backlight[cite: 8, 42].
* [cite_start]**Reverse Mapping Export:** The algorithm finds the closest color in the targeted real-world environment, but seamlessly outputs the pure, saturated Pebble colors (`defined.png`) required for compilation in the Pebble SDK[cite: 41, 43].
* [cite_start]**Pre-processing Controls:** Adjust Brightness and Contrast *before* the color quantization to prevent shadows and highlights from merging into unreadable dark blobs[cite: 35, 36].
* [cite_start]**Advanced Dithering Modes:** Since the Pebble only supports 64 colors, dithering is crucial for creating the illusion of smooth gradients[cite: 19, 37].
    * [cite_start]**Off (Nearest Color):** Fast and clean, best for simple high-contrast graphics[cite: 77, 117].
    * **Atkinson Dithering:** Best for photos. The gold standard for e-paper displays. [cite_start]It distributes only 75% of the calculation error to surrounding pixels, preventing ugly cascading artifacts[cite: 105, 106].
    * [cite_start]**50:50 Checkerboard:** Best for UI elements. Intelligently calculates the exact "missing" color gap and mixes the two optimal distinct colors in a 2x2 grid to create natural, vibrant gradients[cite: 115, 146].

## Prerequisites
[cite_start]To run this tool locally, ensure that the `index.html` file and the four reference palette images are located in the same directory[cite: 61, 72]:
* `defined.png` (Standard Pebble 64-color palette)
* `sun.png` (Simulation under direct sunlight)
* `room.png` (Simulation in standard room lighting)
* `backlight.png` (Simulation with watch backlight turned on)

## How to Use
Try it here: [https://czmanix.github.io/pebble-color-optimizer/](https://czmanix.github.io/pebble-color-optimizer/)

**Workflow:**
1. **Upload Image:** Select your full-color source image.
2. **Reference Palette:** Choose which lighting condition you want to prioritize for color accuracy (e.g., choose "Sun" to make it look best outdoors).
3. **Dithering:** Select your preferred dithering method.
4. **Adjust:** Tweak Brightness and Contrast until the live previews look right.
5. **Export:** Right-click the **Export (Standard)** canvas, save the image, and drop it straight into your Pebble SDK project!
