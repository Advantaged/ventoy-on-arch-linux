# ventoy-on-arch-linux
## Ventoy.md
* Merit to [Ventoy "1"](https://www.ventoy.net/en/doc_start.html) & [Ventoy "2"](https://www.ventoy.net/en/doc_linux_gui.html).

### Prerequisite
1. Update your system

```
yes | sudo pacman -Syyuu

```

In case the kernel was updated, restart you system.

### 1. Install
1. Install the right `exfat` & `ventoy` package (2024-02-29) with the highest version...
```
1 extra/exfat-utils 1.4.0-2 [0 B 237.93 KiB] [Installed]
    Utilities for exFAT file system

1 aur/ventoy 1.0.97-2 [+12 ~1.71]
    A new bootable USB solution

```

2. Proper install command

```
yes | paru -S exfat-utils ventoy

```

### 2. Solve problems

1. Dependencies-problems

If you encounter problems with dependencies, [uninstall the problematic packages with](https://linuxhint.com/remove_package_dependencies_pacman_arch_linux/):

`sudo pacman -Rcns` or `yes | sudo pacman -Rcns` or `yes | paru -Rcns`

2. In case you still have dependencies problems on packages you ***already removed***, reinstall the removed packages and remove it again through the above commands.

3. Appearances Problems

If you use KDE/Plasma the GUI-application can be show falsified because Ventoy use Gtk, to solve this problem under plasma:

* Right-Click on Kickoff ("Application Menu"),

* click on "Edit Applications",

* search for "ventoy",

* click in case on "General" on the right side,

* look for "Program:",

* replace `ventoygui` with `ventoygui --qt5` or add simply one space ➕ `--qt5`,

* click  on "Save" on left-side up,

* & close "KDE Menu Editor".


✅ ***Done & Enjoy***❗️
