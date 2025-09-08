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
updated : 2025-09-01 01:44:00 +0900
---
* TOC
{:toc}

# How to make a Game Theme

## Cloning the Default Theme (SMB)
- In the map editor, click the Manage GameThemes menu.
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
- [[sfmb_how_to_make_parallax_background]]{How to make backgrounds}

## Editing Sprite Files
- In this game, sprites consist of .sprite files and .png files.
- To edit a .sprite file, you need the SpriteEditor tool.
- [[sfmb_how_to_use_sprite_editor]]{How to use SpriteEditor}

## Editing Music Files
- BGM in this game consists of .ogg files and .bgm files.
- A .bgm file stores loop section information for the corresponding .ogg file, and it can be created using the TestSoundLoop.exe program.

## Editing Sound Effect Files
- If your theme uses the same sound effects as SMB, you can remove them.
