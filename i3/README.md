# i3 Window Manager Configuration

This is my custom configuration for the [i3 window manager](https://i3wm.org/), tailored for performance, usability, and aesthetics.

## Features

- Mod key set to `Mod4` (Super/Windows key)
- Terminal: `terminator`
- Application launcher: `dmenu`
- Volume and mic control using `pactl` with media keys
- Workspace switching and moving with `$mod + [1-0]` and `$mod + Shift + [1-0]`
- Touchpad configuration (natural scrolling, tap-to-click)
- Dual keyboard layout (US, RU) toggle via `Alt+Shift`
- Window gaps (`gaps inner 5`, `outer 3`)
- Wallpaper set via `feh`
- Bar: `i3bar` with `i3blocks` or `i3status`
- Mouse cursor and window border tweaks
- Auto-start apps: `nm-applet`, `xss-lock`, etc.

## Usage

To use this configuration:

1. Copy the files to `~/.config/i3/`.
2. Install required dependencies:
    ```bash
    sudo pacman -S i3-wm dmenu terminator feh xss-lock i3blocks xorg-xsetroot xorg-xinput network-manager-applet pulseaudio
    ```
3. Restart i3 or log in to your i3 session.

## Notes

- Touchpad name: `"ASUE120A:00 04F3:319B Touchpad"`
- Customize your wallpaper by replacing `~/.config/i3/wallpaper.jpg`
- To regenerate config with wizard, delete `~/.config/i3/config` and run `i3-config-wizard`

## License

MIT License
