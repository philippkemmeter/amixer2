# amixer2

Bash script that is wrapped around amixer to extend amixer with the following
two new options:
- **sinc sID P**: Increases contents for one mixer simple control
- **sdec sID P**: Decreases contents for one mixer simple control

In addition, the help output is more colorful, if you install the colors.lib.

## Synopsis

    Usage: /usr/local/bin/amixer2 <options> [command]

    Available options:
      -h,--help          This help
      -c,--card N        Select the card
      -D,--device N      Select the device, default 'default'
      -d,--debug         Debug mode
      -n,--nocheck       Do not perform range checking
      -v,--version       Print version of this program
      -q,--quiet         Be quiet
      -i,--inactive      Show also inactive controls
      -a,--abstract L    Select abstraction level (none or basic)
      -s,--stdin         Read and execute commands from stdin sequentially
      -R,--raw-volume    Use the raw value (default)
      -M,--mapped-volume Use the mapped volume

    Available commands:
      scontrols          Show all mixer simple controls
      scontents          Show contents of all mixer simple controls (default command)
      sset sID P         Set contents for one mixer simple control
      sget sID           Get contents for one mixer simple control
      sinc sID P         Increases contents for one mixer simple control
      sdec sID P         Decreases contents for one mixer simple control
      controls           Show all controls for given card
      contents           Show contents of all controls for given card
      cset cID P         Set control contents for one control
      cget cID           Get control contents for one control

## Requirements

This tool wraps around `amixer`. Part of `alsa-utils`.

## Colors

If you want colored output, then you have to put the file `colors.lib` in the
same directory as `amixer2`. So downloading the `colors.lib` is optional, but colors
are cool!
