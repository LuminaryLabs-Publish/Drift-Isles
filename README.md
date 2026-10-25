# Drift Isles

A standalone rolling platformer authored with NexusEngine Studio. Roll across five islands, jump between stones, ride a shuttle and an elevator, collect twenty gold energy shards, then reach the cyan finish marker. Checkpoints preserve your progress after a fall.

## Play

Play at **https://luminarylabs-publish.github.io/Drift-Isles/**. Website mirrors: **https://luminarylabs.dev/games/drift-isles/** and the existing **https://luminarylabs.dev/drift-isles/**. You can also open `builds/web/index.html` in a WebGL-capable desktop browser. The game is bundled and works offline. Alternatively serve `builds/web/` with any static server. No account or private repository access is needed to play this checked-in build.

**WASD / arrows:** move · **Space:** jump · **R:** restart · **Escape:** pause. On-screen movement and jump controls appear for coarse pointers. Sound starts off; enable it with the Sound button. Effects respect reduced motion and can be changed during play.

## Edit in NexusEngine Studio

Use **[Studio 0.7.0 or compatible later](https://luminarylabs.dev/nexus-engine-studio/)**, choose **Open**, and select `project/drift-isles.nexus.json`. Scene objects, meshes, materials and behavior settings remain editable. New Studio projects still start empty. The original Studio 0.6 project is retained in `project/archive/`; the current project uses the upgraded Engine registry and should be opened in Studio 0.7 or compatible later.

The project uses `nexusengine.studio-project/2` and source-format compatibility marker `081fea1cdd9ca1662bc15116e7174d9c27821630`; the executing Engine revision is `e3b9b589c9eaad144ef815ec9fa5ab20f0806424`. Browser and native Studio use the same file. Play is isolated from the authoring documents; Save stores edits, and Export creates a new standalone game.

Moving platforms use a travel offset, one-way time and endpoint pause in their behavior card. They must be root scene objects with solid colliders. Cyan editor paths show their travel. Checkpoints and finish markers are explicit saved behaviors. Jump speed and rolling settings are in Game Settings.

## Rebuild

Node 22+, Git and access to the pinned NexusEngine dependency are required. Run `npm ci` then `npm run build`. Studio is not needed to build or play this game.

The build loads the portable project through Engine's `SceneProject` API, validates it, bundles the Engine-owned configured scene browser host, and generates standalone HTML through Engine's export API. It records the exact Engine revision, source/runtime/output hashes and the module graph. Build guards reject Studio/editor implementations and Build/Agent execution tooling. Registry manifests are portable discovery data and remain available.

NexusEngine's optional `configured-scene-runtime-kit` owns platform movement/carry, jump buffering, checkpoint recovery, scoring, finish conditions, pause/reset/snapshots and browser host adapters. Existing Core Domains retain locomotion, contact, player authority, composition and authoring. Three.js supplies rendering through the Engine Kit's optional browser adapter. The game repo owns the islands, objects, materials and settings. No server-side Studio or Engine service is required to play.

## Repository

- `project/`: editable game source and embedded assets.
- `assets/`: original asset guidance and future imported originals.
- `scripts/`: standalone build adapter for pinned NexusEngine APIs.
- `builds/web/`: independent playable browser release and provenance.
- `validation/`: observed checks, screenshots and limitations.

The build writes the reviewed static allowlist to `builds/web/` and the repository root, including `.nojekyll` for direct static Pages delivery. Public game Pages serves `main` from `/`. The same files are copied to `Website/main/games/drift-isles/` and the existing `Website/main/drift-isles/`. Website Pages serves `main` from the repository root using its existing legacy deployment; there is no separate build branch or custom Actions workflow. Native **Studio** can edit and test this project; a native **game executable** is a separate delivery target.

## Performance audit status

Version 0.2.1 changes static publication and provenance only. The Engine pin and gameplay runtime are unchanged. The audit has identified growing per-frame receipt state, slow-frame time loss and failed-tick recovery defects; rebuilding does not claim to fix them. Reusable repairs belong in NexusEngine.
