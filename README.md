[![License](https://img.shields.io/badge/license-BSD--3.0--Clause-blue.svg?style=flat)](https://github.com/emcrisostomo/macports-utils/blob/master/LICENSE)

macports-utils
==============

`macports-utils` contains the following utilities:

  * `port-gen`: an utility to create a Portfile from a template.

Prerequisites
-------------

`macports-utils` requires the following programs to be present on the `${PATH}`:

  * `curl`
  * `openssl`
  * `zsh`

Getting macports-utils
-----------------

A user who whishes to build this package should get a [release
tarball][release].  A release tarball contains everything a user needs to build
the package on his system, following the instructions detailed in the
Installation section below and the `INSTALL` file.

A developer who wishes to modify this package should get the sources (either
from a source tarball or cloning the repository) and have the GNU Build System
installed on his machine.  Please read `README.gnu-build-system` to get further
details about how to bootstrap this package from sources on your machine.

Getting a copy of the source repository is not recommended unless you are a
developer, you have the GNU Build System installed on your machine, and you know
how to bootstrap it on the sources.

[release]: https://github.com/emcrisostomo/macports-utils/releases

Installation
------------

See the `INSTALL` file for detailed information about how to configure and
install this package.

Usage
-----

port-gen
--------

The syntax to invoke `potfile-gen` is the following:

    $ port-gen -h
    $ port-gen (-v)? (--no-cache)? -u distfile_url
    $ port-gen --version

The available options are:

  * `--no-cache`: to always download the distfile.
  * `-h, --help`: to print a usage message.
  * `-u, --url`: to specify the distfile URL.
  * `-v, --verbose`: to print the summary of the outgoing changesets.
  * `--version`: to print the program version.

Bug Reports
-----------

Bug reports can be sent directly to the authors.

-----

Copyright (c) 2018 Enrico Maria Crisostomo

All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

* Redistributions of source code must retain the above copyright notice, this
  list of conditions and the following disclaimer.

* Redistributions in binary form must reproduce the above copyright notice,
  this list of conditions and the following disclaimer in the documentation
  and/or other materials provided with the distribution.

* Neither the name of the copyright holder nor the names of its
  contributors may be used to endorse or promote products derived from
  this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE
FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL
DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER
CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY,
OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE
OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
