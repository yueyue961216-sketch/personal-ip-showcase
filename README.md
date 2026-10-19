# 虎斑小福 — Personal IP Showcase

A responsive React + Vite + TypeScript showcase with Tailwind CSS and React Three Fiber.

## Run locally

```bash
npm install
npm run dev
```

Open the local URL printed by Vite.

## Production build

```bash
npm run build
npm run preview
```

## Included

- Responsive editorial-style landing page, character profile, palette, quote interaction and footer
- Color swatches copy HEX codes to clipboard
- Quote button selects a random line
- R3F / Three.js scene with orbit controls, lighting and a pedestal
- WebGL fallback and image preview
- `AnimationMixer` support for animation clips in a supplied GLB
- Reduced-motion preference and keyboard focus styles

## 3D model status — important

No 3D character model is fabricated or bundled. The provided character is a 2D image in `public/assets/tabby-catgirl.jpg`. The viewer uses this as an explicit fallback billboard until a real model is supplied.

To add a real model:
1. Put a rigged model at `public/models/tabby-fuku.glb`.
2. Ensure its animation clips are included in the file.
3. Set `use3DModel: true` in `src/data/character.ts` to enable GLB loading. If clip names differ, update clip matching in `src/components/Stage.tsx`.
4. The `modelPath` and all character copy, colors, quotes, animation labels and social links are centralized in `src/data/character.ts`.

The three view buttons currently communicate the selected reference view and label the expected inspection angle. For accurate orthographic front/side/back turnaround, add a model with a consistent origin and adjust camera orientation per selected view; the supplied 2D artwork does not contain real side/back views.

## Notes

- Google Fonts are loaded from Google Fonts; system fallbacks remain available offline.
- Update `hello@example.com` and the example social links before publishing.
