# IMC Character Companion Skill

This repository contains the IMC (Isekai Mercenary Company) companion skill for Codex. It provides the project's visual direction and production contracts for characters, portraits, gameplay sprites, animations, monsters and related review. Its invocation remains `$imc-art-direction`.

The separate `$imc-environment-art-direction` skill in `D:/Godot Projects/IMC-Companion-Skill-Environment` covers hunting/battle backgrounds, playable locations such as the Adventurer Office, scenery and maps.

## Install for Codex

Place this folder at:

```text
%USERPROFILE%\.codex\skills\imc-art-direction
```

The folder must contain `SKILL.md` at its root. The `agents/`, `references/` and `references/media/` folders are part of the skill and should be kept with it.

On the author's machine, the Codex skill path is a Windows directory junction to this repository folder. Changes made through either path therefore update the same files. A clone on another machine needs its own install at the Codex skills path.

## Current runtime note

Walking and running remain unstable in the current game runtime. The skill's walking requirements describe authored animation deliverables; use the planned runtime method before relying on walking or running in-game.
