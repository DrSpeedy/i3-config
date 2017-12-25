# i3-config
Template based multihead i3wm configuration

## Installation:

#### via curl:
```sh
$ sh -c "$(curl -L https://raw.githubusercontent.com/DrSpeedy/i3-config/master/scripts/install-config)"
```

#### manually via git:
```sh
$ git clone https://github.com/DrSpeedy/i3-config.git ~/.config/i3
```

### Enviornment Variables:
Add these to the top of your bashrc/zshrc configurations
```sh
export I3_CONFIG=/path/to/config
export PATH=$I3_CONFIG/scripts:$PATH
```

## Basic usage:
Currently these configs/scripts are designed to go under `$HOME/.dotfiles/i3`, this can easily be changed but all scripts must be updated.

### Generate new config:
```sh
$ genconf
```
Generating a new config will automatically compile all files under `i3/template/*` together into `i3/config` based on priorety numbered priorety.


### Choose new theme:
```sh
$ gentheme <path to theme>      # Apply the colorscheme to the 09-colors.conf template
$ genconf                       # Regenereate the config
$ i3-msg restart                # Restart i3
```
An example theme can be found under `i3/themes/`. This script was inspired by acrisci/i3-style as a way to continue using 
his themes with the template system.

### Multihead mode:
The configuration is already set up to display workspaces 1-5 on `$mon1` and 6-10 on `$mon2` so long as the system is actually displaying on them.
Use: Option 1: docked workstation mode; Option 2: undocked mode; Option 3: TV mode
```sh
$ multiheadmsw <option>
```
This script was put together to switch back and forth between docked/undocked mode on my laptop.
