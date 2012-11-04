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

	eac-crc (filename of WAV audio)

# Output

It prints the EAC CRC to stdout and nothing else.
The CRC is computed by using shntool to feed the raw audio stream without the WAV header into a standard CRC32 computation.

# Author:

[Leo Bogert](http://leo.bogert.de)

# Version:

1.0

# Donations:

[bitcoin:1PB5EnfzE7wg4ciVrMTF3ht4WDq1UYWBFu](bitcoin:1PB5EnfzE7wg4ciVrMTF3ht4WDq1UYWBFu)
	
# License:

GPLv3