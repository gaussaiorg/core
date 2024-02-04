Gaussai Core staging tree 18.0
===========================

|CI|master|develop|
|-|-|-|
|Gitlab|[![Build Status](https://gitlab.com/gaussaipay/gaussai/badges/master/pipeline.svg)](https://gitlab.com/gaussaipay/gaussai/-/tree/master)|[![Build Status](https://gitlab.com/gaussaipay/gaussai/badges/develop/pipeline.svg)](https://gitlab.com/gaussaipay/gaussai/-/tree/develop)|

https://www.gaussai.org

For an immediately usable, binary version of the Gaussai Core software, see
https://www.gaussai.org/downloads/.

Further information about Gaussai Core is available in the [doc folder](/doc).

What is Gaussai?
-------------

Gaussai is an experimental digital currency that enables instant, private
payments to anyone, anywhere in the world. Gaussai uses peer-to-peer technology
to operate with no central authority: managing transactions and issuing money
are carried out collectively by the network. Gaussai Core is the name of the open
source software which enables the use of this currency.


For more information read the original Gaussai whitepaper.

License
-------

Gaussai Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is meant to be stable. Development is normally done in separate branches.
[Tags](https://github.com/gaussaiorg/tags) are created to indicate new official,
stable release versions of Gaussai Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Gaussai Core's Transifex page](https://www.transifex.com/projects/p/gaussai/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Tutorial - Mine for blocks with Microsoft Windows
------------
Mine for blocks with your Windows wallet and the following instructions.

Click here to download the file gaussai-qt-windows.zip.

Open File Explorer and go to your downloads directory.

Extract the zip file gaussai-qt-windows.zip

Open "Run" with the keyboard shortcut winkey + r.

Enter the following text behind "Open": notepad

Press on the button "OK".

Paste the following into notepad.

rpcuser=rpc_gaussai rpcpassword=dR2oBQ3K1zYMZQtJFZeAerhWxaJ5Lqeq9J2 rpcbind=127.0.0.1 rpcallowip=127.0.0.1 listen=1 server=1 addnode=node3.walletbuilders.com

Click on the menu item "File" -> "Save As...".

The open dialog box will appear, click on "Save as type" and select the option "All Files (.)".

Enter the following text behind "File name": gaussai.conf

Click on the menu bar, type the following text %appdata% and press on the enter key. enter

Create the folder Gaussai and open the folder.

Press on the button "Save".

Create a new file with the keyboard shortcut ctrl + n.

Paste the following into notepad.

@echo off set SCRIPT_PATH=%cd% cd %SCRIPT_PATH% echo Press [CTRL+C] to stop mining. :begin for /f %%i in ('gaussai-cli.exe getnewaddress') do set WALLET_ADDRESS=%%i gaussai-cli.exe generatetoaddress 1 %WALLET_ADDRESS% goto begin

Click on the menu item "File" -> "Save As...".

The open dialog box will appear, click on "Save as type" and select the option "All Files (.)".

Enter the following text behind "File name": mine.bat

Click on the menu bar, open the location where you extracted the zip file gaussai-qt-windows.zip.

Press on the button "Save".

Open your wallet and execute mine.bat to mine your first block.


Tutorial - Automated installation and mine for blocks with Ubuntu Desktop
------------
Install and mine for blocks automatically with your Linux wallet.

The tutorial is compatible with Ubuntu Desktop 22.04 and above.

Click here to download the file gaussai-auto.sh.
https://gaussai.org/gaussai-auto-liunx.sh

Open a Terminal window.

Make the install file executable with the following command:

chmod +x $HOME/Downloads/gaussai-auto.sh

Open Files and go to your Downloads directory.

Select the file gaussai-auto.sh, press the right button of your mouse and click on "Run as a Program" to automatically install your wallet and mine your first block.

Enter your Ubuntu user password when requested.
