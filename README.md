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
