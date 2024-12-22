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

Clone this repo into the `qmk_firmware/keyboards/ferris/keymaps/` directory.

### Compiling

After all changes have been made run the following command to create the firmware:

```
qmk compile
```

### Flashing

To flash the board connect it via USB to the computer and run:

```
qmk flash
```

It will poll the keyboard and will flash it when it is in Reset mode. So press the reset button and wait for the flashing of the board.

Once the board is flashed, disconnect it from USB, and connect the other half to the computer, and repeat the flashing procedure.

After both halves are flashed, connect the left half to USB and start typing.

## Misc

### SVG

I've included a picture of the keymap. It can be generated from the JSON file of this keymap. The problem is that this keymap uses custom code, so we don't have a JSON file. The JSON file can be generated with:

```
qmk c2json
```

With this JSON file the SVG can be generated with [Keymap-drawer](https://keymap-drawer.streamlit.app/).
