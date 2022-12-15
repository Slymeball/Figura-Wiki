> **Prerequisites**
> 
> Before starting with this tutorial, please make sure you...
>
> - Know [the basics of scripting](https://github.com/Slymeball/figura-wiki/wiki/The-Basics-of-Scripting)

If you want to do something somewhat cool with your avatar, customizing your nameplates may be the way to go. Your nameplates include the name shown above your head, in the tablist, and in chat.

## Setting Text

The first thing to do with nameplates is changing the contents of them. To do so, make a new script and call it whatever you want. Open this script in your text editor of choice and type the following:

```lua
nameplate.ALL:setText("Hello, nameplate!")
```

In this example, `nameplate` is the API, `ALL` is which nameplate to change (see below for more information), and `setText` tells the interpreter to set the contents of the nameplate(s) specified to the string inside the parentheses.

Checking back in game, you'll notice your nameplate has changed to the string you placed into the parentheses. When you chat, your name will be replaced with your custom nameplate. Looking in the tablist yields the same results.

## Styling Your Nameplate

Lets say that you grew tired of being the same nameplate color as everyone else. You want more style in your name, maybe making it red or purple and bold. Figura allows you to do this through Minecraft's own raw text system. Through this, JSON elements allow you to style text, giving your name more pizazz.

Back to your script, lets change the string now. First of all, clear the content inside of the parentheses and replace it with `''`. Raw text heavily uses quotation marks, so it is suggested to use apostrophes to round off the entire string instead. Your code should look something like this...

```lua
nameplate.ALL:setText('')
```

Now, put a pair of braces inside of the string and fill them in with `"text":"Hello, nameplate!"` Your code should look something like this...

```lua
nameplate.ALL:setText('{"text":"Hello, nameplate!"}')
```

Saving now, you'll notice that your nameplate is the same as last time, but now represented with raw text instead of a basic string.

Now, we'll add some color to it. At the end of the text value, add an optional space, a comma, and `"color":"red"`. The comma separates the two tags and the `color` tag specifies what color should the text be displayed as. Your code should look something like...

```lua
nameplate.ALL:setText('{"text":"Hello, nameplate!", "color":"red"}')
```

Minecraft has default support for sixteen colors, a list can be found on [the Minecraft Wiki](https://minecraft.fandom.com/wiki/Formatting_codes#Color_codes). Along with those, a hexadecimal color can be used, following the format `"color":"#123456"`.

For the last bit, text formatting. Minecraft supports **`bold`**, *`italic`*, <ins>`underline`</ins>, ~~`strikethrough`~~, and `obfuscated` (randomizes what character is displayed each frame).

Now, lets change our nameplate's style one last time to make it [a specific shade of purple](https://colorpicker.me/#a131da "#a131da") and bold. First, we start with our text, which should still be "Hello, nameplate!" In raw text, this should look like...

```json
{"text":"Hello, nameplate!"}
```

Now, we add the color to our nameplate. After doing so, the JSON object should look like...

```json
{"text":"Hello, nameplate!", "color":"#a131da"}
```

Finally, the bolding. To make a text segment bold, just add the tag `bold` as `true` (which can be optionally wrapped in quotation marks). Once done, the object should look like...

```json
{"text":"Hello, nameplate!", "color":"#a131da", "bold":true}
```

Finally, we should put this back into our script, making the final product look like...

```lua
nameplate.ALL:setText('{"text":"Hello, nameplate!", "color":"#a131da", "bold":true}')
```

## Separate Nameplates

To change the nameplates individually, we must change the script's structure. Instead of commiting our nameplate changing in one action, we must separate it into three.

The three types of nameplate all have their own spot in the nameplate API. Find them as listed below.

- `ENTITY` - The nameplate above a player's head.
- `LIST` - The name shown within the tablist.
- `CHAT` - The name shown in chat messages, including all mentions of the player.

These take the place of the `ALL` in the above code and funcionally work the same (except for a few extra functions in `ENTITY`'s category, see more below.)

Check the following example for how to use each category.

```lua
nameplate.ENTITY:setText("Entity Nameplate") -- This nameplate shows above the player.
nameplate.LIST:setText("Tablist Nameplate") -- This nameplate shows in the tablist.
nameplate.CHAT:setText("Chat Nameplate") -- This nameplate shows in chat.
```

Raw text works the same in here as well, so you can use the raw text you created above with these individual nameplates.

## Modifying the Entity Nameplate

Figura also allows you to modify the physical attributes of the entity's nameplate, including but not limited to the position, scale, and visibility of it. 

### `nameplate.ENTITY:setPos(vec3)`

`setPos` moves the nameplate relative to the default position based on the vector supplied. A table is provided below for examples.

| `vec(1, 0, 0)` | `vec(0, 1, 0)` | `vec(0, 0, 1)` |
| --- | --- | --- |
| ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setPos-1-0-0.png?raw=true) | ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setPos-0-1-0.png?raw=true) | ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setPos-0-0-1.png?raw=true)

### `nameplate.ENTITY:setScale(vec3)`

`setScale` changes the size of the nameplate multiplied by the default scale based on the vector supplied. A table is provided below for examples.

| `vec(2, 1, 1)` | `vec(1, 2, 1)` | `vec(1, 1, 2)` |
| --- | --- | --- |
| ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setScale-2-1-1.png?raw=true) | ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setScale-1-2-1.png?raw=true) | ![](https://github.com/Slymeball/Figura-Wiki/blob/main/images/nameplate/setScale-1-1-2.png?raw=true)

### `nameplate.ENTITY.visible` (Editable, `bool`)

`visible` determines whether a nameplate should be rendered. This variable should be set like one would a normal variable.

### `nameplate.ENTITY.setBackgroundColor(vec3/vec4)`

`setBackgroundColor` changes the color of the background behind the text based on the vector supplied. The vector represents an RGB value, with an optional alpha value at the end.

### `nameplate.ENTITY.shadow` (Editable, `bool`)

`shadow` determines whether a nameplate should render a shadow behind the text. `shadow` is incompatible with `outline`. This variable should be set like one would a normal variable.

### `nameplate.ENTITY.outline` (Editable, `bool`)

`outline` determines whether a nameplate should render an outline surrounding the text, much like a glowing sign would. `outline` is incompatible with `shadow`. This variable should be set like one would a normal variable.