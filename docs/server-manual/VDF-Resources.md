# VDF Resources

VDF resources contain Gothic assets such as textures, models, sounds, animations, worlds, or `GOTHIC.DAT`.

Add the VDF files to `config.toml`:

```toml
addon_vdfs = [
  "addons/base.vdf",
  "addons/patch.vdf"
]
```

The paths are relative to the server directory. Files are loaded in the listed order, so later VDFs can replace files from earlier ones.

- Use `.vdf` files.
- Do not use absolute paths or `..`.
- Every VDF must have a different file name.
- A server can use up to 32 VDF files, each up to 2 GiB.
- Only one VDF may contain `GOTHIC.DAT`.
- When using `GOTHIC.DAT`, `data/instances/items.json` must match its item definitions.

Players download and load the configured VDF files automatically when connecting to the server.
