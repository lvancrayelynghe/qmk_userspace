# QMK Userspace

## Install

1. Run the normal `qmk setup` procedure if you haven't already done so -- see [QMK Docs](https://docs.qmk.fm/#/newbs) for details.
2. Fork this repository
3. Clone your fork to your local machine
4. `cd` into this repository's clone directory
5. Set global userspace path: `qmk config user.overlay_dir="$(realpath .)"` -- you MUST be located in the cloned userspace location for this to work correctly
6. Compile normally: `qmk compile -kb your_keyboard -km your_keymap`
7. Add your keymap(s) to the build by running `qmk userspace-add -kb lily58 -km lva`
    * This will automatically update your `qmk.json` file
    * Corresponding `qmk userspace-remove -kb lily58 -km lva` will delete it
    * Listing the build targets can be done with with `qmk userspace-list`


## Build current setup

- Compile `qmk compile -kb lily58 -km lva`
- Flash `qmk compile -kb lily58 -km lva`
