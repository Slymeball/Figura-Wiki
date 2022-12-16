---
layout: default
title: Making an Empty Avatar
parent: Creating an Avatar
nav_order: 1
---

# Making an Empty Avatar
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

{: .important-title }
> Series
> 
> This page is the first in a series with others.

## Installing Fabric Mod Loader

If you do not already have a Fabric install available, make sure to get one from <https://fabricmc.net/use>. Please check the following links for more information.

- [Minecraft Launcher](/Figura-Wiki/docs/install-fabric.html#minecraft-launcher)
- [MultiMC](/Figura-Wiki/docs/install-fabric.html#multimc)
- [Prism Launcher / PolyMC](/Figura-Wiki/docs/install-fabric.html#prism-launcher---polymc)
- [GDLauncher](/Figura-Wiki/docs/install-fabric.html#gdlauncher)
- [ATLauncher](/Figura-Wiki/docs/install-fabric.html#atlauncher)
- [CurseForge](/Figura-Wiki/docs/install-fabric.html#curseforge)

## Installing Figura

Turns out, it's been on [Curseforge](https://www.curseforge.com/minecraft/mc-mods/figura/files/all) and [Modrinth](https://modrinth.com/mod/figura/versions) the whole time. You can also find it in the [Discord server](https://discord.gg/ekHGHcH8Af) and [GitHub Releases](https://github.com/Kingdom-of-The-Moon/FiguraRewriteRewrite/releases).

Figura requires the presence of [the Fabric API](https://modrinth.com/mod/fabric-api) to launch. If it is not installed, Fabric will display a warning and not launch the game.

Now that you have both Figura and Fabric API, drag them both into your mods folder. If you're using the default Minecraft Launcher, this will be located at `%appdata%\.minecraft\mods` on Windows, `~/Library/Application Support/minecraft/mods` on MacOS, and `~/.minecraft/mods` on Linux-based operating systems. If you're using MultiMC or MultiMC forks, you can just open your instance's configuration interface (the "Edit Instance" button), navigate to "Mods", and drag both mods into the interface.

## Creating an Avatar

Now that you have both Figura and Fabric API installed, launch the game. This will put the mods into effect and create the folders necessary to mess with Figura. Navigate to the `.minecraft` or `minecraft` folder mentioned before and open the new `figura` folder. Inside, there should be an `avatars` folder. Open this and create a new folder with any name.

Before continuing, please make sure that your file extensions are turned on. File extensions tell what format a file is in the form of suffixes following the template of `.<FORMAT CODE>`. Please check the text and images below for information on how to turn on file extensions.

| File Explorer | Instructions |
| --- | --- |
| Explorer (Windows 10) | Click "View" in Explorer's ribbon and then check the box "File name extensions" ![Click "View" in Explorer's ribbon and then check the box "Show File Extensions"](https://cdn.discordapp.com/attachments/808155531389698079/866441704693563413/100190d1473193093-hide-show-file-name-extensions-windows-10-a-file_name_extensions-file_explorer.png?size=4096)
| Explorer (Windows 11) | Click "View" in the top bar, navigate to "Show" in the context menu, and check "File Name Extensions" ![Click "View" in the top bar, navigate to "Show" in the context menu, and check "File Name Extensions"](https://cdn.discordapp.com/attachments/808155531389698079/890560150518259722/unknown.png?size=4096)

Go into this folder and create a new text file. Rename it to `avatar.json` and make sure that there is no `.txt` file extension. This file can be completely empty but can contain metadata for name, author, mark color, and version. If you would like to include this metadata, copy the code below and paste it into your `avatar.json`.

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

###### Source provided by Fran, thanks!
{: .no_toc }

Name and authors will show up in the Figura menu, color will change the color of your mark, and version doesn't do anything as of this page's creation.

Now, check your Figura menu by entering a world or server, pausing the game, and clicking the ![](https://github.com/Slymeball/figura-wiki/blob/main/images/figura/buttons/panel.png?raw=true) Figura icon next to the "Open to LAN" button as shown below.

![A picture of a cursor hovering over the Figura menu's button in Minecraft.](https://u.cubeupload.com/Letters_7/Screenshotfrom202207.png)

Now you should be able to find your avatar in the avatar picker.