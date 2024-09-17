# Worlds Without Number Homebrew

A Foundry VTT module to share WWN data between worlds via compendia.

## Installation

1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
2. Click the `Install Module` button.
3. Paste the Module's [Manifest URL](https://raw.githubusercontent.com/sirkerry/wwn-homebrew/main/module.json)
   into the `Manifest URL` field.
4. Click the `Install` button.

| WARNING: If you update this module, FoundryVTT will erase your compendia. |
| ------------------------------------------------------------------------- |

### Preventing Module Update

- Option 1 (easier): Locking your module:
  1. Go to the Add-on Modules tab within the FoundryVTT Configuration and Setup page.
  2. Find this module (WWN Homebrew) in the list, and click the padlock icon.
- Option 2: Updating your `module.json` file:
  1. Go to the Module's installation folder within foundry (`~/Data/modules/wwn-homebrew`) and update the `module.json` file.
  2. Remove lines 108-109 (`url` and `manifest`) and save the file.
  3. Restart Foundry to reload the module.

### Unlock your Compendia!

_Remember_ that you need to unlock your compendia to be able to add things to them.

## Default Setup

This module comes with 9 Default compendia:

- `Homebrew Actors` ([Actors](https://foundryvtt.com/article/actors/))
- `Homebrew Adventures` ([Adventure](https://foundryvtt.com/article/adventure/))    
- `Homebrew Card Stacks` ([Cards](https://foundryvtt.com/article/cards/))
- `Homebrew Items` ([Items](https://foundryvtt.com/article/items/))
- `Homebrew Journal Entries` ([JournalEntry](https://foundryvtt.com/article/journal/))
- `Homebrew Macros` ([Macros](https://foundryvtt.com/article/macros/))
- `Homebrew Playlists` ([Playlists](https://foundryvtt.com/article/playlists/))
- `Homebrew Rollable Tables` ([RollTables](https://foundryvtt.com/article/roll-tables/))
- `Homebrew Scenes` ([Scenes](https://foundryvtt.com/article/scenes/))

## Customize

To change the default setup, edit the `module.json` file. All compendia are defined within the "packs" attribute beginning with line 18.

For example:

```json
{
  "packs": [
    {
      "name": "monsters",
      "system": "wwn",
      "label": "Monsters",
      "path": "./packs/monsters.db",
      "module": "wwn-homebrew",
      "type": "Actor"
    },
    {
      "name": "spells",
      "system": "wwn",
      "label": "Spells",
      "path": "./packs/spells.db",
      "module": "wwn-homebrew",
      "type": "Item"
    }
  ]
}
```

Note: There are no compendium Types for Classes, Foci, Arts, and Spells in Foundry, so the `Item` type is generally used for these.

## Dependencies

- [WWN Game System](https://github.com/SobranDM/foundryvtt-wwn) is required: The Game System adds some SRD Compendia.


