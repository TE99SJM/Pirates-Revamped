# Pirates! Revamped — Agent Instructions

Use CIDER: **Clarify → Inscribe → Divide → Execute → Review**.

1. Read README.md, docs/CIDER_SPEC.md, docs/SOURCE_GAPS.md, and relevant module README, TECHNICAL and TESTING documentation before editing.
2. Preserve source language (C/assembly/C#) and existing design. Never redistribute the game EXE, FPK assets or saves.
3. Inspect exact hook ownership, signatures, save format, module API and launch modes. Do not invent offsets/hashes or make incompatible hooks coexist by weakening manifests.
4. Specify observable acceptance checks and divide larger fixes into dependent tickets. Work in a dedicated PR per issue.
5. Keep software product names unchanged: update version numbers, README and changelog.
6. Routine loader dialogs should be removed in favor of centralized manager authorization and logs.
7. Report exactly which checks were run and whether Windows live-game testing was performed. Do not call a mod stable based on emulation alone.
