[![braus](https://snapcraft.io/braus/badge.svg)](https://snapcraft.io/braus)

# Braus
A small application to select a browser every time you click a link anywhere. This is especially useful if you have multiple browsers or profiles, and you want to be able to open certain links in certain browsers. Very useful for web developers, but also for a lot of other people.

GNU/Linux alternative to apps such as Choosy/Browserchooser/Browserosaurus.

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/braus)

## Build
```
$ git clone <repo>
$ cd braus
$ meson build --prefix=$(pwd)/build
$ ninja -C build install
```

### Local launch
```
$ GSETTINGS_SCHEMA_DIR=build/share/glib-2.0/schemas ./build/bin/braus 
```

## Install

### AUR
* `yay` used as example. You can install as standard [AUR](https://wiki.archlinux.org/index.php/Arch_User_Repository) package.
```
$ yay -S braus
```

### From sources
```
$ git clone <repo>
$ cd braus
$ meson build --prefix=/usr
$ ninja -C build install
```

When you run braus for the first time, it will ask you whether you want to set it as your default browser. Ideally you should make it default to actually get the benefit of an app like this.

#### Setting default browsers for URLs
If you want Braus to open URLs in a specific browser, without selecting it every time use the following syntax:
````
braus --set http://my-fancy-url.com firefox.desktop
braus --set http://other.fancy chromium_chromium.desktop
braus --set http://my-videos.org google-chrome.desktop
````

If you made a mistake, clear the auto mapping list by
```
braus --clear
```

---------------

© 2020 Kavya Gokul

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

