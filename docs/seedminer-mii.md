# Seedminer (Mii)

!> This method requires a GPU that is decently powerful (any dedicated graphics card made in the last few years) and the ability to use the command line. If you don't know how to use it or you don't have a decently powerful GPU, you may ask someone to do this method for you at [our Discord server](https://discord.gg/cysxUu7J3E). You will, however need the following information ready:
  - Your Mii QR Code, uploaded to discord (don't take a screenshot or a photo of the QR code, just send the HNI_XXXX.JPG image only)
  - Your 3DS's ID0 (the 32-character folder inside of `Nintendo 3DS` - check [this troubleshooting guide](placeholder) if you have multiple)
  - Your 3DS model (e.g. New3DS XL, New2DS XL, 2DS, 3DS, 3DS XL, New3DS)
  - Your 3DS's approximate year of manufacturing (could be present behind the frontplate or backplate - If you don't know, just guess the year; It won't be important)

## Downloads
- [Seedminer](https://github.com/zoogie/seedminer/releases/latest) (the Seedminer.zip)
- Any 3.x version of [Python](https://www.python.org/downloads/) installed
  - If you are on Linux, you might have Python 3 installed already, Check by opening a terminal window and enter `python3 -V`. If it returns a version number, this will work for the guide.

## Setting up Seedminer
1. Extract the contents of the Seedminer `.zip` file and move the folder with the name corresponding to your operating system to a location on your computer.
   - Remember the location of this Seedminer folder as it will be used for other files later on.
2. Inside the Seedminer folder, press and hold the SHIFT key and right-click anywhere in the empty space of the folder. From the options that appear, select either Terminal, PowerShell, or Command Prompt to open a command line window.
3. In the command line window, type `py -3 -mpip install pycryptodomex`, then press ENTER to execute the command and allow the installation process to complete.
   - If you encounter an error stating `No module named pip`, you will need to manually install pip. Instructions for installing pip can be found on [this page](https://pip.pypa.io/en/stable/installation/).
4. Power on your console with the SD card inserted.
5. Launch the Mii Maker app.
6. Tap on the `QR Code/Image Options` button.
7. Select the `Save Mii as QR Code` option.
8. Choose any Mii character (if you don't have any, create a new one) and press `OK`.
9. Power off the console.
10. Insert the console's SD card into your computer. Navigate to the `Nintendo 3DS` folder on the SD card and copy the name of the 32-character-long folder located directly inside it.
   - This folder, known as the ID0, is specific to your system. Only one such folder should be present. If you find multiple folders, refer to the troubleshooting section for instructions.
11. Paste the copied ID0 into a document or note for future reference.
12. Navigate to the `DCIM` folder on the SD card.
13. Locate the QR Code file, which should be a `.JPG` file starting with `HNI`.
   - Note that there may be other files in the `DCIM` folder if you use the Nintendo 3DS Camera app.
14. Copy the QR Code file and paste it into the Seedminer folder on your computer.

### Processing and Mining Mii QR
1. Access the [editMii](https://zoogie.github.io/web/miiqr/) website on your computer.
2. Select the `Import from...` option and choose `QR Code`. Upload the Mii QR code that you obtained earlier.
3. Click on `Export to...` and choose `encrypted (.bin)`. This action will initiate the download of a file named `input.bin`.
4. Move the downloaded `input.bin` file to the Seedminer folder.
5. Open the terminal, PowerShell, or Command Prompt window that you opened previously.
6. In the terminal window, enter the command `py -3 seedminer_launcher3.py id0 <id0>`, replacing `<id0>` with the ID0 you previously copied. Make sure to exclude the angle brackets.
7. After the previous command completes, enter the command `py -3 seedminer_launcher3.py mii <model> <year>`.
  - Replace `<model>` with the model of your console (either "new" or "old"). If you're unsure, note that "new" models typically have ZL/ZR buttons and a C-Stick.
  - Replace `<year>` with the year of manufacture of your 3DS (usually found behind the backplate). If you're uncertain about the year, you can leave it empty, and the process will start from the middle.
  - The mining process typically takes around 90 minutes, depending on the performance of your GPU and luck.
  - During the first stage, the offset will likely reach approximately 1500, depending on the console model.
  - If, after the message `movable_part2.sed generation success`, the process progresses beyond offset 100, double-check that you entered the correct ID0. If the ID0 is correct, this method is not suitable, and you should consider updating to the latest version to explore [alternative exploits](placeholder).
  - If you encounter the message `input.bin is invalid size`, recreate the `input.bin` file using your QR Code. If the issue persists, try using a different browser to recreate the `input.bin` file.
  - If you see the message `LFCS has been left blank`, attempt using the opposite console model (e.g., use `mii old` instead of `mii new`).
11. When the process completes, you will find a file named `movable.sed` in the Seedminer folder.

?> Continue to [BannerBomb3 (Legacy)](bb3)
