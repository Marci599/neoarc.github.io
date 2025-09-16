---
layout  : wiki
title   : SFMB - How to make a game theme
summary : 
tag     : sfmb
toc     : true
public  : true
comment : true
parent  : [[sfmb_tutorial]]
latex   : false
date    : 2025-09-01 01:44:00 +0900
updated : 2025-09-15 20:00:00 +0100
---
* TOC
{:toc}

# How to make a Game Theme

## Cloning the Default Theme (SMB)
- In the map editor, click the `Manage GameThemes` button on the `home` tab.
- In the left list, select SMB, then click Clone selected theme at the bottom.
- Enter the name of your theme (e.g., SMBPlus).

## Editing Your Cloned Theme
- A theme consists of the following components:
  - Theme settings
  - Sprite files
  - Music files
  - Sound effect files
    
This document briefly explains how to edit each component.

## Editing Theme Settings
- Theme settings can be edited in the Manage ThemeSettings menu.
- Each item shows a short description at the bottom when clicked.
- Try changing different options and see how they affect the game.
- For more details, check this detailed tutorial: [[sfmb_tutorial_theme_settings.md]]{How to use ThemeSettings}

## Editing Sprite Files
- In this game, sprites consist of `.sprite` files and `.png` files.
- To edit a `.sprite` file, you need the SpriteEditor tool.
- For more details, check this detailed tutorial: [[sfmb_tutorial_sprites]]{How to work with sprites}

## Editing Music Files
- BGM in this game consists of .ogg files and .bgm files.
- A .bgm file stores loop section information for the corresponding .ogg file, and it can be created using the TestSoundLoop.exe program.

## Editing Sound Effect Files
- If your theme uses the same sound effects as SMB, you can remove them.
