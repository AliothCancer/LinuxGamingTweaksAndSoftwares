# LinuxGamingTweaksAndTools
A collection of tweaks and softwares which provide better performance and better playability on GNU / Linux platform.



____________________________________________________________________________________________________
# GAMESCOPE

As far as i know there are two generic ways to get it:
  - Flatpak: You need steam flatpak version (it is very bad if you have game on external drives)
  - Compiling it from source: It's not simple, you have to solve dependencies on your own.
*On arch linux there's the AUR package which compile it automaticallly ( i've never tried it )

Gamescope allows to find the best performance/quality ratio:
- Fsr
- Integer upscaling
- Fps limiter


____________________________________________________________________________________________________
# KERNEL

TWEAKS
- Low latency kernel: Can improve input lag 
- Fsync patches: Kernel above 5.16 is compatible with F-sync out of the box (https://linux-gaming.kwindu.eu/index.php?title=Improving_performance)
- Cpu scheduler: There are cpu scheduler which can boost fps like PDS
*You can easily compile a kernel following https://github.com/Frogging-Family/linux-tkg readme


SOFTWARES
...

____________________________________________________________________________________________________
# MESA VERSION

Latest version on newer hardware


____________________________________________________________________________________________________
# TDP

TWEAKS
- Bios settings


SOFTWARES
- RyzenAdj


____________________________________________________________________________________________________
# PROTON/WINE

TWEAKS

- Use fsr: WINE_FULLSCREEN_FSR=1
- Set fsr strenght: WINE_FULLSCREEN_STR= integer number from 1 to 5



SOFTWARES
- Proton GE latest
- ProtonUp
- Proton beta(on steam settings)


____________________________________________________________________________________________________
# AMDVLK or RADV

*radv is able to use ACO and NGGC


TWEAKS

RADV_PERFTEST=aco
*this is default from mesa version 20+

RADV_FORCE_VRS=2x2
*Variable rate shading. This will improve performance, but reduce quality of shadows. Alternative values: 2x1 or 1x2 to use VRS only in one (x or y) direction[4]. (TODO: which is which?)

RADV_PERFTEST=sam
*Force enable resizable bar/smart access memory. Might improve, but might as well reduce performance.

RADV_DEBUG=novrsflatshading
*Disable VRS for flat shading (only on GFX10.3+)

RADV_PERFTEST=nggc
*Enable NGGC. Can slightly improve performance on RX6000 series, but may reduce performance for other cards. Very low impact (see: https://www.phoronix.com/scan.php?page=article&item=radeon-radv-nggc&num=3 )

*You may find more here: https://docs.mesa3d.org/envvars.html



SOFTWARES
-...

____________________________________________________________________________________________________
# STARTING GAMES IN A SEPARATE GRAPHIC SERVER FOR GAME WINDOW (arch wiki)
https://wiki.archlinux.org/title/gaming#Starting_games_in_a_separate_X_server





