# Hopscotch 🐇

**Vim-style window navigation for macOS. Stop using your mouse, start flying through your windows.**

![Hopscotch Demo GIF](https://place-hold.it/800x450?text=Your+Awesome+Hopping+GIF+Here)
_Replace this with a GIF of the 'Hopping' feature in action._

---

## Why Hopscotch?

As a developer, I live in the terminal and my IDE. Using `hjkl` is second nature, but I was constantly forced to reach for the mouse or trackpad just to switch windows. Hopscotch was built to bring the fluid, keyboard-centric philosophy of Vim to the entire macOS windowing experience.

This is an early-stage project. My goal is to build a tool that becomes an indispensable part of your workflow. To do that, I need your help.

## Features

### Hop: Jump to any window instantly

Activate Hop with a hotkey to overlay letters on all visible windows. Type the corresponding letter to focus that window instantly. It's the fastest way to switch contexts, especially across multiple monitors.

![Hop Feature GIF](https://place-hold.it/600x300?text=Hop+Feature+GIF)

### Navigate: Spatial window movement

Use Vim-style `hjkl` keys to move focus to the nearest window in any cardinal direction (left, down, up, or right). It's like having your windows in a spatial grid you can navigate effortlessly.

![Navigate Feature GIF](https://place-hold.it/600x300?text=Navigate+Feature+GIF)

### Harpoon: Never lose an important window

Mark your most-used windows (like your IDE or terminal) with a simple command. At any time, from any space, you can instantly jump back to a marked window with a dedicated hotkey.

This feature is heavily inspired by the amazing [harpoon plugin](https://github.com/ThePrimeagen/harpoon) for Neovim, created by ThePrimeagen, and aims to bring that same power to macOS windows.

![Harpoon Feature GIF](https://place-hold.it/600x300?text=Harpoon+Feature+GIF)

---

## 📥 Download & Installation

You can download the latest version of Hopscotch from the **[GitHub Releases page][2]**.

1.  Download the `Hopscotch-darwin-x.y.z.dmg` file.
2.  Open the `.dmg` and drag `Hopscotch.app` to your `Applications` folder.
3.  On first launch, macOS will require you to grant Accessibility permissions for Hopscotch to manage windows.

---

## 🙏 I Need Your Feedback!

This app is for you. Your feedback—good, bad, or brutally honest—is the most valuable resource I have right now to make Hopscotch better.

The best way you can help is to let me watch you use the app for the first time on a brief screen-share call. Your fresh perspective is exactly what I'm looking for!

👉 **[If you have 20 minutes, please book a convenient time on my calendar]([YOUR_CALENDLY_LINK])**

If you're short on time or not up for a call, I would still be incredibly grateful for any thoughts you're willing to share. You can:

- Leave a comment on the post where you found this.
- [Create a GitHub Issue][1] for bugs or feature requests.
- Send me an email at hadyos@gmail.com

---

## Configuration

Hopscotch can be customized to fit your workflow. The application's behavior is controlled through a settings file.

Below is an overview of the available options with their default values:

```js
{
  // core
  "core.isDebugMode": false, // Enable debug mode for more verbose logging.
  "core.showDevTools": false, // Show developer tools in the UI. Requires isDebugMode to be true.

  // harpoon
  "harpoon.enabled": true, // Enable or disable the harpoon feature.
  "harpoon.commands.addWindow": "ALT+M", // Shortcut to add the current focused window to the harpoon list.
  "harpoon.commands.toggleQuickMenu": "ALT+N", // Shortcut to show/hide the harpoon quick menu.
  "harpoon.commands.navigateWindow1": "ALT+1", // Shortcut to navigate to the 1st window in the harpoon list.
  "harpoon.commands.navigateWindow2": "ALT+2", // Shortcut to navigate to the 2nd window in the harpoon list.
  "harpoon.commands.navigateWindow3": "ALT+3", // Shortcut to navigate to the 3rd window in the harpoon list.
  "harpoon.commands.navigateWindow4": "ALT+4", // Shortcut to navigate to the 4th window in the harpoon list.
  "harpoon.commands.navigateWindow5": "ALT+5", // Shortcut to navigate to the 5th window in the harpoon list.
  "harpoon.commands.navigateWindow6": "ALT+6", // Shortcut to navigate to the 6th window in the harpoon list.
  "harpoon.commands.navigateWindow7": "ALT+7", // Shortcut to navigate to the 7th window in the harpoon list.

  // hopping
  "hopping.enabled": true, // Enable or disable the window hopping feature.
  "hopping.appearance.targetStyle": "centered", // Style of the hop target overlay. Currently only 'centered' is available.
  "hopping.appearance.targetBorder": "dashed", // Border style for the hop target overlay.
  "hopping.appearance.fontSize": 60, // Font size for the hop target keys.
  "hopping.behavior.keys": "asdfghjklqwertyuiopzxcvbnm", // The characters to use for the hop target keys.
  "hopping.commands.startHopping": "ALT+B", // Shortcut to activate the window hopping overlay.

  // onboarding

  // settings
  "settings.commands.toggleSettings": "CmdOrCtrl+,", // Shortcut to open the settings window.

  // switching
  "switching.enabled": true, // Enable or disable spatial window switching.
  "switching.commands.switchLeft": "ALT+H", // Shortcut to switch focus to the window to the left.
  "switching.commands.switchRight": "ALT+L", // Shortcut to switch focus to the window to the right.
  "switching.commands.switchUp": "ALT+K", // Shortcut to switch focus to the window above.
  "switching.commands.switchDown": "ALT+J", // Shortcut to switch focus to the window below.
}
```

## 🗺️ Roadmap

My focus is currently on stability and refining the core features based on user feedback. Some ideas I'm exploring for the future include:

- Window resizing with the keyboard.
- Screenshotting with the keyboard.
- Recalling (moving) any window to your current MacOS space and to move back.
- Windows and Linux versions.

Have a different idea? Let me know!

---

Made with ❤️ in New Zealand

[1]: https://github.com/hadynz/hopscotch/issues
[2]: https://github.com/hadynz/hopscotch/releases

```

```
