# Installing Xdebug for XAMPP with PHP 7.x

* New: [XAMPP - XDebug Setup for PHP 8](https://odan.github.io/2020/12/03/xampp-xdebug-setup-php8.html)

## Requirements

* XAMPP for Windows: https://www.apachefriends.org/download.html
* [Microsoft Visual C++ Redistributable for Visual Studio 2015, 2017 and 2019](https://support.microsoft.com/help/2977003/the-latest-supported-visual-c-downloads)

## Setup

If the file `C:\xampp\php\ext\php_xdebug.dll` already exists, you can skip the download.

* Download Xdebug for the specific PHP version:

  * PHP 7.4 (64-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.4-vc15-x86_64.dll
  * PHP 7.4 (32-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.4-vc15.dll
  * PHP 7.3 (64-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.3-vc15-x86_64.dll
  * PHP 7.3 (32-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.3-vc15.dll
  * PHP 7.2 (32-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.2-vc15.dll
  * PHP 7.1 (32-Bit): https://xdebug.org/files/php_xdebug-2.9.7-7.1-vc14.dll
  * PHP 7.0 (32-Bit): https://xdebug.org/files/php_xdebug-2.6.1-7.0-vc14.dll
 
* Move the downloaded dll file to: `C:\xampp\php\ext`

* Open the file `C:\xampp\php\php.ini` with Notepad++

* Disable output buffering: `output_buffering = Off`

* Scroll down to the `[XDebug]` section (or create it) and copy/paste these lines:

```ini
[XDebug]
zend_extension = "c:\xampp\php\ext\php_xdebug.dll"
;zend_extension = "c:\xampp\php\ext\php_xdebug-2.9.7-7.4-vc15-x86_64.dll"
xdebug.remote_autostart = 1
xdebug.profiler_append = 0
xdebug.profiler_enable = 0
xdebug.profiler_enable_trigger = 0
xdebug.profiler_output_dir = "c:\xampp\tmp"
;xdebug.profiler_output_name = "cachegrind.out.%t-%s"
xdebug.remote_enable = 1
xdebug.remote_handler = "dbgp"
xdebug.remote_host = "127.0.0.1"
xdebug.remote_log = "c:\xampp\tmp\xdebug.txt"
xdebug.remote_port = 9000
xdebug.trace_output_dir = "c:\xampp\tmp"
;36000 = 10h
xdebug.remote_cookie_expire_time = 36000
```

* Restart Apache

* Click the Github &#9733; Star button :-)

## PhpStorm

* Use the [PhpStorm bookmarklets generator](https://www.jetbrains.com/phpstorm/marklets/) to activate Xdebug from the browser side.
* Enable the Xdebug option: "Can accept external connections". See [screenshot](https://user-images.githubusercontent.com/781074/83182499-ba9e7f00-a126-11ea-88c0-f28d0cbff260.png)

## Netbeans

* Change the Netbeans debugging options: https://user-images.githubusercontent.com/781074/39868196-c98f15a0-5458-11e8-8143-d8c44079e099.jpg
* Change the following key in php.ini: `xdebug.idekey="netbeans-xdebug"`

## Visual Studio Code

* [Installing XDebug on anything for VSCode in 5 minutes](https://technex.us/2020/06/installing-xdebug-on-anything-for-vscode-in-5-minutes/)
* Install the [PHP Debug Adapter for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug).
* [Debug PHP In VSCode With XDebug](https://www.codewall.co.uk/debug-php-in-vscode-with-xdebug/)

## Adobe Brackets

* Install the [PHP Debugger for Brackets](https://github.com/spocke/php-debugger).

## Sublime Text 2 and 3

* Install the [Xdebug Client Package](https://packagecontrol.io/packages/Xdebug%20Client)

## Start debugger from the console

Enter cmd:

```
set XDEBUG_CONFIG="idekey=xdebug"
php test.php
```

## Postman

Add `XDEBUG_SESSION_START=PHPSTORM` as query parameter to the url, e.g.

* http://localhost?XDEBUG_SESSION_START=PHPSTORM


Follow me on [Twitter](https://twitter.com/dopitz) | [Blog](https://odan.github.io)