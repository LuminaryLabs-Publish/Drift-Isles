# Drift Isles 0.1.0

Editable source: `project/drift-isles.nexus.json`. Delivery: `builds/web/index.html`. Studio 0.6.0 source: `1a3bf8a77afa312537c5ff1b5c48ff2ecf22db1f`. Engine: `081fea1cdd9ca1662bc15116e7174d9c27821630`.

- Authored from empty Studio through its object, transform, settings and behavior controls. Fifty organized objects; five islands; twenty energy pickups; shuttle, elevator and final moving crossing; four checkpoints; explicit finish.
- Engine validation passes; compact saved source reloads with content/ID parity. Previous Blue Island compatibility, invalid platform rejection and undo/redo pass (`contracts.json`, `compatibility.json`).
- Full course reached twenty pickups and finish through normal Engine input intents, actual authored triangle surface sampling and zero respawns (`route.json`). The elevator carries the player upward without movement input. This direct runtime route is separate from rendered host proof.
- Keyboard-driven browser and actual packaged macOS arm64 Studio open the project, jump, pause/resume, collect, Stop, inspect platform settings and save (`hosts.json`). Native filesystem save uses real IPC/handlers; automated dialogs select task-owned paths. Browser/native document contents agree.
- Falling after collecting restores the active checkpoint and retains four points (`recovery.json`).
- Standalone HTML runs from a local file offline, collects through keyboard input, pauses and restarts with score reset. No HTTP requests/page errors (`offline.json`).
- Two builds from the clean recorded Studio source produce identical project/runtime/output hashes (`build.json`, release manifest). The adapter rebuilds Studio before exporting to avoid stale runtime input. Dependency licenses accompany the browser release.
- Model screenshot review covers editor overview, native play and independent offline play. This is not independent human approval. A short Space press missed by native frame timing was corrected by queued key presses and rechecked in both hosts. Feedback controls no longer overlap Restart.

Platform limits: packaged native Studio tested on unsigned macOS arm64 only. No Windows/Linux or physical mobile acceptance, general dynamic rigid-body physics, native game executable or perceptual audio review is claimed. Platforms are root leaf meshes. Public HTML plays without private access; rebuilding requires the matching external Studio authoring tool.

No game hosting workflow is configured. Keep game hosting separate from this repository delivery. Temporary validation data is retained only as the reports/screenshots listed here; the editable game and build are deliberate deliverables.

The generated HTML retains upstream Three.js shader strings verbatim, including their whitespace. `.gitattributes` marks this generated output and scopes shader whitespace exclusions to that file; handwritten source keeps normal whitespace checks.
