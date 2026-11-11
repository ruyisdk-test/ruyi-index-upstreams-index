# armbian-os

Armbian rolling (nightly / `os`) images.

The former upstream repository [armbian/os](https://github.com/armbian/os) is **archived**
(2026-11-03) and no longer publishes releases. Images and artifacts are now published from
[armbian/ci](https://github.com/armbian/ci), which hosts the reusable build pipeline for the
nightly, stable, community and apps tracks and attaches the resulting images to its GitHub
Releases (e.g. tag `26.11.0-trunk.128`, 349 assets).

`github` therefore points at `armbian/ci`. The directory keeps its historical name so that
existing external references (test bot upstream keys, links) stay valid.

Notes for packaging:

+ Images are mirrored at `mirror://armbian-archive/cache/os/`, which only keeps the current
  version directory; older versions disappear from the mirror.
+ Only `minimal` variants are produced for the `os` track since `26.11.0-trunk.`*. There are no
  desktop/`xfce` images, so `armbian-spacemit-musepipro-xfce` cannot be bumped from this track.
+ No per-image checksum files are published; `*.checksums` assets only exist for a few `OTA`
  artifacts, so checksums for `img.xz` must be computed locally.
