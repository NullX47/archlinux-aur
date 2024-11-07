![Repo Build Status](https://img.shields.io/github/actions/workflow/status/nullx47/archlinux-aur/run-build-repo.yaml?label=REPO%20BUILD&logo=archlinux&logoColor=white&style=for-the-badge)
![Renovate](https://img.shields.io/github/actions/workflow/status/nullx47/archlinux-aur/run-renovate.yaml?label=renovate&logo=RenovateBot&logoColor=white&style=for-the-badge)  
![GitHub release (release name instead of tag name)](https://img.shields.io/github/v/release/nullx47/archlinux-aur?display_name=release&include_prereleases&label=Latest%20Repo%20Build&logo=archlinux&style=for-the-badge)  
![Packages Count](https://img.shields.io/endpoint?url=https://gist.githubusercontent.com/nullx47/627f5c8e17e8deb5326a692079b04625/raw/count-arch-packages.json)


## My Archlinux repo
This is an unofficial repository for Arch Linux.  
Originaly intended to fit my needs and build custom or unavailable packages.

### How to use it
- Trust my public key:
```
pacman-key --init
curl -sL 'https://keybase.io/apinon/pgp_keys.asc?fingerprint=%' | sudo pacman-key -a -
pacman-key --lsign-key %
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
