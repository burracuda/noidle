# NOIDLE // System Dashboard V1

A high fidelity, dual platform interactive dashboard prototype built for NoIdle. This application features a custom-built 3D geospatial engine, real-time audio visualization, and a proprietary dual-theme system ("Modern" vs. "Retro System 7").

---

##  Key Features

### 1. Custom Geospatial Engine (The Globe)
*   **Zero-Dependency 3D:** Built entirely in HTML5 Canvas without heavy libraries like Three.js.
*   **Z-Depth Layering:** Features a custom rendering pipeline that calculates horizon lines to prevent clipping artifacts.
*   **Interactive Interpolation:** Continents fade smoothly around the sphere's edge using a calculated alpha mask.

### 2. Audio Intelligence & Visualization
*   **Generative Oscilloscope:** Uses complex sine summation math to simulate an organic analog signal that reacts to playback state.
*   **Responsive Player Architecture:**
    *   **Desktop:** Integrated widgets.
    *   **Mobile:** Sticky footer player with expandable waveform and touch-friendly controls.

### 3. Dual-OS Theme Engine
*   **Hot Swappable UI:** The app runs on a Context Provider that instantly switches the entire UI.
*   **Modern Mode:** Clean typography (DM Mono), sharp vectors, and high-contrast bounding boxes.
*   **Retro Mode (System 7):** A pixel perfect emulation of 90s monochrome displays, utilizing CSS `image-rendering: pixelated`, SVG dither patterns, and CRT scanline overlays.

### 4. Responsive Layout Architecture
*   **Desktop:** Strict 3-column fixed "Bento" grid. No body scroll.
*   **Mobile:** Vertical scroll stack with sticky headers and native touch interactions.

---

##  Tech Stack

*   **Core:** React 18 (via CDN for rapid portability).
*   **Styling:** Tailwind CSS (Utility-first styling engine).
*   **Graphics:** HTML5 Canvas API (Globe & Audio).
*   **Architecture:** Single-File Component Structure (SFC).

**Why this architecture?**
The entire application is contained within a lightweight architecture that requires no build steps, node servers, or complex deployment pipelines. 
It can be hosted anywhere statically and loads instantly.

---

##  Project Structure

*   **Data Layer:** `projectsData` contains the JSON structure for artists, tracks, and locations.
*   **Theme Context:** Handles the state for Modern/Retro switching and global color variables.
*   **Components:**
    *   `<GeoGlobe />`: The physics and rendering logic for the map.
    *   `<AudioPlayerWidget />`: The oscilloscope and playback controls.
    *   `<AppContent />`: The layout logic handling Mobile vs. Desktop breakpoints.

---

##  Future Roadmap (Backend Integration)

This V1 release is a **Frontend Release Candidate**. The UI is ready to be hooked up to a live database.

---

**©M All Rights Reserved.
