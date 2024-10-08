# s2space

A tech test for a mp version of s2s set in space that's based on mp_s2s by [cat or not](https://github.com/catornot).

## Dependencies

As of now, this mod doesn't require any dependencies
## Removed Dependencies

Dependencies that are needed for the original mp_s2s mod but not for this one.

* [cat or not's utils](https://northstar.thunderstore.io/package/cat_or_not/cat_or_nots_utils/)

* [maps plus](https://northstar.thunderstore.io/package/cat_or_not/maps_plus/)

* [DrivableDropShip](https://northstar.thunderstore.io/package/cat_or_not/DrivableDropShip/)

## Debug

set the `s2s_strip_debug` convar to ``1`` and reload the map.

## Installation

This section isn't required (or possible) if you downloaded the mod from thunderstore.

### Concat compressed files

Because of file size large files like the bsp and vpks are compressed and splitted into multiple files. To concat them into their original files just run `concat_assets.sh` or `concat_delete_assets.sh` in the mods root directory.

```bash
cat compressed/assets.tar.gz.* > compressed/assets.tar.gz
tar -xvf compressed/assets.tar.gz
rm -f compressed/assets.tar.gz*
```

### Compressing heavy files

GitHub only allows files up to 100MB and git lfs is shit please split your files instead.

run compress_assets.sh or do this:

```bash
tar cvzf - vpk/client_mp_s2s.bsp.pak000_000.vpk vpk/englishclient_mp_s2s.bsp.pak000_dir.vpk mod/maps/mp_s2s.bsp | split --bytes=90MB - compressed/assets.tar.gz.
```
