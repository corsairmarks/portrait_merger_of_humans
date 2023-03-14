# Overview

You didn't ask for it and you probably hate it already! I've combined the new and old human portraits into two unified portrait sets.  What's the difference you ask?  The `human` portrait group (which appears first in species selection) puts each new portrait before the matching legacy portrait, while the `human_legacy` portrait group (appears second in appearance selection) puts each legacy portrait before the matching new portrait.

# Changes

Updates both the new and legacy human portrait selectors so that both groups use all the human portraits.

This mod overwrites two files from the Stellaris game:

* `gfx\portraits\portraits\07_portraits_human.txt` - alters the human portrait groups to use all human portraits in both groups (this one is most important)
* `gfx\models\portraits\human\new_human\_new_human_portrait_entities.asset` - reduces the scale on the new human portraits to make their size closer to the legacy portraits (from 0.81 to 0.78)

If anyone who understands working with Stellaris meshes reads this - I think the "issue" is that the legacy human mesh has its content closer to the origin, thus making the legacy humans appear shorter.  The actual texture files are the same dimensions and (when viewed with a graphics editor) approximately the same height at the shoulder.  If anyone would like to help me adjust the legacy human meshes, I would appreciate it.  I would like to give them similar "height" to the new portraits, which should be possible because the bottom of their graphics are already cut off in the game display.

## Compatibility

Built for Stellaris 3.7 "Canis Minor" and backwards-compatible with version 3.5 "Fornax."  **_Yes_**, this is achievement compatible and can be added or removed from your game at any time.

Will not work with other portrait mods that also edit the `07_portraits_human.txt` file, but _should_ work with mods that add clothing or attachments to the legacy human portraits.

## Changelog

* 1.0.0 Initial version
* 2.0.0 Update for Stellaris version 3.6 "Orion" (and changes from version 3.5 "Fornax") - `hair` to `attachment`
* 2.1.0 Flagged as compatible with Stellaris 3.7 "Canis Minor" - no actual changes

## Source Code

Hosted on [GitHub](https://github.com/corsairmarks/portrait_merger_of_humans)

### Development Notes

It is best to clone this repository into `<Stellaris User's Directory>/Paradox Interactive/Stellaris/mod`, and then make a connection to the `mod` folder via a `*.mod` file's `path` property.  That will ensure the game can see the files, and also that CWTools will parse them.  Also note that the README.md file exists in the `mod` directory but is symbolically linked in the root directory.