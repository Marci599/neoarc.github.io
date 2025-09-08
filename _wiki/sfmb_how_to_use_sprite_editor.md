---
layout  : wiki
title   : SFMB - How to use sprite editor
summary : 
tag     : sfmb
toc     : true
public  : true
comment : true
parent  : [[sfmb_tutorial]]
latex   : false
date    : 2021-06-22 01:37:00 +0900 
updated : 2025-09-09 12:37:00 +0100
---
* TOC
{:toc}

# How SpriteEditor works & how to download. 

## Download & Setup
- Where:
	- For beta testers pinned messages in the `#resource-sprite` channel.
 	- For DEMO users pinned in the `#demo-game-themes` channel.
- How
	- Download the latest version.
	- Move it into your `Mario Multiverse` folder next to `Mario.exe`.
	- You can open this here.
 	- Make sure to check for updates on the Options etc. tab.
	- Then use the open button to open the `.sprite` files.
		- Or you can associate the `.sprite` files with SpriteEditor and open the `.sprite` file directly.
- Setup layout: You can rearrange the windows by grabbing the top of the window border and start dragging. 
	- In this case, small arrow icons will appear, if you drag one into it, it will attach the window to the edge of another.
- ![gif1](https://user-images.githubusercontent.com/40640441/122874734-9e720f00-d333-11eb-991e-88491c2b0a44.gif)

## Panes
There are several docking-panes(windows) in SpriteEditor. 

### Preview pane
- Here you can see the animations and sprites with the correct offset.
- The intersection of the two lines is the origin of the current subject.
- <img width="355" height="403" alt="image" src="https://github.com/user-attachments/assets/e1cb0c56-425a-4776-ac10-70a8e1a6423c" />


### Properties pane
- This is where the properties of things appear if you click on it.
 
### Animations pane
- If you click on one, the animation with the correct offset will appear in the `preview` windows.
- You can also create your own animation but name of animations are pre-defined in game program.
	- Eg. `Walk`, `AirSpin`, etc...
- If you click on one of them, its properties will appear in the `properties` window. 
	- There you can set which frame to start from (FirstFrame) 
	- And how many of the upcoming sprite frames it should use. (FrameCount). 
	- Here you can also set the delay between frames (-1 is the default).
- ![image2](https://user-images.githubusercontent.com/40640441/122876146-71266080-d335-11eb-832f-949099e70306.png)
		
### Sprite frames pane
- If you click on one of them, it will appear in the `preview` window with the correct offset and its properties will appear in the properties window. 
- Here you can set the area where the sprite is, but this happens automatically when you `double click` on it.
- ![gif2](https://user-images.githubusercontent.com/40640441/122875522-aaaa9c00-d334-11eb-9995-283d946766fb.gif)
- You can also set the offset here, but this is easier with the small arrow icons in the Home tab. With the offset you can shift the sprite from the center of the origin on the x and y coordinate.
- ![gif3](https://user-images.githubusercontent.com/40640441/122875978-3de3d180-d335-11eb-82b1-6342ad9ae62f.gif)
#### Common origins
- Center Bottom:
	- Players
	- Enemies
 	- Background Objects
	- Items.
 	- So most things that interacts with the ground 
- Left Top (x:0; y:0):
	- Background Layers
	- Fonts
 	- Most UI related resources

## Hotkeys
- CTRL + MouseWheel: Zoom
- W, A, D, X key: Move offset

## Fin.
- That’s not all, but other things might be easier to figure out if you try things you don’t know, because that’s one of the best way to learn.
- If something is still not clear, DM me, the author (**Marci599**) on discord and I will try to help.

