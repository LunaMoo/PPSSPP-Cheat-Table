# Cheat table for PPSSPP
 Updated on 1.16.6-346 
 x64 version required for AOB script, through there's an x86 version for 1.2.2 release under the legacy scripts.
 
 This cheat table, doesn't include any cheats, it was made to automatize process of creating simple cheats and calculating addresses for PPSSPP's disassembly to make it easier start for creating more advanced cheats.
 
 
 
 To use CE with PPSSPP, you have to select MEM_MAPPED under edit->settings->scan settings in CE.

 If you suffer from not able to freeze or change values via cheat engine attached to PPSSPP you might run one of the workaround scripts first, depending on which CE version you're using:
 - Win 10 bug workaround(activate before anything else) avoids "???" on value change
 - (for CE SSE4_AVX2) Win 10 bug workaround(activate before anything else) avoids "???" on value change

 (if you use renamed CE executable for some reason, you might want to edit one of those scripts for your needs)


 Quick instructions:
 - just use "Attach to PPSSPP" or do it yourself via CE option,
 - make sure to run a game within PPSSPP,
 - use "PPSSPP scripts aob x64",
 - use one of the "Limit Scan Range" settings,
 - search for variables normally,
 - never use CE assembly or any advanced CE functions for PSP games, it doesn't support MIPS arch,
 - if you for whatever weird reason want to look for MIPS code in hexadecimal format through CE search you will have to disable JIT in PPSSPP, this is NOT needed for normal usage,
 - if you find some value you want to create simple cheat from, you can add it to cheat table, rename and while having it selected activate "Select cheat entry and click on the square left from this text to convert address" this will print calculated addresses for PPSSPP disassembly, but also a basic cheat formatted in CWCheat format for you.