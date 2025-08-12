# Summary
Keyboard setup for my devices with a Norwegian keyboard layout.

# Motivation
I type everyday of the week. It makes sense to have a keyboard that is more efficient and ergonomic to use. This project aims to:

1. Simplify typing important characters that are normally cumbersome to reach.
2. Prevent fingers straying too far away from the home row.
3. Extend the keyboard, not change it. I want to preserve my touch typing muscle memory, and remain proficient when using other computers.

# Features
 - Make Ctrl+Alt behave as AltGr to access certain 3rd level characters such as `{`, `[`, `~`, etc.
 - Sensical remap for `~` and `$`.
 - Tap `LeftShift` and `RightShift` to toggle *programming mode* which replaces useless characters such as `æ`, `ø`, `å` with better characters such as `{ }` and `[ ]`.
 - Home row mods to simplify typing keys that are hard/cumbersome to reach.
 - Extended functionality for capslock
    - `shift` + `capslock` maps to `escape`
    - `capslock` + `key on right home row` maps to `ctrl` + `function key (f1-f12)` 

 Full specification can be read in the [design doc](design.md).


# Setup
1. Install [keyd](https://github.com/rvaiya/keyd)
2. Copy config 
```bash
sudo cp keyd/* /etc/keyd/default.conf
```
3. Apply config
```bash
sudo keyd reload
```