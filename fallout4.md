# Fallout 4 - GOG Version 1.10.163.0
My system specs:  
AMD Ryzen 7 5700X  
AMD Radeon RX 7600  
32GB DDR4 3200  
WINE 8.21  

## Installation
required pacakges: `wine winetricks`  
- Create a new WINE prefix (optional)
- install dxvk with `winetricks dxvk`
- install the game using GOG's installer
- run `winecfg` and under the Graphics tab check: Automatically capture the mouse in full-screen windows and Emulate a virtual desktop (set its resolution to match your screen resolution)

## Setup & Running
Start by running the games launcher and set up your graphic settings, exit the launcher when done.  
Run the game once using the main executable and exit.  
Edit Fallout4.ini and Fallout4Prefs.ini, add the following lines under **[Controls]** to both files:  
```ini
bMouseAcceleration=0
bBackgroundMouse=1
```
You can now play the game! :3  

## Troubleshooting
If you're having audio problems such as: Character speech not playing, music not playing, menu sfx not playing:  
you are likely missing gstreamer plugins for windows media audio, installing those should fix the issue  
alternatively you can install the missing codecs within WINE itself, either through winetricks or by installing for example the K-Lite Codec Pack - Basic (check the windows media audio and windows media video checkboxes when asked about what codecs to install)  
