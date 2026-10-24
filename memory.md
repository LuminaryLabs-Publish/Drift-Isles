# Project decisions

- This repo owns Drift Isles content, its standalone build, build adapter and evidence. Private NexusEngine Studio owns the editor and reusable course controls. NexusEngine owns authoring documents, composition and locomotion/contact services.
- The editable source is `project/drift-isles.nexus.json`, not hand-edited generated HTML. Meshes/materials and all course behavior configuration are embedded Engine-managed documents. Scene groups do not count as additional objects.
- Fifty objects: five islands, five foundations, two fixed stepping stones, three moving platforms, four checkpoint markers, one finish marker, twenty energy pickups, eight beacons, player and camera.
- Requires Studio 0.6.0 or compatible later and the recorded exact Engine revision. Studio 0.5 does not execute the new course controls.
- The committed standalone HTML plays offline without Studio. Rebuilding requires the matching external Studio checkout. Keep dependency licenses and provenance with the build; do not copy private Studio development source into this repo.
- Keep optional synthesized sound off until enabled; support reduced motion. New Studio projects remain empty. This is a deliberate game deliverable, not temporary validation data.
