---
icon: fas fa-stream
order: 5
---

This section teaches you how to change asset colors.

#What you will need
A hex editor such as [HxD](https://mh-nexus.de/en/downloads.php?product=HxD20){:target="_blank"}\
The [launcher_LZ.bin](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=1943849394&range=A1:A2){:target="_blank"} and [hud_LZ.bin](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=1696778699&range=A1){:target="_blank"} tabs of the HOME Menu Asset Documentation

# Changing Colors
1. Locate the name of the asset you want to change. Your asset may be on one of several different pages.
2. Once you have located what you would like to change, open the file with the name of the spreadsheet tab in HxD.
	- the launcher_LZ.bin tab would be the launcher.lz file.
3. Look over to the "Offsets (hexidecimal)" column.
4. Copy the offset in the row of the asset you would like to recolor.
5. In HxD, press ctrl + G to open the "Go to" prompt. Paste in the offset of your asset and remove the `0x` from it.
6. Press Ok.
7. In the spreadsheet again, look at the "Color (hexidecimal)" column.
8. locate the color of your asset.
9. In HxD, find the value that was in the "Color (hexidecimal)" tab of the spredsheet.
	- If you can't find the color use the second color value
10. Find the hexidecimal value of the color you would like to change it to.
	- There are several online resources to do this for you.
11. Replace the old color value with your new one.
	- For example, if the old color was `46 46 46` (green), you would replace it with for say, `89 CF F0` (blue).
12. Hit ctrl + S or go to File >> Save to save the file.
13. Test your changes by using steps 4-5 in [Start](/start#layeredfs)!