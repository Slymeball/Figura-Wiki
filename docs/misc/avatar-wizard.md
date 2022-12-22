---
layout: default
title: The Avatar Wizard
parent: Miscellaneous Pages
---

# The Avatar Wizard
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

The Avatar Wizard (sometimes known as the avatar creator) allows beginners to easily create an avatar with templates and an easy way to fill in metadata. As fields are ticked or filled, more options will appear.

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/wizard/blank.png?raw=true)

The **Name** is what your avatar will show as its name in the wardrobe list[^1], avatar information, and trust menu. This is equivalent to the `name` tag in the `avatar.json` file.

[^1]: Only applicable if the "Wardrobe File Names" setting is off.

---

After the name of the avatar is filled, the author, model, and script options unlock.

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/wizard/name.png?raw=true)

The **Author** field shows in the avatar information and shows who created the avatar. This is equivalent to the `author`/`authors` tag in the `avatar.json` file.

---

The **Include a Model** option will generate a model from the templates you pick in the toggles that appear.

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/wizard/model.png?raw=true)

- **Custom Player Model** gives you the basic six parts (with an extra six for layers) of a player model.
  - **Slim (Small) Arms** makes the arms of the custom player model one pixel thinner.
- **Cape Template** generates a rectangle that uses the Cape parent.
- **Elytra Template** generates two rectangles that use their respective Elytra parent.

<br>

- **Held Items Pivot** adds bones for both held item pivots.
- **Spyglass Pivot** adds a bone for the spyglass pivot.
- **Held Item Pivot** adds a bone for the held item pivot.
- **Parrots Pivot** adds bones for both parrot pivots.

---

The **Include a Script** option will generate a script from the templates you pick in the toggles that appear.

![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/panel/wizard/script.png?raw=true)

- **Hide Vanilla Armor** hides the vanilla armor. I don't know what else to tell you.
- **Hide Vanilla Cape** hides the vanilla cape.
- **Hide Vanilla Elytra** hides the vanilla elytra.
- **Include dummy events** gives you a basic `ENTITY_INIT`, `TICK`, and `RENDER` event register.