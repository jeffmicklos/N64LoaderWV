# N64 ROM Loader for Ghidra by Warranty Voider

this is a loader module for ghidra for N64 roms (.z64, .n64, .v64)
- fixes endianess (little, big, mixed) at loading
- loads ram, rom and boot section into ghidra
- it can use a pattern file to scan for symbol hints
- it can load symbol files from N64sym

this allows a rom to be labeled, disassembled and decompiled

credits:
- [blackgamma7](https://github.com/blackgamma7) for fixing memory layout stuff, adding register symbols and various small changes [see merge commit](https://github.com/zeroKilo/N64LoaderWV/commit/46137048775a41f4b54c08cf3c3fab1bcb962219)
- [dmattia](https://github.com/dmattia) for adding build instructions for mac

requires JDK 13

[![Alt text](https://img.youtube.com/vi/3d3a39LuCwc/0.jpg)](https://www.youtube.com/watch?v=3d3a39LuCwc)

[![Alt text](https://img.youtube.com/vi/fhI3Vpw7FVk/0.jpg)](https://www.youtube.com/watch?v=fhI3Vpw7FVk)

## Build from Source (Mac)

```bash
brew install java
brew install gradle
brew cask install ghidra

export GHIDRA_INSTALL_DIR=`brew cask ls ghidra | grep ghidra | sed 's/^.*-> \(.*\)ghidraRun.*/\1/'`
```

Then whenever you're ready to build, run

```bash
gradle
```

and it will create a zip file in `/dist` that you can use that file as the extension in Ghidra
