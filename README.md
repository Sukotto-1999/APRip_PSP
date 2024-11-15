# APrip_PSP
**Description:** This is a series of patches that can be applied for certain PSP games, to make it playable on CFW or Adrenaline emulator. The project is inspired by APrip by Alex Free.

These patches are in .xdelta format which can be applied via DeltaPatcher. We've included some screenshots of the effects that happen in a side folder.

## Supported Games
DJ Max Portable Clazziquai Edition (KOR) (ULKS-46190)  
Fantasy Golf Pangya Portable (K0R) (ULKS-46164)  
Fantasy Golf Pangya Portable (JAP) (ULJM-05440)  
Pangya Fantasy Golf (US) (ULUS-10438)  
DJ Max Portable Black Square (KOR) (ULKS-46189)  
DJ Max Portable Black Square (JAP) (ULJM-06034)  
DJ Max Fever (US) (ULUS-10403)  
The Idolm@ster SP Perfect Sun (JAP) (ULJS-00167)  
The Idolm@ster SP Wondering Star (JAP) (ULJS-00168)  
The Idolm@ster SP Missing Moon (JAP) (ULJS-00169)  
Soul Calibur: Broken Destiny (EUR) (ULES-01298) (see workarounds for US and JAP versions)  
DJ Max Portable Hot Tunes (KOR) (ULKS-46240) (original and 1.10)  
DJ Max Portable 3 (KOR) (ULKS-46236) (original and 1.02)  
DJ Max Portable 3 (US) (ULUS-10538) (original and 1.01)  
DJ Max Portable 3 (JAP) (ULJM-05836)  

## Failed check, causes and effects

**Various DJMax Games**
After playing the game for a few minutes, the anti-piracy will; Add distortion to the background music before exceeding the pitch over time, randomize the playback speed of the keysounds and SFX audio, and/or flicker the graphics list to randomly skip drawing textures causing the screen to flash rapidly. After attempting to change the song one or two times, It will lock up the game. This is completely seizure inducing.

The full videos of the effects that happen in the DJMax games can be found here:
https://youtu.be/f9JciTN5FNc
https://youtu.be/Q09HtRAEhLQ

**Pangya Fantasy Golf**
The game hangs upon startup.

**The Idolm@ster SP**\
The game displays an anti-piracy screen of death if the check fails. If the check fails on startup, after the screen of death appears, it will loop the title screen.

Translation:
Could not detect legitimate system software.
This product can only be guaranteed to work with legitimate system software.

## Read notes for xdelta patches

**DJMax Portable Clazziquai Edition**\
This patch completely removes references to .ISO, .CSO, .DAX or any references especially usbisoloader.pbp. Patch by 2CH.

**DJMax Portable Black Square**\
The anti-piracy code may seem unused in the Japanese version but is present in the decrypted executable and vayay's patch was ported to the Japanese version, but the patch may work.

**DJMax Portable Hot Tunes (original)**\
This patch was ported from the 1.10 patch to the original version, this patch may work for but it has not been tested extensively. Original patch by REVENGE.

**Soul Calibur Broken Destiny (EUR)**\
Only works on CFWs prior to 5.50 GEN-B and is not neccesary for newer CFWs. A CWCheat code to do the same exists but is included in a side note.

**The Idolm@ster SP (JAP, ALL EDITIONS)**\
This patch completely removes the ScePauth protection from the game and is based on version 1.2 dating from March 2009. The original .ppf patches are included in a side folder as well.

## Unsupported Games with workarounds

**DJMax Portable 3 (on startup)**

**Effect:** Game crashes on startup.

**Workaround:**
Use cfwblock.prx. Make sure you enable the Hide CFW folders in the CFW.

**DJMax Portable 2**

**Effect:** Similar to being mentioned above.

**Workaround:**
Use a no-UMD driver.

**Evangelion Jo**

**Effect:** Game displays an anti-piracy screen of death upon startup and won't proceed.

**Workaround:**
Use the following CWCheat code to bypass title screen and quickly start a new game (or it will return to the title screen unless game is restarted) or update your CFW and use cfwblock.prx:



	_C0 SCEPauth Workaround (partial)
	_L 0x20277488 0x24020000
	_L 0x20277490 0x24020000
	_L 0x20277494 0x24020000
	_L 0x20277498 0x24020000

**Ys. vs Sora no Kiseki**

**Effect** 
Collusion detection turns off during battles and the characters clip through and respawn back. The boss battles won't respawn too.

**Workaround**
Use ISO_Tool to Prometheus patch the game using the DIVA2 method, or update your CFW.

**Kingdom Hearts Birth by Sleep**

**Effect:** 
Hangs on a black screen on startup or during one of the last boss battles.

**Workaround**
Use ISO_Tool to auto-patch the game with the KHBBS patch, or update your CFW.

**IDOLM@STER SP (Download Plus)**

**Effect:** See above.

**Workaround:**
Use this CWCheat code or update your CFW:



	_C0 ScePauth Fix
	_L 0x200B7254 0x24040000
	_L 0x200B87E4 0x24040000
	_L 0x2018AA78 0x04400000
	_L 0x2018AA8C 0x24020000
	_L 0x2018AAA0 0x24020000
	_L 0x203C15C8 0x00000000
	_L 0x203C15D0 0x00000000
	_L 0x203C15D4 0x00000000

**Fullmetal Alchemist Brotherhood (JP)**

**Effect:** Game displays an anti-piracy screen of death and won't proceed.

**Workaround:**
Use this CWCheat code or update your CFW:

	_C0 CFW FIX
	_L 0xD016FCBC 0x003003FF
	_L 0x1016FCBC 0x00000000

**Aces of War:**

**Effect:** Game stops loading and hangs if loading a mission or returning back.

**Workaround:**
Convert the game to .cso or .dax and use LME-2.3/PRO, make sure you turn off the ISO cache in the CFW settings.

**Soul Calibur Broken Destiny (US/JAP)**

**Effect:** Game hangs and displays a 4-letter code on the bottom right.

**Workaround:**
Update your CFW.

**Bust-a-Move Deluxe (US/PAL):**

**Effect:** Game crashes after the Majesco logo and sometimes sends the PSP to a complete K.O.

**Workaround:**
Convert the game to .cso and then use LME-2.3/PRO. You can also optionally press the Start button repeatedly to skip the Majesco logo and bypass the crash.

## Final notes
For DJMax Fever, the only difference between the UMD and PSN versions aside from the removal of the copy protection are 2 missions that are impossible to complete (in UMD versions) which is why the PSN version of the game is the only version of DJMax Fever to be supported on PSP RetroAchievements.

The patches for the DJMax games technically does not fix the Album section where it automatically presses the DOWN button on PPSSPP emulator. The album section should seem fine on hardware.
