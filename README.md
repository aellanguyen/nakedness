# NAKEDNESS

An interactive artwork about exposure, vulnerability, and the limits of looking.

Live website: https://nakedness-unveiling.risengrebe2.chatgpt.site/

## Run locally

No build step or package installation is required. From this repository:

```sh
python3 -m http.server 8000 --directory dist
```

Open http://localhost:8000. Use HTTPS or localhost for webcam access.

## Interaction

Choose **Enter with your hand**, then **Enable camera**. Move the ring near a petal until it lights up, pinch your thumb and index finger, hold the pinch, and move your hand outward. Open your fingers before selecting another petal.

Mouse/touch dragging and keyboard Enter/Space are available as alternatives. Sound is optional. Reduced motion follows your device preference.

## Implementation

- Procedural SVG flower with eight independently removable petals and a curled sleeping silhouette.
- MediaPipe Hand Landmarker 0.10.21, normalized pinch recognition, pointer smoothing, expanded petal targets, and short tracking-loss grace.
- Timed reveal, crossing into darkness, closing question, and restart.
- Synthesized Web Audio ambience; no recorded sound assets.

Camera frames are processed locally, without recording or uploading. Fonts and MediaPipe are loaded from public CDNs and require internet access. Physical webcam behavior still needs testing across devices. This version uses SVG artwork rather than custom Blender models or WebGL.
