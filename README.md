# Pebble Photo Optimizer

## Overview
Pebble Photo Optimizer is a web-based tool designed to help developers and designers convert full-color images into optimized 64-color assets for Pebble Time smartwatches. 

**Try it live:** [https://czmanix.github.io/pebble-color-optimizer/](https://czmanix.github.io/pebble-color-optimizer/)

Developing for Pebble's e-paper display can be challenging. What looks great on a bright computer monitor often loses contrast on the actual watch under different real-world lighting conditions. Standard conversion tools mathematically map colors to the standard palette, but the physical display often washes out details.

This tool solves this by using hardware simulation palettes. It calculates the best color match based on how colors actually appear in real life, and reverse-maps them to generate the pure standard Pebble color code.

## Features
* **Live Environment Previews**: See how your image will look across different lighting conditions side-by-side: Direct Sunlight, Standard Room lighting, and Backlight.
* **Pre-processing Controls**: Adjust Brightness and Contrast before color quantization to prevent shadows and highlights from merging into unreadable dark blobs.
* **Advanced Dithering Modes**: Choose between Nearest Color (Off), Atkinson Dithering, and a 50:50 Checkerboard mix to create natural, vibrant gradients.

## How to Use
1. **Upload Image**: Select your full-color source image.
2. **Reference Palette**: Choose which lighting condition you want to prioritize for color accuracy.
3. **Dithering**: Select your preferred dithering method.
4. **Adjust**: Tweak Brightness and Contrast until the live previews look exactly right.
5. **Export**: Right-click the **Export (Standard)** canvas and save the generated image for your Pebble SDK project.
