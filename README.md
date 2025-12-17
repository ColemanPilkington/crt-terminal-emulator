# crt-terminal-emulator
This repository has the configurations and supplemental information about how to make a terminal look like a CRT.

## NOTE
-This is the first "how-to guide" that I have made about a program that I have not built myself.
There may be slight inaccuracies for non-MacOS steps. My intent is to have various options
so that both MacOS and Linux users can follow along easily. If there are any issues with 
these steps, please let me know so I may change the instructions!

## System Requirements
- MacOS or Linux. Windows is **not** natively supported.
- Bash and Z-shell have been tested. Other shells have not been tested,
however Ghostty states that it is compatable with all shells.
---

## Step 1: Install Ghostty Terminal Emulator
- Ghostty is only available for MacOS(Apple silicon and Intel chips) and Linux.
- Ghostty is a terminal emulator that supports shaders and graphical overlays.

You can install Ghostty [here](#https://ghostty.org) 
or you can install through the terminal.

MacOS via Homebrew:
```
% > brew install --cask ghostty
```
Arch / Arch-based Linux:
```
% > sudo pacman -S ghostty
```
Fedora:
```
% > sudo dnf install ghostty
```
Ubuntu / Debian - not guaranteed to be in a stable repo yet.
Search for a suitable package using:
```
% > apt search ghostty
```
if no packages are found, you'll need to either build from source or use a 
distro package manager wrapper. 

## Step 2: Setup the ghostty config file

- Ghostty looks in ~/.config/ghostty/config when starting up. If we create this file,
the emulator will automatically apply these changes when we start up a new terminal.
-NOTE: for testing to see new effects, sometimes the entire emulator app needs
to be exited and reoppened. Sometimes "sourcing" or creating a new terminal 
window will suffice, however closing app is the safest bet.

Create the new configuration file like this:
```
% > touch ~/.config/ghostty/config
```
There is **no file extension on purpose**
