# QWEN.md - Project Context File

## Project Overview
**Project Name:** poc_ar_page (Proof of Concept - Augmented Reality Page)  
**Type:** HTML-based Augmented Reality Web Application  
**Purpose:** A simple proof-of-concept demonstrating AR object placement in a web browser using Google's model-viewer library.

## Project Structure
```
poc_ar_page/
├── index.html          # Main HTML file containing the AR viewer
├── README.md          # Basic project documentation
├── QWEN.md            # Project context for AI agents
└── source/
    └── model.glb      # 3D model file in GLB format
```

## Technology Stack
- HTML5
- CSS3
- JavaScript (via Google's model-viewer library)
- WebGL (for 3D rendering)
- WebXR (for AR capabilities)
- 3D model: GLB format (with fallback to USDZ for iOS)

## Features
- AR object placement using `ar-placement="floor"`
- WebXR support for modern AR browsers
- Quick Look support for iOS devices
- Camera controls for manual 3D model viewing
- Responsive design (full viewport)

## Implementation Details
The project uses Google's `<model-viewer>` component to handle the complex AR rendering. Key features include:
- `ar` attribute enables AR functionality
- `ar-modes="webxr scene-viewer quick-look"` specifies supported AR platforms
- `camera-controls` allows manual manipulation of the 3D model
- Custom "Place Object in AR" button styled with CSS

## Building and Running
1. **Local Development:** Serve the `index.html` file via a local web server (due to WebXR API requiring HTTPS or localhost).
   - Using Python: `python -m http.server 8000`
   - Using Node: `npx http-server`
   - Using XAMPP (as currently configured): Place in htdocs and access via Apache
2. **No Build Required:** This is a pure HTML/CSS/JS implementation with no compilation needed.

## Development Conventions
- Single HTML file architecture
- External library loaded via CDN (Google's model-viewer)
- Responsive design using viewport units (vw/vh)
- Mobile-first approach for AR compatibility

## Dependencies
- Google's model-viewer library (loaded from unpkg CDN)
- GLB formatted 3D model file
- WebXR compatible browser (Chrome, Edge, Safari)

## Notes
- The project currently has minimal styling and functionality
- Only one 3D model (`model.glb`) is included in the source directory
- AR functionality may vary based on device and browser capabilities
- For iOS devices, an optional `model.usdz` file should be provided (currently only GLB exists)