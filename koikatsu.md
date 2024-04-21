# Koikatsu and Koikatsu Sunshine
My system specs:  
AMD Ryzen 7 5700X  
AMD Radeon RX 7600  
32GB DDR4 3200  
WINE 8.21  

## Installation
required pacakges: `wine winetricks`  
- Create a new WINE prefix (optional)
- install dxvk and fonts with `winetricks allfonts dxvk ole32`
- Install the game
Note: You may need to run the installer with a Japanese locale. Please refer to your distros documentation on how to set up locales.
to do this set the LANG enviroment variable as `LANG=ja_JP.UTF-8` and then run the Setup file.
- Install any updates you have for the game or install the HF-Patch (for modding and easy updating)  

## Setup & Running
If you're running a modded game using HF-Patch and BepinEx add this registry key:  
`wine reg add "HKEY_CURRENT_USER\Software\Wine\DllOverrides" /v winhttp /t reg_sz /d native,builtin /f`  
Disable WPF hardware acceleration to prevent graphical glitches with launchers, dnspy:  
`wine reg add "HKEY_CURRENT_USER\SOFTWARE\Microsoft\Avalon.Graphics" /v DisableHWAcceleration /t REG_DWORD /d 1 /f`  
Prevent mouse focus loss issues:  
`wine reg ADD 'HKEY_CURRENT_USER\Software\Wine\X11 Driver' /v UseTakeFocus /d 'N' /f`  
