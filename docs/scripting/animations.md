---
layout: default
title: Adding Model Animations and Keybinds
parent: Scripting Tutorials
---

# Adding Model Animations and Keybinds
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Making custom animations can be a great way to give new life to your avatar.

## Making an Animation

Figura allows for animating your avatar through Blockbench animations. This includes knowledge on how to use Blockbench, make a model, and add animations to it. This tutorial does not show how to use these tools, but only how to play animations through Figura.

## Playing an Animation

Playing an animation in Figura is as simple as one line:

```lua
animations.Example.Animation:play()
```

In this example, `animations` is the API, `Example` is the model in which the animation resides, `Animation` is the name of the animation, and `play` tells Figura to play the animation on your avatar.

If you go back in game and reload your avatar, you'll see that it immediately plays when your avatar is loaded. That's no use, as you'll rarely want an animation to start that way, hence...

## Creating a Keybind

To make our avatar animate on a keybind, we must first set a keybind up. Making a basic, empty keybind only takes one line, which will look something like:

```lua
local animKey = keybinds:newKeybind("Play Animation", "key.keyboard.h")
```

In the example...

- `local animKey` will be how we refer to the keybind from now on. `:newKeybind` both registers a keybind and returns the keybind, allowing for modifications via chaining and variables.
- `keybinds` is the global API used to register keybinds.
- `:newKeybind` tells Figura to make and return a new keybind.
- `"Play Animation"` is the name of the keybind and will show in the keybind menu.
- `"key.keyboard.h"` is the default key that will trigger the keybind. To see a full list of these, type `/figura docs enums keybinds` into Minecraft chat.

Now, returning to Minecraft, your avatar still doesn't animate on this keybind. Going into the Figura panel and clicking the ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/figura/icons/keybinds.png?raw=true) icon, you'll see that your keybind *is* registered, so what's preventing your animation from playing?

## Animating on Keybind

The code above doesn't tell Figura to play your animation once the keybind is pressed. To fix this, we'll go ahead place the animation call inside a function known as `animKey.press()`. This function's name will change depending on what you named your keybind variable, but the ending should always be `.press()`

```lua
local animKey = keybinds:newKeybind("Play Animation", "key.keyboard.h")

function animKey.press()
    animations.Example.Animation:play()
end
```

Returning to Minecraft and pressing your keybind key, you'll notice that your model starts animating.

## Animating on Action Wheel

Maybe you don't like taking up valuable keys on your keyboard and would rather use a quick to access and use GUI to trigger your animation. This is where the action wheel comes into play. Assuming that you already know how to set up an action wheel and an action inside of it, we'll continue on. If not, please wait for a tutorial.

To make your action do something on left click, add an `:onLeftClick()` to your action and put a function inside containing your play instruction from earlier. It should look something like this:

```lua
wheel:newAction()
    :title("Play Animation")
    :onLeftClick(function()
        animations.Example.Animation:play()
    end)
```

We will continue on in the tutorial with the previous keybind example.

## Pinging Your Animation

However, you'll notice that others are unable to see your animation. This is because your keybind presses are not synced between all players. To do this, you'll need the help of ping functions. See [the tutorial for pings](https://www.slyme.xyz/Figura-Wiki/docs/scripting/pings.html) for more information.

TL;DR: You can make a function a ping function by putting `pings.` before your function's name.

Just make a new pinged function, put your animation call in it, and call the function in your keybind.

```lua
function pings.playAnimation()
    animations.Example.Animation:play()
end

local animKey = keybinds:newKeybind("Play Animation", "key.keyboard.h")

function animKey.press()
    pings.playAnimation()
end
```