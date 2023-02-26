---
layout: categories
icon: fas fa-stream
order: 1
---
This page will include the basics for modifying your 3ds's home menu. From the sleep screen to animations, we will be taking a look at the ideas behind most of the documentated modifications for your home menu and how to perform them.


# Prep Work
## Requirements
- A windows or Linux pc (maybe Mac too). 
- A modded 3ds running Luma3ds. 
- An internet connection (just for downloading tools). 
- An SD card or Micro SD card, depending on the model of your console.
- An SD card adapter for your computer. 



## Obtaining Your Home Menu
1. Boot into godmode9. This will be holding start on boot for most users. 
2. Navigate to CTR Nand/title/00040030/
3. Select the tidlow for your region:
    - EUR: `00009802`
    - JPN: `00008202`
    - KOR: `0000A902`
    - USA: `00008F02`
4. Navigate to content/
5. Select 0000000*.tmd (\* being a number) and hit "TMD file options..."
6. Select "Build CIA (standard)
7. Turn off the console, and insert the sdcard into the computer.
8. Make a copy of your home menu CIA in sd:/gm9/out and store it somewhere safe.



## Preparing Your Home Menu for Modifications.

### Downloads
    - [HMRT](https://github.com/schrmh/HMRT)
    
###Steps    
1. Download and extract HMRT. 
2. Make a copy of your home menu and name it `HomeMenu.cia`
3. Open the HMRT script for your OS (bat is windows, sh is Linux and Mac) 
    - The windows version of HMRT can have some issues. If you run in to any just use the Linux sh script in Wsl. 
4. Select the option for Full Rebuild. 




# The Fun Part! 
Skip to any section you would like to learn how to do. There is no particular order from this point on.
