# linux

Personal dotfiles for Alpine, Arch, Debian and Fedora.

## install

    git clone https://github.com/Shroudmoa/linux ~/linux
    cd ~/linux
    ./bootstrap

Components are selected interactively. Configs are symlinked from this repo
into `~/.config`, so `git pull` updates them live. Existing files are moved to
`~/.dotfiles-backup/<timestamp>/`.

## flags

    --all                install every component
    --only nvim,fish     install selected components
    --copy               copy files instead of symlinking
    --no-deps            skip package installation
    --fonts              download JetBrainsMono NF and CaskaydiaCove NF
    --dry-run            print actions without changing anything
    --yes                assume yes, no prompts
    --help               show usage

## notes

Package tables live in `deps/`, one file per package manager. AUR packages in
`deps/aur` are installed with paru or yay when available.

`nvim/` is already an NvChad starter config, no separate clone is needed. The
installer deploys it and runs `Lazy! restore`.

`waybar`, `swaync` and `quickshell` configs are not part of this repo, so the
hypr component only warns about them.

On Alpine, Hyprland needs edge/testing and the hypr scripts assume systemd.

`--fonts` needs `curl` and `unzip`.
