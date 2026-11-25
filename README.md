# Pirates! Revamped

Community-authored mod manager and experimental mods for **Sid Meier's Pirates! (2004)**.
This source snapshot was assembled from the project's available archives on 2026-11-25. It is **not a validated release** and is not an importable set of compiled mods.

## Contents

| Path | Available source version | Status |
| --- | --- | --- |
| `mod-manager/` | 4.3.2 | Logging source; later reported 4.3.3 not recovered |
| `mods/ship-traffic/` | 0.3.6 | Experimental, crash investigations open |
| `mods/adaptive-sailing-speed/` | 0.2.1 | Experimental |
| `mods/ship-battle-allies/` | 0.1.1 | Experimental, known control/post-battle issues |
| `mods/crew-allocator/` | 0.3.3 | Experimental; Fire action issue |
| `mods/crew-happiness/` | 0.1.1 | Experimental |
| `mods/infinite-merchant-gold/` | 0.1.0 | Experimental |
| `mods/port-management/` | 0.1.0 | Experimental combined legacy implementation |
| `mods/port-attack/` | 0.2.1 | Experimental standalone implementation |
| `mods/port-menu/` | 2.1.0 | Experimental managed friendly-port menu alternative |
| `mods/graphics/` | 2.0.3 metadata/docs | Standalone binary's matching source not verified |

Graphics C# implementation also exists in `mod-manager/PiratesModModules/graphics/source/`. This is **not proven to match** the standalone Graphics 2.0.3 binary. No new gameplay features were invented while collecting source.

## Safety and compatibility

- **No commercial game executables or assets, injected DLLs, loaders, or Windows binaries are included.** Build from source on your own Windows development system.
- Back up saves, and test volatile modules with a **new disposable campaign**. Ship Traffic has its own relocated save layout and **must not** be assumed compatible with existing saves.
- Ship Traffic 0.3.6 deliberately declares a conflict with Ship Battle Allies 0.1.1; do not bypass it by editing a manifest.
- Port Management, Port Attack, and Port Menu can own similar hooks. Do not enable overlapping mods until an exact-hook audit confirms coexistence.
- This repository is for code review and collaboration, **not a declaration that every mod builds or works in the live game**.

## For contributors

Read `AGENTS.md`, `docs/CIDER_SPEC.md`, the relevant module's README and tests, and `docs/AGENT_PROMPTS.md`. Complete issues using focused PRs.

The original source ZIP names, SHA-256 checksums and omissions are in `docs/PROVENANCE.json`. Licenses remain with their respective modules. Source files retain their original language and structure.