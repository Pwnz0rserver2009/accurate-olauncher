# Project Status
The original Olauncher is on hiatus, so if something breaks and a fork doesn't fix it, you're screwed.

## How to build from source
The commands must be run in the following order to build from source:
- `decompile.sh`
  - Downloads original jar and decompiles it
- `init.sh`
  - Turns decompiled sources into a git repository
- `applyPatches.sh`
  - Applies OLauncher patches to the decompiled sources
- `mvn clean package`
  - Compiles the patched launcher
- `genredist.sh` (optional)
  - Make sure you've run `git submodule update --init` as this script uses the `AutoOL` submodule.
  - Generates the redistributable JAR - Do not distribute the JARs in `olauncher/target`!
