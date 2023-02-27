---
icon: fas fa-stream
order: 2
---
This page will include the basics for modifying your 3ds's home menu. From the sleep screen to animations, we will be taking a look at the ideas behind most of the documentated modifications for your home menu and how to perform them.



Skip to any section you would like to learn how to do. There is no particular order from this point on.

---

# Sleep Screen

This section teaches you about modifying the sleep screen.

### You will need
[MSBT Editor](https://github.com/IcySon55/3DLandMSBTeditor/releases){:target="_blank"}\
[Color Documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=461605719&range=A1){:target="_blank"} `sleep_LZ.bin (moderated)` tab.\
A hex editor such as [HxD](https://mh-nexus.de/en/downloads.php?product=HxD20){:target="_blank"}

#### Changing Text
1. Extract and open MsbtEditor.exe
2. Select `File >> Open` and navigate to your HMRT folder from [Start](/start#preparing-your-home-menu-for-modifications).
3. Navigate to `ExtractedRomFS/message`.
4. Enter the `<region_language>` folder, region being the region of your console, and language being the language selected on the console.
5. Open menu_msbt.lz.
6. Locate all the sections containing text related to the sleep menu.
    - lau_b_shutdown
    - lau_press_pow_u0
    - lau_press_pow_u1
    - lau_press_pow0
    - lau_press_pow1
    - lau_press_pow2
    - lau_press_pow3
    - lau_press_pow4
    - lau_press_pow5
    - lau_press_pow5_flw
7. Edit any text you would like. For newlines, copy the weird looking character and paste it wherever you would like to go to the next line.
8. When finished with your edits, click save.

#### Changing Colors
1. Navigate to your HMRT folder from [Start](/start#preparing-your-home-menu-for-modifications).
2. Navigate to `ExtractedRomFS`.
3. Open `sleep.lz` in HxD, or your prefered hex editor.
4. Open the [color documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=461605719&range=A1){:target="_blank"} and find the asset you would like to recolor.
5. Hit Ctrl + G.
6. Copy and paste the offset from the `Offsets (hexidecimal)` column.
7. Locate the value from the `Color (hex)` column.
8. Replace it with whatever color you like.
9. When finished editing, save the file.

---

# Animations

This secton goes over the basics of changing animations. They are a bit complicated. We will be using the example of a spinning cursor (Thanks sven64!).

### You will need
[Switch toolbox](https://github.com/KillzXGaming/Switch-Toolbox){:target="_blank"}\
[Kuriimu2](https://github.com/FanTranslatorsInternational/Kuriimu2){:target="_blank"}

### Spinning Cursor
1. Extract and launch Kuriimu2.exe.
2. Install the .Net 3 framework if it asks you to.
3. Select `File >> Open`.
4. Navigate to your HMRT folder from [Start](/start#preparing-your-home-menu-for-modifications).
5. Navigate to `ExtractedRomFS`
6. Open `launcher.lz`.
7. Select the `anim` section. This is where all the animations for your home menu are stored.
	- In this example we will be using the file that contains the cursor animation loop.
8. Locate and right click LncCsr_00_Loop.bclan
9. Select Extract.
10. Save the file in a place you can find easily.
11. Extract and open Toolbox.exe from Toolbox-Latest.zip
12. Select `File >> Open`
13. Locate your extracted `LncCsr_00_Loop.bclan` and open it.
14. It will now open in a switch toolbox subwindow. Open the file inside switch toolbox.
15. Open the `Animation Info` section.
	- This is where animaion data is stored.
16. Expand and right click `W_CsrLgt_00` and hit "Add Animation Group".
	- `W_CsrLgt_00` is the main cursor color (needs fact checking)
17. Hit Ok.
18. Right click your new animation group and hit "Add Target" to add an animation.
19. From the dropdown select "Rotate Z" to add a rotation animation on the Z axis.
20. Right click your new animation, and hit "Add Keyframe" two times.
	- This is the start and end of the animation.
21. Select your first keyframe (Key Frame 0) and change the slope value to 3.
	- This might be the interpolation type (fact checking needed)
22. Select your second keyframe (Key Frame 1) and change the slope value to 3. 
23. Change the Frame value to 60, this will make the animation loop every 60 frames.
24. Change Value to 180. 
	- Because we have a `RotateZ` animation, this will rotate it 180 degrees every time the animation loops.
25. Right click `Animation Info` on the left pane and hit "Add Animaton Group"
	- This adds a new group of animations.
26. Name it `W_CsrF_00` and hit Ok.
	- This will animate the drop shadow (fact checking needed).
27. Right click it and hit "Add Animation Group".
28. Change the target to "Rotate Z" then hit Ok.
29. Repeat steps 18-24.
30. Close the window you have been working in. The left pane will start with `- LncCsr_00_Loop.bclan`.
31. Click the floppy disk save button in the top left and hit Ok.
32. Return to your Kuriimu2 window.
33. Right click `LncCsr_00_Loop.bclan` and hit "Replace".
34. Open the `LncCsr_00_Loop.bclan` you just edited.
35. Click the floppy disk save button in the top left.
36. Try out your animation on your console!

---

# Moving Assets
In this secton we will look at how to move assets.

### What you will need
A hex editor such as [HxD](https://mh-nexus.de/en/downloads.php?product=HxD20){:target="_blank"}\
[Asset Documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=1696778699&range=A1){:target="_blank"}

### Moving wifi, play coins, and other assets.
1. Navigate to your HMRT folder from [Start](/start#preparing-your-home-menu-for-modifications)
2. Open hud.LZ in HxD or another hex editor.
3. Locate the name of the asset you want to move in the [asset documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=1696778699&range=A1){:target="_blank"} under the `Name` column.
4. In HxD, press ctrl + F.
5. Select the "Text-String" tab.
6. Copy in the name of the asset you are moving and hit OK.
7. Move 24 spaces to the right to get to the position values.
8. After moving 24 spaces you are on the X position. The next four colums define that.
9. Just past the X position is the Y position. The next four columns define the Y position.
10. After making your changes, save the file.

---