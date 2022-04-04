# LinuxGamingTweaksAndSoftwares
A collection of tweaks and softwares which provide better performance and better playability on GNU / Linux platform.



____________________________________________________________________________________________________
# GAMESCOPE

  INFO

  On ubuntu:
  
      sudo add-apt-repository ppa:ar-lex/gamescope
      sudo apt-get update
      sudo apt install gamescope

Gamescope allows to find the best performance/quality ratio:
- Fsr
- Integer upscaling
- Fps limiter


____________________________________________________________________________________________________
# KERNEL

INFO
- Low latency kernel: Can improve input lag 
- Fsync patches: Kernel above 5.16 is compatible with F-sync out of the box (https://linux-gaming.kwindu.eu/index.php?title=Improving_performance)
* You can also check if Esync is enabled with 'ulimit -Hn' command, if this returns more than 500,000 than ESYNC IS ENABLED! otherwise follow https://www.christitus.com/ultimate-linux-gaming-guide/ 

- Cpu scheduler: There are cpu schedulers which can boost fps like PDS

*You can easily compile a kernel with a cpu-scheduler of your choice following https://github.com/Frogging-Family/linux-tkg readme



TWEAKS

...



SOFTWARES

...

____________________________________________________________________________________________________
# MESA VERSION

- ... 


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
* Example on steam launch options: WINE_FULLSCREEN_FSR=1 %command%
* If there's a wrong letter the game won't start

SOFTWARES
- Proton GE latest
- ProtonUp
- Proton beta(on steam settings)


____________________________________________________________________________________________________
# AMDVLK or RADV

INFO
- radv is able to use ACO and NGGC


TWEAKS for radv

- RADV_PERFTEST=aco
*this is default from mesa version 20+

- RADV_FORCE_VRS=2x2
*Variable rate shading. This will improve performance, but reduce quality of shadows. Alternative values: 2x1 or 1x2 to use VRS only in one (x or y) direction[4]. (TODO: which is which?)

- RADV_PERFTEST=sam
*Force enable resizable bar/smart access memory. Might improve, but might as well reduce performance.

- RADV_DEBUG=novrsflatshading
*Disable VRS for flat shading (only on GFX10.3+)

- RADV_PERFTEST=nggc
*Enable NGGC. Can slightly improve performance on RX6000 series, but may reduce performance for other cards. Very low impact (see: https://www.phoronix.com/scan.php?page=article&item=radeon-radv-nggc&num=3 )

*You may find more here: https://docs.mesa3d.org/envvars.html



SOFTWARES
- ...

____________________________________________________________________________________________________
# STARTING GAMES IN A SEPARATE GRAPHIC SERVER FOR GAME WINDOW (arch wiki)
https://wiki.archlinux.org/title/gaming#Starting_games_in_a_separate_X_server





