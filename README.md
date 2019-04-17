# IBAMR Project Settings and Packages for Sublime Text 3

To install on a Mac:
1. [Install Sublime Package Control](https://packagecontrol.io/installation)
2. Close Sublime Text
3. Open Terminal and input the following commands:
```
# Navigate to the Sublime Text 3 Package directory:
cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/

# Delete the User folder within this directory:
rm -r User

# Copy the contents of the User directory from the repository to ~/Library:
cp -r /path/to/IBAMR-sublime-settings/User
```
4. Open Sublime Text.
Package Control will automatically download the necessary Sublime Text packages.
5. Reset the [Material Theme](https://github.com/equinusocio/material-theme).
6. Close Sublime Text.

There is also a Sublime Text Project file template for IBAMR that is intended to be placed in the IBAMR source code directory.  To set up this project:
```
cd /path/to/IBAMR
cp scripts/project_templates/sublime/ibamr.sublime-project.template ./ibamr.sublime-project
```
The `.gitignore` file is configured so that files named `*.sublime-project` or `*.sublime-workspace` are not tracked by git.  This facilitates customization of the project files.  Currently, the intention is for new project templates to go into the main IBAMR repository.

To get code full completion, it is necessary to create a `compile_commands.json` file.  An extremely rudimentary script to do this is currently provided in `IBAMR/scripts/setup_compile_commands.sh`.  It requires users to install `scan-build` and `compdb`:
```
pip install scan-build
pip install compdb
```

NOTES:
1. These settings configure Sublime Text to use the [Fira Code](https://github.com/tonsky/FiraCode) font.  Instructions on installing Fira Code are available [here](https://github.com/tonsky/FiraCode/wiki).
2. You may want to install `clang-format` and `cppcheck`.
3. Locations of some key directories for code completion are specfied in the [SublimeLinter](http://www.sublimelinter.com) settings.
4. Theme settings do not seem to be preserved upon initial package setup.
