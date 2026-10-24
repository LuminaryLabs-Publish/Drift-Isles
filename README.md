# Drift Isles

A standalone rolling platformer authored with NexusEngine Studio. Roll across five islands, jump between stones, ride a shuttle and an elevator, collect twenty gold energy shards, then reach the cyan finish marker. Checkpoints preserve your progress after a fall.

## Play

Open `builds/web/index.html` in a WebGL-capable desktop browser. The game is bundled and works offline. Alternatively serve `builds/web/` with any static server. No account or private repository access is needed to play this checked-in build.

**WASD / arrows:** move · **Space:** jump · **R:** restart · **Escape:** pause. On-screen movement and jump controls appear for coarse pointers. Sound starts off; enable it with the Sound button. Effects respect reduced motion and can be changed during play.

## Edit in NexusEngine Studio

Use **[Studio 0.6.0 or compatible later](https://luminarylabs.dev/nexus-engine-studio/)**, choose **Open**, and select `project/drift-isles.nexus.json`. Scene objects, meshes, materials and behavior settings remain editable. New Studio projects still start empty. Studio 0.5 does not support this course's moving platforms, checkpoints and jumping; opening it there does not establish correct gameplay.

The project uses `nexusengine.studio-project/2` and Engine revision `081fea1cdd9ca1662bc15116e7174d9c27821630`. Browser and native Studio use the same file. Play is isolated from the authoring documents; Save stores edits, and Export creates a new standalone game.

Moving platforms use a travel offset, one-way time and endpoint pause in their behavior card. They must be root scene objects with solid colliders. Cyan editor paths show their travel. Checkpoints and finish markers are explicit saved behaviors. Jump speed and rolling settings are in Game Settings.

## Rebuild

Node 22+, a local checkout of the matching private NexusEngine Studio revision, and its installed dependencies are required to rebuild through this authoring tool. In a clean, committed Studio checkout run `npm ci`; then in this repository run `npm run build`. The adapter builds Studio first so it cannot reuse a stale runtime. Set `NEXUS_STUDIO_PATH=/absolute/path/to/NexusEngine-Studio` if Studio is not a sibling checkout.

This public repo does not vendor private Studio development source. The reproducible build adapter reads the external Studio tool, validates this project, and uses the same export template as its Export button. It records the Studio revision, project hash, runtime hash and output hashes in `builds/web/release.json`. Retain the dependency licenses with the game.

## Repository

- `project/`: editable game source and embedded assets.
- `assets/`: original asset guidance and future imported originals.
- `scripts/`: build adapter for the external Studio tool.
- `builds/web/`: independent playable browser release and provenance.
- `validation/`: observed checks, screenshots and limitations.

No Pages workflow or hosting configuration is added by this project. Native **Studio** can edit and test this project; a native **game executable** is a separate delivery target.
