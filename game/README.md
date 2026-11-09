# Hollow Blocks

A short Minecraft-style survival game that runs in the browser, built for iPhone Safari first.
Survive three nights. Dig and build by day; at night tall, gaunt zombies with glowing eyes come for you,
and they move faster when you aren't looking at them.

Everything is in one file, `index.html`. It loads Three.js r128 from cdnjs and generates every
texture, model and sound at runtime, so there are no other assets.

## Play it on iPhone

1. Host `index.html` anywhere that serves HTTPS (GitHub Pages works: Settings → Pages → deploy from `main`, then open `/game/`).
2. Open the page in Safari.
3. Tap Share → **Add to Home Screen**. Launching from the icon gives a full-screen build with no address bar.
4. Rotate to landscape. Sound starts after the first tap.

## Controls

| Touch | Keyboard / mouse |
| --- | --- |
| Left side: drag to walk | WASD or arrows |
| Right side: drag to look | Mouse (click once to capture the pointer) |
| Tap: hit zombie or break block | Left click |
| Hold or Place button: place block | Right click |
| Jump button | Space |
| Hotbar: tap a slot | 1–4 |

## Resolution

"Native retina" renders at the device's full pixel ratio (up to 3x) with antialiasing and 64px block
textures. If a device can't hold about 40 fps, the game steps the render scale down a notch and steps
it back up when there is headroom. "Balanced" caps the scale at 1.5x for older phones.

## Local testing

Open `index.html` over any static server (`python3 -m http.server`), not from `file://`, so the
Three.js script and fonts can load.
