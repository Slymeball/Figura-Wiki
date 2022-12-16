---
layout: default
title: Trust Menu
parent: The Figura Panel
---

# Trust Menu
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

# Quick Access

The trust menu is where the limits on each avatar is set.

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/trust.png?raw=true)

## Red - Filter Options
Filters the player list below.

- ![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/icons/hide_nonfigura.png?raw=true) Show/Hide Non-Figura Players
- ![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/icons/hide_offline.png?raw=true) Show/Hide Offline Players

## Orange - Player List
From this, you can pick any player online (or offline) and move them up or down the trust list.

## Yellow - Avatar Preview
Shows the currently selected player's avatar or a question mark if an offline player or group is selected. Middle clicking resets the pan and rotation of the preview.

## Green - Trust Slider
Selects the trust level for the selected player. In later versions of 0.1.0, you can also move players by holding a click on their left-side card.

## Teal - Reload All Avatars
Clears the cache of all avatars and gets all avatars from the backend again.

## Blue - Manage Permissions
Allows the player to edit the specific limits on each player or group. See below for more information.

## Unpictured - Context Menu
Allows you to copy the name or UUID of a player, refresh, or change their trust. Right click a card to access.

# Permission Menu

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/trust-expanded.png?raw=true)

- Init Instructions [int] is how many lines of code can be executed when an entity or skull is loaded.
- World Tick Instructions [int] is how many lines of code can be executed on a world tick.
- Tick Instructions [int] is how many lines of code can be executed on an entity tick.
- World Render Instructions [int] is how many lines of code can be executed on a world render (each frame the world is rendered).
- Render Instructions [int] is how many lines of code can be executed on an entity render (each frame the entity is rendered).
- Max Complexity [int] is how many faces can be displayed.
- Max Particles [int] is how many particles can be played each second.
- Max Sounds [int] is how many particles can be played each second.
- Avatar Sounds Volume [int] controls how loud sounds scripted into the avatar can be.
- Animation Complexity [int] is how many animation channels can be loaded at once. Not played, *loaded*.
- Max Texture Size [int] is how large textures generated with the Texture API can be.
- Vanilla Model Change [bool] allows avatars to modify the vanilla model.
- Nameplate Change [bool] allows scripts to alter the nameplates of players.
- Render Offscreen [bool] allows avatars to render offscreen.
- Custom Sounds [bool] allows avatars to play sounds not provided by the game.
- Custom Player Heads [bool] allows avatars to replace the in-game player head with their own custom model.