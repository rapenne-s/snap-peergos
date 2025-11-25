# peergos packaged as snap

This repository purpose is to package [peergos web-ui](https://github.com/peergos/web-ui) as a snap.

[![Get it from the Snap Store](https://snapcraft.io/en/light/install.svg)](https://snapcraft.io/peergos)

# How to install

Make sure you have `snap` installed, then run: `snap install peergos`

# How to update

Although your system certainly offer to update snap program as part of a routine job, you can force it manually with: `snap refresh peergos`

# How to use

Run `peergos`

# Where are peergos internal data?

By default, peergos data are stored in `$HOME/snap/peergos/current/`, this can be changed by defining a new path in the environment variable `PEERGOS_PATH` when running `peergos`.

# Limitations

Because of snap sandboxing rules, peergos snap is not allowed to read dotfiles from your home directory.

When using the **Sync** feature, the error `Mount point not found` appears due to the sandboxing. This is because peergos tries to list mountpoints and it is not allowed to do so. The only drawback, apart the extra error, is that peergos is not able to verify the free disk space to stop synchronizing if the filesystem is nearly full.
