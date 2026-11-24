# Vendor blobs — Infinix X689B (X689B-GL)

Proprietary vendor partition contents extracted from `vendor_a.img`.

## Source

| Field | Value |
|---|---|
| Source image | `vendor_a.img` (ext4, volume label `vendor`) |
| Image size | 1,250,951,168 bytes (~1.17 GiB) |
| Image SHA-256 | `a70040950d1952cb9efecaffecb94929f7b4db5a3b81fd9fbd792ca1db6eaa63` |
| Device | Infinix X689B / X689B-GL |
| Board / SoC | `Infinix-X689B` / MediaTek MT6768 |
| Vendor build | Android 11, `RP1A.200720.011`, incremental `230606V270` |
| Build date | Tue Jun 6 19:21:32 CST 2023 |
| Security patch | 2023-06-05 |
| Fingerprint | `Infinix/X689B-GL/Infinix-X689B:11/RP1A.200720.011/230606V270:user/release-keys` |

The properties above come from `build.prop` inside the image.

## Contents

Exact mirror of the `/` (root) of the vendor partition:

- `app/`, `bin/`, `etc/`, `firmware/`, `lib/`, `lib64/`, `odm/`, `overlay/`, `res/`, `thh/`, `data/`
- `build.prop`, `default.prop`, `ro.prop`, `rw.prop`, `ueventd.rc`

Statistics:

- 1,874 regular files, 182 symlinks, 73 directories
- ~839 MiB of file data (~844 MiB on disk)

`MANIFEST.tsv` records the original path, mode, uid, gid, size, and SHA-256 of
every file (or the symlink target). Git does **not** preserve file ownership,
SELinux labels, or xattrs — use the manifest if you need to restore them.

## Extraction

The image was read directly with `debugfs` from e2fsprogs:

```
debugfs -R "rdump / <output-dir>" vendor_a.img
```

`e2fsck -fn` reported the filesystem as clean. No files were modified.

## Legal note

These are proprietary binary blobs. Copyright and distribution rights belong to
Infinix Mobility Limited, MediaTek, and their respective suppliers. They are
hosted here only for personal backup / development and restoration on the device
they came from. Redistribution may require permission. Use at your own risk.
