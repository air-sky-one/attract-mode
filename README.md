# attract-mode

1. Installation
  * image "Motion Blue" :
    * YouTube link : https://www.youtube.com/watch?v=3pzxL7dKqUA
    * Download link : https://mega.nz/#!ABVEQI5J!X0YsPYPqm62_C9P905TlAyLh0RYGZMTPoDhzE4lqoYg
    * Decryption key if it’s asked for: !X0YsPYPqm62_C9P905TlAyLh0RYGZMTPoDhzE4lqoYg
  * Windows : SDFormatter + Win32DiskImager
  * upgrade everything (very long ~ 2h)

2. PS3 Constrollers
  * install driver through Retropie main menu
  * reboot with PS3 controller plugged in with USB cable
  * pair with Shanwan
  * push buttons while pairing
  * config controller through ES
  * from Retropie Setup entry menu, launch Retroarch */!\ WARNING /!\ Activate Rewind + Don't ever save a retroacrh conf from a game. If so, général conf will be omittied !!!*
    * driver -> menu = xmb
    * menu config wallpaper (TODO), color = dark, animated menu = false
    * input config (PS3 Mapping)
      * up = 4 
      * down = 6
      * left = 7
      * right = 5
      * analog left up = up
      * analog left down = down
      * analog left left = left
      * analog left right = right
      * L3 = 1
      * L1 = 10
      * L2 = 8
      * select = 0
      * start = 3
      * home = 16
      * analog right up = Uneg
      * analog right down =Upos
      * analog right left = Zpos
      * R3 = 2
      * R1 = 11
      * R2 = 9
      * square = 15
      * cross = 14
      * circle = 13
      * triangle = 12
    * Hotkeys mapping
      * rewind = 7 = left
      * fast forward hold = 5 = right
      * enable menu button = 16 = home
      * quit = 3 = start
      * reset = 14 = cross
      * menu = 12 (dont' succed to change it) = triangle
      * savestate = 15 = square
      * loadstate = 13 = circle
      * savestate slot up = 4 = up
      * loadstate slot down = down
      * previous disk = 10 = L1
      * next disk = 11 = R1
    * Configuration Save on exit = On 
  * */!\ Controller mapping :* https://github.com/RetroPie/RetroPie-Setup/wiki/RetroArch-Configuration#default-joypad-hotkeys
  * */!\ Change "Select" by "Home" :* https://github.com/RetroPie/RetroPie-Setup/wiki/RetroArch-Configuration#determining-button-values

3. Mausberry Power Switch
  * Links :
    * http://mausberry-circuits.myshopify.com/pages/setup
    * https://github.com/recalbox/recalbox-os/wiki/Mausberry-Switch-Power-On-off-%28EN%29
  * Steps : 
    * ssh connection : ssh pi@retropie (pwd: raspberry)
    * cd Retropie-Setup/tools
    * mkdir mausberry
    * cd mausberry
    * sudo wget http://files.mausberrycircuits.com/setup.sh
    * sudo bash setup.sh
    * sudo reboot
    
4. External Storage
  * https://github.com/RetroPie/RetroPie-Setup/wiki/Running-ROMs-from-a-USB-drive

5. Scrapper

6. Shader
  * Download that https://github.com/pinkeen/libretro-common-shaders-glsl/blob/master/scanline.glsl into :
  * something like that (i just remembre that yo uhave to access from smb instead of ssh for convinience) smb:\\Retropie\configs\Retroarch\shader\shader
  * go on folder above, create a scanline.glsl from crt-pi.glsl and replace the name into the file
  * go to retroarch.cfg and change video-shader to scaneline.glsl

6. In Game : 
  * Rewind : https://github.com/libretro/Lakka/wiki/Rewind
  * Save state : https://retropie.org.uk/forum/topic/241/strategy-for-save-states-and-saves/3

7. Video Intro
  * Full custom templates !!!! : https://www.velosofy.com/template/intro-template-090
  * Futur : https://www.youtube.com/watch?v=I9WQVoVSWwM&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=12
  * Loading : https://www.youtube.com/watch?v=F-8islalTN8&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=13
  * Qasar PS1 : https://www.youtube.com/watch?v=zPgISBwRhSo&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=28
  * Retro gaming : https://www.youtube.com/watch?v=Q8tFidG43-4&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=35
  * Glitch : https://www.youtube.com/watch?v=sgHz35ikAkY&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=49

0. Deprecated
  * image "pure" : http://smartretro.co.uk/forums/viewtopic.php?f=3&t=8277
    * for video snaps : https://github.com/mickelson/attract/wiki/Compiling-on-the-Raspberry-Pi-%28Raspbian-Jessie%29 > Method 2: build FFmpeg with mmal support (hardware accelerated video decoding) (Long)
  * Since you installed ffmpeg after attractmode you need to update/reinstall attractmode. You can do this by using the retropie setup and and under attractmode choose "Update from source".
