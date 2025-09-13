# untmp
Export your containers or make your changes permanant.
Options:
1. Make an squashfs and...
* 1.1 put it in /srv/containers               --srv, -s
* 1.2 put it in /var/lib/tmplinux             --def, -d
* 1.3 put it in the current working directory (default)

2. Copy the rootfs to an folder and...
* 2.1 put it in /srv/chroots                  (default)
* 2.2 put it in the current working directory --cwd, -c

## Syntax
```
untmp [type] (--flags) [name]
```

## Examples
Make your changes from the latest tmparch container permanant
```
untmp sfs --def tmparch
```
or:
```
untmp 1.2 tmparch
```
Turn the current working directory into an chrot with the container with the hostname `container-AbC3`
```
untmp folder -c c-AbC3
```
or:
```
untmp 2.2 c-AbC3
```
Make the latest tmpgentoo container into an sfs that could be installed onto an system
```
untmp sfs tmpgentoo
```
or:
```
untmp 1.3 tmpgentoo
```

