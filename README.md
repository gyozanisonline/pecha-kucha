# MRS — Mid-Semester Recap

Static presentation deck for the MRS (Mycelium Rosetta Stone) project — a Python simulation brain → OSC → TouchDesigner installation about primeval forests as superorganisms.

Built as a scroll-snap single-page site with a fullscreen mode, RTL Hebrew with an EN toggle, an interactive 3D point-cloud viewer (Three.js + GLTFLoader + MeshSurfaceSampler), embedded POPX simulation videos with hover-lightbox, and a closing system walkthrough.

## Run locally
```sh
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

## Keyboard
- `F` — toggle fullscreen
- `←` / `→` — navigate slides (RTL-aware)
- top-left button — switch HE ⇄ EN
- bottom-left button — fullscreen

## Structure
```
index.html              single-page deck (all CSS + JS inline)
prompts.js              Gemini visual-study captions
images/                 PDF-source images, portfolio frames, sketch
media/popx/             three POPX simulation MP4s + posters
media/closing/          system walkthrough MP4 + poster
models/                 GLB models loaded by the 3D viewer
```

## Notes for deployment
- One GLB asset (`Meshy_AI_ficus_0328003833_texture.glb`, 511 MB) was
  excluded from the repo because it exceeds GitHub's 100 MB file
  ceiling. The `Ficus` entry in the JS `MODELS` array was removed
  accordingly. To restore it, either compress with Draco/Meshopt or
  host externally and reference by URL.
- Total model payload is ~491 MB; consider lazy-loading or a CDN
  for production.

## Project
Yoel Zajdner — WIZO Haifa, Year 4 — May 2026.
