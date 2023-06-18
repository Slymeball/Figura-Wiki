---
layout: default
title: Settings
parent: The Figura Panel
nav_order: 3
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
- Sound Indicator [bool] shows a 🔊 in an avatar's nameplate if it is playing sound, regardless if it is a vanilla sound or custom sound.
- Chat/Entity/List customizations [dropdown] allows Figura and avatar scripts to change the nameplate in each category.

## Script

- Print Output [dropdown] chooses where your avatar's logging and errors will be printed.
- Print Number Length [int] determines how long a decimal can be when printed.
- Format Script [dropdown] chooses how formatted your script should be when interpreted.

## Rendering

- Iris Compatibility Fix [dropdown] chooses what fixes to implement to work with Iris.
- Render Parts Pivot [dropdown] chooses which models to show the pivots of when hitboxes are turned on.
- First Person Hands [bool] toggles whether a script can modify the first person hands.
- First Person Matrices [bool] toggles whether matrices should be updated in first person.

## Action Wheel

- Action Wheel Button [key] picks which keybind should be used to show the action wheel.
- Action Wheel Mode [dropdown] picks the bind behavior and whether the action wheel should run the selected action on release.
- Action Wheel Size [number] changes the size of the action wheel.
- Selected Action's Text [dropdown] selects where and how the title of the action is displayed.
- Slots Indicator Text [dropdown] selects where the action wheel's overflow dropdown should be displayed. If it is in the same spot as the hovered action's text, the latter will take priority.
- Item Decorations [bool] toggles the durability, count, and other overlays on items.

## UI Settings

- Figura Inventory [bool] toggles between Minecraft and Figura's paper doll rendering.
- GUI Head Rotation [bool] toggles whether the head in Figura's preview should be rotated based on the in-game player's rotation.
- Avatar Portrait [bool] allows Figura to show renders of avatars in the tablist and permission list.
- Wardrobe File Names [bool] makes the wardrobe use file names over avatar names.
- Background Scroll Speed [number] controls the speed of the backgroud animation in the Figura panel.
- Player Popup Scale [number] controls the scale of the player popup in-game.
- Player Popup Min/Max Size [number] controls the minimum/maximum size of the player popup.
- Toast Display Time [number] controls how long a Figura toast is on screen.
- Toast Title Display Time [number] controls the delay until the text in a Figura toast is swapped.
- Text Scroll Speed [number] controls how quick long text on buttons should scroll.
- Text Scroll Delay [int] controls how long until long text on buttons should scroll after stopping in ticks.

## Paperdoll

{: .information }
> When hovering over options in this section, a paper doll will be rendered in the correct spot.

- Enable paperdoll [bool] allows the paper doll to be rendered.
- Always on [bool] allows the paper doll to be rendered regardless of state.
- First Person only [bool] denies Figura the ability to show the paper doll in Third Person.
- Remove Invisibility [bool] renders the paper doll even if the player has invisibility.
- Paperdoll Scale/X/Y/Pitch/Yaw [number] determines the position, rotation, and scale of the paper doll.

## Misc

- Popup Menu [key] picks which keybind should be used for the popup menu.
- Reload Avatar [key] picks which keybind should reload the local avatar.
- Panic Button [key] picks which keybind should stop rendering all Figura avatars.
- Wardrobe Button [key] picks which keybind should open the wardrobe.
- Menu Button Location [dropdown] chooses where the button for the Figura panel should be.
- Figura Update Channel [dropdown] chooses which update channel should be used for warning the user about a new version.
- Default Permission Level [dropdown] picks which Permission level new players will use.
- Emojis [dropdown] allows Figura to parse messages for emojis registered within Figura.
- Enable Easter Eggs [bool] allows all easter eggs in Figura to be used.

## Dev

{: .warning }
> The following options are experimental and should be used with caution. In case of error, reset an option.

- Cloud Connection Toasts [bool] shows a toast whenever you are connected/disconnected from the backend.
- Log non-host scripts [bool] toggles whether logs and errors on other avatars should be printed to your logs.
- Log Pings [dropdown] toggles whether and where logs of pings should be shown.
- Sync Pings [bool] toggles whether pings should only be executed if recieved from the backend.
- Chat Messages [bool] toggles whether sending chat messages can be sent from avatar scripts.[^1]
- Figura Folder Location [string] gives the path to where the Figura folder is.
- Figura Cloud IP [string] gives the addresses for both the authentication server and backend.
- Clear Cache [button] clears the avatar and UI cache. It does not reset settings or permissions.
- Redownload Assets [button] grabs the latest emoji set and translations and reloads resources.
- Clear Avatar Data [button] resets all avatar configurations saved via `config`. It does not reset settings or permissions.
- Force Smooth Avatar [bool] forces avatars to use smooth shading normals.

[^1]: Messages sent with Figura will still be signed and can still be reported to Mojang. Figura does not take responsibility for any effects that can occur from the usage of Chat Messages.