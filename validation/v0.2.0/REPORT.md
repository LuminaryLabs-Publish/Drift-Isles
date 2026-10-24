# Drift Isles 0.2 / Engine-owned static game

Engine pin: `e3b9b589c9eaad144ef815ec9fa5ab20f0806424`. Runtime: optional `configured-scene-runtime-kit`. Build and browser entry import only NexusEngine APIs; Studio is not a build or runtime dependency. Three.js remains the browser rendering provider through the Engine-owned optional adapter.

- Old 0.6 project migrates via Engine Project transactions, retaining fifty scene objects and all non-derived document contents/IDs. The original is archived; source format compatibility marker is distinct from the executing Engine revision.
- Full-course Engine runtime passes twenty pickups, platform/elevator carry and finish with no respawns. Checkpoint fall recovery retains score. Installed API identity/idempotency, snapshot replay/reset and invalid snapshot rejection pass (`engine-runtime.json`).
- Studio browser and actual packaged macOS arm64 host open the project through the Engine Kit, jump/collect/pause, edit platform properties, undo/redo, save via browser/native handlers and export offline games. Browser/native documents match. Native dialogs choose task-owned filesystem paths through main-process automation (`studio-hosts.json`).
- Engine-only `npm run build` passes twice with identical release hashes. `runtime-modules.json` verifies no Studio/editor implementation or Build/Agent execution modules. Registry manifest modules are portable discovery data, not compiler execution.
- Local static route, homepage link/preview, keyboard play, pause/restart, reduced motion and independent offline HTML pass (`local-web.json`). Model screenshot review is separate from independent human approval.
- Consumer dependency installation reports zero vulnerabilities. The Engine development dependency audit separately has pre-existing findings; those Build/MCP/development implementations are not bundled into this game.

Publication destination is `Website/main/drift-isles/`, served at `https://luminarylabs.dev/drift-isles/` through legacy Pages main/root. No build branch, custom Actions workflow or deployment YAML change is introduced. Public identity/hashes and production browser proof are recorded after deployment.

Limits: kinematic configured platforms/rolling rather than a general rigid-body solver; unsigned macOS arm64 native Studio checked, not Windows/Linux or physical mobile. A native game executable and perceptual audio review are not claimed. The game is playable without private access; rebuilding requires access to the pinned Engine package.
