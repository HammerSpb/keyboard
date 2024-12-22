# keyboard

My Gallium keyboard layout for Ferris Sweep and ANSI!

# Sweep

This project contain the files needed to compile the custom keymap for the Ferris Sweep.

## Keymap (TODO)

The keymap consists of 3 layers (actually 4). I use home-row mods to get all the Shift, Control, Alt, and GUI action in an easy to reach position.

![keymap layout](keymap.svg)

### Layer 0 (TODO)

### Layer 1 (TODO)

### Layer 2 (TODO)

### Layer 3 (TODO)

### Layer 4 (TODO)

## Compiling and flashing

### Prerequisites

A working version of QMK is required. See https://docs.qmk.fm/#/newbs_getting_started

### Getting started

Install Using Homebrew (macOS, some Linux)

```
brew install qmk/qmk/qmk
export QMK_HOME='~/qmk_firmware' # Optional, set the location for `qmk_firmware`
qmk setup  # This will clone `qmk/qmk_firmware` and optionally set up your build environment
```

By default it will be install to `~/qmk_firmware` folder

Clone this repo into a `gallium-keyboard`

```
git clone https://github.com/HammerSpb/keyboard.git gallium-keyboard
```

Create a directory insdide `Ferris/Sweep` keyboard folder

```
mkdir ~/qmk_firmware/keyboards/ferris/keymaps/gallium-keyboard
```

Copy content of `gallium-keyboard/qmk` to the `gallium-keyboard` folder

```
cp -r qmk/* ~/qmk_firmware/keyboards/ferris/keymaps/gallium-keyboard
```

### Compiling

Now you could compile it

```
qmk compile -kb ferris/sweep -km gallium-keyboard
```

After that `qmk` will create `hex`-firmware file in `~/qmk_firmware/` folder with the name `ferris_sweep_gallium-keyboard.hex`

### Flashing

First, you have to install `Qmk Toolbox`

```
brew install qmk-toolbox
```

To flash the board connect it via USB to the computer (one half) you have to run `QMK Toolbox`

Click `Open file` button and select `~/qmk_firmware/ferris_sweep_gallium-keyboard.hex`

Make sure your cpu is `ATmega32U4` (I'm using Elite-C controller)

`Short` two small holes at the top of connected half of keyboard to `reset` it.

You will see ready message in the console log of `Qmk Toolbox`

Go to `Tools/EEPROM` menu and select `Left Half`

Now you could press `Flash`

If everything wnet fine you could disconnect left half and connect right half of the keyboard and repeat the process by `Resetting` first, then selecting `Right Half` in `Tools/EEPROM` menu and then `Flash` it.

Now you could disconnect `right half` and connect full keyboard and start using it.

After both halves are flashed, connect the left half to USB and start typing.
