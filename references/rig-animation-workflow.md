# Approved Godot motion reference

## Scope

Retain the approved mannequin as a motion and timing reference. The separately generated Valerie parts attempt failed handedness and whole-body proportion review; its production and assembly instructions are removed from the current workflow. Do not resume that experiment or assign drawing to the user. Default to [localized edits and reuse of intact approved artwork](localized-animation-workflow.md) where suitable, with important action poses established first for broader movement. A future explicit request for a cutout rig requires a fresh plan, not automatic reuse of the rejected parts.

## Locate the approved baseline

The user approved the right-facing placeholder walk on 2026-09-15, then confirmed that it was smooth like the supplied Unicorn Overlord gameplay reference. Find `tools/animation-lab/right-walk-v1/` in the active IMC checkout. Read its `README.md`, `approval.json`, and current sources. Use repository-relative discovery instead of assuming the saved project and a Codex worktree contain the same files. If absent, check available IMC checkouts before rebuilding or claiming the template is unavailable.

The lab contains a standalone `project.godot`, an editable `walk_rig.tscn` with AnimationPlayer tracks, `build_rig.gd`, frame export, native/browser previews, and verification tools. `approval.json` hashes the approved scene and sprite sheet. The `.gdignore` in its parent directory excludes the lab from the main game's Godot import scan; it does not exclude it from Git. Preserve source, instructions, approval evidence, and a useful review preview in version control. Godot's `.godot/` cache remains ignored. An untracked lab is not yet committed or pushed; report that distinction honestly.

## Use as a movement guide

Inspect or export the approved right-facing walk's contact, passing and support poses to guide character animation. Skip rebuilding and reapproving the same generic mannequin. Preserve the baseline; make a separate copy only when a requested motion study needs adaptation. This guide does not require cutting the approved character into parts.

The current builder and checker use fixed mannequin dimensions, joint paths, stride, and a 1.2-second example cycle. They are not a universal automatic retargeter. Transfer the gait's timing, support changes and joint relationships while retaining the approved character's own proportions, contact geometry and props. Never stretch artwork or separately resize body pieces to fit the mannequin. Fixed mannequin limb checks cannot certify a different character's anatomy. A held book or weapon may require different arm motion.

Baseline approval does not approve the adapted character, other directions, running or attacks. Keep Right > Left > Down > Up review order where the user has requested it. Account for asymmetric artwork rather than automatically mirroring. Review primary movement before adding justified secondary motion under the animation contract. The placeholder deferred clothing and bust motion and is not evidence those features are complete.

## Preserve the reference honestly

The mannequin's source animation lives in Godot's editable scene/tracks. Its browser preview must display the actual exported frames, not silently substitute a different JavaScript animation. Running `build_rig.gd` overwrites the generated scene, so preserve manual scene edits before rebuilding. Review the resulting character separately at target display size; a smooth mannequin alone does not validate the character's anatomy, shading, contacts or costume.

## Lessons from the video and approved prototype

Maintain controlled head/torso motion, clear alternating support, coherent knee/ankle articulation, stable painted materials, and separate secondary motion. Do not invent additional whole-body motion merely to make every part visibly change.

Distinguish authored poses, pose duration, rig keyframes, and display/capture frames. A 16-pose one-second animation on a 60-FPS display naturally shows each pose for roughly three or four display frames. That arithmetic is an example, not a measurement of Unicorn Overlord. The supplied screen recording includes variable capture timing and manual stepping; it does not establish an exact source pose count, deliberate hold schedule, or universal timing for every action in that game.

Repeated display frames and intentional timing holds are valid. The later clarification also permits deliberately repeated drawings within the 16 delivered slots when they express planned timing; do not invent differences to satisfy unique-image counts or replace missing action with filler. Record frame-to-drawing mapping and durations. The lab balances its two half-strides with durations around the frame-1/frame-8 anchors; its 1.2-second tempo is an approved starting point, not a compulsory tempo for all characters/actions. Do not impose work/greeting dwell timing on walking.

Review the rendered 16-frame export at normal speed as well as the continuous rig and frame slider. A smooth continuous rig can lose important motion when sampled. Continuously translating a held PNG pose can also show small contact stepping: dense rig contact checks cannot certify zero sliding in the exported version. Use both in-place and traveling previews. Preserve technical checks and explicit user approval as separate evidence.
