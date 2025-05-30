Sure! Here’s a Flameshot Setup Guide in the format you requested:

---

## 📸 Flameshot Setup Guide

### ✅ What is Flameshot?

**Flameshot** is a powerful, easy-to-use screenshot tool with a graphical interface and annotation features. It allows you to take screenshots, annotate them (draw arrows, boxes, highlight areas, add text), and upload or save images quickly. It’s perfect for minimal window managers like i3.

---

### 🖥️ Step 1: Install Flameshot

#### Arch Linux:

```bash
sudo pacman -S flameshot
```

#### Debian/Ubuntu:

```bash
sudo apt update
sudo apt install flameshot
```

#### Fedora:

```bash
sudo dnf install flameshot
```

#### macOS (Homebrew):

```bash
brew install flameshot
```

---

### ⚙️ Step 2: Basic Usage

Run Flameshot GUI:

```bash
flameshot gui
```

This lets you select a screen area interactively and then annotate the screenshot before saving or copying.

---

### 🧰 Step 3: Configure Flameshot with i3

To use Flameshot efficiently with i3wm, bind it to a hotkey in your i3 config file `~/.config/i3/config`. For example, to bind Flameshot to the **Print Screen** key:

```bash
bindsym Print exec --no-startup-id flameshot gui
```

You can also bind it to a key combination, for example `Mod+Shift+s`:

```bash
bindsym $mod+Shift+s exec --no-startup-id flameshot gui
```

After editing your config, reload i3 with `Mod+Shift+R`.

---

### 🖌️ Step 4: Flameshot Annotation Tools Overview

After triggering Flameshot GUI, you can:

* Draw rectangles, circles, arrows, lines
* Highlight areas
* Add text
* Blur sensitive info
* Undo/redo edits before saving
* Save, copy to clipboard, or upload screenshot

---

### 💾 Step 5: Save Location & Clipboard

By default, after editing, Flameshot lets you save anywhere or copy the screenshot to clipboard. You can customize the default save path or behavior via command-line options or scripts.

---

### 🚀 Step 6: Launch Flameshot at Startup (Optional)

Add Flameshot to your i3 startup programs to have the tray icon available:

```bash
exec --no-startup-id flameshot &
```

This lets you access Flameshot quickly from the tray (if you run a tray in i3).

---

### 🔧 Step 7: Advanced Command-Line Options

* Take a full-screen screenshot and save it automatically:

```bash
flameshot full -p ~/Pictures/Screenshots
```

* Take a screenshot of an area without GUI (silent mode):

```bash
flameshot gui -r
```

* Copy screenshot directly to clipboard:

```bash
flameshot gui -c
```

* Upload screenshot to image hosting and get the URL:

```bash
flameshot gui -u
```

---

### 📚 Additional Resources

* Official GitHub: [https://github.com/flameshot-org/flameshot](https://github.com/flameshot-org/flameshot)
* Arch Wiki: [Flameshot](https://wiki.archlinux.org/title/Flameshot)
* Man page: `man flameshot`

---

If you want, I can help you set up example i3 keybindings or scripts for Flameshot!
