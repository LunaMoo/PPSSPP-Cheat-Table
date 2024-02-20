# Cheat table for PPSSPP
## Updated on 1.16.6-346 (now fully, previous version I forgot about updating conversion script)
 x64 version required for AOB script, through there's an x86 version for 1.2.2 release under the legacy scripts.<br><br>

 This cheat table doesn't include any cheats, it was made to automatize the process of creating simple cheats and calculating addresses for PPSSPP's disassembly to make it easier start for creating more advanced cheats.<br><br>
 
 To use CE with PPSSPP, you have to select MEM_MAPPED under edit->settings->scan settings in CE.

 If you suffer from not able to freeze or change values via cheat engine attached to PPSSPP you might run one of the workaround scripts first, depending on which CE version you're using:
 - Win 10 bug workaround(activate before anything else) avoids "???" on value change
 - (for CE SSE4_AVX2) Win 10 bug workaround(activate before anything else) avoids "???" on value change

 (if you for some reason use renamed CE executable, you might want to edit one of those scripts for your needs)<br><br>


## Quick instructions:
 - use "Attach to PPSSPP" or do it yourself via CE option,
 - make sure to run a game within PPSSPP,
 - use "PPSSPP scripts aob x64",
 - use one of the "Limit Scan Range" settings,
 - search for variables normally,
 - never use CE assembly or any advanced CE functions for PSP games, it doesn't support MIPS arch,
 - if you for whatever weird reason want to look for MIPS code in hexadecimal format through CE search you will have to disable JIT in PPSSPP, this is NOT needed for normal usage,
 - if you find some value you want to create simple cheat from, you can add it to cheat table, rename and while having it selected activate "Select cheat entry and click on the square left from this text to convert address" this will print calculated addresses for PPSSPP disassembly, but also a basic cheat formatted in CWCheat format for you.<br><br>

 
 ## FAQ
 Q: PSP model in PPSSPP affects game's memory limit?<br>
 A: No. It was in the ancient PPSSPP versions, but this was breaking commercial games hence memory limit is only increased via special homebrew flag(MEMSIZE in param.sfo) and hardcoded list of remasters/prototypes.
 
 Q: My value address changes between game runs, cheats are useless?<br>
 A: That's normal in most modern games, learn MIPS and use PPSSPP disassembly to create a cheat which changes the game code that reads or writes that value instead. You could also find pointers, but to do that without knowledge is bothersome and with knowledge you can do better.
 
 Q: Why CWheat patching 0x00000000 adress is patching 0x08800000 in PPSSPP?<br>
 A: That's just CWCheat format choice, 0x08800000 is the start of user memory on PSP.
 
 Q: Why the start of the user memory is always 0?<br>
 A: Games load at an offset of 0x4000, never really wondered about this, but it's same on real hardware, most people me included use it commonly as a code cave to put our own scripts into.
 
 Q: My cheat doesn't work on real hardware while working fine in PPSSPP or the other way around, sometimes cheats stop working between PPSSPP versions, what's happening?<br>
 A: PPSSPP's memory allocation isn't perfect, ocassionally it improves breaking basic cheats in affected games, it's better to modify game's code than variables stored in memory which in most cases will avoid those problems while also be safer.
 
 Q: How to make my cheats safer?<br>
 A: Aside from the mentioned learning low level programming and changing game code, you can also add test codes like 0xE type to avoid writing memory if your test doesn't match, for example only patch address X with your cheat if address Y matches the exact same game version or even specific place in that game, constantly freezing some value in memory will cause many games to be unstable and in some cases glitch or ruin your savedata.
 
 Q: My cheat freezes HP, but some enemies can still kill me, how to fix it?<br>
 A: Freezing HP value is not a God Mode cheat, if you get more damage than your HP, game might detect it as death even if you get your hp back moment later, reducing "Refresh rate" in PPSSPP cheat menu can help, but it's really poor workaround for a really bad cheat, it's always better and safer to change how the game reacts on values by reprogramming it and making it do all the work than wasting resources fighting against the game which might at times still fail leading to unforseen problems.
 
 Q: Are there any emulator specific CWCheats?<br>
 A: Yes, 0xA code types exist only in PPSSPP and will probably not work in parasite projects like libretro, currently they allow 2 things - adding gamepad vibrations(due to lack of demand only on windows) and control over post process shaders controlled via cheat parameters or values from game memory. It never got a lot of publicity through and as such no projects are known to use them.
 
 Q: Can cheats do X/Y/Z?<br>
 A: Yes, the limit is your imagination, patching game memory isn't limited to cheats either, we can have right analog patches in games that never had analog controls, framerate patches, resolution patches, LOD patches, modifying game's behaviour, HP regen, difficult etc. they can also be used to work-around emulation issues and actual game bugs, as a matter of fact they allow to mod the games in more creative ways than plugins and are more accessible, but it's all about low level programming and some people believe it's soo hard they don't even try learning unless needing it for work or school.
 
 Q: Why bother with cheats and not just write PSP plugins?<br>
 A: PSP SDK requirement is enough to avoid it and the fact it attracts people that prefer to learn something obsolete outside of their small plugin world compared to learning assembly which is similar between archs, teaches you how software actually works and is used worldwide in many cool projects is another.
