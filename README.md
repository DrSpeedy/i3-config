# i3-config
Template based multihead i3wm configuration


## Basic usage:
Currently these configs/scripts are designed to go under `$HOME/.dotfiles/i3`, this can easily be changed but all scripts must be updated.

##### Generate new config:
```sh
$ /path/to/scripts/genconf
```
Generating a new config will automatically compile all files under `./template/*` together into `./config` based on priorety numbered priorety.


##### Choose new theme
```sh
$ /path/to/scripts/gentheme <path to theme> > /path/to/template/09-colors.conf
$ /path/to/scripts/genconf
```
An example theme can be found under `./themes/`. This script was inspired by acrisci/i3-style as a way to continue using 
his themes with the template system.

##### Multihead mode
The configuration is already set up to display workspaces 1-5 on `$mon1` and 6-10 on `$mon2` so long as the system is actually displaying on them.
Use: Option 1: docked mode; Option 2: undocked mode
```sh
$ /path/to/scripts/multiheadmsw <number>
```
This script was put together to switch back and forth between docked/undocked mode on my laptop.
