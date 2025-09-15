---
layout  : wiki
title   : SFMB - How to use the MapEditor ThemeSettings
summary : 
date    : 2021-03-02 23:44:35 +0900
updated : 2025-09-15 20:00:00 +0100
tag     : sfmb
toc     : true
public  : true
comment : true
parent  : [[sfmb_tutorial]]
latex   : false
---
* TOC
{:toc}

# Summary

- This wiki explains how you can create and configure game themes using the ThemeSettings editor found in the MapEditor.
- You can manage things such as:
  - Animated parallax auto-scrolling background layers
  - Custom sky colors
  - Background objects
  - Override which resources specific themes should use
- This wiki doesn't cover everything, but you can easily figure the rest out by yourself. I hope this helps!

# Enter `Theme definitions`

2. Click the `Manage GameThemes` button on the `home` tab of the Map Editor.
   - <img width="814" height="113" alt="image" src="https://github.com/user-attachments/assets/3299c0ff-107c-43d1-bf7e-7a820ea7a60a" />
3. Select a theme you want (and are able) to edit.
   - To modify an existing theme, clone it and name it something like `{GameTheme}_fix`.
   - To make a new custom theme, clone a theme you want it to be based on and name it as you wish.
   - You can read a bit more about creating themes in this tutorial: [[sfmb_how_to_make_game_theme]]{How to make a game theme}.
4. If it's not already, set the `Theme Version` to `2`!
   - <img width="632" height="86" alt="image" src="https://github.com/user-attachments/assets/5ff871a4-ce17-48c1-96b6-2e68d5f1d876" />
5. Click the `Edit ThemeDefinitions` button at the bottom of the window.

# Themes

- On the `Theme` tab you can see all the themes that your GameTheme clone contains.
- You can add and remove as many of them as you want.
- If the name of your background music file doesn't match the name of your theme, you can define which file it should play by entering the name of that file here.
- By changing the `Environment` you can set the following:
  - `Plain`				-> Nothing special, default.
  - `UnderWater`		-> Makes the entire theme swimmable.
  - `Airship`			-> The camera and liquid layers move up and down.
  - `Castle with lava` 	-> Adds a lava liquid layer by default.
- You can also override which themed resource the theme should use by filling in the values under `Sprite Inheritance`.
  - For example, when both your Underground and Space themes should use the `MapObjectUnderground` spritesheet, you can set the `MapObjectSprite` of the Space theme to Underground.
    - You can leave it empty for Underground. If the name of a theme matches the name of a themed resource (theme name: `Mars`, resource name: `MapObjectMars`) it will use that by default.
      - <img width="831" height="365" alt="image" src="https://github.com/user-attachments/assets/6dd07c65-1366-4638-815d-5e957e7579e2" />
- We will get back to the other options here later.

# Background layers

1. Make sure the background layer resources are created and configured correctly (`.png` & `.sprite` files).
   - If not, check this detailed tutorial: [[sfmb_tutorial_sprites]]{How to work with sprites}
2. Click `Background Layer`.
   - <img width="158" height="166" alt="image" src="https://github.com/user-attachments/assets/a929b168-a5d4-4750-9d97-63bec30c846d" />
3. To add a layer resource, click `Add`, then enter the name of the layer file without the word "Layer". -e.g.- `OverworldClouds`.
4. Set the `FixedTo` field as follows:
   - `Bottom`			-> Things you want to appear on the ground or only once vertically (e.g. hills, towers, city, water).
   - `Bottom + Repeat`	-> Things in the sky or vertically repeating backgrounds (e.g. clouds, underground).
   - `Top & Bottom`	-> Don't use if possible.
5. Adjust the `ScrollRatio` to make the layers feel further away or closer to the camera.
   - Most games use two layers for parallax scrolling: one at 0.25 `ScrollRatio` and the other at 0.5 `ScrollRatio`.
   - There is an option to make the scroll ratio different on the x and y axes, but this can cause very unnatural visuals and should only be used in very specific cases.
     - <img width="684" height="549" alt="image" src="https://github.com/user-attachments/assets/57d60fbd-ee6d-41d8-96e6-b6ef54eed11a" />
6. Test it to see if it feels and looks good.
7. If you need, set the `AutoScroll` values to make the background layer scroll by itself. **Make sure the parallax scrolling feels and looks right before setting up the autoscroll!**
8. To use these, you have to enter the added names to a theme, in order, separated by commas without spaces (e.g. `OverworldHills,OverworldClouds`). Layers cover each other from front to back.
   - <img width="1046" height="221" alt="image" src="https://github.com/user-attachments/assets/a56edc10-0d87-45b9-8138-03ea8d988fda" />

# Background colors

Here you can create named background colors.
1. Add and name a background color (e.g. `Sky`).
2. Set its color.
	- <img width="766" height="590" alt="image" src="https://github.com/user-attachments/assets/aa543475-79fa-41dd-bb53-1fc513460c34" />
4. Go back to the `Theme` tab, select a theme, and enter the name of the `Background Color` in the `BgColor` field.
	- <img width="358" height="102" alt="image" src="https://github.com/user-attachments/assets/3127d47d-4cbb-464c-9d26-57ce836e0b79" />
You should ignore the `Color of {something}` fields on the main ThemeSettings window.
- <img width="883" height="202" alt="image" src="https://github.com/user-attachments/assets/89836205-14ae-4bbf-af3e-94a6addd8122" />

# Fin.

1. These are still just the basics, there are still plenty of options in `ThemeSettings`.
2. If something is not clear, DM me, the author (marci599), and if I'm available I’ll try to help.
