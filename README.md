# Marble shell theme
Shell theme for GNOME DE. Based on https://www.pling.com/p/1939902/.

![Available colors:](https://shields.io/badge/-Available%20colors:-0d1117?style=flat-square)
![red](https://shields.io/badge/-red-red?style=flat-square)
![yellow](https://shields.io/badge/-yellow-yellow?style=flat-square)
![green](https://shields.io/badge/-green-green?style=flat-square)
![blue](https://shields.io/badge/-blue-blue?style=flat-square)
![purple](https://shields.io/badge/-purple-purple?style=flat-square)
![pink](https://shields.io/badge/-pink-pink?style=flat-square)
![or different Hue color.](https://shields.io/badge/-or%20different%20Hue%20color.-0d1117?style=flat-square)

## 🏞 Screenshots

<details><summary>Click me 🐈</summary>

Icon theme: https://github.com/vinceliuice/Colloid-icon-theme
#### Overview [[Blur My Shell](https://extensions.gnome.org/extension/3193/blur-my-shell/) / Light / Dark] (Fold [light](https://gitlab.gnome.org/GNOME/gnome-backgrounds/-/raw/gnome-45/backgrounds/fold-l.jpg?ref_type=heads) / [dark](https://gitlab.gnome.org/GNOME/gnome-backgrounds/-/raw/gnome-45/backgrounds/fold-d.jpg?ref_type=heads))
![Overview with Blur My Shell](./readme-images/overview_blur-my-shell.png?raw=true "Overview with Blur My Shell")
![Overview in light mode](./readme-images/overview_light.png?raw=true "Overview in light mode")
![Overview in dark mode](./readme-images/overview_dark.png?raw=true "Overview in dark mode")

#### Panel
![Panel look](./readme-images/panel.png?raw=true "Panel look")
#### Quick settings ([Fresh green leaves with fragile veins](https://www.pexels.com/photo/fresh-green-leaves-with-fragile-veins-6423448/) / [Close-Up Photo of Wrinkled Parchment Paper](https://www.pexels.com/photo/close-up-photo-of-wrinkled-parchment-paper-7233131/))
![Quick settings look](./readme-images/qs.png?raw=true "Quick settings look")

#### Modal dialog ([Wide Angle Photography of Mountain](https://www.pexels.com/photo/wide-angle-photography-of-mountain-1612559/))
![Modal dialog look](./readme-images/modal.png "Modal dialog look")
#### Calendar & notifications ([Wallpaper](https://www.zedge.net/wallpaper/7e10d448-6440-405d-a847-30b6146eeb55))
![Calendar & notifications look](./readme-images/notifications.png?raw=true)

#### Dash ([Dash To Dock](https://extensions.gnome.org/extension/307/dash-to-dock/ "Dash To Dock"))
- Position and size:
  - Icon size: 42px.
- Appearance:
  - Shrink the dash.
  - Default opacity.

![Dash look](./readme-images/dash.png?raw=true "Dash look")

</details>

## 🚧 Requirements
- GNOME 43, 44, 45. Correct functionality on other versions is not guaranteed.
- [User Themes](https://extensions.gnome.org/extension/19/user-themes/ "User Themes") extension.
- [GNOME Tweaks](https://gitlab.gnome.org/GNOME/gnome-tweaks "GNOME Tweaks").
- Python 3.2+.

## 💡 Installation
1. Open the terminal.
2. Clone the git repository and change the directory:
   ```shell
   git clone https://github.com/imarkoff/Marble-shell-theme.git
   cd Marble-shell-theme
   ```
3. Run the program (install all accent colors, light & dark mode): 
   ```shell
   python install.py -a
   ```
   - [more vibrant color](./readme-images/qs.png?raw=true) in active buttons:
      ```shell
      python install.py -a --filled
      ``` 
4. After successful file creation open GNOME Tweaks, go to `Appearance - Themes - Shell`.
5. Select the shell theme you want.


## 🖥️ GDM theme

![GDM theme](./readme-images/gdm.png?raw=true)

1. Open the terminal.
2. Go to the directory with the theme.
3. Run the program with the `--gdm` option
   ```shell
   sudo python install.py --gdm (--your color) (--is filled)
   ```
    - Example:
        ```shell
        sudo python install.py --gdm --blue --filled
        ```
4. After successful file restart GDM service:
   ```shell
   sudo systemctl restart gdm
   ```

- 🗑️ If you want to remove the theme, run the program with the `--remove` option:
    ```shell
    sudo python install.py --gdm -r
    ```
- ☠️ If you got a death screen, you can switch to the console with the `Ctrl + Alt + F3` key combination, log in, go to the `Marble-shell-theme` directory and run the command above. If it doesn't help, try reinstalling `gnome-shell` package.


## 🏮 Installation tweaks

#### Install default color
You can install several themes in one string: `python install.py --red --green --blue`

| Option    | Description                         |
|-----------|-------------------------------------|
| -a, --all | Install all available accent colors |
| --red     | red theme only                      |
| --pink    | pink theme only                     |
| --purple  | purple theme only                   |
| --blue    | blue theme only                     |
| --green   | green theme only                    |
| --yellow  | yellow theme only                   |
| --gray    | gray theme only                     |

#### Install custom color
| Option | Secondary option | Description                              |
|--------|------------------|------------------------------------------|
| --hue  | (0 - 360)        | Generate theme from Hue prompt [0 - 360] |
| --name | NAME             | Custom theme name                        |

#### Theme colors
| Option   | Description                    |
|----------|--------------------------------|
| --filled | Make accent color [more vibrant](./readme-images/qs.png?raw=true) |

#### Optional theme tweaks
| Option | Secondary option | Description                                                |
|--------|------------------|------------------------------------------------------------|
| --mode | light / dark     | light / dark theme only                                    |
| --sat  | (0 - 250)        | custom color saturation (<100% - reduce, >100% - increase) |

#### Panel tweaks

**Panel default size**

![Panel default size](./readme-images/tweaks/panel-default-size.png "Panel default size")

**Panel without button background**

![Panel without buttons background](./readme-images/tweaks/panel-no-pill.png "Panel without buttons background")

| Option                     | Secondary option | Description                    |
|----------------------------|------------------|--------------------------------|
| -Pds, --panel_default_size |                  | set default panel size         |
| -Pnp, --panel_no_pill      |                  | remove panel button background |
| -Ptc, --panel_text_color   | #abcdef          | custom panel HEX(A) text color |

#### Overview tweaks

**Launchpad icon**

![Dash with launchpad icon](./readme-images/tweaks/dash-with-launchpad.png "Dash with launchpad icon")

| Command     | Description                                   |
|-------------|-----------------------------------------------|
| --launchpad | Change Show Apps icon to MacOS Launchpad icon |

#### Examples
| Command                                        | Description                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| -a                                             | Install all accent colors with light & dark mode                     |
| --all --mode dark                              | Install all accent colors with dark mode only                        |
| --purple --mode=light                          | Install purple accent color with light mode only                     |
| --hue 150 --name coldgreen                     | Install custom coldgreen accent color, light & dark mode             |
| --red --green --sat=70                         | red, green accent colors, 70% of the stock saturation                |
| --hue=200 --name=grayblue --sat=50 --mode=dark | custom grayblue accent color, 50% of the stock saturation, dark mode |
