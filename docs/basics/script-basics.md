---
layout: default
title: The Basics of Scripting
parent: Creating an Avatar
nav_order: 3
---

# The Basics of Scripting
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---


The last great thing every avatar should have is a script. Figura uses the Lua programming language to script things that should happen in your avatar, ranging from animations to nameplate modification to a wheel that makes player-controlled function calling much easier.

## Installing Visual Studio Code

To program in Lua, you must have any plain text editor, but I recommend something like Visual Studio Code. To get Visual Studio Code (or as it will be referred to, VSC), go to their downloads page at <https://code.visualstudio.com/Download>. VSC, unlike the Visual Studio made for .NET programming, is monetarily free and **is based** on open source technologies. If you do not want to or cannot install VSC, you can access it online at <https://vscode.dev>.

## Getting Extensions

The reason I recommend VSC for Figura scripting is because there is already a Figura extension for it. Once you're in the editor, look for the icon with four squares, one disconnected, on the left toolbar. This will open the Extensions panel, where you can manage your installed extensions and get new ones from the marketplace. Click the search bar and type "Figura" into it. You'll see one labeled "Figura" by none other than Manuel_ (although named Manuel-Underscore here). Click the Install button to install the extension. Alternatively, you can go to [this link](https://marketplace.visualstudio.com/items?itemName=Manuel-Underscore.figura) to directly install it from your browser.

The Figura extension requires a language server. Type "Lua" into the search bar and install the extension created by sumneko. You can also click [this link](https://marketplace.visualstudio.com/items?itemName=sumneko.lua) for a direct link to the extension. 

As of right now, you must tell the Figura extension that you are programming for 0.1.0. This can be done by right-clicking on the icon for it and clicking on Extension Settings. Make sure the target function is `0.1.0`.

## Starting a Script

Now that you have your workspace ready, open up your avatar's folder. You can do this by clicking on `File > Open Folder...`, using the keyboard shortcut `CTRL+K CTRL+O`, or by dragging the folder into the window. Next, navigate to your avatar's folder using the Explorer pane.

Create a file inside your avatar's folder with the file extension `.lua`. This will tell Figura that this file is a script file and should be executed.

## Lua Syntax

To get basic syntax out of the way, lets learn about variables, statements, and conditionals.

```lua
--[[
Variables can be set using the following syntax. They can be set to the 
following types:
--]]

a = true -- Boolean (True/False)
b = 3 -- Integer (Whole Number)
c = 27.63 -- Float (Fractioned Number)
d = "Hello, World!" -- String (Text)
e = {true,10,"idhr CV 3ic6ebenz;#83;£8;#?"} -- Array (Numbered List)

f = {
    [1] = false,
    [true] = "Cheeseburger",
    ["foo"] = 7
} -- Object (Keyed List)
```

```lua
--[[
Accessing these variables are quite easy. Just put their name down and their contents will be there instead.
---]]

print(a)
-- Prints: true

print(b)
-- Prints: 3

print(c)
-- Prints: 27.63

print(d)
-- Prints: Hello, World!

-- The reason I used e[2] was to select speficially the second index of the array, which was 10.
print(e[2])
-- Prints: 10

print(f[true]) -- Same reason for this one, just now specifying any type.
-- Prints: Cheeseburger
```

```lua
--[[
For our first full program, lets create a function that increases an input variable by 3 only if the input is less than or equal to 10. If the input fails the first check and is not specifically 17, it is increased by 1. If it fails both checks, increase the number by 20. After everything, return the output.
--]]

-- "function" tells the interpreter that the following is a function, "increaseNumber()" is the name of our function, and v is the input variable.
function increaseNumber(v)

    -- This is the standard conditional. If a value is greater than, less than, exactly, or not exactly than another value, do a thing.
    if v <= 10 then 
        v = v + 3

    -- To have another check after one fails, you can do an "elseif" statement. It will not check if the first conditional succeeds.
    elseif v ~= 17 then
        v = v + 1

    -- If you do not have a condition to check for, you can just type "else".
    else
        v = v + 20

    -- To tell the interpreter that the section has ended, you must include an "end".
    end

    -- This returns the value and exits the function. You are done.
    return v
end

-- You can call functions from another statement, which will feed the return value like any other variable.
print(increaseNumber(2))
-- Prints: 5

-- We told the interpreter that things should be increased by 3 if it's *at most* 10. 10 is at most 10, so it gets increased by 3.
print(increaseNumber(10))
-- Prints: 13

print(increaseNumber(42))
-- Prints: 43

print(increaseNumber(17))
-- Prints: 37

-- You can also call the function when setting a variable.
x = increaseNumber(6)
print(x)
-- Prints: 9

-- You can also call the function standalone, but the function above isn't built for it.
increaseNumber(13)
```

That's it for the basics! I hope you learned something useful from that.

###### Big thanks to GrandpaScout for noticing some flaws and then immediately going to #general. Very helpful, next time please DM me.
{: .no_toc }