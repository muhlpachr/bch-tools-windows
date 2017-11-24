<a href="https://www.bigclown.com/"><img src="https://bigclown.sirv.com/logo.png" width="200" height="59" alt="BigClown Logo" align="right"></a>

# BigClown Tools for Windows
For Microsoft Windows 7, 8, 10 (32bit and 64bit).

NOTE: Internet connectivity is required during installation. Be patient during Downloading and Extracting, some packages (e.g. GNU ARM Embedded Toolchain) are huge.

## Instalation

1. Execute PowerShell

    * `Win + x` `i` on Windows 10 or
    * Execute **Command Prompt** `cmd.exe` from Start and then `powershel` or
    * Execute **Windows PowerShell** from Start

    Prompt should start with `PS `

2. Make sure Powershell 3 is installed

        $psversiontable.psversion.major

    Major version should be 3 or higher.

    If you are on Windows 8 or 10 you should be all set, on Windows 7 install [Windows Management Framework 3.0](https://www.microsoft.com/en-us/download/details.aspx?id=34595) where PowerShell 3 is included. After installation execute PowerShell (see 1.).

3. Install [Scoop](http://scoop.sh/) command-line installer for Windows

    * `set-executionpolicy remotesigned -scope currentuser`
    * `iex (new-object net.webclient).downloadstring('https://get.scoop.sh')`

    You may have a look at [Scope Dcocumentation](https://github.com/lukesampson/scoop/wiki/Quick-Start)

4. Add repositories to Scoop (Scoop name them Buckets)

    * `scoop bucket add extras`
    * `scoop bucket add bigclown https://github.com/muhlpachr/bch-tools-windows.git`
    * `scoop update`

## Install individual BigClown toolset components

### BigClown Toolchain

In PowerShell execute:

    **`scoop install bigclown-toolchain`**

Components:
* [GNU ARM Embedded Toolchain](https://developer.arm.com/open-source/gnu-toolchain/gnu-rm)
* [GNU Make](https://www.gnu.org/software/make/)
* [USB DFU Device Firmware Upgrade Utilities](http://dfu-util.sourceforge.net)
* [BigClown Firmware Tool](https://github.com/bigclownlabs/bch-firmware-tool)

TIP: Install [concfg](https://github.com/lukesampson/concfg) utility to import and export Windows console settings like fonts and colors:
* `scoop install concfg`
* `concfg import solarized medium`

### BigClown Hardware Drivers TODO

## Install all BigClown tools

* TODO

Made with &#x2764;&nbsp; by [**HARDWARIO s.r.o.**](https://www.hardwario.com/) in the heart of Europe.
