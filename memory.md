# Project decisions

- This repo owns Drift Isles content, its standalone build, build adapter and evidence. NexusEngine owns the reusable configured-scene runtime/project/browser/export Kit. Private Studio owns editing panels and consumes those APIs. NexusEngine owns authoring documents, composition and locomotion/contact services.
- The editable source is `project/drift-isles.nexus.json`, not hand-edited generated HTML. Meshes/materials and all course behavior configuration are embedded Engine-managed documents. Scene groups do not count as additional objects.
- Fifty objects: five islands, five foundations, two fixed stepping stones, three moving platforms, four checkpoint markers, one finish marker, twenty energy pickups, eight beacons, player and camera.
- The current migrated project requires Studio 0.7.0 or compatible later and the recorded exact Engine revision. Studio 0.5 does not execute the new course controls.
- The committed standalone HTML plays offline without Studio. Rebuilding uses this repo's pinned NexusEngine dependency and esbuild, without Studio. Keep dependency licenses and provenance with the build; do not copy private Studio development source into this repo.
- Keep optional synthesized sound off until enabled; support reduced motion. New Studio projects remain empty. This is a deliberate game deliverable, not temporary validation data.

- Website deploys static `main` from its root. Publish the reviewed browser allowlist at this public repository root for `https://luminarylabs-publish.github.io/Drift-Isles/`, and mirror it into `Website/games/drift-isles/` plus the existing `Website/drift-isles/`; the homepage Play link points to the public Pages deployment. Preserve all deployment YAML.
- The 0.6 original is archived before registry migration. `projectCompatibilityCommit` records the source-format baseline; `engineCommit` records the actual executing Engine revision.

- 0.2.1 is a delivery-only rebuild. Engine gameplay/performance defects remain explicitly recorded; no runtime optimization is implied by the new publication routes.
