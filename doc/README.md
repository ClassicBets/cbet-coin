ClassicBets Core
=====================

Setup
---------------------
[ClassicBets Core](https://classicbets.net) is the original ClassicBets client and it builds the backbone of the network. However, it downloads and stores the entire history of ClassicBets transactions; depending on the speed of your computer and network connection, the synchronization process can take anywhere from a few hours to a day or more. Thankfully you only have to do this once.

Running
---------------------
The following are some helpful notes on how to run ClassicBets on your native platform.

### Unix

Unpack the files into a directory and run:

- bin/32/classicbets-qt (GUI, 32-bit) or bin/32/classicbetsd (headless, 32-bit)
- bin/64/classicbets-qt (GUI, 64-bit) or bin/64/classicbetsd (headless, 64-bit)

### Windows

Unpack the files into a directory, and then run classicbets-qt.exe.

### OSX

Will be available on July'19 !
Unpack the files into a directory, and then run classicbets-qt.

### Need Help?

* Join our Discord server [Discord Server](https://discord.classibets.com)

Building
---------------------
The following are developer notes on how to build ClassicBets on your native platform. They are not complete guides, but include notes on the necessary libraries, compile flags, etc.

- [OSX Build Notes](build-osx.md)
- [Unix Build Notes](build-unix.md)

Development
---------------------
The ClassicBets repo's [root README](https://github.com/ClassicBets/cbet-coin/blob/master/README.md) contains relevant information on the development process and automated testing.

License
---------------------
Distributed under the [MIT/X11 software license](http://www.opensource.org/licenses/mit-license.php).
This product includes software developed by the OpenSSL Project for use in the [OpenSSL Toolkit](https://www.openssl.org/). This product includes
cryptographic software written by Eric Young ([eay@cryptsoft.com](mailto:eay@cryptsoft.com)), and UPnP software written by Thomas Bernard.
