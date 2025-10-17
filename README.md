
![20250823_010835](https://github.com/user-attachments/assets/8688cacf-d952-409d-94af-bc1824356b18)

# <ins>Move Anything Fork</ins>

## What is this project?
This is a fork of [Move Anything](https://github.com/bobbydigitales/move-anything) with a few key additional features:

### Added feature: Knob LED sweeps
When turning knobs from 0-127, the relevant knob LED will sweep across a color spectrum to make the value easy to see at a glance.

By default, these go from black (0) through to white (127).

### Added feature: Knob banks
This extends the 9 physical knobs (the 8 knobs above the tracks, plus the 9th volume knob) to 8 banks, for a total of 72 virtual knobs. 

Knob banks are accessed by pressing the even-numbered sequencer buttons across the bottom (in between the odd numbered buttons used for muting/soloing tracks). The relevant button will light up indicating that knob bank is selected.

The knob banks are:
* **Bank 1** MIDI CC71 - CC79, displayed with black/white colors
* **Bank 2** MIDI CC14 - CC22, displayed with a synthwave color scheme
* **Bank 3** MIDI CC23 - CC31, displayed with rose colors
* **Bank 4** MIDI CC35 - CC43, displayed with rainbow colors
* **Bank 5** MIDI CC44 - CC52, displayed with black/white colors
* **Bank 6** MIDI CC53 - CC61, displayed with a synthwave color scheme
* **Bank 7** MIDI CC102 - CC110, displayed with rose colors
* **Bank 8** MIDI CC111 - CC119, displayed with rainbow colors

These values are chosen to retain compatibility with the Move Anything project (so bank 1 values are unchanged from the default) and to avoid clashes with reserved or commonly used MIDI CC values.

### Added feature: Display only odd rows
When clicking the jog wheel, Move Anything by default swaps between the top 4 and bottom 4 rows. 

This feature adds a new 3rd mode to only display rows 1, 3, 5 and 7 (or rows 00, 02, 04, 06 on the M8). So clicking the jog wheel toggles between Top -> Bottom -> Odd rows

This only-odd-rows is useful if you structure your M8 tracks to only use every other row. Many performers choose to do this for live performances, because it allows you to loop chains, rather than have them automatically progress to the next chain.


## How to install

1. Install Move Anything using the [regular instructions](https://github.com/bobbydigitales/move-anything)

2. Download the two [altered](https://github.com/damian-/move-anything/blob/dev/src/move_m8_vlpp.js) [files](https://github.com/damian-/move-anything/blob/dev/src/move_virtual_knobs.mjs) and copy to your move:

```bash
curl -fsSL https://raw.githubusercontent.com/damian-/move-anything/dev/src/move_virtual_knobs.mjs -o /tmp/move_virtual_knobs.mjs && scp /tmp/move_virtual_knobs.mjs ableton@move.local:/data/UserData/control_surface_move/
```

```bash
curl -fsSL https://raw.githubusercontent.com/damian-/move-anything/dev/src/move_m8_vlpp.js -o /tmp/move_m8_vlpp.js && scp /tmp/move_m8_vlpp.js ableton@move.local:/data/UserData/control_surface_move/
```

3. Hit the key combo on move (shift + volume + wheel) to start and connect your M8


## Move Anything

Other features of Move Anything are still available. 

Move Anything is a framework that lets you write your own code for the Ableton Move. It gives you access to:
* The pads (note number, velocity, and polyphonic aftertouch values)
* The 9 endless encoders with relative and absolute values available
* Capacitive touch messages.
* All buttons.
* Setting the colors of everything that can have a color set.
* Display as a 128x64 1 bit framebuffer (it's just balck and white);
* Audio from the line-in and mic
* Audio out through the speakers and line out
* MIDI in/out via the USB-A port. You can also connect multiple USB-MIDI devices to the USB-A port using a hub and receive and send MIDI to all of them.
* Move Anything is non-destructive and lives alongside the regular Move software. You can quickly launch Move Anything using a key combination from the regular Move software, and quickly return to the regular Move software when you're done.

## Credit to Move Anything Contributors
@talktogreg, @impbox, @deets, @bobbyd

## Community
Join us on Discord: https://discord.gg/Zn33eRvTyK

