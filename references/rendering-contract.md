# IMC contours, backgrounds and compositing

User direction clarified on 2026-09-14 after reviewing Elsie against white, in the small animation preview and inside the Adventurer Office. These are production and review requirements; they do not authorize editing approved artwork during discussion or skill maintenance.

## Reference roles

- [Unicorn Overlord character](media/uo-character-contours.png), copied unchanged from `D:/Download/unicorn overlord chara.png`: continuous contours, selective line weight, readable material shapes and controlled detail. This is not a new IMC body-proportion, identity, outfit or camera reference.
- [PawPop 2](media/pawpop-2-background-style.png), copied unchanged from `C:/Users/Tristixa-/Downloads/PawPop 2.png`: the user's selected background rendering direction after comparing sprites on three environments. Study the background's linework, material simplification, controlled shading, depth and character staging. Its two pasted sprites illustrate compositing; they do not establish new character identities, proportions or baked background content. The shrine setting, cherry blossoms, night lighting and exact camera are scene-specific examples.
- [Unicorn Overlord battle scene](media/uo-battle-composition.jpg), copied unchanged from `D:/Download/UO_09_6_Beginning-of-Battle.jpg`: supporting reference for character separation, depth and grounding. PawPop 2 supersedes its painterly surface treatment as the background rendering target. Its battle-camera scale does not replace IMC's gameplay camera requirements.

The user's existing gameplay proportion reference in the IMC project remains authoritative. Do not replace it with these references merely because they illustrate cleaner rendering.

## Clean contours and restrained outline weight

Both portraits and gameplay sprites need clean, continuous, intentional contours. Increase outline weight a little relative to the earlier thin Elsie treatment, especially where the outer silhouette needs support. Judge the increase at the actual portrait/gameplay display size; do not prescribe the same pixel width for different resolutions or thicken every facial and costume line equally. Keep fine interior lines and controlled variation between lit and shadowed edges. Avoid a heavy cartoon border or a uniform black sticker outline.

Reject broken or doubled contours, scratchy perimeter marks, isolated dark speckles, bright/dark/chroma fringes, and pixel stair-stepping inconsistent with the illustrated style. Hair locks, cuffs, fingers and boots must remain deliberate shapes through extraction and downscaling. Preserve intentional thin strands and antialiased edges; aggressive alpha thresholds or eroding the silhouette are not acceptable shortcuts. Clean linework also includes readable interior seams and folds rather than clusters of noisy tiny strokes.

Review the native export, its intended display size and an enlarged inspection view. Check on light, mid-gray and dark grounds, then in the intended room with its UI. A tiny GIF preview can hide defects, while magnifying a raster can reveal normal pixels; neither alone proves production quality. Animation contours must remain stable across all frames without thickness flicker, crawling edge noise or changing costume boundaries.

## Frame-to-frame color and lighting consistency

Use a practical visual tolerance for animation. The user accepts slight shading variation, with the accepted Elsie animation as an example of acceptable variation, not a requirement to copy her palette onto other characters. Small highlight or shadow differences that do not distract at the intended playback speed and gameplay size are acceptable. Do not repeatedly regenerate a good animation to chase identical pixels. Obvious changes in skin complexion, sudden material-color jumps, or distracting exposure/color-temperature flicker require correction.

Keep one approved appearance reference as the color and lighting anchor for every generation group or frame edit, alongside the relevant pose reference. Preserve the character's underlying skin tone and the recognizable colors of hair, clothing and metal. Maintain a coherent light direction, softness, intensity, shadow tint, exposure and color temperature across the clip unless the action explicitly includes a lighting change. Shading can move naturally as the body turns or clothing folds; consistency does not mean freezing highlights to screen coordinates. A named setup such as three-point lighting alone does not establish continuity.

Review materials separately in playback and adjacent frames, including the last-to-first transition. Prioritize the face and other exposed skin, then hair and large clothing areas. Compare similar visible regions under comparable orientation, allowing natural pose-dependent shadows; do not demand equal RGB values from differently lit surfaces. Use enlarged views to diagnose a visible problem, not to reject harmless differences only noticeable under magnification. Whole-frame or broad upper-body color averages cannot certify complexion consistency: different materials and changing visible areas can cancel each other out.

For an authorized shading repair, protect the accepted poses, proportions, contours, blink, secondary motion, timing and transparency. Target the affected material where possible. Do not compensate for an overly red coat by applying a blanket grade that makes skin pale, greenish or otherwise changes the complexion. A broader correction is acceptable only if separate material review confirms it improves continuity without introducing visible color changes elsewhere. Unchanged alpha proves silhouette preservation, not unchanged interior artwork or consistent skin tone; inspect those separately. Save a recoverable revision and verify the exported playback before claiming the repair succeeded. This guidance does not authorize regenerating already accepted assets during skill maintenance.

## Background direction: PawPop 2

Use crisp Japanese 2D-HD/chibi JRPG environment rendering designed to support detailed cel-shaded sprites. This user-selected direction replaces the earlier broadly painterly background target. High resolution is welcome; "2D-HD" does not request pixel art, photorealistic materials or a glossy 3D render. Inspect the retained PawPop 2 image when briefing or reviewing a background, rather than relying on the style label alone.

### What to carry into IMC

- **Contours and depth:** The foreground gate, lanterns, railings, paving and rocks have deliberate anime contours and readable silhouettes. Use clean, controlled line weight and clear form boundaries on nearby objects. Reduce edge contrast and tiny detail with distance; reserve atmospheric softness for distant scenery. Keep the character's ground plane crisp.
- **Materials and shading:** Stone reads through large tile outlines, beveled planes and a few broad color variations; wood through structure and sparse grain; rock through grouped angular planes. Use controlled cel-shading with selective soft light transitions. Minimal painterly texture means limiting surface noise, not eliminating volume or material distinction. Avoid blanket scratches, grain, tiny cracks, speckles and physically detailed surface rendering.
- **Foliage:** Build leaves and flowers into graphic clusters with a readable outer silhouette and grouped light/shadow colors. A few distinct leaves or petals can accent the cluster; every leaf need not compete for attention. The reference's pink blossoms are optional subject matter, not IMC's default vegetation.
- **Composition:** The open, medium-detail paving gives the characters a clear shared ground plane. Larger framing objects and richer prop clusters sit around this space, while landmarks remain legible farther back. Provide usable paths and natural actor staging without filling every area with decoration. A quiet area can still contain purposeful floor joints, furnishing or broad wall shapes.
- **Color and light:** PawPop 2 groups cool environmental colors and warm lantern light into coherent areas. Carry forward that organization, with palette and light sources chosen for the actual room, region and time of day. Saturated color is allowed when grouped deliberately. Avoid scattered glints and lighting effects behind faces; do not copy blue night lighting into every interior.

Choose silhouette separation using the whole cast's hair, clothes and expected movement. Keep useful environmental detail and a sense of place; do not solve readability by placing a blank dark rectangle or character-shaped halo behind every Officer. Preserve credible lighting rather than making all characters uniformly brighter than their surroundings. The reference's shadow also helps grounding, so do not attribute the entire improvement to background style alone.

### Original layouts and integration

For new or redesigned rooms, create a composition around the department's work, furnishing, circulation and atmosphere. The user prefers original designs over repainting the current Adventurer Office. Use existing floor plans and game data to understand connections and functional needs; do not attach the current room texture as a layout lock unless the task asks to retain it. Rendering style does not prescribe shrine architecture, a side-on battle camera or one universal room arrangement.

Distinguish an exact replacement from a redesign. An exact replacement must fit existing camera, staging and occlusion coordinates. A redesign may change those coordinates while retaining the location's gameplay purpose; record the needed walkable-area, entrance, interaction, sprite-position and foreground-occlusion adjustments for later integration. A candidate request alone does not authorize those code changes. Keep UI overlay space and intended aspect ratio in the brief, and assess the scene with representative approved sprites at actual gameplay size. Existing sprites retain their approved appearance during background review.

Use separate runtime contact shadows beneath characters, anchored to the feet/ground point and rendered under the sprite. A soft, flattened ellipse with tunable width, opacity and edge softness can supply the grounding visible in PawPop 2 without regenerating sprite frames. Keep it stable during idle, adapt it only when motion or elevation warrants, and respect furniture occlusion. Shadows cast by static scenery can remain in the background; do not bake detached character shadows or people into an empty environment. Review light direction, floor contact and desk occlusion together with the background.

### User-supplied prompt anchor

Preserve this as the baseline visual approach, then add the actual location, composition, camera, palette, lighting and runtime requirements:

> Crisp 2D-HD / chibi JRPG environment art designed to support detailed cel-shaded character sprites. Clean anime linework on foreground objects, simplified material rendering, controlled cel-shading, medium-detail tiled surfaces, graphic foliage clusters, minimal painterly texture, sharp readable silhouettes, and restrained atmospheric softness only in distant layers.

Keep final empty backgrounds free of characters, character contact shadows, UI, unrequested text and pseudo-writing. Review the image for the described properties; repeating the prompt is not proof of a style match.

## Diagnose an integration mismatch before changing artwork

When an approved sprite looks rough only after integration, first compare the same frozen frame, scale, position and background with the current material and a plain alpha-rendering path. Inspect source alpha, color fringes, import filtering and downsampling; an already transparent export may still be receiving a legacy chroma-key shader. Its presence is a hypothesis to test, not proof of damage.

Then inspect the unchanged sprite on neutral grounds and in the room to distinguish an authored/extracted edge defect from background competition. Choose a rendering correction only when the comparison supports it. If the artifact is already present in the export, targeted contour/alpha cleanup requires an authorized asset revision. Consider local background refinement after these checks. Do not regenerate identity, change proportions, blanket-blur the room or permanently alter import settings merely because one preview looks off. Record what was actually verified; a frozen-frame comparison does not establish motion stability.
