---
icon: fas fa-stream
order: 3
---

This secton goes over the basics of changing animations. They are a bit complicated. We will be using the example of a spinning cursor (Thanks sven64!).

# You will need
[Switch toolbox](https://github.com/KillzXGaming/Switch-Toolbox){:target="_blank"}\
[Kuriimu2](https://github.com/FanTranslatorsInternational/Kuriimu2){:target="_blank"}

# Spinning Cursor
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
36. Try out your animation on your console by using steps 4-5 in [Start](/start#layeredfs)!
