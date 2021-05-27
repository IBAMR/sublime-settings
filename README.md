# IBAMR Project Settings and Packages for Sublime Text 4

The following instructions will set up the packages and basic configuration on a Mac.
**_NOTE_:** They will remove any customization that you may have already made to Sublime, and so use with caution.
1. [Install Sublime Package Control](https://packagecontrol.io/installation)
2. Close Sublime Text
3. Open Terminal and input the following commands:
```
# Navigate to the Sublime Text 4 Package directory:
cd ~/Library/Application\ Support/Sublime\ Text/Packages

# (NOTE: For Sublime Text 3, this directory is named ~/Library/Application\ Support/Sublime\ Text\ 3/Packages)

# Delete the User folder within this directory:
rm -r User

# Copy the contents of the User directory from the repository to ~/Library:
cp -r /path/to/IBAMR-sublime-settings/User
```
4. Open Sublime Text.
Package Control will automatically download the necessary Sublime Text packages.
5. Close Sublime Text.

There is also a Sublime Text project file template for IBAMR that is intended to be placed in the IBAMR source code directory.  To set up this project:
```
cd /path/to/IBAMR
cp scripts/project_templates/sublime/ibamr.sublime-project.template ./ibamr.sublime-project
```
The `.gitignore` file in IBAMR is configured so that files named `*.sublime-project` or `*.sublime-workspace` are not tracked by git.  This facilitates customization of the project files.

To get code full completion, it is necessary to install `clangd`, which is provided by the `llvm` package in Homebrew.
Once `clangd` is available, it is necessary create either a `compile_commands.json` file or a `compile_flags.txt` file.
The purpose of this file is to inform `clangd` of key compiler flags.
Our current recommendation is to create a `compiler_flags.txt` file, since this allows code completion to work "out of the box" for any source code file in the project.

An extremely rudimentary script is also available to create a `compile_commands.json` file in `IBAMR/scripts/setup_compile_commands.sh`.  This script requires users to install `scan-build` and `compdb`:
```
pip install scan-build
pip install compdb
```

NOTES:
1. These settings configure Sublime Text to use the [Fira Code](https://github.com/tonsky/FiraCode) font.  Instructions on installing Fira Code are available [here](https://github.com/tonsky/FiraCode/wiki).
2. You may wish to install `clang-format` and `cppcheck`, although recent versions of `clangd` also will format code using `clang-format`.
