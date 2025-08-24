# ATV Quad Power Racing 2 HostFS Setup
Patches and setup required to use host filesystem file loading in ATV Quad Power Racing 2 (Playstation 2)

# Instructions
### Extract the game files to a folder.

If your game is in ISO format use 7-Zip or similar to extract the contents.

### Add `.ELF` to game executable

Locate the main game executable (same name as the game's serial number, e.g. `SLUS_205.70` or `SLES_508.50`) and rename it to have a `.ELF` extension.

### Add game directory to PCSX2 and assign disc to executable

### Get the QuickBMS extraction tool.

https://aluigi.altervista.org/papers/quickbms.zip

### Get the QuickBMS script provided in this repository.

[atvqpr2.bms](bms/atvqpr2.bms)

### Use QuickBMS with the script to unpack the `ATV.BAH` and `ATV.BAD` files located in the extracted game folder.

Run `quickbms.exe` and select the `atvqpr2.bms` script when prompted. Then select the `ATV.BAH` file and choose the game folder as the output directory.

Choose `overwrite all` if prompted.

This is how the folder structure should look after extraction:


### Edit `USER.XML` and set `mUseArchive` to `0`.

Open `USER.XML` in a text editor and change `mUseArchive="1"` to `mUseArchive="0"`.



Save and close the file.

### Download the patch file from this repository.

See [compatible games table](#compatible-games).

### Place the patch file in `pcsx2/patches` directory.

### Enable the patch in the game properties.

# Compatible games
|                     **Name**                      | **Serial** | **Patch**           |
|:-------------------------------------------------:|:----------:|:-------------------:|
| ATV Quad Power Racing 2 (USA)                     | SLUS-20570 | [Patch](patches\SLUS-20570_9E1EAE73.pnach)  |
| ATV Quad Power Racing 2 (Europe)                  | SLES-50850 | [Patch](patches\SLES-50850_9E1EAE73.pnach)  |
| ATV Quad Power Racing 2 (Demo)                    | SLED-51364 | [Patch](patches\SLED-51364_E0AA1E96.pnach)  |
| ATV Quad Power Racing 2 (Beta)                    | SLUS-20570 | [Patch](patches\SLUS-20570_567C6358.pnach)  |