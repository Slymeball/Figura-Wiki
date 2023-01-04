---
layout: default
title: Nameplate
parent: Scripting APIs
---

# Nameplate
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Targeters

### `nameplate.ENTITY`

The nameplate typically above the player's head. Supports newlines.

### `nameplate.LIST`

The nameplate shown in the tablist.

### `nameplate.CHAT`

The nameplate shown in chat messages and mentions.

### `nameplate.ALL`

Every nameplate shown above.

## Common Calls

### `:setText(string)`

Sets the text of the nameplate selected. JSON text can be used here, and so can newlines in `ENTITY` nameplates. Newlines added in `LIST` and `CHAT` will be replaced with spaces. When the argument is `nil`, the selected nameplate will be reverted to the server's default.

### `:getText()`

Gets the current text of the selected nameplate. Returns a string if set and `nil` if not.

Returns string or `nil`.

## `ENTITY` Calls

### `:setPos(vec3)`

Sets the position of the `ENTITY` nameplate. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Alternatively, you can use `(number, number, number)` as an XYZ pair.

### `:getPos()`

Returns the current position of the `ENTITY` nameplate as a `vec3` or `nil` if not set. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Returns vec3 or `nil`

### `:setScale(vec3)`

Sets the scale of the `ENTITY` nameplate. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Alternatively, you can use `(number, number, number)` as an XYZ pair.

### `:getScle()`

Returns the current scale of the `ENTITY` nameplate as a `vec3` or `nil` if not set. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Returns vec3 or `nil`

### `:setBackgroundColor(vec3/vec4)`

Sets the background color and opacity of the `ENTITY` nameplate. If ran from any other nameplate, your script will error with "attempt to call a nil value."

There are many other ways to represent a BG color, including...
- `(vec3)` - {R, G, B}
- `(vec3, number)` - {R, G, B}, a
- `(number, number, number)` - R, G, B
- `(number, number, number, number)` - R, G, B, a

### `:setVisible(bool)`

Returns the visibility of the `ENTITY` nameplate. Instead of passing a variable through parentheses, this must be set like a variable. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Returns boolean.

### `:setOutline(bool)`

Returns the visibility of an outline surrounding the text of the `ENTITY` nameplate. Instead of passing a variable through parentheses, this must be set like a variable. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Returns boolean.

### `:setShadow(bool)`

Returns the visibility of a shadow behind the text of the `ENTITY` nameplate. Instead of passing a variable through parentheses, this must be set like a variable. If ran from any other nameplate, your script will error with "attempt to call a nil value."

Returns boolean.