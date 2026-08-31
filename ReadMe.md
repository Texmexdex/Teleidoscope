# TeXmExDeX's Teleidoscope

A real-time, infinite recursive self-mosaic generator running entirely in client-side WebGL2. 

Point it at any image, and the engine deconstructs the macro picture into an endlessly nested grid where every constituent tile is a color-mapped, self-similar reflection of the entire whole.

## Features

* **Continuous Fragment-Space Recursion:** Bypasses CPU tree traversal limits by executing recursive sub-tiling directly on the GPU via WebGL2 fragment shaders.
* **Continuous Multi-Scale LOD Blending:** Evaluates adjacent octave scales simultaneously to cross-fade sub-tiles into view at sub-pixel thresholds, eliminating visual stepping, popping, and mipmap blur.
* **Dynamic High-Frequency Fidelity Injection:** Preserves fine source edges and details on coarse grids by carrying screen-space luminance ratios back into the nested color table.
* **Perceptual Luminance Calibration:** Automatically extracts channel-by-channel logarithmic gamma mappings to normalize mean tile brightness, preventing highlight blowouts and shadow crushing down deep recursion chains.
* **Infinite Octave-Band Anchor:** Re-anchors viewport coordinate origins during infinite zoom dives to prevent 32-bit floating-point precision jitter.
* **High-Resolution Vector Exporter:** Re-renders the scene at custom output dimensions (up to 16K) with true recursive depth rather than bitmap upscaling.
* **Zero Server Overhead:** 100% client-side execution. Supports drag-and-drop, clipboard pasting (`Ctrl+V`), and local file loading with zero data leaving the browser.

## Controls

* **Scroll / Pinch:** Continuous zoom in / out
* **Click & Drag:** Pan viewport
* **Double-Click:** Center and dive into targeted tile
* **Dive Button (`D` or `Space`):** Toggle autonomous infinite zoom loop
* **Fit (`F`):** Reset viewport to default frame
* **Hide Controls (`C`):** Collapse control sidebar

## Tech Stack

* **Rendering Engine:** WebGL2 (GLSL ES 3.00)
* **Frontend:** Vanilla HTML5 / CSS3 / JavaScript (Zero dependencies)
* **Fonts:** Archivo & IBM Plex Mono
