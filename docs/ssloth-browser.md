# SSLoth-Browser

!> If you have updated your console to the current version using a cartridge, it may not be possible to bypass the browser version check. In this situation, it is recommended to remain on your current firmware and seek assistance from the [Skyybrew](https://discord.gg/cysxUu7J3E) community on Discord.

## Downloads
- [SafeB9SInstaller](https://github.com/d0k3/SafeB9SInstaller/releases/download/v0.0.7/SafeB9SInstaller-20170605-122940.zip)
- [boot9strap](https://github.com/SciresM/boot9strap/releases/download/1.4/boot9strap-1.4.zip)
- [Luma3DS](https://github.com/LumaTeam/Luma3DS/releases/latest) (`Luma3DS.zip`)
- [universal-otherapp](https://github.com/TuxSH/universal-otherapp/releases/latest) (`otherapp.bin`)

## Preparation
1. Power off your console.
2. Insert your SD card into your computer.
3. Copy the file `otherapp.bin` to the root of your SD card and rename it to `arm11code.bin`.
   - Ensure that the file is placed in the initial directory of the SD card, not inside the Nintendo 3DS folder.
   - If the file doesn't have a `.bin` extension, do not add it to the filename.
4. Copy both `boot.firm` and `boot.3dsx` from the Luma3DS `.zip` file to the root of your SD card.
5. Create a folder named `boot9strap` on the root of your SD card.
6. Copy both `boot9strap.firm` and `boot9strap.firm.sha` from the boot9strap `.zip` file to the `/boot9strap/` folder on your SD card.
7. Copy the file `SafeB9SInstaller.bin` from the SafeB9SInstaller `.zip` file to the root of your SD card.
8. Reinsert the SD card into your console.
9. Power on your console.

## SSLoth
1. Launch the System Settings application.
2. Go to `Internet Settings` -> `Connection Settings`.
3. Select your network connection slot and choose `Change Settings` -> `Next Page (right arrow)` -> `Proxy Settings`.
4. Set `Proxy Settings` to `Yes` and click on `Detailed Setup`.
5. Set the Proxy Server to `ssloth.nintendohomebrew.com` and the Port to `8080`.
6. Click OK and then Save.
7. Perform a connection test by clicking `Test` when prompted. The test should succeed.
8. Click OK to continue.
9. Press `Back` twice and then click `Close` to return to the HOME Menu.

## SafeB9SInstaller
1. On the HOME Menu, simultaneously press the Left and Right shoulder buttons to open the camera.
2. If you are unable to open the camera, open the Internet Browser and manually enter the URL: `https://zoogie.github.io/web/nbhax/`.
3. Tap the QR code button and scan the QR code provided at [this link](http://api.qrserver.com/v1/create-qr-code/?color=000000&bgcolor=FFFFFF&data=https%3A%2F%2Fzoogie.github.io%2Fweb%2Fnbhax&qzone=1&margin=0&size=400x400&ecc=L).
4. If you encounter a crash or an error code, refer to the [troubleshooting guide](placeholder) for assistance.
5. If you receive a security certificate warning, press (A) to allow the connection.
6. Tap the "PROCEED TO HAXX" button.
7. If the exploit is successful, you will be booted into SafeB9SInstaller.
8. If you encounter an error, consult the [troubleshooting guide](placeholder) for further assistance.

## boot9strap
1. When prompted, enter the specific key combination displayed on the top screen to initiate the boot9strap installation.
  - If any step on the lower screen appears in red-colored text and you are not prompted to enter a key combination, refer to the [troubleshooting guide](placeholder) for assistance.
2. Once the installation process is complete, press the (A) button to reboot your console.
3. Your console should now boot into the Luma3DS configuration menu.
4. The Luma3DS configuration menu provides various settings for the Luma3DS custom firmware. For this guide, it is recommended to leave all options at their default settings (no checking or unchecking).
5. If your console powers off when you attempt to turn it on, ensure that you have properly copied the `boot.firm` file from the Luma3DS `.zip` to the root directory of your SD card.
6. Press the `(Start)` button to save your settings and reboot your console.

## Restoring proxy profiles
1. Launch the System Settings application on your console.
2. Navigate to `Internet Settings` and select `Connection Settings`.
3. Click on the network connection slot that you want to modify.
4. Navigate to Change Settings, then select `Next Page (right arrow)` and choose `Proxy Settings`.
5. Set `Proxy Settings` to `No`.
6. Click OK, then select Save to save the changes.
7. When prompted, click `Test` to perform the connection test. The test should succeed.
8. Finally, power off your console.

?> Continue to [finalizing setup](finalizing)
