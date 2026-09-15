# Localized animation from preserved artwork

Use for restrained idle and suitable gestures or repairs where much of an approved sprite should remain still. Broad actions may need substantial pose changes; do not force a walk or attack into a tiny edit mask. This reference defines a workflow, not an already implemented masking helper or a completed animation. Follow active generation/editing tool requirements and inspect available compositing utilities before claiming a capability has been executed.

## Plan before drawing

An instruction such as "Liliana only breathes and blinks" is sufficient user input. Codex converts it into a compact production plan without asking the user to design masks or every frame. Record:

- The exact approved master sprite/revision, common canvas, scale and anchor. Preserve an unchanged source copy and its hash. Using a base only as a generation reference does not enforce preservation.
- The full action arc: rest, restrained movement, settle and loop return; the intended timing and source drawing used by each of the 16 delivered frame slots. Follow the animation contract for the single blink and settled work/greeting frame-8 hold. Deliberate reuse is allowed; there is no requirement for 16 distinct drawings.
- The moving regions and stable landmarks. For an idle, normally keep stance, feet, equipment and most face/hair pixels fixed; limit breathing to the relevant ribcage/blouse region. Any shoulder/head movement must be intentional, not an accidental consequence of the word "breathing."
- One primary action and only justified secondary motion. Clothing-aware bust response stays local and preserves volume/fastenings. Smooth, restrained movement takes priority over making every part visibly move; walking still requires real steps and attacks require readable action.

For more complex motion, establish and review the important contact, passing or action poses before filling transitions. The Godot mannequin may supply movement guides without requiring a generated parts kit. Compare transitions against both neighbors where available and the fixed appearance master; chaining only from the previous generated frame can accumulate drift.

## Enforce protected pixels

1. Define the allowed edit mask before generation, in the master canvas coordinates. For a blink, include eyelids and only the necessary neighboring eye area. Include any intended blended boundary in the allowed mask. Do not enlarge it afterward merely to excuse unrelated changes.
2. Request the localized artwork edit with the approved appearance as reference. Where a controlled local deformation of existing artwork is suitable, it can preserve painted shading without a fresh drawing; inspect the deformation for stretched linework, seams and unwanted changes to rigid details.
3. Assemble the final RGBA frame from the preserved master plus the edited patch, applying the patch only through the allowed mask. Do not deliver a full generated frame just because its prompt requested preservation. Keep final dimensions and alignment fixed; do not independently auto-fit poses. Pure patch placement must not change unrelated pixels.
4. Compare final RGBA pixels against the master outside the complete allowed-mask support, including its feathered edge. The changed-pixel count must be zero there before claiming exact preservation. Save masks and comparison evidence with the production run. Do not use RGB averages, silhouette bounds or image hashes alone to certify localized preservation.
5. Inspect the edited region and its boundary on light, gray and dark backgrounds and in playback. Exact protection outside the mask does not prove the eyelids, skin shading or motion inside it are correct. Maintain the rendering contract's practical tolerance there: minor harmless variation is acceptable; visible complexion changes or distracting flicker are not.

Use a stable master for protected areas, with previously accepted patches reused where appropriate. When several patches overlap, plan their composition order and compare against the expected composite rather than silently undoing a prior edit. For a moving silhouette, the allowed region must cover the old and new positions and any revealed background/surface. Prepare newly exposed artwork once and reuse it; never leave the old arm underneath its moved copy. Do not freeze a genuinely moving region merely to pass the comparison.

Verify at the common working resolution. If delivery requires downscaling, apply the same uniform transform to the baseline and all frames, account for the resampling filter's reach in the mapped mask, and check the delivered PNGs too. Do not claim export-level equality from a pre-export check alone. Keep lossless PNG playback as the artwork reference when a GIF conversion changes color or transparency.

## Reduce work without lowering the result

- Generate only the needed new drawing states. A blink may reuse a few eye patches, including open eyes from the master; planned holds reuse a finished drawing rather than regenerating it. Record reuse honestly.
- Validate basic motion and stable regions before secondary details and packaging. Add local breathing/cloth response progressively; do not regenerate the whole body to add a small effect.
- Repair the affected patch or frame and inspect adjoining transitions. Do not regenerate an accepted group for one localized failure. If the same approach keeps failing, diagnose mask, geometry, appearance or motion planning before another equivalent retry; do not spend repeated calls polishing the wrong action.
- Reuse compatible extraction, timing, slider-preview and export tools. Preserve alpha from an already transparent master; avoid repeated whole-character chroma removal or independent normalization. Do not redesign a preview application for every character.
- Run targeted checks after local changes and retain a final complete playback, loop/hold, shading, scale, edge and protected-pixel review. Re-run broader checks when later edits invalidate them, not simply because another file was packaged. File counts and unique-image counts cannot replace visual review.
- Record generation/edit call counts, retries and elapsed time for generation waits, processing and review where measurable. Distinguish one-time tooling setup from per-animation cost. Do not infer a historical timing breakdown from file timestamps or promise a fixed faster turnaround before measuring the pilot.

## Review and scope

Codex prepares the plan, artwork, masks/composition, timing and review output. The user reviews and can optionally paint corrections; no drawing assignment is implied. Deliver the source/patches, masked-assembly evidence, source-to-frame mapping, durations and an actual PNG-frame preview. Clearly state which checks ran and what remains unverified.

The agreed next experiment is one restrained Liliana idle using these controls, when the user asks to start it. Do not begin walking, replace existing approved clips, integrate assets into the game, or run image generation merely because this reference was updated. Carry the user's latest choices forward without making them repeat the conversation.
