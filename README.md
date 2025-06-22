# Hopscotch 🐇

**Vim-style window navigation for macOS. Stop using your mouse, start flying through your windows.**

![Hopscotch Demo GIF](./assets/hopscotch-hopping.gif)

---

## Why Hopscotch?

As a developer, I live in the terminal and my IDE. Using `hjkl` is second nature, but I was constantly forced to reach for the mouse or trackpad just to switch windows. Hopscotch was built to bring the fluid, keyboard-centric philosophy of Vim to the entire macOS windowing experience.

This is an early-stage project. My goal is to build a tool that becomes an indispensable part of your workflow. To do that, I need your help.

## Features

### Hop: Jump to any window instantly

Activate Hop with a hotkey to overlay letters on all visible windows. Type the corresponding letter to focus that window instantly. It's the fastest way to switch contexts, especially across multiple monitors.

![Hop Feature GIF](./assets/hopscotch-hopping.gif)

### Navigate: Spatial window movement

Use Vim-style `hjkl` keys to move focus to the nearest window in any cardinal direction (left, down, up, or right). It's like having your windows in a spatial grid you can navigate effortlessly.

![Navigate Feature GIF](./assets/hopscotch-switching.gif)

### Harpoon: Never lose an important window

Mark your most-used windows (like your IDE or terminal) with a simple command. At any time, from any space, you can instantly jump back to a marked window with a dedicated hotkey.

This feature is heavily inspired by the amazing [harpoon plugin](https://github.com/ThePrimeagen/harpoon) for Neovim, created by ThePrimeagen, and aims to bring that same power to macOS windows.

![Harpoon Feature GIF](./assets/hopscotch-harpoon.gif)

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

Below is an overview of the available options with their default values. Note: All keyboard
shortcut commands are defined using [Electron's accelerator][4] format.

```js
{
  "core.isDebugMode": false
  "core.showDevTools": false
  "core.enableWindowHighlight": true

  "harpoon.commands.markWindow": "CMD+SHIFT+A"
  "harpoon.commands.toggleQuickMenu": "CMD+SHIFT+M"
  "harpoon.commands.navigateToWindow1": "OPTION+1"
  "harpoon.commands.navigateToWindow2": "OPTION+2"
  "harpoon.commands.navigateToWindow3": "OPTION+3"
  "harpoon.commands.navigateToWindow4": "OPTION+4"
  "harpoon.commands.navigateToWindow5": "OPTION+5"
  "harpoon.commands.navigateToWindow6": "OPTION+6"
  "harpoon.commands.navigateToWindow7": "OPTION+7"

  "hopping.appearance.targetStyle": "centered"
  "hopping.appearance.targetBorder": "dashed"
  "hopping.appearance.fontSize": 60
  "hopping.behavior.keys": "asdfghjklqwertyuiopzxcvbnm"
  "hopping.commands.startHopping": "CMD+SHIFT+H"


  "settings.commands.openSettings": 

  "switching.commands.switchLeft": "CMD+SHIFT+H"
  "switching.commands.switchRight": "CMD+SHIFT+L"
  "switching.commands.switchUp": "CMD+SHIFT+K"
  "switching.commands.switchDown": "CMD+SHIFT+J"
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

* `hopscotch://harpoon/markWindow`
* `hopscotch://harpoon/toggleQuickMenu`
* `hopscotch://harpoon/navigateToWindow1`
* `hopscotch://harpoon/navigateToWindow2`
* `hopscotch://harpoon/navigateToWindow3`
* `hopscotch://harpoon/navigateToWindow4`
* `hopscotch://harpoon/navigateToWindow5`
* `hopscotch://harpoon/navigateToWindow6`
* `hopscotch://harpoon/navigateToWindow7`
* `hopscotch://hopping/startHopping`
* `hopscotch://settings/openSettings`
* `hopscotch://switching/switchLeft`
* `hopscotch://switching/switchRight`
* `hopscotch://switching/switchUp`
* `hopscotch://switching/switchDown`

---

Made with ❤️ in New Zealand

[1]: https://github.com/hadynz/hopscotch/issues
[2]: https://github.com/hadynz/hopscotch/releases
[3]: https://calendly.com/hadynz/hopscotch-interview
[4]: https://www.electronjs.org/docs/latest/api/accelerator
