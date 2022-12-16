---
layout: default
title: Settings
parent: The Figura Panel
---

# Settings
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Nameplate

- Enable Self Nameplate [bool] shows your own nameplate in third person and the paper doll.
- Nameplate in GUI [bool] shows your own nameplate in the panel preview and your inventory.
- Chat/Entity/List customizations [dropdown] allows Figura and avatar scripts to change the nameplate in each category.

## Script

- Print Output [dropdown] chooses where your avatar's logging and errors will be printed.
- First Person Hands [bool] toggles whether a script can modify the first person hands.
- Print Number Length [int] determines how long a decimal can be when printed.
- Format Script [dropdown] chooses how formatted your script should be when interpreted.

## Action Wheel

- Action Wheel Button [key] picks which keybind should be used to show the action wheel.
- Action Wheel Mode [dropdown] picks the bind behavior and whether the action wheel should run the selected action on release.
- Action Wheel Size [float] changes the size of the action wheel.
- Selected Action's Text [dropdown] selects where and how the title of the action is displayed.
- Item Decorations [bool] toggles the durability, count, and other overlays on items.

## UI Settings

- Background Scroll Speed [float] controls the speed of the backgroud animation in the Figura panel.
- Player Popup Scale [float] controls the scale of the player popup in-game.
- Player Popup Min/Max Size [float] controls the minimum/maximum size of the player popup.
- Avatar Portraits [bool] allows Figura to show renders of avatars in the tablist and trust list.
- Figura Inventory [bool] toggles between Minecraft and Figura's paper doll rendering.
- Toast Length [float] controls how long a Figura toast is on screen.
- Long Toast Swap [float] controls the delay until the text in a Figura toast is swapped.

## Paperdoll

- Enable paperdoll [bool] allows the paper doll to be rendered.
- Always on [bool] allows the paper doll to be rendered regardless of state.
- First Person only [bool] denies Figura the ability to show the paper doll in Third Person.
- Paperdoll Scale/X/Y/Pitch/Yaw [float] determines the position, rotation, and scale of the paper doll.

## Misc

- Popup Menu [key] picks which keybind should be used for the popup menu.
- Reload Avatar [key] picks which keybind should reload the local avatar.
- Panic Button [key] picks which keybind should stop rendering all Figura avatars.
- Menu Button Location [dropdown] chooses where the button for the Figura panel should be.
- Update Type [dropdown] chooses which update channel should be used for warning the user about a new version.
- Enable Easter Eggs [bool] allows all easter eggs in Figura to be used.

## Dev

{: .warning }
> The following options are experimental and should be used with caution. In case of error, reset an option.

- Backend Connection Toasts [bool] shows a toast whenever you are connected/disconnected from the backend.
- Render Parts Pivot [dropdown] picks which pivots should be visible when viewing hitboxes.
- Log non-host scripts [bool] toggles whether logs and errors on other avatars should be printed to your logs.
- Log Pings [dropdown] toggles whether and where logs of pings should be shown.
- Sync Pings [bool] toggles whether pings should only be executed if recieved from the backend.
- Chat Messages [bool] toggles whether sending chat messages can be sent from avatar scripts. :warning: Messages sent with Figura will still be signed and can still be reported to Mojang.
- Figura Folder Location [string] gives the path to where the Figura folder is.
- Auth Server/Backend IP [string] gives the addresses for both the authentication server and backend.