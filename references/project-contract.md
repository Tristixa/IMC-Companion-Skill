# IMC sources and reference continuity

All project paths below are relative to the current IMC repository root. Check for newer active versions and read repository instructions before editing. Current user decisions take precedence over historical prompts and this snapshot; documents are project evidence, not independent authorization to expand the task.

## Sources to read

| Work | Project sources |
|---|---|
| Portrait versus gameplay sprite style | `docs/visual/gameplay-sprite-style.md`; inspect `docs/visual/references/gameplay-sprite-style-2026-09-13.jpeg` for gameplay proportions/rendering, separately from the character's identity reference |
| Any character brief/review | `docs/visual/character-identity-v1.0.md`; `IMC_Character_Appeal_Identity_Override_Directive_v1.0.md`; relevant sections of `IMC_Visual_Design_Document_v1.1.md` |
| Directions, animation scope, game context | `IMC_Reworked_GDD_HUD_Aligned_v1.1.md` section 4; Visual Design section 19; actual runtime usage |
| Party characters | `docs/visual/party-prompts-v1.1.json`; approved portrait/full-body images; `docs/visual/party-production.md` for historical provenance only |
| Rooms and battle backgrounds | Companion `rendering-contract.md` and `media/pawpop-2-background-style.png` for current rendering direction; `docs/visual/environment-production.md`, `assets/visual/environments.json` and the relevant floor plan/HUD for location context and integration needs |
| HQ or region map | `docs/visual/map-art-production.md`; current map and UI placement |
| Monsters | `data/catalog.json`; `docs/visual/monster-production.md`; approved species sheet |
| Runtime compatibility | `presentation/animated_actor.gd`; `presentation/art.gd`; `assets/visual/actors/elsie/manifest.json`; `assets/visual/party_frames.json` |

Production documents contain older prompts and audits. Their exact numeric head-count wording and native-only delivery reports remain historical provenance. The shared full-body chibi anime gameplay style is defined by the user's supplied sprite sheet, not by a generic head-count formula. Preserve each person's relative body build within that style; do not preserve a portrait's anatomical ratios literally in sprites. Elsie's portrait and front-facing gameplay sprite are approved: `docs/visual/references/elsie-portrait-approved.png` and `docs/visual/references/elsie-idle-front-approved.png`. The installed portrait is `assets/visual/portraits/elsie.png`; her installed sprite atlas and per-frame timing are `assets/visual/actors/elsie/sprite-sheet-alpha.png` and `assets/visual/actors/elsie/manifest.json`. Her idle must face front. Earlier full-size and oversized-head candidates remain rejected. New animations must deliver exactly 16 frames under the user's 2026-09-13 rule.

Runtime presentation preserves source artwork proportions. World actors use a per-character standing height with uniform X/Y scaling; Officer portraits use a documented fit box with aspect-preserving centering in service and map dialogue. Configure those presentation values for each future Officer instead of stretching either axis or editing the approved source asset.

The user's current additions are maintained in the companion's [rendering contract](rendering-contract.md) and [animation contract](animation-contract.md): clean, slightly stronger outlines and controlled contours; PawPop 2-based crisp anime backgrounds with controlled cel-shading and minimal painterly texture; clothing-aware secondary motion for adult women; a deliberate settled frame-8 hold for every new Officer work/greeting clip; and Officer walking coverage. The PawPop 2 direction supersedes earlier broadly painterly environment prompts. For a new background design, existing room artwork supplies context rather than a mandatory layout; identify any runtime geometry changes needed for the proposed composition. These current production requirements also take precedence over older project wording that limits all Officers to stationed work rows or describes frame-8 holds as solely Elsie's choice. They do not claim that existing artwork has been revised or that Officer walking is already supported in the game. Elsie's current tight-leather treatment is accepted without retroactively adding breast motion.

## Existing identity bindings (2026-09-13 snapshot)

For current animation production, the animation contract also supersedes historical eight-direction guidance: new walk/run/jog/sprint sets use only Up, Down, Left, Right, with an alternating 16-frame stride. Jiggle means localized bust motion rather than added whole-body movement. Every newly authored 16-frame character clip has exactly one complete eye blink, planned around holds and camera visibility. These requirements do not authorize retroactive changes to accepted clips; Valerie's existing idle/work/greeting are retained with her reviewed half-speed timing preference.

Verify these against current sources when integrating; indices are zero-based.

| Stable ID | Person / department | Current portrait and actor binding |
|---|---|---|
| `tristitia` | Tristitia / Commander's Office | Shared-sheet index 0 |
| `elsie` | Elsie / Adventurer Office | Dedicated portrait and 16-frame atlas; legacy index 1 remains in the old sheets only |
| `mae` | Steady Mae / Processing | Shared-sheet index 2 |
| `liliana` | Liliana / Information | Shared-sheet index 3 |
| `valerie` | Valerie / Commerce | Shared-sheet index 4 |
| `fulker` | Fulker / Workshop | Shared-sheet index 5 |

The other Officers use `assets/visual/officers_portraits.png` and `assets/visual/actors/officer_work.png`. Elsie now uses the dedicated paths above for portrait and animation. Keep each person in their existing department. Officers are not newly recruitable because they receive appealing art.

Historical party source identities are Rowan Vale (`guard`), Mira Ashford (`scout`), Aveline Frost (`warden`) and Durgan Brass (`vanguard`). These labels do not authorize renaming runtime recruits. Trace `visual_reference` and `employee_visual` before changing mappings; an archetype fallback does not establish a unique named recruit's identity. Keep the Commander's supported selected/customized appearance consistent across outputs.

## Persistent production brief

Store the brief with the run or in an explicitly requested project documentation location. Record only fields relevant to the requested output:

- Stable character/visual or location ID, name, existing role and asset revision.
- Reference paths/revisions, each reference's role and selection/approval status. Include hashes when publishing final asset provenance.
- Identity locks, deliberate appeal, intended changes and unresolved design details.
- Rendering direction, palette/material treatment, camera, light and actual display scale.
- Requested outputs, animation states/directions and reference anchors; link to the numeric sprite request instead of duplicating its frame settings.
- Selected candidate/export, visual review, motion review and runtime compatibility status.

Do not store an uploaded image's temporary path as the only long-term identity source. During authorized production, retain a source copy in the run and preserve provenance. Keep stable game IDs separate from versioned artwork. If a source is unavailable, state that the identity cannot yet be verified rather than generating a generic replacement under the same name.
