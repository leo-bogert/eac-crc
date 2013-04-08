eac-crc
=======

# Description

A bash script to compute the CRC of WAV files which Exact Audio Copy shows in its log files.

# Installation:

This script was written on Ubuntu 12.04 amd64. It should work on any Debian-based Distribution.
For using it, the following packages need to be installed:

	shntool
	rhash

# Syntax:

For normal operation:

	eac-crc (filename of WAV audio)

To only print the version number:

	eac-crc --version

# Output

Upon success, it prints the EAC CRC to stdout and nothing else. The CRC is computed by using shncat to feed the raw audio stream without the WAV header into a standard CRC32 computation.

Upon failure of shncat (for example when the input file is not found), nothing is printed to stdout. An error message is printed to stderr and the exit code of shncat is returned.

# Exit code

The exit code is zero upon success and non-zero upon failure.

Upon failure, the exit code of shncat or rhash might be returned.
Shncat is piped to rhash and bash option "pipefail" is used to obtain the exit code. For determining which exit code is returned upon failure, read up the "pipefail" bash option.

# Author:

[Leo Bogert](http://leo.bogert.de)

# Version:

1.2

# Donations:

[bitcoin:1PB5EnfzE7wg4ciVrMTF3ht4WDq1UYWBFu](bitcoin:1PB5EnfzE7wg4ciVrMTF3ht4WDq1UYWBFu)
	
# License:

GPLv3
