# IMC character contours, color continuity and compositing

User direction clarified on 2026-09-14 after reviewing Elsie against white, in the small animation preview and inside the Adventurer Office. These are production and review requirements; they do not authorize editing approved artwork during discussion or skill maintenance.

## Reference roles

- [Unicorn Overlord character](media/uo-character-contours.png), copied unchanged from `D:/Download/unicorn overlord chara.png`: continuous contours, selective line weight, readable material shapes and controlled detail. This is not a new IMC body-proportion, identity, outfit or camera reference.

Environment design and its PawPop 2 references live in the separate `imc-environment-art-direction` skill. Use an approved room as compositing context during character QA; redesigning that room is a separate deliverable.

The user's existing gameplay proportion reference in the IMC project remains authoritative. Do not replace it with these references merely because they illustrate cleaner rendering.

## Clean contours and restrained outline weight

Both portraits and gameplay sprites need clean, continuous, intentional contours. Increase outline weight a little relative to the earlier thin Elsie treatment, especially where the outer silhouette needs support. Judge the increase at the actual portrait/gameplay display size; do not prescribe the same pixel width for different resolutions or thicken every facial and costume line equally. Keep fine interior lines and controlled variation between lit and shadowed edges. Avoid a heavy cartoon border or a uniform black sticker outline.

Reject broken or doubled contours, scratchy perimeter marks, isolated dark speckles, bright/dark/chroma fringes, and pixel stair-stepping inconsistent with the illustrated style. Hair locks, cuffs, fingers and boots must remain deliberate shapes through extraction and downscaling. Preserve intentional thin strands and antialiased edges; aggressive alpha thresholds or eroding the silhouette are not acceptable shortcuts. Clean linework also includes readable interior seams and folds rather than clusters of noisy tiny strokes.

Review the native export, its intended display size and an enlarged inspection view. Check on light, mid-gray and dark grounds, then in the intended room with its UI. A tiny GIF preview can hide defects, while magnifying a raster can reveal normal pixels; neither alone proves production quality. Animation contours must remain stable across all frames without thickness flicker, crawling edge noise or changing costume boundaries.

## Frame-to-frame color and lighting consistency

For stationary regions in a localized animation, preserve the approved source pixels through [masked assembly and verification](localized-animation-workflow.md#enforce-protected-pixels). A prompt to keep lighting unchanged is not enforcement. Reusing the actual artwork prevents unnecessary changes in its shading and proportions. Exact protected-region equality is a compositing invariant; the practical tolerance below applies inside legitimately edited or moving regions, not to accidental repainting outside the planned mask.

Use a practical visual tolerance for animation. The user accepts slight shading variation, with the accepted Elsie animation as an example of acceptable variation, not a requirement to copy her palette onto other characters. Small highlight or shadow differences that do not distract at the intended playback speed and gameplay size are acceptable. Do not repeatedly regenerate a good animation to chase identical pixels. Obvious changes in skin complexion, sudden material-color jumps, or distracting exposure/color-temperature flicker require correction.

Keep one approved appearance reference as the color and lighting anchor for every generation group or frame edit, alongside the relevant pose reference. Preserve the character's underlying skin tone and the recognizable colors of hair, clothing and metal. Maintain a coherent light direction, softness, intensity, shadow tint, exposure and color temperature across the clip unless the action explicitly includes a lighting change. Shading can move naturally as the body turns or clothing folds; consistency does not mean freezing highlights to screen coordinates. A named setup such as three-point lighting alone does not establish continuity.

Review materials separately in playback and adjacent frames, including the last-to-first transition. Prioritize the face and other exposed skin, then hair and large clothing areas. Compare similar visible regions under comparable orientation, allowing natural pose-dependent shadows; do not demand equal RGB values from differently lit surfaces. Use enlarged views to diagnose a visible problem, not to reject harmless differences only noticeable under magnification. Whole-frame or broad upper-body color averages cannot certify complexion consistency: different materials and changing visible areas can cancel each other out.

For an authorized shading repair, protect the accepted poses, proportions, contours, blink, secondary motion, timing and transparency. Target the affected material where possible. Do not compensate for an overly red coat by applying a blanket grade that makes skin pale, greenish or otherwise changes the complexion. A broader correction is acceptable only if separate material review confirms it improves continuity without introducing visible color changes elsewhere. Unchanged alpha proves silhouette preservation, not unchanged interior artwork or consistent skin tone; inspect those separately. Save a recoverable revision and verify the exported playback before claiming the repair succeeded. This guidance does not authorize regenerating already accepted assets during skill maintenance.

## Diagnose an integration mismatch before changing artwork

When an approved sprite looks rough only after integration, first compare the same frozen frame, scale, position and background with the current material and a plain alpha-rendering path. Inspect source alpha, color fringes, import filtering and downsampling; an already transparent export may still be receiving a legacy chroma-key shader. Its presence is a hypothesis to test, not proof of damage.

Then inspect the unchanged sprite on neutral grounds and in the room to distinguish an authored/extracted edge defect from background competition. Choose a rendering correction only when the comparison supports it. If the artifact is already present in the export, targeted contour/alpha cleanup requires an authorized asset revision. Consider local background refinement after these checks. Do not regenerate identity, change proportions, blanket-blur the room or permanently alter import settings merely because one preview looks off. Record what was actually verified; a frozen-frame comparison does not establish motion stability.
