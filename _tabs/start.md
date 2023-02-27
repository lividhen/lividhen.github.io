---
icon: fas fa-stream
order: 1
---
This page will start you off so you can make modifications to your home menu.

---
# Requirements
- An x86_64 computer running Windows, Linux, or Mac Os (feedback needed for that last one) . 
- A modded 3ds running Luma3ds. 
- An internet connection (just for downloading tools). 
- An SD card or Micro SD card, depending on the model of your console.
- An SD card adapter for your computer OR ftp access on your console. 
  
  
  
# Obtaining Your Home Menu
1. Boot into godmode9. This will be holding start on boot for most users. 
2. Navigate to `CTR Nand/title/00040030/`
3. Select the tidlow for your region:
    - EUR: `00009802`
    - JPN: `00008202`
    - KOR: `0000A902`
    - USA: `00008F02`
4. Navigate to `content/`
5. Select `0000000*.tmd` (\* being a number) and hit "TMD file options..."
6. Select "Build CIA (standard)" 
7. Turn off the console, and insert the sdcard into the computer.
8. Make a copy of your home menu CIA in sd:/gm9/out and store it somewhere safe.
  
  
  
# Preparing Your Home Menu for Modifications

### Downloads
[HMRT](https://github.com/schrmh/HMRT){:target="_blank"}
    
### Steps    
1. Download and extract HMRT. 
2. Make a copy of your home menu and name it `HomeMenu.cia`
3. Open the HMRT script for your OS (bat is windows, sh is Linux and Mac) 
    - The windows version of HMRT can have some issues. If you run in to any just use the Linux sh script in WSL. 
4. Select option `1` to extract your home menu CIA. 
5. Then select option `5` to decompress all the files we will be editing.

Note: HMRT does not work in mac paralells.
  
  
  
# Layeredfs
In this guide we will be using layeredfs, as it is better for faster iterations and is easier to undo if you break something. Files are loaded from the sdcard in place of the ones that are inside the application files, similar to what [Magisk](https://github.com/topjohnwu/Magisk){:target="_blank"} does on Android.

### On 3ds
1. Hold select on boot. 
2. Enable game patching.
3. Hit start to save. 

### Sd card setup
1. Insert your sdcard into your pc.
2. Navigate to `sd:/luma/titles`.
3. Create a folder with the full title id of your home menu region.
	- EUR: `0004003000009802`
	- JPN: `0004003000008202`
	- KOR: `000400300000A902`
	- USA: `0004003000008F02`
4. After making edits, select option `6` in HMRT.
5. Place your edited file on the sdcard in the folder you just created, in the same directory structure it was in the extracted home menu.
	- (eg. `sd:/luma/titles/0004003000008F02/romfs/sleep_LZ.bin`)
