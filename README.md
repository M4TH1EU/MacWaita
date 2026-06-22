# MacWaita

An automated hybrid GNOME icon theme. It combines the system-level integration of [MoreWaita](https://github.com/somepaulo/MoreWaita) with the application icons from [MacTahoe](https://github.com/vinceliuice/MacTahoe-icon-theme).

## Installation

1. Download the latest `.zip` from the [Releases](../../releases/latest) page.
2. Extract the archive and move the `MacWaita` folder to your local icons directory:
```bash
   mv MacWaita ~/.local/share/icons/
```

3. Apply the theme using GNOME Tweaks.

*(For system-wide installation, move the folder to `/usr/share/icons/` instead).*

## Build Process

This theme is not manually maintained. A GitHub Action runs daily to pull the latest upstream changes and publish a new release.

The build script:

1. Clones MoreWaita to use as the base.
2. Clones MacTahoe.
3. Updates the `index.theme` name to `MacWaita`.
4. Overwrites `MoreWaita/scalable/apps/` with the contents of `MacTahoe/src/apps/scalable/`.
5. Zips and publishes the final directory.

## Credits

All icon design work belongs to the original authors:

* Base theme: [MoreWaita](https://github.com/somepaulo/MoreWaita) by somepaulo
* Application icons: [MacTahoe](https://github.com/vinceliuice/MacTahoe-icon-theme) by vinceliuice
