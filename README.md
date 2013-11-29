The interactive PHP debugger
============================

Implemented as a SAPI module, phpdbg can excert complete control over the environment without impacting the functionality or performance of your code.

phpdbg aims to be a lightweight, powerful, easy to use debugging platform for PHP5.4+

Features
========

 - Stepthrough Debugging
 - Flexible Breakpoints (Class Method, Function, File:Line, Address, Opcode)
 - Easy Access to PHP with built-in eval()
 - Easy Access to Currently Executing Code
 - Userland API
 - SAPI Agnostic - Easily Integrated
 - PHP Configuration File Support
 - JIT Super Globals - Set Your Own !!
 - Optional readline Support - Comfortable Terminal Operation
 - Remote Debugging Support - Bundled Java GUI
 - Easy Operation - See Help :)

Planned
=======

 - Improve Everything :)

Installation
============

To install **phpdbg**, you must compile the source against your PHP installation sources, and enable the SAPI with the configure command.

```
cd /usr/src/php-src/sapi
git clone https://github.com/krakjoe/phpdbg
cd ../
./buildconf --force
./config.nice
make -j8
make install-phpdbg
```

*Note: php must be configured with the switch --with-readline for phpdbg to support history, autocompletion, tab-listing etc*

Command Line Options
====================

The following switches are implemented (just like cli SAPI):

 - -n ignore php ini
 - -c search for php ini in path
 - -z load zend extension
 - -d define php ini entry

The following switches change the default behaviour of phpdbg:

 - -v disables quietness
 - -s enabled stepping
 - -e sets execution context
 - -b boring - disables use of colour on the console
 - -I ignore .phpdbginit (default init file)
 - -i override .phpgdbinit location (implies -I)
 - -O set oplog output file
 - -q do not print banner on startup
 - -r jump straight to run
 - -E enable step through eval()

*Note: passing -rr will cause phpdbg to quit after execution, rather than returning to the console*

Screeny
=======

<img src="https://raw.github.com/krakjoe/phpdbg/master/tutorials/phpdbg.png" alt="screenshot"/>

Getting Started
===============

See the tutorials for help getting started with phpdbg: https://github.com/krakjoe/phpdbg/blob/master/tutorials/intro.md
