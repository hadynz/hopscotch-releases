# Hopscotch

Hopscotch is a Vim-inspired desktop management tool for macOS, providing powerful keyboard-driven control over your windows.

## Features

- **Harpoon:** Mark your most-used windows and jump to them instantly with a keyboard shortcut.
- **Hopping:** Overlay letters on your open windows and switch to any of them by typing the corresponding letter.
- **Keyboard Navigation:** Use Vim-style `hjkl` keys to navigate between windows spatially.

## Configuration

Hopscotch can be customized to fit your workflow. The application's behavior is controlled through a settings file. Below is an overview of the available options.

#### core

- `core.isDebugMode`: Enable debug mode for more verbose logging.
- `core.showDevTools`: Show developer tools in the UI. Requires isDebugMode to be true.

#### hopping

- `hopping.enabled`: Enable or disable the window hopping feature. (default: `true`)
- `hopping.appearance.targetStyle`: Style of the hop target overlay. Currently only 'centered' is available. (default: `"centered"`)
- `hopping.appearance.targetBorder`: Border style for the hop target overlay. (default: `"dashed"`)
- `hopping.appearance.fontSize`: Font size for the hop target keys. (default: `60`)
- `hopping.behavior.keys`: The characters to use for the hop target keys. (default: `"asdfghjklqwertyuiopzxcvbnm"`)
- `hopping.commands.startHopping`: Shortcut to activate the window hopping overlay. (default: `"ALT+B"`)

#### harpoon

- `harpoon.enabled`: Enable or disable the harpoon feature. (default: `true`)
- `harpoon.commands.addWindow`: Shortcut to add the current focused window to the harpoon list. (default: `"ALT+M"`)
- `harpoon.commands.toggleQuickMenu`: Shortcut to show/hide the harpoon quick menu. (default: `"ALT+N"`)
- `harpoon.commands.navigateWindow1`: Shortcut to navigate to the 1st window in the harpoon list. (default: `"ALT+1"`)
- `harpoon.commands.navigateWindow2`: Shortcut to navigate to the 2nd window in the harpoon list. (default: `"ALT+2"`)
- `harpoon.commands.navigateWindow3`: Shortcut to navigate to the 3rd window in the harpoon list. (default: `"ALT+3"`)
- `harpoon.commands.navigateWindow4`: Shortcut to navigate to the 4th window in the harpoon list. (default: `"ALT+4"`)
- `harpoon.commands.navigateWindow5`: Shortcut to navigate to the 5th window in the harpoon list. (default: `"ALT+5"`)
- `harpoon.commands.navigateWindow6`: Shortcut to navigate to the 6th window in the harpoon list. (default: `"ALT+6"`)
- `harpoon.commands.navigateWindow7`: Shortcut to navigate to the 7th window in the harpoon list. (default: `"ALT+7"`)

#### switching

- `switching.enabled`: Enable or disable spatial window switching. (default: `true`)
- `switching.commands.switchLeft`: Shortcut to switch focus to the window to the left. (default: `"ALT+H"`)
- `switching.commands.switchRight`: Shortcut to switch focus to the window to the right. (default: `"ALT+L"`)
- `switching.commands.switchUp`: Shortcut to switch focus to the window above. (default: `"ALT+K"`)
- `switching.commands.switchDown`: Shortcut to switch focus to the window below. (default: `"ALT+J"`)

## Installation

_Installation instructions will be added here._

## Support

Encountered a bug? Would like to request a feature? An app does not work well with Hopscotch?

Please let me know through:

- Open a [GitHub Issue][1]
- Email me at hadyos@gmail.com

---

Made in New Zealand

[1]: https://github.com/hadynz/hopscotch/issues
