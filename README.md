FirefoxPortable
===============

Portable Firefox for Linux (ia32 and amd64 for now)

FXLoader v1.1.1 is a BASH based shell script to run Mozilla Firefox 'Portable' (meaning: no installation required, all user data, including extensions and plugins, will be kept inside the program directory) off of any USB thumb drive or USB hard drive being formatted in a Linux filesystem (FAT32, exFAT or NTFS will not work!).

Usage:

- git clone the repository
- cd into the directory
- chmod +x FXLoader
- ./FXLoader

Upon first start the script will determine your platform (32-Bit or 64-Bit Linux) and download the appropriate archive from Mozilla's servers. That's why there's no Firefox binaries provided. Once downloaded and unpacked Firefox will launch automatically with some defaults taking the 'portable' mode into consideration.

Notes:
- While this makes Firefox portable across systems, you need to keep in mind that if you ran the initial setup on a 64-Bit system it will only work on a 64-Bit system again. If you need to have a 32-Bit and 64-Bit version you need to create yourself two directories each containing the corresponding version (i.e. FirefoxPortable32 and FirefoxPortable64).
- Firefox will make use of any browser plugin installed on your system. As for Adobe Flash Player on 64-Bit system: Invoke FXLoader --help and read the help text.

The script takes the following commandline parameter:

FXLoader -h | --help -> Help text
FXLoader --mkdesktop -> Creates a .desktop file if you plan on running Firefox just off your hard drive from within your user folder.
FXLoader --rmdesktop -> Removes the .desktop file

Everything not matching the above switches will be treated as a passed URL / Argument and forwarded to the Firefox main program.
