<div align="center">

# Polito 🎬

**Video editor.** I don't really write code — I vibe-code the tools my own editing work needs, and keep going until they exist.

[YouTube](https://www.youtube.com/@Politoo) · [X](https://twitter.com/thatkidpolito)

</div>

---

Nearly everything here started as one problem: getting real game footage, characters and maps into Unreal so they can actually be lit, framed and cut.

## Vesper — Call of Duty → Unreal Engine

A four-part pipeline that takes the games apart read-only and rebuilds them as editable Unreal content.

| Project | What it does |
| --- | --- |
| **Vesper** | Desktop exporter. 25 map-reader routes and 15 asset profiles across the series. External reads only — no hooks, no writes to the game. |
| **Vesper for Unreal** | Scene importer. Rebuilds `.vesper` packages: world geometry, static/dynamic instances, materials, terrain, splines, decals, lights and animated props. |
| **VesperCast** | CAST model, material and animation importer for UE 5.8, with 14 per-game shader profiles. |
| **VesperLiveLink** | Streams live in-game cameras plus animated hands, weapons, bodies and bots into UE 5.8, then records them as editable Sequencer takes — 9 game profiles. |

## Cinematic & demo tools (running in the game)

Built so demos and matches can be replayed, re-cameraed and captured properly.

| Project | Game | What it does |
| --- | --- | --- |
| **S2MP Mod Demo** | WWII | Demo playback with dolly camera paths, free cam, ProRes capture, CineBots and automatic match recording. |
| **t9-demo-client** | Black Ops Cold War | Local bot-match recording, native demo playback, cinematic cameras and Lua scripting. |
| **H1 CoD4 Demo** | Modern Warfare Remastered | H1-Mod client with a demo system, plus a CoD4 `.dm_1` → MWR `.dm_h1` converter. Model swapper, dolly paths, remastered replay of original COD4 recordings. |
| **H1 Demo System** | MWR | The demo subsystem itself: recording, playback, camera paths, frame capture and CoD4 conversion. |
| **ColdWar Demo Tool** | BO Cold War | Captures loaded Theater replays as native `.demo` files. |
| **CoD Demo Name Editor** | CoD4 / BO1 / MW2 / MW3 | Portable renaming of players inside recorded demos. |

## Unreal editor plugins (useful outside Call of Duty)

- **BetterNodes** — graph layout for Blueprints and Materials. Chain layout, Subway and Manhattan wiring, real reroute points, path tracing, flat node styling, one-undo.
- **BetterUI** — reversible flat editor theme. Graphite / Charcoal / Slate, accent colours, corner radius, spacing presets, export/import. Nothing on disk is overwritten.
- **MVM Camera** — places camera shots directly against Sequencer animation: scrub, fly, press **K**. Generates the smooth camera curves between shots. Built for my own P_CineCamera + AccumulationDOF setup.

## Other games' asset pipelines

- **OWM Importer** — native UE importer for Overtools/DataTool Overwatch assets: heroes, skins, cosmetics, maps, materials and animations, with no Blender or FBX step. Two builds: an accurate native one and a Public build with the full Asset Library UI.
- **SSO LiveLink** — asset browser and exporter for installed Star Stable Online archives: 79,821 indexed entries, static mesh/texture preview, OBJ/PNG and full environment exports.
- **Operator2MetaHuman** — turning a Call of Duty operator into a working MetaHuman with facial rig, game skin, equipment and helmet intact. In progress.

## COD4 era mods

Where all of this started — mods built purely to make COD4 footage look good.

- **IW3 Enhancer Mod** — model and asset replacement for COD4, works with old demos.
- **IW3 Textures Mod** — full wall/ground texture overhaul. Works with IW3xo and COD4x.
- **MWR to IW3** — swaps COD4 player and world weapon models for their MWR versions.
- **Polito Special Mod** — MWR models, viewhands and Promod POV weapons/animations.

## Deep research

- **Vestige** — converting MWII map assets and rebuilding fastfiles to run inside MWIII. Currently at a working geometry preview of a converted Strike world.
- **VesperWorldLink** — the reverse direction: sending Unreal-authored geometry into the game's native model system. Probe-only checkpoint.
- **OW1 Sandbox** — offline Overwatch 1.74 sandbox: metadata libraries, local launcher and map/bot/lobby research.

## Small fixes

- **SmartCastMerger** — repairs the material/texture bug that ModelMerger introduces when merging `.cast` models.
- **CAST Anim Layerer** — layers one `.cast` animation over another, bone by bone.
- **UECast BO7 Fix** — repairs Black Ops 7 materials after a UECast import, natively in C++.
- **Ghosts PC Safe Area Fix** — fixes the hard HUD edges Ghosts gets with a smaller safe area.
- **CoD Config Console** — desktop config editor for BO6/BO7/Warzone/MWIII/Vanguard/Cold War, plus Delta Force and Overwatch presets.

---

<sub>Most of these are works in progress. The READMEs are honest about what is finished, what is approximated and what is still unproven.</sub>
