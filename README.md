# i3 Configuration

This is a custom i3 window manager configuration with keybindings, workspace settings, and additional enhancements for a seamless tiling window management experience.

## Features
- **Custom Keybindings**: Easily launch applications, manage workspaces, and control window focus.
- **Theming & Colors**: Defined colors for focused, inactive, and urgent windows.
- **Custom Gaps & Borders**: Smart gaps and pixel borders for a sleek look.
- **i3bar Configuration**: Displays status, workspace indicators, and system tray.
- **Startup Applications**: Automatically launches essential applications.
- **Lockscreen & Power Management**: Integrated with `betterlockscreen`.
- **Multimedia Key Support**: Volume control with `pamixer` and refresh `i3blocks`.

## Installation

1. Copy the configuration file to your i3 configuration directory:
   ```sh
   git clone git@github.com:WhoisCipher/i3-config.git
   mkdir -p ~/.config/i3
   cp config ~/.config/i3/config
   ```
2. Restart i3:
   ```sh
   i3-msg restart
   ```

## Keybindings

### Applications
| Keybinding          | Action |
|---------------------|--------------------------------|
| `$mod + Return`    | Open terminal (ghostty) |
| `$mod + Shift + Return` | Open browser (chromium) |
| `$mod + d`         | Open application launcher (rofi) |

### Workspaces
| Keybinding          | Action |
|---------------------|------------------------------|
| `$mod + [1-10]`    | Switch to workspace |
| `$mod + Shift + [1-10]` | Move window to workspace |

### Window Management
| Keybinding         | Action |
|--------------------|------------------------------|
| `$mod + Left`     | Focus left |
| `$mod + Down`     | Focus down |
| `$mod + Up`       | Focus up |
| `$mod + Right`    | Focus right |
| `$mod + Shift + Left`  | Move window left |
| `$mod + Shift + Right` | Move window right |
| `$mod + f`        | Toggle fullscreen |
| `$mod + Shift + f` | Toggle floating mode |
| `$mod + Shift + q` | Kill focused window |

### Multimedia Keys
| Keybinding         | Action |
|--------------------|------------------------------|
| `XF86AudioMute`   | Toggle mute |
| `XF86AudioLowerVolume` | Decrease volume |
| `XF86AudioRaiseVolume` | Increase volume |

## Auto-Start Applications
These applications are automatically launched at startup:
- **Terminal**: `ghostty`
- **Web Browser**: `brave`
- **Music Player**: `spotify`
- **Compositor**: `picom`
- **Wallpaper**: Set with `feh`
- **Caps Lock Utility**: `caps_util`

## Lockscreen
- `$mod + l`: Lock screen (`betterlockscreen -l`)
- `$mod + Shift + l`: Lock and suspend (`betterlockscreen -s`)

## Status Bar (i3blocks)
The bar is positioned at the bottom and shows:
- Workspace indicators
- System tray
- Status updates (battery, volume, etc.)

## Caps Lock Util
If you wish to use the caps lock util that overlays content in the middle of the screen and notifies CAPS: ON then:
   ```sh
   sudo cp ~/.config/caps_util /usr/local/bin
   ```
NOTE: Changes will take affect on restart

## Additional Notes
- The wallpaper is set using `feh` and should be located at `~/Wallpaper/minimal_gradient.png`.
- The compositor `picom` is enabled for transparency and effects. For picom config visit [Picom Config](https://github.com/WhoisCipher/picom-config)
