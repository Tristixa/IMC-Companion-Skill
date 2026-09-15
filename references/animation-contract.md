# IMC animation counts, timing and integration

Before new Officer animation production, use a user-approved gameplay sprite matching the project's `docs/visual/gameplay-sprite-style.md` and its user-selected reference image. Portrait approval or successful extraction does not approve sprite proportions. Follow the separate portrait, single-sprite and animation stages; the style-reference archer's combat actions do not add combat to an Officer's scope.

## Frame guidance

The user's current production rule (2026-09-13) is exactly **16 frames for every new IMC animation**. This supersedes earlier recommended ranges in Visual Design v1.1 section 19.3. It covers each required idle, work, interaction, movement, turn and combat clip; it does not require roles to acquire unrelated actions. A later explicit user request may override the count.

A generation candidate pool may contain extra poses; select and assemble exactly 16 delivered frames and record the source drawing for each frame. The user's later clarification permits deliberate reuse: 16 frame slots do not require 16 unique drawings. A planned held pose may occupy successive slots unchanged; record the mapping and durations rather than claiming each slot is a newly drawn pose. Do not add meaningless motion to satisfy uniqueness checks or use repetition to conceal missing contacts, transitions or required actions. Keep the delivered manifest authoritative. Other existing 6/8-frame sheets remain unchanged until their integration is requested; they are not a Godot limit. Retain existing installed timing until a revision is requested. For new Officer work/greeting clips, use the hold-pose rule below.

Frame count is pose sampling; FPS is playback speed. With uniform durations, seconds = frames / FPS. Sixteen frames at 16 FPS and eight frames at 8 FPS both last one second. When timing uses per-frame durations, the animation length is their sum. Preserve intentional anticipation, contact/impact and recovery timing; do not speed up an action merely to hide weak poses.

For localized artwork reuse, follow [localized-animation-workflow.md](localized-animation-workflow.md). To use the approved Godot mannequin as a motion reference, follow [rig-animation-workflow.md](rig-animation-workflow.md); its approval does not select the retired generated-parts workflow. Distinguish unique drawings, delivered frame slots, AnimationPlayer keys and repeated display/capture frames. Judge the actual 16-frame export and its durations separately from continuous rig playback; do not infer a game's source pose count from a screen recording's repeated frames. Unique-image counts are descriptive evidence, not a pass/fail requirement.

In sprite-gen, record counts, FPS, loop and action in the supported numeric request (`states.<state>`) and keep the request authoritative through extraction and composition. Record direction order, cell dimensions, padding, body scale and foot pivots using the pipeline's documented fields. Inspect the installed schema/help rather than inventing custom fields the pipeline will ignore. Additional IMC notes belong in the brief until an actual integration adapter supports them.

For example, a requested one-second, 16-frame attack can use `frames: 16`, `fps: 16`, `loop: false`, with anticipation, strike, follow-through and recovery described in `action`. This is an example, not the default duration for every attack.

## Shared character scale across clips

Use the approved gameplay base sprite as the size and proportion reference for every pose, animation, direction and separately generated batch of that character. Keep one common pixel scale, coordinate frame and grounded foot baseline through generation, extraction, assembly and runtime integration. A new work/greeting clip must not make the character grow relative to idle. Record the base reference, its displayed standing height and stable anatomical measurements in the production brief; reuse the same reference in every generation group.

Compare head size, shoulder/ribcage scale, torso length, hips, limb lengths and boot size where the pose and camera make those measurements comparable. Allow real articulation: nodding, leaning, crouching, raised hands, swinging cloth and foreshortening can change the occupied silhouette without changing the person's size. Do not force all poses to have identical bounding-box width/height or warp anatomy to achieve it. Small natural drawing variation is acceptable; an obvious growth/shrink jump or compressed/lengthened body between clips is not.

During extraction and fitting, verify the actual scale transform against that shared base. Do not independently auto-fit each pose, strip, quarter or state to fill its available cell; raised props and wider gestures must not rescale the whole character. Preserve common scale with padding and placement, and use a larger common canvas if needed. Equal cell dimensions, aligned feet, or matching each row's maximum height are not proof of consistency. If a size mismatch is already drawn into the source, flag the affected poses for an authorized correction rather than concealing it with per-state runtime zoom or normalizing every silhouette independently.

Review all clips together at one fixed display scale and pivot, alongside the approved base. Compare neutral/start/end poses directly; inspect both adjacent frames and generation-group boundaries. For stationed Officers, explicitly play idle-to-work, work-to-idle, idle-to-greeting and greeting-to-idle transitions, including the held idle/end pose against the next clip's first pose. Check both the exported atlas and the game: compare source landmarks, frame rectangles, standing-height metadata, scale and pivots before attributing a size jump to Godot import. Bounding-box measurements are supporting evidence, not a substitute for visual pose/anatomy review. Skill maintenance alone does not authorize changing existing approved artwork or runtime settings.

## Officer action coverage and frame-8 holds

The user's 2026-09-14 rule makes idle, work, greeting/interaction and walking required outputs for a newly requested complete Officer animation set. A currently stationed Officer still needs walking in the production brief. Use the four cardinal directions specified below, aligned with the intended camera; do not omit walking because the current runtime only stations Officers at desks. Officers do not acquire combat actions. A request for one sprite, a portrait or documentation remains limited to that request.

For every new Officer work and greeting clip, choreograph three phases within the same 16-frame animation:

| Phase | Frames (one-based) | Required behavior |
|---|---|---|
| Enter | 1-7, arriving at 8 | Move from the starting pose into the intended activity. |
| Dwell | 8, held by timing | A complete, balanced resting pose that remains believable for several seconds. |
| Conclude/return | 9-16 | Finish the activity and return smoothly to the starting pose for the next loop. |

Use Elsie's existing tempo as the default for new Officer work/greeting: about one second of advancing poses plus a two-second extra hold on frame 8, giving roughly a three-second loop. The hold length remains configurable when requested. Keep this established extra pause in frame 8's duration, including its normal frame time plus the extra hold, so the frame-8 choreography remains intact. This does not prohibit intentional repeated drawings elsewhere in the planned 16-slot timeline. Do not count a hold twice through both repeated slots and extra duration unintentionally. This extends the frame-8 policy beyond Elsie; older documents describing it as solely her setting are historical. It does not impose Elsie's idle/end-frame hold on every Officer or add a frame-8 pause to walking or combat.

Frame 8 must not be a suspended transition: feet and body weight are supported, the gesture has arrived, eyes/head face the activity, and hands and props have reached a natural position. A raised hand can be a valid held greeting when the posture is intentional and settled. For reading, the paper is already raised and her gaze rests on it at frame 8; frames 9-16 finish reading and lower/stow it. Secondary motion must settle before this held frame rather than freeze at an overshoot. Review frames 7/8/9 together and play the full multi-second hold during QA; selecting a convenient frame after generation is not sufficient choreography.

A single held sprite is still during the dwell, including hair, cloth and body. Continuing breathing or other movement during the dwell would require a separately requested hold animation/runtime treatment; do not promise it from a static frame. These three phases are one clip with timing metadata, not three newly implemented runtime states.

Valerie's existing idle/work/greeting frames were accepted as usable at the reviewed preview's Half speed (0.5x), not its Normal speed. Retain those images when correcting her walking; use that reviewed half-speed playback, including its hold behavior, when a timing update or integration is requested. This is a Valerie-specific acceptance decision, not a universal slower tempo or approval to regenerate her three accepted clips. Skill maintenance alone does not change their preview or runtime timing.

## Exactly one eye blink per animation

Every newly authored 16-frame character clip must contain exactly one complete eye-blink event: open eyes, close, then reopen. This applies to idle, work, greeting, each walk/run/jog/sprint direction, attacks and other character actions, independent of gender. One blink is one contiguous close-and-reopen event; it may span multiple frames and does not mean one closed-eye frame or one blink per second. Do not add a second blink, repeated flutter or alternating winks. A looping clip repeats its single blink once per cycle.

Plan and record the blink's frame numbers in the action brief before generation. Keep the complete event inside the 16 frames, with eyes open at both loop boundaries and at deliberate dwell poses such as work/greeting frame 8 or an idle frame-16 hold. Choose non-held frames whose actual playback durations allow a brief natural blink; do not freeze half-closed/closed eyes for seconds or let extraction introduce extra closures. For a rear-facing or otherwise hidden-eye view, retain the same blink plan without turning the head or drawing visible eyes solely to show it; record the blink as occluded and visually unverifiable in that view.

Count close-and-reopen events in the delivered frames and review them at the intended playback speed, through holds and across the loop seam. Check any visible eye for accidental extra closures or facial flicker. This production rule does not authorize remaking previously accepted clips, including Valerie's retained idle/work/greeting.

## Adult female secondary motion

For adult women, "jiggle physics" means localized bust secondary motion authored into the sprite frames, not a new physics system or rig and not whole-body motion. Apply it to every animation with movement, including idle, work, greeting, walking, running, jogging, sprinting and combat where that action belongs to the character. Let the bust subtly lag and settle in response to the intended action; do not add extra torso rocking, hip swaying, root displacement or whole-body bouncing to manufacture jiggle. Keep the main action controlled and balanced. Natural body movement required by a gesture or gait is still valid; it is separate from the localized secondary motion.

Maintain the approved anatomy, volume, costume coverage and fastening points across the sequence. Amplitude and damping depend on body build, pace and clothing support. Avoid arbitrary size changes, texture flicker or moving rigid armor as if it were unsupported fabric. Tight supportive leather or armor can have little or no visible movement. Elsie's existing tight-leather animation is explicitly accepted without a retrofit for this feature. Settle the bust before deliberate holds, and verify that its motion does not drive unrelated body parts.

Inspect the [sprite reference](media/secondary-motion-sprite-2026-09-14.jpeg) and [short video reference](media/secondary-motion-video-2026-09-14.mp4) before briefing this motion. They are unchanged copies of `D:/Download/Jiggle Sprite.jpeg` and `D:/Download/Jiggle Video Ref.mp4`; the video is a 0.8-second, eight-frame example. They supply motion relationships only, not character identity, costume, pixel rendering, proportions or frame count. IMC's approved illustrated style, 16-frame rule and user-required four-direction movement coverage still apply. Hair and cloth follow the actual action independently; do not make every element bounce identically.

For locomotion, plan secondary motion as a separate per-frame track after the leg/contact track below. At each foot landing, the clothed bust may lag the torso by a small amount, rebound, then settle before the next landing; the second step repeats this response. Use the reference sheet's successive front/profile poses to study the relationship, not its exact amplitude, anatomy or shorter row count. Record the intended bust position/contour for each frame against stable shoulder, collar, ribcage and waist landmarks. Preserve overall volume, lacing, straps, garment coverage and costume construction; do not manufacture motion by moving the entire torso or randomly changing breast size. Front and profile views should show a readable but clothing-appropriate response when the outfit allows it. A rear view can legitimately occlude that response; never add whole-body sway to make hidden bust movement visible. During QA, compare adjacent frames and playback at gameplay scale. A sentence in the prompt or tiny random contour flicker is not evidence that the motion exists.

## Directions and genuine motion

For all newly produced character walk/run/jog/sprint sets, generate exactly four directions: Up, Down, Left, Right. Do not generate diagonals or expand to eight directions based on the historical GDD or existing renderer. This explicit user rule supersedes the former eight-direction Officer default; a later explicit user request may override it. Each delivered direction has its own 16 frames; sixteen frames shared across all directions does not satisfy this. Officer work rows and battle action rows are not directional rows. Preserve the correct state/direction order and asymmetric identity details; do not manufacture missing views by mirroring asymmetric costumes. Existing runtime directions are an integration concern, not permission to add generated views or rewrite current gameplay during production.

Author walking and all running variants as a continuous alternating stride using this one-based 16-frame plan. Right/left refer to the character's anatomical legs, not screen sides; forward/back refer to the travel direction.

| Phase | Frames | Leg movement |
|---|---|---|
| Starting extension | 1 | Right leg fully forward, left leg fully back, within a natural stride rather than locked or hyperextended knees. |
| First exchange | 2-8 | Smoothly bring the left leg forward and right leg back; frame 8 reaches left fully forward, right fully back. |
| Return exchange | 9-16 | Smoothly bring the right leg forward and left leg back, returning toward the frame-1 phase. |

Treat frame 16 as the last moving sample before frame 1, not a duplicated endpoint with an extra pause. Keep positions and motion continuous through 7/8/9 and 15/16/1/2. The two exchanges should have a balanced cadence despite the numbered anchors. No work/greeting frame-8 dwell applies to locomotion.

Before generating a locomotion direction, make a numbered pose plan for all 16 frames. Label each leg by **anatomical** right/left, identify its hip-to-knee-to-ankle chain, mark which foot supports or is swinging, and note the expected foot contact/clearance. Also make a direction-specific mapping between anatomical legs and the camera view; screen-left/right alone is unreliable in profiles, crossed poses and rear views. Use the approved appearance anchor for identity, and fix the opposite contact poses at frames 1 and 8 before filling the transitions. This example is a motion plan to adapt to the character's costume and pace, not permission to omit any frame:

| Frame | Anatomical right leg | Anatomical left leg | Weight/contact cue |
|---|---|---|---|
| 1 | Extended forward, heel contacting | Extended back, toe releasing | Right accepts weight. |
| 2 | Slightly farther back relative to hips | Back heel lifts | Right supports. |
| 3 | Tracks back toward/beneath hips | Knee bends, foot clears behind | Right supports. |
| 4 | Tracks farther back | Bent knee and foot pass beneath hips | Right supports. |
| 5 | Approaches rear extension | Lifted knee advances ahead | Right supports; avoid a high marching kick. |
| 6 | Rear foot stays grounded | Shin unfolds ahead, foot still clear | Right still supports. |
| 7 | Rear toe stays grounded until the next contact | Forward heel approaches ground | Right still supports; no unsupported gap. |
| 8 | Fully back | Fully forward, heel contacting | Left accepts weight; no hold. |
| 9 | Back heel lifts | Slightly farther back relative to hips | Left supports. |
| 10 | Knee bends, foot clears behind | Tracks back toward/beneath hips | Left supports. |
| 11 | Bent knee and foot pass beneath hips | Tracks farther back | Left supports. |
| 12 | Lifted knee advances ahead | Approaches rear extension | Left supports; avoid a high marching kick. |
| 13 | Shin unfolds ahead, foot still clear | Rear foot stays grounded | Left still supports. |
| 14 | Forward heel approaches ground | Rear toe stays grounded | Left still supports; no unsupported gap. |
| 15 | Extends farther forward, just above ground | Moves farther back, toe grounded | Left supports while preparing frame-1 landing. |
| 16 | Nearly reaches frame-1 contact pose | Nearly reaches frame-1 rear pose, toe grounded | Last moving sample; next frame lands without a jump. |

Check each generated pose against **both** the immediately preceding pose and the fixed numbered plan. Compare leg identity, joint articulation, planted-foot travel relative to the hips, swing-foot clearance, body scale and pivot. Keep the approved appearance anchor in every generation group so chaining from the previous image does not accumulate costume/anatomy drift. Do not use a rejected motion pose as a guide for the next group. Inspect 1/2, 7/8/9 and 15/16/1 together and play the entire loop before accepting further groups or exporting. If a leg switches identity, support changes early, both feet slide, or the seam jumps, correct and review the affected poses and adjoining transitions before continuing; do not pad with duplicates, hide the defect by speeding playback, or certify the set from valid files alone. If guided generation repeatedly fails, keep the set as an unapproved candidate and use a more controlled pose method or direct frame correction in a separately authorized production pass.

Plan and inspect the bust track alongside this pose plan where applicable: mark each contact's small lag, rebound and settle against fixed torso and garment landmarks. The two footfalls can produce two subtle secondary responses in one 16-frame walk; this does not change the separate rule of exactly one eye blink. Reject an apparently stable gait if the required visible response is absent, or if apparent jiggle is only torso bounce, inconsistent volume or clothing flicker.

Show articulated hips, knees and ankles, alternating support, foot lift/clearance and believable landing. During walking, the supporting foot stays planted relative to the ground as the body advances; for an in-place preview it travels backward relative to the torso while the swing foot lifts and passes forward. Do not slide both feet, shuffle, stumble or merely translate rigid legs between extremes. Running/jogging/sprinting retain the phase plan with pace-appropriate contact and airborne phases instead of reusing a walking stance unchanged. Keep body scale, framing and foot pivots stable, with only restrained action-appropriate weight transfer; localized bust motion must not introduce extra body wobble. Record cycle duration, direction order and pivots; runtime movement speed must match the stride when integrated.

Sprite-gen's short-action default is four frames and humanoid walk/run remain experimental until motion QA passes. Those are tooling reliability notes, not IMC's art specification. A 16-cell sheet may still contain incoherent or missing action. Keep 16 delivered slots, distinguish reused drawings and any interpolated frames from newly authored poses, and verify the required action instead of demanding 16 different pixel hashes. Intentional holds remain valid timing choices. Locomotion must still preserve alternating support and its continuous loop; stationary-idle holds are not a substitute for walking transitions.

Review the selected exported sequence for:

- Actual articulated action progression and meaningful anticipation/contact/recovery.
- Identity, anatomy, costume mass and material consistency; no face/body changes or flickering ornaments.
- Frame-to-frame color and lighting consistency under [the rendering contract's practical tolerance](rendering-contract.md#frame-to-frame-color-and-lighting-consistency): slight shading differences are acceptable; obvious complexion changes, material-color jumps and distracting lighting flicker are not. Review skin and other materials separately in playback, including the loop boundary, rather than certifying consistency from image-wide averages.
- [Shared base-relative scale across clips and generation batches](#shared-character-scale-across-clips), stable feet/pivots, appropriate ground contact, alternating support for locomotion and no unexplained foot sliding; inspect actual state transitions as well as each isolated loop.
- Loop seam continuity for loops; correct completion/held final pose for one-shots and defeat.
- Required directions, clear silhouette at gameplay size and no clipped weapons, hair or effects.
- Correct frame count, durations, atlas rectangles and transparency, without chroma halos or texture contamination.
- Clean, stable outer contours and interior lines at gameplay size; follow `rendering-contract.md` for outline and background checks.
- For Officer work/greeting, a fully resolved frame-8 pose, natural arrival/departure and secondary motion settled through the actual hold duration.
- Clothing-appropriate secondary motion where applicable, with stable anatomy and no unsignaled changes of volume or costume.
- Bust motion localized to that region rather than extra root/torso/hip oscillation, with deliberate main-body movement and settled holds; for clothing that allows visible motion, verify the per-frame lag/rebound/settle against fixed garment landmarks rather than a prompt claim.
- Exactly one complete blink per 16-frame clip where eyes are visible, open eyes during holds and across the seam, and explicitly recorded occlusion for hidden-eye views.
- Four cardinal directions only for new locomotion; check each numbered pose's anatomical leg and support assignment against the fixed plan and its preceding frame, then verify right-forward frame 1, left-forward frame 8, articulated foot contact and the 16-to-1 seam in playback.

Review playback plus contact sheets and available motion evidence. Automated pixel checks cannot certify appeal or locomotion. Report unverified contacts as unverified rather than inferring them from the bottommost silhouette.

## Current runtime compatibility

Snapshot verified after Elsie's 2026-09-13 integration; re-read the code before future integration:

- `presentation/animated_actor.gd::_select_sheet` defaults to eight columns. Commander idle uses six, Commander walk eight; most Officer/staff and party/monster actions still use eight.
- Elsie is an integrated exception: her dedicated `assets/visual/actors/elsie/manifest.json` supplies 16-frame state rows, frame rectangles, per-frame durations and pivots. Her idle holds frame 16 for one extra second; work and greeting hold frame 8 for two extra seconds. `presentation/hq.gd` chooses ambient idle/work, and the service-menu flow in `presentation/app.gd` starts/stops greeting.
- `_update_frame` uses the manifest duration sequence for Elsie and retains uniform-FPS fixed-grid playback for existing actors. This is not a generic drop-in adapter for every future 16-frame asset; integrate each role's actual states and directions deliberately.
- The 2026-09-14 walking requirement and shared Officer hold choreography are production requirements. Elsie's currently installed set still contains only idle/work/interact; Officer locomotion and generic direction routing are not implemented by updating this skill. Track walking deliverables and runtime activation separately when their production/integration is requested.

A future authorized integration should read per-animation frame rectangles/counts, timing, loop behavior and pivots, with compatible handling for existing assets. Update relevant bounds/shader grid assumptions and export mappings together. Verify an existing six/eight-frame sequence and a new sixteen-frame sequence, including state changes, loop/one-shot completion and contact/impact timing. Check actual gameplay effects instead of assuming the presentation update cannot affect them.

Do not implement that runtime change as a side effect of creating a skill or generating a candidate. State delivery status accurately: concept candidate, visually reviewed export, or integrated and verified in IMC. File-format validity alone is not integration verification.
