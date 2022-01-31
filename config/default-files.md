---
description: Default files created when loading the plugin for the first time.
---

# Default Files

## Configuration Files

#### GUISettings.yml

```
GUI:
  Settings:
    GUI-Size: 27
    GUI-Name: '&8Select a pack'
  MainItems:
    Use-Current-World:
      Material: STAINED_CLAY
      Damage: 13
      Amount: 1
      Name: '&a&lUse Current World ResourcePack'
      Lore:
      - ''
      - '&7Click to select!'
      GUI-Location: 12
    Select-World:
      Material: STAINED_CLAY
      Damage: 14
      Amount: 1
      Name: '&c&lSelect World ResourcePack'
      Lore:
      - ''
      - '&7Click to select!'
      GUI-Location: 14
Worlds-GUI:
  Settings:
    GUI-Size: 27
    GUI-Name: '&8Select a world'
  Items:
    world:
      Material: DIAMOND_BLOCK
      Damage: 0
      Amount: 1
      Lore:
      - ''
      - '&7Click to download defined resourcepack!'
      GUI-Location: 10
    world_nether:
      Material: DIAMOND_BLOCK
      Damage: 0
      Amount: 1
      Lore:
      - ''
      - '&7Click to download defined resourcepack!'
      GUI-Location: 11
    world_the_end:
      Material: DIAMOND_BLOCK
      Damage: 0
      Amount: 1
      Lore:
      - ''
      - '&7Click to download defined resourcepack!'
      GUI-Location: 12

```

#### Messages.yml

```
Accept-Message: '&aYou have accepted the pack request!'
Declined-Message: '&cYou have declined the resource-pack request!'
Successfuly-Downloaded-Message: '&aSuccessfully downloaded the resource-pack!'
Failed-Downloaded-Message: '&cThere was an error downloading the resourcepack, please
  inform the staff members!'
Error-Message: '&6Error: error on checking request!'
```

#### Settings.yml

```
Resourcepack-URL: some.url.here
Global-Resourcepack: true
Resourcepack-Command: rp
Command-Case-Sensitive: false
Use-Join-Bypass-Permission: false
Send-Resourcepack-On-Join: false
Accepted-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
Declined-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
Successfuly-Downloaded-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
Failed-Download-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
Messages:
  Enable-Accepted-Message: true
  Enable-Declined-Message: true
  Enable-Successfuly-Downloaded-Message: true
  Enable-Failed-Downloaded-Message: true
```
