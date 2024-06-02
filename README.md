# Star Trek Resurgence Steam Deck Configuration
At its default settings, Star Trek Resurgence runs pretty poorly on the Steam Deck, and there is no way to change the visual settings using the in-game GUI. Fortunately for us, Star Trek Resurgence is a UE4 title and has a fairly standard config file we can edit to ease up on our poor APU.

## Instructions
1. Start the game at least one time, go into the Settings and set the resolution to 1280x800. Make sure Fullscreen is unchecked. Personally, I also uncheck motion blur, but feel free to leave it on if you enjoy the effect of the setting.
2. Quit the game and then Switch to Desktop Mode.
3. Navigate to the config file location.
    - If the game is installed on the internal storage, you should be able to find the config file here: ```$HOME/.steam/steam/steamapps/compatdata/2653940/pfx/drive_c/users/steamuser/AppData/Local/StarTrekGame/Saved/Config/WindowsNoEditor/```
    - If you have the game stored on SD card, it will be at a similar path but from the root of your SD card. Usually, the SD card is mounted as ```primary``` and can be found on the left sidebar: ```/primary/steamapps/compatdata/2653940/pfx/drive_c/users/steamuser/AppData/Local/StarTrekGame/Saved/Config/WindowsNoEditor/```
4. Either download and replace the file ```GameUserSettings.ini``` from my github (if you do, EXAMINE THE FILE CONTENTS FIRST, it's just good security practice!) or copy and change the contents of the config file you wish to alter.
    - The quality settings range from 0-3, 0 meaning Low and 3 meaning Ultra.
    - I have found that setting ```sg.ShadowQuality``` at anything above 0 absolutely tanks performance.
    - For smoothness, I highly recommend using the ```sg.ResolutionQuality=80.000000, bUseVSync=True, FrameRateLimit=30.000000``` settings from my config file, whatever you choose to do.
    - I also recommend disabling the SteamOS frame limiter and enabling screen tearing in the Steam Deck performance menu per-game settings to allow the UE4 engine's Vsync and frame limiter handle the frame pacing as it seems this game REALLY doesn't agree with Valve's implementation.
5. Save your changes and exit. Then, right click on the ```GameUserSettings.ini``` file and click Properties.
6. On the file Properties window, go to the Permissions tab and set all three permissions settings to Can Only View.
7. Click Okay to save the changes. This makes the file Read-Only in order to prevent the game from making changes to it.
8. Return to Gaming Mode using the shortcut on the desktop.
9. Launch the game and see how it runs!
