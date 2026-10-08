# opensuse-tumbleweed-oxwm



install x11 packages

```bash
sudo zypper install -t pattern x11
```

install x11 devel packages

```bash
sudo zypper install \
    libX11-devel \
    libXinerama-devel \
    libXft-devel \
    fontconfig-devel \
    freetype2-devel \
    libXrandr-devel \
    libXext-devel \
    libXrender-devel
```

install oxwm defaults and basic tools

```bash
sudo zypper install alacritty dmenu git-core neovim zig0.16
```

clone and build

```bash
git clone https://github.com/tonybanters/oxwm
cd oxwm
zig build -Doptimize=ReleaseSmall --prefix /usr
```

create ~/.xinitrc

```bash
touch ~/.xinitrc
```

add to `~/.xinitrc`

```bash
!#/bin/bash

exec wm
```

after logging in, use `startx` to launch x11



