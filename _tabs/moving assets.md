---
icon: fas fa-stream
order: 4
---

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
