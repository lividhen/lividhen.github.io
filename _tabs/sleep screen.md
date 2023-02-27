---
icon: fas fa-stream
order: 2
---

This section teaches you about modifying the sleep screen.

# You will need
[MSBT Editor](https://github.com/IcySon55/3DLandMSBTeditor/releases){:target="_blank"}\
[Color Documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=461605719&range=A1){:target="_blank"} `sleep_LZ.bin (moderated)` tab.\
A hex editor such as [HxD](https://mh-nexus.de/en/downloads.php?product=HxD20){:target="_blank"}

# Changing Text
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

# Changing Colors
1. Navigate to your HMRT folder from [Start](/start#preparing-your-home-menu-for-modifications).
2. Navigate to `ExtractedRomFS`.
3. Open `sleep.lz` in HxD, or your prefered hex editor.
4. Open the [color documentation](https://docs.google.com/spreadsheets/d/1Q-Im3P5zSqNi6zYqaXtyS138hCdcIJDY7WxRt_FWdrg/edit#gid=461605719&range=A1){:target="_blank"} and find the asset you would like to recolor.
5. Hit Ctrl + G.
6. Copy and paste the offset from the `Offsets (hexidecimal)` column.
7. Locate the value from the `Color (hex)` column.
8. Replace it with whatever color you like.
9. When finished editing, save the file.
