# This repository is **deprecated** in favor of better written and better maintened software by **TUXEDO Computers**:
# [TUXEDO drivers](https://gitlab.com/tuxedocomputers/development/packages/tuxedo-drivers)
# [TUXEDO Control Center](https://github.com/tuxedocomputers/tuxedo-control-center)

# ite-829x-ui
An UI for the Linux driver ite-829x

## This script must interact with the driver as root!
There are 2 easiest solutions for this:  
1 - Add a line like this `*YOUR_USERNAME* ALL = NOPASSWD: *PATH_TO_THE_BINARY*/ite-829x` to the file `/etc/sudoers` (replace the text between *);  
2 - Install `pkexec` and replace all `sudo` mentions on the script with `pkexec`;  

## Dependencies
- ite-829x (https://github.com/matheusmoreira/ite-829x)
- bash
- zenity
- grep
- xargs
- sed

## GUI:
```
ite-829x-ui --gui
```

## Command line usage:
### Loading configs (for when the OS boots)
```
ite-829x-ui --load
```

### Effects rotation (for keyboard bindings)
```
ite-829x-ui --toggle -e rotate
```

### Effects selection
```
ite-829x-ui --set -e [0 to 7]
```

### Brightness toggle (for keyboard bindings)
```
ite-829x-ui --toggle -bs [up or down]
```

### Brightness selection
```
ite-829x-ui --set -bs [0 to 4]
```

### Speed toggle (for keyboard bindings)
```
ite-829x-ui --toggle -s [up, down or step ()for cycling]
```

### Speed selection
```
ite-829x-ui --set -s [0 to 3]
```

### Color selection (all keys)
```
ite-829x-ui --set -r [red] -g [green] -b [blue]
```
