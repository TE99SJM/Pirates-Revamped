# CIDER specification — source inventory and bug triage

## Clarify
The goal is to consolidate the **best available inspectable source**, not falsely declare the newest mod stable. Source archives previously supplied in the Pirates! project are the inputs. Keep executable/game assets out of GitHub.

## Inscribe — acceptance checks
- One module directory per distinct mod, with original README, manifest, license, source and tests where provided.
- Record source archive names, hashes, omissions and confidence in docs/PROVENANCE.json.
- Explicitly mark standalone Graphics 2.0.3 source and Manager 4.3.3 source as unrecovered.
- No binary game distribution; preserve hook conflict safety and save compatibility.
- Record build/tests actually run and separate from live Windows gameplay.

## Divide — tickets
1. Source provenance and safe import.
2. Ship Traffic 0.3.6 runtime stabilization and spawn counters.
3. Ship Battle Allies 0.1.1 control and battle-exit crash (depends on 2 for combined support).
4. Port conquest / nation-selection crash and hook audit.
5. Port cargo / menu polish (coordinate with 4).
6. Crew Allocator Fire and ground movement (separate gameplay checks).
7. Manager multi-import/no-dialog, graphics and trade edge cases.

## Execute and Review
Work in focused commits on feature branches, one issue per PR. Review the full diff, run static/package tests and describe Windows test gaps. Never force-enable conflicts without proof.
