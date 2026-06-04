# Razorpay Sprint '26 — Landing Page Recreation

A 3D, scroll-driven landing page recreating the look and the signature motion of
[razorpay.com/sprint/26](https://razorpay.com/sprint/26) — *The Age of AI-Native Payments*.

> Motion / UI study for learning purposes. Not affiliated with Razorpay.

## The signature motion
- **Electric-blue (`#0039FF`) flooded WebGL stage** with blue fog for depth.
- **White-wireframe shoe models walking down a runway** — translucent white
  surface + wireframe overlay (the "blueprint" look).
- **Scroll = forward camera travel.** Each shoe runs a phase-offset step cycle,
  producing a walking wave down the line.
- **Lenis** smooth scrolling, mouse parallax, and scroll-reveal content
  sections (`01`–`06`) that take over once the hero journey ends.

## Tech
- [Three.js](https://threejs.org/) (WebGL) via a CDN import map
- [Lenis](https://github.com/darkroomengineering/lenis) smooth scroll (vendored locally as `lenis.min.js`)
- A GLTF shoe model from the Khronos sample assets (CDN), with a procedural
  wireframe fallback if the model can't be fetched
- Fonts: Geist, Inter, Instrument Serif

## Run
The page uses ES modules, so serve it over HTTP — do **not** open it via `file://`:

```bash
python -m http.server 8000 --directory .
# then open http://localhost:8000/
```

## Files
- `index.html` — everything: markup, styles, the Three.js scene, and scroll logic
- `lenis.min.js` — vendored smooth-scroll library
