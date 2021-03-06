# arpspoof for macOS

This repo extracts the arpspoof util from macOS fixed
[dsniff](https://www.monkey.org/~dugsong/dsniff/) toolkit forked from [@ggreer](https://github.com/ggreer). The installing script itself is free, I
don't mind any commercial usage. And that means all the users should be fully
responsible to any consequences caused by using this script.

    arpspoof

    Redirect packets from a target host (or from all hosts) intended for
    another host on the LAN to ourselves.

    Copyright (c) 1999, 2000 Dug Song <dugsong@monkey.org>
    All rights reserved, all wrongs reversed.

    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions
    are met:

    1. Redistributions of source code must retain the above copyright
       notice, this list of conditions and the following disclaimer.
    2. Redistributions in binary form must reproduce the above copyright
       notice, this list of conditions and the following disclaimer in the
       documentation and/or other materials provided with the distribution.
    3. The name of author may not be used to endorse or promote products
       derived from this software without specific prior written permission.

    THIS SOFTWARE IS PROVIDED ''AS IS'' AND ANY EXPRESS OR IMPLIED WARRANTIES,
    INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY
    AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL
    THE AUTHOR BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
    EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
    PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS;
    OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY,
    WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR
    OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
    ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

### Clone the sources

```BASH_SOURCE
git clone https://github.com/SuperMarcus/macos-arpspoof.git
cd macos-arpspoof
```

### Using the script

It's pretty convenient to use the `./build` script to compile and install the
program. But first of all you should make sure that you've got your
[Homebrew](http://brew.sh) installed.

Run the following code to install Homebrew

```BASH_SOURCE
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Compiling

To compile the source, execute the following code

```BASH_SOURCE
./build build
```

The `./build` script supports custom compiler. If you want to use other
compilers, pass the path of the compiler as an argument like the following

```BASH_SOURCE
./build build "/usr/bin/gcc"
```

### Installing

The `./build` script can install the binary program and man page of the program.
Run the following commands

```BASH_SOURCE
./build install
```

If you would like to install the program to another place, pass the place you
want to install the program as an argument

```BASH_SOURCE
./build install ~/Desktop
```

Note that if you specified the custom location, man pages will not be installed

### Uninstalling

The `./build` script could help you uninstall the program when you no longer
need it

```BASH_SOURCE
./build uninstall
```
