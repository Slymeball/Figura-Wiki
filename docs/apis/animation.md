---
layout: default
title: Animation
parent: Scripting APIs
---

# Animation
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Root Calls

### `animations:getAnimations()`

Returns a table with all animations sorted by containing model.

Returns table.

### `animations:getPlaying()`

Returns a table with all playing animations.

Returns table.

### `animations:stopAll()`

Stops all playing animations.

## Targeting an Animation

To target an animation, follow the format `animations.<MODEL>.<ANIM_NAME>`. Depending on your animation's name, you may have to do `animations.<MODEL>[<ANIM_NAME>]`.

## Animation Playing Calls

### `:play()`

Starts or resumes playing the specified animation.

### `:stop()`

Stops the specified animation and returns animated parts back to their original positions.

### `:pause()`

Pauses the specified animation without returning animated parts back to their original positions. To continue playing the animation, use `:play()`.

### `:restart()`

Plays the specified animation from the start, even if it was paused.

### `:setPlaying(bool)`

Plays or stops the animation depending on the boolean passed as an argument.

### `:getPlaybackState()`

Gets the animation's playback state.

Returns string.

### `:setTime(number)`

Sets the current seek of the animation in seconds.

### `:getTime(number)`

Gets the current seek of the animation in seconds.

Returns number.

## Animation Settings Calls

### `:blend(number)`

Sets the keyframe blend factor.

Returns animation.

### `:getBlend()`

Gets the keyframe blend factor.

Returns number.

### `:length(number)`

Sets the animation's length in seconds.

Returns animation.

### `:getLength()`

Gets the animation's length in seconds.

Returns number.

### `:loop(string)`

Sets the animation's loop mode.

Returns animation.

### `:getLoop()`

Gets the animation's loop mode.

Returns string.

### `:loopDelay(number)`

Sets the time between each animation loop in seconds.

Returns animation.

### `:getLoopDelay()`

Gets the time between each animation loop in seconds.

Returns number.

### `:offset(number)`

Sets the time skipped each animation play and loop in seconds. <!-- I really don't know either TBH. -->

Returns animation.

### `:getOffset()`

Gets the time skipped each animation play and loop in seconds.

Returns number.

### `:overridePos(bool)`

Sets the animation's ability to override a vanilla part's position.

Returns animation.

### `:getOverridePos()`

Sets the animation's ability to override a vanilla part's position.

Returns boolean.

### `:overrideRot(bool)`

Sets the animation's ability to override a vanilla part's rotation.

Returns animation.

### `:getOverrideRot()`

Sets the animation's ability to override a vanilla part's rotation.

Returns boolean.

### `:overrideScale(bool)`

Sets the animation's ability to override a vanilla part's scale.

Returns animation.

### `:getOverrideScale()`

Sets the animation's ability to override a vanilla part's scale.

Returns boolean.

### `:override(bool)`

Sets the animation's ability to override all vanilla part transforms.

Returns animation.

### `:priority(int)`

Sets the animation's priority.

Returns animation.

### `:getPriority()`

Gets the animation's priority.

Returns integer.

### `:speed(number)`

Sets the animation's speed in seconds. Negative numbers will "invert" the animation.

Returns animation.

### `:getSpeed()`

Gets the animation's speed in seconds.

Returns number.

### `:startDelay()`

Sets the time before the animation is played in seconds.

Returns animation.

### `:getStartDelay()`

Gets the time before the animation is played in seconds.

Returns number.