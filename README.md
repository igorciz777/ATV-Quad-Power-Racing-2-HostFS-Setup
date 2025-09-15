# ATV Quad Power Racing 2 HostFS Setup
Patches and setup required to use Host Filesystem in ATV Quad Power Racing 2 (Playstation 2)

>[!WARNING]
>The way patches setup HostFS ingame is probably not the best/intended way so expect lags/crashes

# Instructions
## Extract the game files to a folder.

If your game is in ISO format use 7-Zip or similar to extract the contents.
![atv1](https://github.com/user-attachments/assets/ed190744-c089-4af7-83d6-d9c248c1ebf0)

## Add `.ELF` to game executable

Locate the main game executable (same name as the game's serial number, e.g. `SLUS_205.70` or `SLES_508.50`) and rename it to have a `.ELF` extension.

![atv6](https://github.com/user-attachments/assets/2af97fd7-0580-499b-998f-f5e66132b9a0)

## Add game directory to PCSX2 and assign disc to executable

Open PCSX2 >`Settings`>`Add Game Directory`

Right click added game >`Properties`

![atv7](https://github.com/user-attachments/assets/ee15ac44-4e75-4908-afa4-999029d983e0)

## Get the QuickBMS extraction tool.

[QuickBMS Site](https://aluigi.altervista.org/quickbms.htm)

Direct link: https://aluigi.altervista.org/papers/quickbms.zip

## Get the QuickBMS script provided in this repository.

[atvqpr2.bms](bms//atvqpr2.bms)

## Use QuickBMS with the script to unpack the `ATV.BAH` and `ATV.BAD` files located in the extracted game folder.

Run `quickbms.exe` and select the `atvqpr2.bms` script when prompted. Then select the `ATV.BAH` file and choose the game folder as the output directory.

![atv2](https://github.com/user-attachments/assets/de1a3bae-82cf-403c-81ea-d7d376d55dc1)

Choose `overwrite all` if prompted.

This is how the folder structure should look after extraction:

![atv9](https://github.com/user-attachments/assets/ba7c43c1-a09f-4ba8-9cef-552c3e696292)


## Edit `USER.XML` and set `mUseArchive` to `0`.

Open `USER.XML` in a text editor and change `mUseArchive="1"` to `mUseArchive="0"`.

![atv3](https://github.com/user-attachments/assets/0cf293bd-80e4-4c2b-9b77-739ffdfa5cb8)

Save and close the file.

## Download the patch file from this repository.

See [compatible games table](#compatible-games).

## Place the patch file in `pcsx2/patches` directory.

![atv4](https://github.com/user-attachments/assets/46c88827-1fb1-40cd-a201-0b567c43c481)

## Enable the patch in the game properties.

![atv8](https://github.com/user-attachments/assets/55ebe1c2-844d-496b-85bd-c31a72ddf57a)

## Enable Host Filesystem in the game properties

![atv10](https://github.com/user-attachments/assets/590bdba8-b01a-4a72-98ea-f085e4123e00)

---

# Compatible games
|                     **Name**                      | **Serial** | **Patch**           |
|:-------------------------------------------------:|:----------:|:-------------------:|
| ATV Quad Power Racing 2 (USA)                     | SLUS-20570 | [Patch](patches//SLUS-20570_9E1EAE73.pnach)  |
| ATV Quad Power Racing 2 (Europe)                  | SLES-50850 | [Patch](patches//SLES-50850_9E1EAE73.pnach)  |
| ATV Quad Power Racing 2 (Demo)                    | SLED-51364 | [Patch](patches//SLED-51364_E0AA1E96.pnach)  |
| ATV Quad Power Racing 2 (Beta)                    | SLUS-20570 | [Patch](patches//SLUS-20570_567C6358.pnach)  |
