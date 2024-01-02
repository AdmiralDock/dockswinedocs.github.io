# Fallout: New Vegas - GOG Version 1.4.0.525(a)
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

## Setup & Running
Start by running the games launcher and set up your graphic settings, exit the launcher when done.  
The game by default runs too fast (even with v-sync turned on) so we need to tell DXVK to limit the framerate.  
Do this by using the enviroment variable `DXVK_FRAME_RATE="60"`  

You can now launch the game via the main executable :3  
