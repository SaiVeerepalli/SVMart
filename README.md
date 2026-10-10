# SVMart — Living Village Web Game (Prototype v0.1)

Mobile-friendly 3D browser prototype for the SVMart mini-mart tycoon and living-village concept.

## Run / publish
- Upload the contents of this folder to a GitHub repository.
- In GitHub: Settings → Pages → Deploy from a branch → select `main` and `/ (root)`.
- Open the published URL on Android or desktop.
- For local testing, run `python -m http.server 8000` from this folder and open `http://localhost:8000`. Do not open the HTML directly as a `file://` URL.

## Prototype features
- Three.js 3D scene with selected Kenney GLB models for commercial/residential buildings, cars, delivery vehicles, and mini-market props.
- SVMart storefront, neighborhood, roads, lane markings, crosswalks, parking bays and parked/moving vehicles.
- NPC villagers with local state-machine routines: work, shop, go home, rest, meet friends and head to parking.
- Time/day progression, funds, happiness, simulated shopping income and community event feed.
- Controls to add a shop, vehicle, villager, parking bay, and change simulation speed.
- Village AI Advisor uses local rules and current game state. It is not a cloud LLM in this prototype.

## Important limits
- Three.js loads from jsDelivr, so the first launch requires internet. The game logic runs locally and does not require a game backend or paid server.
- Save/load persistence, full pathfinding, collision-aware traffic, parking allocation, detailed inventory/economy, character animation rigs, and real LLM conversations are future work.
- Do not put private API keys in a public frontend. For real LLM calls, use an optional secure proxy/backend or an on-device model.

## Asset licenses
Models included here are selected from the user's Kenney asset packs. The original `License.txt` files for each used pack are preserved in `licenses/`. Kenney asset packs are commonly distributed under CC0; confirm each included license before redistribution. Official information: https://kenney.nl/support. The four packs previously flagged for extra verification remain outside this prototype.

## Contents
- `index.html` — game UI, simulation and 3D renderer
- `assets/` — selected GLB models used by the prototype
- `licenses/` — original license text for source packs
- `ASSET_MANIFEST.json` — asset-to-source mapping
