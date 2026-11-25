# Copy/paste bug-fix prompts for coding agents

Every agent must read AGENTS.md, docs/CIDER_SPEC.md, the relevant module source, README, technical notes and tests. Follow CIDER. Preserve C/C#/assembly, don't rename software, don't invent hook addresses/hashes, and open a focused PR. Provide reproduction steps, observed acceptance checks, actual tests, and an explicit unverified Windows gameplay status.

## Agent 1 — Ship Traffic
Examine `mods/ship-traffic` 0.3.6. Reproduce spawn-rate anomalies and crashes after ship battles. Audit relocated 1,024-record ship array, the 100-model pool, save format 110 and `.traffic_savegame`, AI time skips, cooldowns, ownership and manager hooks. Add read-only counters for spawn/despawn/reject, reasons and nation, verifying the 50–800% controls affect actual spawns. Preserve Traffic API v1 and declared conflict with Ship Battle Allies until a combined byte-accurate hook audit proves safe. Add emulated bounds/counter tests and a repeatable Windows plan.

## Agent 2 — Allied ship battles
Examine `mods/ship-battle-allies` 0.1.1. Reproduce player flagship controls going unresponsive during a three-ship fight and game crashing on battle exit. Audit player-keyboard ownership, AI ally navigation, targeting, captain HUD, target pointer lifetime and post-battle world restoration. Preserve national flags and true non-player AI. Treat Traffic 0.3.6 as incompatible until integration is tested. Deliver isolated state-cleanup tests, real Windows battle checklist, PR.

## Agent 3 — Port conquest crash
Inspect `mods/port-management`, `mods/port-attack` and `mods/port-menu`. Reproduce crash on choosing replacement nationality after town conquest and on leaving defeated town. Map every overlapping menu/land-battle/victory hook before changes. Audit city ownership mutation, return addresses, stack/register restoration, camera and UI cleanup and campaign save. Keep packages standalone and refuse duplicate hook ownership. Test successful faction change plus return to sea on disposable campaign before claiming fixed.

## Agent 4 — Port cargo and menu
Coordinate with Agent 3. Remove Collect available production. Rename Manage stored cargo to Manage cargo. Implement correct deposit/retrieve from constructed buildings, with stock conservation and capacity tests. Fix attack option missing in eligible ports; place it immediately above Sail away in the combined menu. Preserve native service choices and avoid introducing a second owner for the same hook. Verify building availability, empty/full inventory, repeated transfers, and departure without crash.

## Agent 5 — Crew Allocator and movement
Examine `mods/crew-allocator` 0.3.3. Resolve greyed Fire action by reading `fire_diag`, comparing original and allocated roster, and preserving valid target/LOS rules. Separately fix open-terrain move+melee attack consuming two moves: should cost only one unless tree/terrain modifier requires the second. Keep ranged behavior unchanged. Add deterministic transition tests and a live-game checklist; do not force-enable Fire.

## Agent 6 — Launcher, graphics, trading and no-dialogs
Examine `mod-manager` 4.3.2 source; do not assume this equals the later reported 4.3.3 runtime. Add batch multi-ZIP/folder import and friendly one-click compile/launch flow. Remove routine loader dialogs after manager authorization; keep errors in logs, ensure clean exit codes. The standalone Graphics 2.0.3 source is unverified: audit manager graphics code before reusing it. Target centered 4:3 high-fidelity fullscreen appearance with black side bars, main-monitor detection and robust Alt-Tab. Investigate chieftain sugar trade accepting only two units per visit without guessing which mod caused it. Test 5-package import and targeted Windows scenarios and report gaps.
