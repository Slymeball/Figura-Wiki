<!-- ---
layout: default
title: Adding Model Animations
parent: Scripting Tutorials
--- -->

# Adding Model Animations
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

## Playing on Keybind

To make our avatar animate on a keybind, we must first set a keybind up.