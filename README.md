# nixos-config

`sudo ln -s ~/nixos-config /etc/nixos`
once applied run `sway --unsupported-gpu` to start the gui. If on the laptop keyboard, add `XKB_DEFAULT_LAYOUT=dvorak`.

USB drives should mount automatically, but if they don't use `udiskctl (un)mount -b /dev/sdX`.
Toggle between `dvorak` and `us` keyboard layouts with caps lock.

- Use `nmtui` to manager network stuff.
- Use `spt` for Spotify. You need to have your spotify password on disk at a `chmod 600` `.local/spotifyd_pass` file.
- If you need full battery charge before taking the laptop to-go, run `sudo tlp fullcharge`.
- For now `systemctl --user start docker` to enable docker on a per-run basis. I had it `enable`d in systemctl, but an upgrade broke that when the symlink changed.
- `nix-shell -p kooha` for screen recording.

## TODO

- move Insomnia collections over
- move over rust build settings
- try https://github.com/uowuo/abaddon
- fix move workspace freeze
- try moving from vscode to helix (once https://github.com/helix-editor/helix/pull/2507 and https://github.com/helix-editor/helix/pull/5768) are merged, or off the flake in the ts branch if you get impatient
