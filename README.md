-=(MCR1_Senhor notes)=-

Tested: Working Video 720p, 1080p & Sound

Dev notes: 

* Issue on MiSTer https://github.com/MiSTer-devel/Arcade-MCR1_MiSTer/issues/11 

* Fixed on Senhor:

File /rtl/cmos_ram.vhd updated with a newer one.

In /rtl/mcr1.vhd added lines 188 and 189
```
up_data        : out std_logic_vector(7 downto 0);
cmos_wr        : in std_logic
```

also in /rtl/mcr1.vhd
```
--wram : entity work.dpram
lines 723 through 736

replaced with: 
wram : entity work.cmos_ram
Lines 738 through 751
```
___
# Midway MCR1 port for MiSTer

[Original readme](readme_orig.txt) (mostly irrelevant to MiSTer)

# Keyboard inputs :
```
   ESC         : Coin 1
   F1          : Start 1P
   F2          : Start 2P 
   UP,DOWN,LEFT,RIGHT arrows : Player 1
   LCtrl : Fire A
   LAlt  : Fire B


   MAME/IPAC/JPAC Style Keyboard inputs:
     5           : Coin 1
     6           : Coin 2
     1           : Start 1 Player
     2           : Start 2 Player
     R,F,D,G     : Player 2
     A           : Fire2 A
     S           : Fire2 B 
	
 Joystick support. 
```
# Games

### Kick
Up to 2 players.
Supported 2 control modes: Joystick/Spinner
1. Left/Right - movement, A - Kick, B - Speed
2. Spinner    - movement, A - Kick, B - Speed

### Solar Fox
Up to 2 players.
Up/Down/Left/Right - movements, A - Fire, B - Speed
 
# Unsupported Games
Draw Poker (gambling machine for casino)
 
 
# ROMs
```
                                *** Attention ***

ROMs are not included. In order to use this arcade, you need to provide the
correct ROMs.

To simplify the process .mra files are provided in the releases folder, that
specifies the required ROMs with checksums. The ROMs .zip filename refers to the
corresponding file of the M.A.M.E. project.

Please refer to https://github.com/MiSTer-devel/Main_MiSTer/wiki/Arcade-Roms for
information on how to setup and use the environment.

Quickreference for folders and file placement:

/_Arcade/<game name>.mra
/_Arcade/cores/<game rbf>.rbf
/_Arcade/mame/<mame rom>.zip
/_Arcade/hbmame/<hbmame rom>.zip
