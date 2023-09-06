# mips-intellisense README

Rich language services for MIPS Assembly, and support for debugging with SPIM.

## Features

Current:

- Syntax highlighting support for MIPS in `.s` or `.asm` files (not working)

## Requirements

[Compile your own instance of SPIM from the QtSPIM SourceForge](https://sourceforge.net/p/spimsimulator/code/HEAD/tree/README#l130)

If you are using Windows, it is strongly recommended that you use [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install), as
the build process will be MUCH easier. No need to mess with Cygwin or anything like that.

### Basic Procedure (for Linux)

1. Download the latest version of SPIM from SourceForge.
   ```sh
   wget https://sourceforge.net/code-snapshots/svn/s/sp/spimsimulator/code/spimsimulator-code-r764.zip
   ```
2. Decompress it and enter the directory. Use the appropriate commands to decompress the format it downloads as.
   ```sh
   unzip spimsimulator-code-r764.zip
   cd spimsimulator-code-r764/
   ```
3. Install dependencies from your package manager of choice:
   ```sh
   sudo apt install gcc make bison flex
   ```
4. Enter the SPIM directory, and change any necessary path names in the `Makefile`:
   - EXCEPTION_DIR -- The full pathname of the directory in which to install the spim exception handler (exceptions.s).
   - BIN_DIR -- The full pathname of the directory in which spim should be installed.
   - MAN_DIR -- The full pathname of the directory in which the manual pages for spim should be installed.

5. Compile and install SPIM
   ```sh
   make
   sudo make install
   ```

## Extension Settings

More info soon

## Known Issues

Syntax highlighting does not work

## Release Notes

See [CHANGELOG.md](CHANGELOG.md)
