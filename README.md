BLAKESUM
========

Utility to calculate BLAKE-256 or BLAKE-224 checksums.


Installation
------------

From source, if you have Go installed:

	$ go get github.com/dchest/blakesum

Alternatively, download the binary.


Usage
-----

	blakesum [-224] [filename1] [filename2] ...

By default calculates BLAKE-256 sum. Pass option "-224" before filenames to
calculate BLAKE-224.  If no filenames specified, reads from stdin.


Examples
--------

	$ echo -n "Hello world" | blakesum
	7ad560fefa2d287892478dccc5c724694fe21a2f8b004486cc87f76c40618575

	$ echo -n "Hello world" | blakesum -224
	fde00425968221a451c6f06f008bddc44cfdb9d8190507d0fd063707

	$ blakesum /bin/sh /etc/bashrc
	BLAKE-256 (/bin/sh) = b162509ca9f0920d41cec68cb0a2d4037b8d0a89463d888f8e971be085da6786
	BLAKE-256 (/etc/bashrc) = 1cf1a48d8c7bbd8410f270208bb60276b063fcf23608f6c3198b26391cff4e1e
