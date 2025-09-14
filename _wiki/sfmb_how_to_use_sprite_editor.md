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

# What is SpriteEditor, how to download & how it works.

## What is SpriteEditor
Néhányan úgy gondolják, hogy az MM SpriteEditor egy sprite készítő program, mint mondjuk az Aseprite, azonban ez nem így van. Az MM SpriteEditor lényege, hogy a kompatibilis sprite sheet-eket (pl. Item.png) és sprite-okat (pl. LayerOverworld.png) bekonfigurálhassuk. Ezek a konfigurációk a sprite sheet nevével megegyező .sprite fájlba kerülnek mentésre (pl. Item.sprite). De mit jelent hogy bekonfigurálhassuk? kérdezheted.
- <img width="500" alt="image" src="https://github.com/user-attachments/assets/328752f2-dab0-4576-9c4a-fa539688960d" />
- <img width="500" alt="image" src="https://github.com/user-attachments/assets/0ca6aaef-a367-4a72-8ac8-dadc3c12e691" />

Egy sprite sheet több sprite-ból áll. Ezek a sprite-ok a sprite sheet-en különböző helyen helyezkedhetnek el, különböző méretekben. A sprite editor elsődleges célja ezeket beállítani.
Ezen kívűl itt tudod beállítani, hogy:
- a játék a subject eredeti origójához képest mennyire legyen eltolva az x y kordinátán,
- a játékosoknak hol helyezkedjen el sprite frame-enként a helmet-ük (Buzzy, Spiny, Pumpkin and Santa) és hogy milyen irányba és szögbe álljanak,
- hol helyezkedjen el a propellerük és hogy azok a játékos előtt, mögött vagy sehol se látszódjanak,
- és az ellenségeknek hol helyezkedjen el a szárnyuk / szárnyaik.

Van olyan is, amikor egy kép nem sprite sheet-et tartalmaz, hanem csak egy sprite-ot, mint modjuk az animálatlan hátterek (pl SMB LayerOverworld.png).

És természetesen vannak kivételek is, amikor egy sprite sheet-hez / sprite-hoz nem lehet .sprite file-t készíteni, nem lehet konfigurálni, mivel a játék kódjában van bekonfigurálva (pl. TileOverworld)

## Download & Setup
- Where:
	- For beta testers: pinned messages in the `#resource-sprite` text channel.
	- For DEMO users: pinned in the `#demo-game-themes` forum channel.
- How
	- Download the latest version.
	- Move it into your `Mario Multiverse` folder next to `Mario.exe`.
	- Open it there.
 	- Make sure to check for updates on the Options etc. tab.
  		- <img width="755" height="139" alt="image" src="https://github.com/user-attachments/assets/318f8bf7-61f0-4d72-975e-205e41bc0927" />
	- Open a `.sprite` file.
		- You can use the open button inside the SpriteEditor program
  			- <img width="376" height="138" alt="image" src="https://github.com/user-attachments/assets/c4ceff03-9cd6-4d79-96c4-be5b391aaa4f" />
		- or you can associate the `.sprite` files with SpriteEditor and open the `.sprite` file directly.
  			1. <img width="670" height="232" alt="image" src="https://github.com/user-attachments/assets/9e5bf572-143a-4a2c-83d2-b85064b0c123" />
	 		2. <img width="446" height="621" alt="image" src="https://github.com/user-attachments/assets/80a06ea0-5968-45cc-b674-11d22bee628a" />
			3. <img width="1028" height="378" alt="image" src="https://github.com/user-attachments/assets/98e02d1d-02e4-4483-9b14-931fe2b1b2b2" />
   		- You can also click on the program icon and open recently opened sprites.
     - It's also possible to create a .sprite file from a png with the `new` button, but sometimes it's easier to just copy paste an existing one.

 
- Setup layout: You can rearrange the windows by grabbing the top of the window border and start dragging. 
	- In this case, small arrow icons will appear, if you drag one into it, it will attach the window to the edge of another.
- ![gif1](https://user-images.githubusercontent.com/40640441/122874734-9e720f00-d333-11eb-991e-88491c2b0a44.gif)

## Panes
There are several docking-panes (windows) in SpriteEditor. 

### Preview pane
- Here you can see the animations and sprites with the set offset.
- The intersection of the two lines is the origin of the current subject.
	- <img width="355" height="403" alt="image" src="https://github.com/user-attachments/assets/7b282998-2d05-447d-bf1e-0db48674501f" />

### Properties pane
- This is where the properties of `Sprite frames` or `Animations` appear if you click on them.

### Sprite frames pane
- If you click on one of them, it will appear in the `Preview` window with the set offset and its properties will appear in the `Properties` window. 
- Here you can set the area where the sprite is, but this happens automatically when you `double click` on it.
	- ![gif2](https://user-images.githubusercontent.com/40640441/122875522-aaaa9c00-d334-11eb-9995-283d946766fb.gif)
- You can also set the offset here, but this is easier with the small arrow icons in the Home tab. With the offset you can shift the sprite from the center of the origin on the x and y coordinates.
	- ![gif3](https://user-images.githubusercontent.com/40640441/122875978-3de3d180-d335-11eb-82b1-6342ad9ae62f.gif)
#### Common origins
- Center Bottom:
	- Players
	- Enemies
 	- Background Objects
	- Items.
 	- So most things that can interact with the ground 
- Left Top (x:0; y:0):
	- Background Layers
	- Fonts
 	- Most UI related resources
 
### Animations pane
- If you click on one
	- the animation with the set offset will appear in the `Preview` pane.
	- and its properties will appear in the `Properties` pane. 
		- There you can set which frame to start from (`FirstFrame`) 
		- How many of the upcoming sprite frames it should use. (`FrameCount`). 
		- The delay between frames (-1 means to use the default) (`Delay`).
  		- And if it should loop or play once (`LoopType`)
- You can also create your own animation but name of animations are defined in game.
	- Some by the ThemeSettings
 		- Eg. Background Objects, Background Layers
	- And some by internal game code 
		- Eg. Players, Enemies
- Sometimes you only create an "animation" to reference it from the ThemeSettings editor. That means you don't create a real animation with frames, you basically just name a sprite to reference it later.
	- Eg. Background Objects or SMB World Flags.
- And lastly some spritesheets don't support `aniamtions` at all. Those use predefined sprite frames indexes for specific sprites.
	- For example in the `Helmet.sprite` file the `sprite frame` with the index 7 is always the frint facing spiny helmet sprite no metter what.
 	- You can read the full list in this page: [[sfmb_sprite_index]]{Sprite indexes}
 
## Player sprites
- For all the possible animations, you can check already existing player `.sprite` files.
- When working with player sprites you not only need to create and configure each `Sprite frame` and `Animation`, but also the helmet and propeller offsets. But before you do that, make sure that the `Helmet` resource (`.png` & `.spirte` files) is already created and configured.
### Helmets
- Select a `Sprite frame` on the `Sprite frames` pane and click on the `Helmet` item. This displays the helmet sprite in the `Preview` pane.
	- <img width="365" height="109" alt="image" src="https://github.com/user-attachments/assets/bc0d255c-f6d7-4669-848e-9ec7af0e2ea6" />
 	- <img width="219" height="398" alt="image" src="https://github.com/user-attachments/assets/e55a72f9-b8dd-4ea8-b39f-5fbc521abdd6" />
	- You can change which helmet to display by changing the selected item in the `Helmet preview`.
 		- <img width="164" height="88" alt="image" src="https://github.com/user-attachments/assets/a987aa88-67a7-4159-84b6-a35cfed83819" />
- To change the offset of the helmet you need to use the same arrow icons on the `Home` tab that you use for changing the offset of the `Sprite frames`.
- You also need to define what direction the player is looking if its head is visible by selecting an item in the `Face direction for Helmet`, so that the correctly orientated helmet can be displayed.
	- <img width="225" height="90" alt="image" src="https://github.com/user-attachments/assets/406bc0e0-5885-4f5b-b421-65998ffc698a" />
- It's also possible to change the angle of the helmet by changing the `FaceAngle` field in the `Properites` pane.
	- Eg. when the player is looking up or is ground pounding.
		- <img width="219" height="361" alt="image" src="https://github.com/user-attachments/assets/858c1490-b047-400b-a267-ea7d2955a57b" />

### Propeller
You only need to set it when configuring players with the propeller powerup.
- Click the `propeller` item in order to display it in the `Preview` pane.
- It's basically the same thing as the helmets, but without face directions.
- You can change its Z order (behind or in front of player sprite) or hide it competely for specific situations.
	- <img width="138" height="88" alt="image" src="https://github.com/user-attachments/assets/570e226a-1103-4b83-8f39-40264c6c8a07" />


## Enemies
// TODO

## Hotkeys
- CTRL + MouseWheel: Zoom
- W, A, D, X key: Move offset

## Fin.
That’s not all, but other things might be easier to figure out if you try things you don’t know, because that’s one of the best way to learn.
If something is still not clear, DM me, the author (**Marci599**) on discord and I will try to help.

