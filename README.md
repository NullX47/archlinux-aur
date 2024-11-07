![Repo Build Status](https://img.shields.io/github/actions/workflow/status/nullx47/archlinux-aur/aur_repo_build.yml?label=REPO%20BUILD&logo=archlinux&logoColor=white&style=for-the-badge)
![GitHub release (release name instead of tag name)](https://img.shields.io/github/v/release/nullx47/archlinux-aur?display_name=release&include_prereleases&label=Latest%20Repo%20Build&logo=archlinux&style=for-the-badge)  
![Packages Count](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/nullx47/132942d2df637468bab091c818632abb/raw/count-arch-packages.json)


## My Archlinux repo
This is an unofficial repository for Arch Linux.  
Originaly intended to fit my needs and build custom or unavailable packages.

### How to use it
- Trust my public key:
```
pacman-key --init
curl -sL 'https://keybase.io/nullx47/pgp_keys.asc?fingerprint=5CD03BF7BFB59CF89BC920028D0C96815D9E7713' | sudo pacman-key -a -
pacman-key --lsign-key 5CD03BF7BFB59CF89BC920028D0C96815D9E7713
```

- Edit `/etc/pacman.conf` with:
```
[archlinux-aur]
Server = https://github.com/NullX47/$repo/releases/download/$arch
SigLevel = Required
```

- Then update the DB:
```
pacman -Syy
```
