---
layout: default
title: Figura FAQ
nav_order: 2
---

# The Unofficial (Rewritten) Figura FAQ
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{: .note }
> This FAQ only features questions and answers relating to the rewrite of Figura.

## General Questions

### Where can I download Figura?

Turns out, it's been on [Curseforge](https://www.curseforge.com/minecraft/mc-mods/figura/files/all) and [Modrinth](https://modrinth.com/mod/figura/versions) the whole time. You can also find it in the [Discord server](https://discord.gg/figuramc) and [GitHub Releases](https://github.com/FiguraMC/Figura/releases).

### Where can I find avatars to download and use?

To find full avatars, go to [#🎭丨avatar-showcase](https://discord.com/channels/1129805506354085959/1129823434705227846) in the [Discord server](https://discord.gg/figuramc) and select the (![](https://github.com/Slymeball/figura-wiki/raw/main/images/figura/icons/upload.png?raw=true) download available) tag. Likewise, avatar parts (models, scripts, etc) can be found in [#📦丨assets-browser](https://discord.com/channels/1129805506354085959/1129823477235458192). If you're looking for avatars and assets older than July 15th that haven't been reposted, you probably won't see it ever again.

### Why isn't Optifine/Optifabric not working?

~~Figura ***does not*** support Optifine due to its closed-source nature and overall uncompatable rendering engine. Instead, [try some alternatives](https://lambdaurora.dev/optifine_alternatives/).~~

Apparently, Figura supports Optifine and Optifabric now. Nice job, devteam! However, please still [try alternatives to Optifine](https://lambdaurora.dev/optifine_alternatives/). Even if Figura supports it, that doesn't mean other mods will be compatible.

## File System Questions

### What is the file system? How do I use it?

The Figura file system is the way avatars are sorted in Figura. To access the avatars folder, go to your `.minecraft` folder and navigate to `./figura/avatars`. A quick shortcut to this folder is in the Figura wardrobe, just click the ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/figura/icons/folder.png?raw=true) **Avatar Folder** button.

Avatar folders have a specific format to follow. Check below for info.

```
└ ./figura/avatars
    └ AvatarName *`
        ├ avatar.json
        ├ model.bbmodel *^`
        ├ script.lua *^`
        └ sound.ogg *^`

* = Can be named anything, just make sure the file type stays the same.
^ = Is not required for an avatar to load.
` = Can be placed in subfolders.
```

Subfolders with names starting with `.` will not be loaded by Figura.

### What is an `avatar.json` and how do I make one?

An `avatar.json` file is required for Figura to recognise an avatar and holds metadata about the avatar. This includes...

- `name` [string] - The name of the avatar, shown in the wardrobe list, avatar information, and logs.
- `author`/`authors` [string/array] - The author(s) of the avatar, shown in avatar information.
- `version` [string] - The version of Figura an avatar was made to interact with. This shows as a badge when a player tries to view an avatar not on the same version as them.
- `color` [string] - The accent color used in the avatar's badge and avatar information.
- `autoScripts` [array] - A list of all scripts that should be run in what order. If this field is specified, all scripts not inside this array or not required will not be executed.
- `customizations` [object] - A table of model parts with modifications to apply to each. This section is quite complex, so please check the following example.

#### `avatar.json` Example

```json
{
    "name": "Example Avatar",
    "authors": ["Author1", "Author2"],
    "version": "0.1.0_rc-10",
    "color": "#123456",
    "autoScripts": ["script1", "script2"],
    "customizations": {
        "model.part": {
            "visible": false,
            "moveTo": "model.bone",
            "parentType": "Head",
            "primaryRenderType": "GLINT",
            "secondaryRenderType": "END_PORTAL"
        }
    }
}
```

#### Depreciated Tags

These tags have been removed from Figura for one reason or another.

- `pride` [string] - This tag used to change the badge's texture to a pride flag, but was removed in favor of a more backend-centered system.

## Modeling Questions

<!--| todo: get toast's help with this, he seems like the kind of person who knows about modeling
    | edit oct. 10 2023: haha yeah no i don't think i'll be getting his help with this ever.
-->

### How do I make my avatar glow?

Although you cannot make your avatar use the [Glowing effect](https://minecraft.fandom.com/wiki/Glowing) using Figura (you can only approximate it), you *can* give it an emission texture.

To make an emissive texture, set the name of a texture to `%texturename%_e` where `%texturename%` is the name of a non-emissive texture. After that, erase parts of the texture that you do not want to glow.

## Scripting Questions

### How do I hide the player model?

To put it simply, you can disable everything (player, armor, cape, elytra, and held items) by inserting the following into a script.

```lua
vanilla_model.ALL:setVisible(false)
```

To disable a whole group of objects, use one of the commands below.

```lua
vanilla_model.PLAYER:setVisible(false) -- Player Model
vanilla_model.INNER_LAYER:setVisible(false) -- Player Model: Inner Layer
vanilla_model.OUTER_LAYER:setVisible(false) -- Player Model: Outer Layer

vanilla_model.ARMOR:setVisible(false) -- Armor
vanilla_model.CAPE:setVisible(false) -- Cape
vanilla_model.ELYTRA:setVisible(false) -- Elytra
vanilla_model.HELD_ITEMS:setVisible(false) -- Held Items
```

If you would like even more control, check the list of vanilla model objects by typing `/figura run printTable(vanilla_model)` into Minecraft. This way, you can see every cube and part that makes up the default model and you can insert it into your script.

### Where can I find documentation for Figura's scripting?

Figura actually provides a documentation command in-game! Just type `/figura docs` and let auto-completion help you find your code inquiries.

~~Instead of launching the game every time you want to get a result, you can type `/docs` into the [#bot-junk](https://discord.com/channels/805969743466332191/824741434078396468) channel on the [Discord server](https://discord.gg/ekHGHcH8Af). Although it may be clunkier, it works well in support scenarios.~~ Prisma no longer has the /docs command and instead searches Figs' documentation.

If you would like something that implements directly into Visual Studio Code, Manuel_ provides a Figura extension with built-in documentation. You can download it on the VSC marketplace using the built-in extensions tab or by using [this link](https://marketplace.visualstudio.com/items?itemName=Manuel-Underscore.figura). 

A community member with the name applejuice has an online webpage that delivers the content from the in-game documentation and places it in an easier to read format. You can find it at <https://applejuiceyy.github.io/figs/>

### How can I get support?

You can ask a question at any time through the [#❔️丨hellp Forum](https://discord.com/channels/1129805506354085959/1129811341620809870) (yes, it is spelt hellp) in the [Discord server](https://discord.gg/figuramc). People are usually on stand-by and can help you with any issue you have.

Alternatively, you can request an avatar, script, model, or texture using the [#💌丨commissioners](https://discord.com/channels/1129805506354085959/1129953370673786970) channel. People offer their services in this channel either out of their own free will or out of monetary gain, so please be kind.
