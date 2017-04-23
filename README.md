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
    * /!\ Conf per Emulator  /!\ Warning !!! In case of there is a conf set for a specific emulator and you want to keep general config, go to /opt/retropie/configs select your emulator and modifiy retroarch.cfg to match the one in an other system which has general conf.
  * */!\ Controller mapping :* https://github.com/RetroPie/RetroPie-Setup/wiki/RetroArch-Configuration#default-joypad-hotkeys
  * */!\ Change "Select" by "Home" :* https://github.com/RetroPie/RetroPie-Setup/wiki/RetroArch-Configuration#determining-button-values

3. Don't display RunCommand tool when launching a game
  * Go To RunCommand utility
  * Disable "Launch Menu"
  * https://github.com/retropie/retropie-setup/wiki/runcommand#configuring-runcommand

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
  * smb://retropie/configs/all/retroarch/shaders (i just remembre that you have to access from smb instead of ssh for convinience) smb:\\Retropie\configs\Retroarch\shader\shader
  * go on folder above, create a scanline.glsl from crt-pi.glsl and replace the name into the file
  * go to retroarch.cfg and change video-shader to scaneline.glsl

7. N64 Audio volume
  * mupen64plus.cfg is erased each time you start a game so first :
  * /opt/retropie/emulators/mupen64plus/bin $ sudo nano mupen64plus.sh 
    * In function SetAudio :
      * change
      * AUDIO_PLUGIN="mupen64plus-audio-omx"
      * by 
      * AUDIO_PLUGIN="mupen64plus-audio-sdl"
  * in /opt/retropie/configs/n64/mupen64plus.cfg
    * Change
    * AudioPlugin = "mupen64plus-audio-omx.so"
    * By 
    * AudioPlugin = "mupen64plus-audio-sdl.so"
  * https://github.com/recalbox/recalbox-os/issues/596
  * explanation here : https://retropie.org.uk/forum/topic/1756/n64-mupenplus-sound-volume/3
  * https://www.reddit.com/r/RetroPie/comments/47ywux/sound_issues_with_some_emulators/?st=izwtf4x0&sh=e6c0ca12

8. N64 Hotkeys 
  * mupen64plus.cfg is erased each time you start a game so first :
  * /opt/retropie/emulators/mupen64plus/bin $ sudo nano mupen64plus.sh 
    * Comments the 2 lines above : 
      * iniConfig “=” “\” $configdir/n64/mupen64plus.cfg”
      * iniSet “${hotkeys_m64p[$i]} “$bind”
      * These lines are just after : # write hotkey to mupen64plus.cfg
      * DOC : http://blog.petrockblock.com/forums/search/?bbp_search=hotkey
  * in /opt/retropie/configs/n64/mupen64plus.cfg
    * Put 
    * Joy Mapping Stop = "J0B16/B3"
    * Joy Mapping Save State = "J0B16/B11"
    * Joy Mapping Load State = "J0B16/B10"
9. In Game : 
  * from Retropie Setup entry menu, launch Retroarch */!\ WARNING /!\ Activate Rewind + Don't ever save a retroacrh conf from a game. If so, général conf will be omittied !!!*
  * Rewind : https://github.com/libretro/Lakka/wiki/Rewind
  * Save state : https://retropie.org.uk/forum/topic/241/strategy-for-save-states-and-saves/3

10. Chante TimeZone
  * https://www.raspberrypi.org/forums/viewtopic.php?t=4977&f=5
  * Copy tzselect return in bach
  * Past it in /home/pi/.profile at the end of the file to make it permanent

11. Game Station Theme V2 HD
  * Download theme : 
    * http://forum.attractmode.org/index.php?topic=505.0
    * http://forum.attractmode.org/index.php?action=dlattach;topic=505.0;attach=850
  * Unzip it there : /home/pi/.attract/layouts
  * Video wheel is too slow on pi 3 with a large amounbt of games in a system (has also side effects with PS3 controller)
    * go to : /home/pi/.attract/layouts/Game Station HD/layout.nut
    * change :
      * m_obj.height = wheel_h[slot] + p * ( wheel_h[slot+1] - wheel_h[slot] );
      * to
      * m_obj.height = ( wheel_h[slot] + p * ( wheel_h[slot+1] - wheel_h[slot] ) ) / 2;
    * It will divide the height of the element in the will, but won't increase the number of visible element in the wheel
    * Config the Layout to display wheel image and not span in the wheel

12. Video Intro
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
