# Notes about what and why should be installed on new computer

## Soft to install, order doesn't matter

1) guake (from sources)
2) vscode
3) dropbox client
4) firefox nightly (set proxy config from `.pac` file for `.onion` access)
5) telegram
6) jetbrains toolbox
7) pycharm
8) datagrip
9) dbeaver
10) gimp (through flatpak)
11) krita (from ppa, also install debugging symbols and translations)
12) gedit
13) chromium-browser
14) spotify (configure their debian repo)
15) kleopatra (probably, tests will show that I should install `scdaemon`)
16) protonmail bridge
17) thunderbird
18) arduino ide (from `.tar.gz` on official site, it updates automatically)
19) audacity
20) blender
21) discord
22) wire
23) riot
24) okular (for `fb2`, yeah, too much qt dependencies, but it's worth of it)
25) pidgin with otr (with new `exploit.im` account)
26) pidgin-otr (enable, generate new key in pidgin)
27) htop
28) obs studio (has it's own ppa)
29) virtualbox (deb package on official site)
30) redshift (enable autorun)
31) remmina
32) transmission
33) vlc
34) apt-transport-tor
35) tor (add nightly package repositories into `/etc/apt/sources.list`, use `.onion` repo links, [guide](https://2019.www.torproject.org/docs/debian.html.en#apt-over-tor))
36) deb.torproject.org-keyring
37) tor browser (extract in `Soft`, start it, and create link on panel)
38) openvpn
39) python3-dev
40) pip (follow instructions on readthedocs, don't forget -H flag for sudo, and first make python3 alias with instruction below)
41) pipenv (currently `pip install --user --upgrade pipenv`, but may appear in popular distros in future, `~/.local/bin` should be in `PATH`)
42) clang
43) docker (guide on official site, as for `Sat Oct  5 20:46:03 EEST 2019` `add-apt-repository` broken, so deb source should be added manually. After installation proceed post-installation steps in docs)
44) docker-compose (`pip install --user docker-compose`)
45) zsh + oh my zsh
46) git
47) build-essential
48) ipython (`pip install --user jupyter`)
49) pyenv,  [here is the installer](https://github.com/pyenv/pyenv-installer), don't forget to install python build dependencies
50) screenfetch
51) virtualenv (`sudo -H pip install virtualenv`, only after all aliasing and pip installing will be done)
52) poetry
53) python3-venv


### Firefox nightly addons
1) Decentraleyes
2) Firefox Multi-Account Containers
3) LanguageTool
4) React Developer Tools
5) Todoist
6) Tomato Clock
7) uBlock Origin
8) LastPass
9) Redirector
    1) Import settings from `Redirector.json`

## Some configuration, in case xfce, order doesn't matter

1) Change guake hotkey to `Home`
2) Add `guake` to autostart
3) Check `infinite scrolling` in `guake`
4) Copy ssh keys from dropbox to `.ssh` and set them proper mode
5) Import `pgp` keys from dropbox into `Kleopatra`
6) Turn on firefox sync
7) Add thunderbird to autostart and install `KeepInTaskbar` addon. Also, install `TT DeepDark` theme. `~/.thunderbird` can be archived and moved from the old computer, but new thunderbird should be stated at least once. [Guide.](https://support.mozilla.org/en-US/kb/moving-thunderbird-data-to-a-new-computer).
8) If protonmail bridge used, then local password for `protonmail` account in Thunderbird should be changed.
9) Make `Soft` and `Projects` directories
10) Add `nightly.desktop` to the home directory
11) Set up wallpaper from dropbox
12) Set `Solarized Dark Higher Contrast` guake theme
13) Set `Adwaita Dark` gtk theme
14) Set `Adwaita Dark` gtk theme for `guake`
15) Log in at JetBrains Toolbox
16) To change greeter background: `sudo rm /usr/share/backgrounds/linuxmint/default_background.jpg` & `sudo cp ~/wallpaper.jpg /usr/share/backgrounds/linuxmint/default_background.jpg`.

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

[ArchWiki](https://wiki.archlinux.org/index.php/Dell_XPS_13_(9360)#Wireless) + [Dell driver](https://github.com/kvalo/ath10k-firmware). Thanks [kvalo](https://github.com/kvalo).
Also, update BIOS.


### proxy.pac

To specify `.pac` path in forefox, you should go `Preferences` -> `Network Settings` -> `Automatic proxy configuration URL`
and specify something like `file://<path_to_dot_pac_file>`.


### Digital wellbeing

#### Loading pause
1) https://github.com/OskarDamkjaer/FirefoxDelayWebpage
2) List of energy-consuming resources:
```
hckrnews\.com
reddit\.com
facebook\.com
news\.ycombinator\.com
youtube\.com
linux\.org.ru
habr\.com
```
