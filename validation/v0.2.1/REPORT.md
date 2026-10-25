# Drift Isles 0.2.1 static delivery

Rebuilt directly on unchanged NexusEngine e3b9b58. Source 3e6a225; root publication d4c0998; Website publication e0e9f50. Primary public Pages serves the game from main/root. Website mirrors it under /games/drift-isles/ and preserves /drift-isles/. All three routes return the expected release metadata and file hashes. Homepage Play links to public Pages. Deployment YAML is unchanged.

Local audit used NexusAuditor 0.2.2 with actual native static servers, installed headless Chromium and the existing builds. Standalone collection/pause, Studio save/reopen/Play/Stop/source preservation and offline exported gameplay pass.

Performance remains FAIL: actual renderer-free simulation grows from 7.76ms median near step 100 to 68.69ms near step 600 while movement receipts grow from 100 to 600. Failed-tick recovery also remains unfixed. This release changes delivery/provenance, not gameplay or performance; HTML bytes match the prior release. Headless browser timing used software rendering and is not hardware performance proof.

Temporary test contexts, downloads and local servers were cleaned.
