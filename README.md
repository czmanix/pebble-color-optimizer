# Pebble Photo Optimizer

## Overview
[cite_start]Pebble Photo Optimizer is a web-based tool designed to help developers and designers convert full-color images into optimized 64-color assets for Pebble Time smartwatches[cite: 4, 34]. 

**Try it live:** [https://czmanix.github.io/pebble-color-optimizer/](https://czmanix.github.io/pebble-color-optimizer/)

[cite_start]Developing for Pebble's e-paper display can be challenging[cite: 4]. [cite_start]What looks great on a bright computer monitor often loses contrast on the actual watch under different real-world lighting conditions[cite: 4]. [cite_start]Standard conversion tools mathematically map colors to the standard palette, but the physical display often washes out details[cite: 31].

[cite_start]This tool solves this by using hardware simulation palettes[cite: 5]. [cite_start]It calculates the best color match based on how colors actually appear in real life, and reverse-maps them to generate the pure standard Pebble color code[cite: 38, 41].

## Features
* [cite_start]**Live Environment Previews**: See how your image will look across different lighting conditions side-by-side: Direct Sunlight, Standard Room lighting, and Backlight[cite: 8, 42].
* [cite_start]**Pre-processing Controls**: Adjust Brightness and Contrast before color quantization to prevent shadows and highlights from merging into unreadable dark blobs[cite: 35, 36].
* [cite_start]**Advanced Dithering Modes**: Choose between Nearest Color (Off), Atkinson Dithering, and a 50:50 Checkerboard mix to create natural, vibrant gradients[cite: 117, 146].

## How to Use
1. [cite_start]**Upload Image**: Select your full-color source image[cite: 34].
2. [cite_start]**Reference Palette**: Choose which lighting condition you want to prioritize for color accuracy[cite: 52].
3. [cite_start]**Dithering**: Select your preferred dithering method[cite: 116].
4. [cite_start]**Adjust**: Tweak Brightness and Contrast until the live previews look exactly right[cite: 35].
5. [cite_start]**Export**: Right-click the **Export (Standard)** canvas and save the generated image for your Pebble SDK project[cite: 43].
