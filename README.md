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

6. In Game : 
* Rewind : https://github.com/libretro/Lakka/wiki/Rewind
* Save state : https://retropie.org.uk/forum/topic/241/strategy-for-save-states-and-saves/3

7. Video Intro
* Futur : https://www.youtube.com/watch?v=I9WQVoVSWwM&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=12
* Loading : https://www.youtube.com/watch?v=F-8islalTN8&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=13
* Qasar PS1 : https://www.youtube.com/watch?v=zPgISBwRhSo&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=28
* Retro gaming : https://www.youtube.com/watch?v=Q8tFidG43-4&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=35
* Glitch : https://www.youtube.com/watch?v=sgHz35ikAkY&list=PL_ik_t59tpUxdncwMtsFNjIxfiMipQLla&index=49

0. Deprecated
  * image "pure" : http://smartretro.co.uk/forums/viewtopic.php?f=3&t=8277
    * for video snaps : https://github.com/mickelson/attract/wiki/Compiling-on-the-Raspberry-Pi-%28Raspbian-Jessie%29 > Method 2: build FFmpeg with mmal support (hardware accelerated video decoding) (Long)
  * Since you installed ffmpeg after attractmode you need to update/reinstall attractmode. You can do this by using the retropie setup and and under attractmode choose "Update from source".
