# Signal Library

Plugin block definitions for FastTrack Studio's Signal system.

Each JSON file captures a complete introspection snapshot of a DAW plugin:
- Plugin identity (name, vendor, type, parameter count)
- Full raw parameter dump from REAPER
- `PluginBlockDef` scaffold for virtual module/block organization
- Per-block `ParamCuration` and `MacroBank` configs (added during curation)

## Generating entries

```bash
# Introspect a single FX (track 0, FX slot 0)
fts daw introspect 0 0

# Introspect all FX across all tracks into this repo
fts daw introspect --all --output-dir ./plugins
```

## Directory structure

```
plugins/
├── <vendor-slug>/
│   ├── <plugin-slug>.json
│   └── ...
```
