---
layout: default
title: Pinging Information to Non-Host Clients
parent: Scripting Tutorials
---

# Pinging Information to Non-Host Clients
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Have you ever noticed how, when manually calling an animation, creating a particle, playing a sound, etc., it doesn't show up on other people's ends? These's a fix for this, and it's called pings.

## What *Are* Pings?

Pings (or ping functions) are functions that, when called, send themselves to the backend to be called on others' clients. This is neccesary to sync things called with a keybind, action wheel, or anything that can only be detected on the host's end (like flying).

## How do I use them?

To make a function a ping function, just put `pings.` before the function's name. For example,

```lua
function pings.sendLog(v)
    log(v)
end
```

will send the log specified with `v` to all clients. Of course, this log will only show up if "Log non-host scripts" is set to true.

Pings are able to support 1 kilobyte of data per second. Any more and your pings will be ratelimited with a toast at the top right of your screen warning you as such.
