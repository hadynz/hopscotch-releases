# Hopscotch 🐇

**Vim-style window navigation for macOS. Stop using your mouse, start flying through your windows.**

![Hopscotch Demo GIF](https://github.com/user-attachments/assets/8a2f0a64-4296-46cd-90ab-cb95b50f60f2)

---

## Why Hopscotch?

As a developer, I live in the terminal and my IDE. Using `hjkl` is second nature, but I was constantly forced to reach for the mouse or trackpad just to switch windows. Hopscotch was built to bring the fluid, keyboard-centric philosophy of Vim to the entire macOS windowing experience.

This is an early-stage project. My goal is to build a tool that becomes an indispensable part of your workflow. To do that, I need your help.

## Features

### Hop: Jump to any window instantly

Activate Hop with a hotkey to overlay letters on all visible windows. Type the corresponding letter to focus that window instantly. It's the fastest way to switch contexts, especially across multiple monitors.

![Hop Feature GIF](https://github.com/user-attachments/assets/8a2f0a64-4296-46cd-90ab-cb95b50f60f2)

### Navigate: Spatial window movement

Use Vim-style `hjkl` keys to move focus to the nearest window in any cardinal direction (left, down, up, or right). It's like having your windows in a spatial grid you can navigate effortlessly.

![Navigate Feature GIF](https://github.com/user-attachments/assets/6cc8a40d-2d76-4f71-9ee6-ad30568caea5)

### Harpoon: Never lose an important window

Mark your most-used windows (like your IDE or terminal) with a simple command. At any time, from any space, you can instantly jump back to a marked window with a dedicated hotkey.

This feature is heavily inspired by the amazing [harpoon plugin](https://github.com/ThePrimeagen/harpoon) for Neovim, created by ThePrimeagen, and aims to bring that same power to macOS windows.

![Harpoon Feature GIF](https://github.com/user-attachments/assets/be79af21-876e-4f80-ae76-de81118c1598)

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

👉 **[If you have 20 minutes, please book a convenient time on my calendar]**

If you're short on time or not up for a call, I would still be incredibly grateful for any thoughts you're willing to share. You can:

- Leave a comment on the post where you found this.
- [Create a GitHub Issue][1] for bugs or feature requests.
- Send me an email at hadyos@gmail.com

---

## Configuration

Hopscotch can be customized to fit your workflow. The application's behavior is controlled through a settings file.

Hopscotch is configured via a `hopscotch.json` file. The application searches for this file in the following locations, in order of precedence:

1.  `~/.hopscotch.json`
2.  `~/.config/hopscotch/hopscotch.json`
3.  `~/Library/Application Support/Hopscotch/hopscotch.json`

The first file found will be used. If no configuration file exists in any of these locations, Hopscotch will create a new one for you at the default path: `~/.hopscotch.json`.

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

## 🧩 Complementary Tools

Hopscotch excels at window navigation. To further reduce mouse usage, consider these powerful companions:

- **[Homerow](https://www.homerow.app/)**: Brings Vimium-style controls to the entire OS, allowing you to click any UI element with your keyboard.
- **[LeaderKey](https://github.com/mikker/LeaderKey.app)**: A launcher that uses a Vim-like leader key to give you quick, memorable shortcuts for apps and commands.
- **[Mouseless](https://mouseless.click/)**: Another excellent app for keyboard-centric users.

---

## 🔗 URL Scheme

Hopscotch supports URL schemes to allow control from other apps and scripts. You can use these to create your own workflows in tools like Raycast, Alfred, or the LeaderKey app.

The basic format is `hopscotch://<feature>/<command>`. Here are the supported commands:

* `hopscotch://harpoon/addWindow` — Shortcut to add the current focused window to the harpoon list.
* `hopscotch://harpoon/toggleQuickMenu` — Shortcut to show/hide the harpoon quick menu.
* `hopscotch://harpoon/navigateWindow1` — Shortcut to navigate to the 1st window in the harpoon list.
* `hopscotch://harpoon/navigateWindow2` — Shortcut to navigate to the 2nd window in the harpoon list.
* `hopscotch://harpoon/navigateWindow3` — Shortcut to navigate to the 3rd window in the harpoon list.
* `hopscotch://harpoon/navigateWindow4` — Shortcut to navigate to the 4th window in the harpoon list.
* `hopscotch://harpoon/navigateWindow5` — Shortcut to navigate to the 5th window in the harpoon list.
* `hopscotch://harpoon/navigateWindow6` — Shortcut to navigate to the 6th window in the harpoon list.
* `hopscotch://harpoon/navigateWindow7` — Shortcut to navigate to the 7th window in the harpoon list.
* `hopscotch://hopping/startHopping` — Shortcut to activate the window hopping overlay.
* `hopscotch://settings/toggleSettings` — Shortcut to open the settings window.
* `hopscotch://switching/switchLeft` — Shortcut to switch focus to the window to the left.
* `hopscotch://switching/switchRight` — Shortcut to switch focus to the window to the right.
* `hopscotch://switching/switchUp` — Shortcut to switch focus to the window above.
* `hopscotch://switching/switchDown` — Shortcut to switch focus to the window below.

---

Made with ❤️ in New Zealand

[1]: https://github.com/hadynz/hopscotch/issues
[2]: https://github.com/hadynz/hopscotch/releases
[3]: https://calendly.com/hadynz/hopscotch-interview
