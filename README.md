# Carve
Simple command line tool to carve data out of a file using start and end memory addresses

# Usage

```
usage: carve [-h] [-s START_ADDRESS] [-e END_ADDRESS] [--hex] file

positional arguments:
  file                  Path to the file

optional arguments:
  -h, --help            show this help message and exit
  -s START_ADDRESS, --start-address START_ADDRESS
                        Beginning memory address to carve
  -e END_ADDRESS, --end-address END_ADDRESS
                        End memory address to carve
  --hex                 Format output as ASCII hex
```

# Example

Regular use
```
$ ./carve -s 0x001 -e 0x030 /etc/passwd
#
# User Database
#
# Note that this file is c[amorris] ~/Projects/carve 
```

Hex output
```
$ ./carve -s 0x001 -e 0x030 --hex /etc/passwd
230a2320557365722044617461626173650a23200a23204e6f7465207468617420746869732066696c652069732063
```
