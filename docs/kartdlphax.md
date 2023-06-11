# kartdlphax

?> In order to follow this method, you will need..
- A second 3DS with custom firmware (source 3DS), it has to be the same region as the 3DS you're trying to modify (target 3DS)
  - Both of the 3DS must be USA, JPN, or EUR region consoles
- A physical or digital copy of Mario Kart 7 which also has to be the same region as both 3DS 
- An SD card for both 3DS

## Downloads
the **Source 3DS** (the one with custom firmware):
  - [kartdlphax](https://github.com/PabloMK7/kartdlphax/releases/latest) (`plugin.3gx`)
  - [Luma3DS 3GX Loader Edition](https://github.com/PabloMK7/Luma3DS_3GX/releases/latest) (`boot.firm`)

the **Target 3DS** (the 3DS you're trying to mod):
  - [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/download/v0.0.7/SafeB9SInstaller-20170605-122940.zip)
  - [boot9strap](https://github.com/SciresM/boot9strap/releases/download/1.4/boot9strap-1.4.zip)
  - [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest) (`Luma3DS.zip`)
  - [unSAFE_MODE](https://github.com/zoogie/unSAFE_MODE/releases/latest) (`RELEASE.zip`)

## Button Check (target 3DS)
1. Power on your **target 3DS** console.
2. When you see the HOME Menu, press and hold the Left and Right shoulder buttons simultaneously.
3. The camera applet should appear on the screen.
4. Power off your console.

## Preparation (source 3DS)
1. Insert the SD card of the **source 3DS** into your computer.
2. Copy the `boot.firm` file from the Luma 3GX Loader Edition to the root directory of the **source 3DS**'s SD card, replacing any existing file.
   - Note: The root directory refers to the initial directory on your SD card where you can see the `Nintendo 3DS` folder, but it is not inside that folder.
3. Copy the `plugin.3gx` file from kartdlphax to the appropriate directory on the **source 3DS**'s SD card based on your copy of Mario Kart 7:
   - For USA region: `luma/plugins/0004000000030800`
   - For EUR region: `luma/plugins/0004000000030700`
   - For JPN region: `luma/plugins/0004000000030600`
   - Create the `plugins` and `0004000...` folders if they don't already exist.
4. Eject the SD card from your computer and insert it back into the **source 3DS**.

## Preparation (target 3DS)
1. Insert the SD card of the **target 3DS** into your computer.
2. Copy both the `boot.firm` and `boot.3dsx` files from the standard Luma3DS `.zip` to the root directory of the **target 3DS**'s SD card.
3. Create a folder named `boot9strap` in the root directory of the SD card.
4. Copy both the `boot9strap.firm` and `boot9strap.firm.sha` files from the boot9strap `.zip` to the `/boot9strap/` folder on the SD card.
5. Copy the `Safeb9SInstaller.bin` file from the SafeB9SInstaller `.zip` to the root directory of the SD card.
6. Copy the `usm.bin` file from the unSAFE_MODE `.zip` to the root directory of the SD card.
7. Create a folder named `3ds` on the root directory of the SD card.
8. Copy the `slotTool` folder from the unSAFE_MODE `.zip` to the `3ds` folder on the SD card.
9. Eject the SD card from your computer and insert it back into the **target 3DS**.

## Kartdlphax
1. Power on the **source 3DS**.
2. If prompted to set up Luma3DS, press the `START` button to save the configuration without making any changes.
3. Once on the HOME Menu, press the Left Shoulder button, Down D-Pad, and Select buttons simultaneously to open the Rosalina menu.
4. Select `Enable plugin loader` from the menu.
5. Press the B button to exit the Rosalina menu.
6. Launch Mario Kart 7 on the **source 3DS**.
7. Ensure that wireless connectivity is enabled.
8. Go to `Local Multiplayer`, and a menu should appear.
   - If the screen freezes, hold the power button for 15 seconds to force the **source 3DS** to power off, then try again.
9. If you have launched kartdlphax before, the last selected settings will be loaded. If they are correct, select `Use settings` and skip the next steps. If they are NOT correct, select `Change settings` and proceed.
10. Select your **target 3DS** console type (Old 3DS family or New 3DS family).
11. Select the appropriate exploit type based on your firmware version:
    - For firmware version 11.16.0, select `xPloitInjector (11.16)`.
    - For firmware version 11.17.0, select `xPloitInjector (11.17)`.
12. A confirmation menu will appear. If the settings shown on the top screen are correct, select `Use settings`.
    - If the settings are incorrect, select `Change settings` and modify them accordingly.
13. Press `Create Group`.
    - If the **source 3DS** freezes at this point and you're using a cartridge, try installing the cartridge to the system before proceeding.
14. Power on the **target 3DS**.
15. Ensure that wireless connectivity is enabled on the **target 3DS**.
16. Open the Download Play application on the **target 3DS** and select "Nintendo 3DS".
17. Join the group created by the **source 3DS**.
18. On the **source 3DS**, select `Start` once it has detected the **target 3DS**.
19. Once multiplayer has loaded on the **target 3DS**, navigate to `Grand Prix` > `50cc` > choose any driver > `Mushroom Cup` > `OK`.
20. Wait for a while, and a percentage should be displayed on the **source 3DS**.
21. If the exploit was successful, the **target 3DS** will boot into the 3DS ROP xPloit Injector.
    - If the exploit wasn't successful, power off both the **source 3DS** and the **target 3DS**, then start again from the beginning of the kartdlphax section.
22. Press the X button to inject unSAFE_MODE.
    - If the injection is successful, the screen will turn green, and the **target 3DS** will automatically power off.
    - If the screen turns red, power off the **target 3DS**, then start again from the beginning of the kartdlphax section. If the issue persists, seek help at the [Skyybrew Discord Server](https://discord.gg/cysxUu7J3E).

## unSAFE_MODE
1. With the **target 3DS** still powered off, hold the following buttons together: Left Shoulder, Right Shoulder, D-Pad Up, and A.
2. While still holding the buttons, power on the **target 3DS** console.
3. Continue holding the buttons until the 3DS boots into Safe Mode, which will display the "system update" menu.
4. Press `OK` to accept the update (Note: This is not an actual update; it's part of the exploit).
5. When asked, select `I accept` to accept the terms and conditions.
6. The update will fail with the error code 003-1099, which is expected.
7. When prompted with `Would you like to configure Internet settings?`, select `Yes`.
8. On the following menu, navigate to `Connection 1` > `Change Settings` > `Next Page (right arrow)` > `Proxy Settings` > `Detailed Setup`.
9. If the exploit was successful, your console will have booted into SafeB9SInstaller.
    - If the console freezes on a white screen instead, hold the POWER button until it turns off, then retry this section.
    - If the console freezes on a red screen, it means you're missing the `usm.bin` file from the root of your SD card.
    - If you encounter a different error, refer to the [troubleshooting guide](placeholder) for assistance.

## Installing boot9strap
1. Follow the on-screen instructions in SafeB9SInstaller.
   - If a step on the lower screen has red-colored text and you aren't prompted to do a key combo, consult the troubleshooting guide.
2. Once the installation is complete, press the A button to reboot the console.
3. Your console should now boot to the Luma3DS configuration menu.
4. For this guide, do not make any changes to the settings; leave them at their default values.
5. If your console shuts down when you try to power it on, make sure you have copied the `boot.firm` file from the Luma3DS `.zip` to the root of the SD card.
6. Press the Start button to save and reboot the console.

## Restoring WiFi Configuration Profiles
1. Launch the Download Play application on the **target 3DS**.
2. Wait until you see the two buttons.
   - Do not press both of them.
3. Simultaneously press the Left Shoulder button, D-Pad Down, and Select buttons to open the Rosalina menu.
4. Select `Miscellaneous options` from the menu.
5. Choose `Switch the hb. title to the current app.` and press the B button to continue.
6. Press the B button to return to the Rosalina main menu.
7. Press the B button to exit the Rosalina menu.
8. Press the Home button and close the Download Play application.
9. Relaunch the Download Play application.
10. Your console should load the Homebrew Launcher.
11. Launch slotTool from the list of homebrew.
12. Select `RESTORE original wifi slots 1,2,3`.
13. Your console will then reboot.

?> Continue to the next step: [Finalizing Setup](finalizing).
