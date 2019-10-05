# Notes about what and why should be installed on new computer

## Soft to install, order doesn't matter

1) guake (from sources)
2) vscode
3) dropbox client
4) firefox nightly
5) telegram
6) jetbrains toolbox
7) pycharm
8) datagrip
9) dbeaver
10) gimp
11) krita
12) gedit
13) chromium-browser
14) spotify
15) kleopatra
16) protonmail bridge
17) thunderbird
18) arduino ide
19) audacity
20) blender
21) discord
22) wire
23) riot
24) fbreader
25) gajim with otr
26) htop
27) wine + run some program through wine
28) winetricks
29) obs studio
30) virtualbox
31) pidgin
32) redshift
33) remmina
34) scp
35) transmission
36) vlc
37) tor
38) openvpn
39) python3-dev
40) pip (follow instructions on readthedocs, don't forget -H flag for sudo, and first make python3 alias)
41) pipenv (follow instructions on readthedocs)
42) clang
43) docker
44) docker-compose
45) vagrant
46) zsh + oh my zsh
47) git
48) httpie
49) gcc
50) build-essential
51) ipython
52) pyenv (https://github.com/pyenv/pyenv-installer)
53) screenfetch

## Some configuration, in case xfce, order doesn't matter

1) Change guake hotkey to `Home`
2) Add `guake` to autostart
3) Check `infinite scrolling` in `guake`
4) Copy ssh keys from dropbox to `.ssh` and set them proper mode
5) Import `pgp` keys from dropbox into `Kleopatra`
6) Turn on firefox sync
7) Add thunderbird to autostart and install `KeepInTaskbar` addon, `~/.thunderbird` can be archived and moved from the old computer, but new thunderbird should be stated at least once. [Guide.](https://support.mozilla.org/en-US/kb/moving-thunderbird-data-to-a-new-computer)
8) Setup all thunderbird accounts (proton, bunch of gmails).
9) Make `Soft` and `Projects` directories
10) Add `nightly.desktop` to the home directory
11) Add some cute wallpaper
12) Set `Lavandula` guake theme
13) Set `Adwaita Dark` gtk theme

### Make logitech k380 function keys default

```shell script
sudo apt install gcc, build-essential
git clone https://github.com/jergusg/k380-function-keys-conf
cd k380-function-keys-conf
./build.sh
```

Then, run command that appeared in stdout and turn off & turn on keyboard.

Thanks [jergusg](https://github.com/jergusg)!

### Alias python to python3

```shell script
sudo update-alternatives --install /usr/bin/python python /usr/bin/python3 1
```

### Dell XPS

[ArchWiki](https://wiki.archlinux.org/index.php/Dell_XPS_13_(9360)#Wireless) + [Dell driver](https://github.com/kvalo/ath10k-firmware)
Also, update BIOS.
