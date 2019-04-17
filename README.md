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

NOTES:
1. These settings configure Sublime Text to use the [Fira Code](https://github.com/tonsky/FiraCode) font.  Instructions on installing Fira Code are available [here](https://github.com/tonsky/FiraCode/wiki).
2. You may want to install `clang-format` and `cppcheck`.
3. Locations of some key directories for code completion are specfied in the [SublimeLinter](http://www.sublimelinter.com) settings.
4. Theme settings do not seem to be preserved upon initial package setup.

asdf
