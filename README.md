# python-pixi-environment
This repository includes a test pixi environment for the gw1774 class being held in Albuquerque, New Mexico in late January 2024. Instructions for installing pixi and the class environment are given below.

## Clone this repository

Clone this repository by opening Powershell on Windows or the terminal on MacOS and Linux. Clone the repository in a directory of your choosing (_e.g._ `training_classes\`) using

```bash
git clone https://github.com/jdhughes-usgs/python-pixi-environment.git
```

This will create a `python-pixi-environment` subdirectory in the directory the `git clone` command was executed in.

## Install pixi

Installation of pixi is relatively simple. Additional information on installing pixi can be found at https://pixi.sh/#installation

### Windows
Open PowerShell and type the following

```powershell
iwr -useb https://pixi.sh/install.ps1 | iex
```

If you get a error indicating `iwr : The request was aborted: Could not create SSL/TLS secure channel` try the following

```powershell
[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 Invoke-WebRequest -Uri https://pixi.sh/install.ps1 | iex
```

Note: Only x86_64 versions of Windows are supported

### MacOS and Linux

Open a terminal and type the following

```bash
curl -fsSL https://pixi.sh/install.sh | bash
```

### Test the pixi installation

Close PowerShell on Windows or the terminal on MacOS and Linux and reopen PowerShell or the terminal. Type the following command

```bash
pixi
```

If the pixi installation was successful, the following should be written to the screen

```text
A package management and workflow tool

Usage: pixi.exe [OPTIONS] <COMMAND>

Commands:
  completion  Generates a completion script for a shell
  init        Creates a new project
  add         Adds a dependency to the project
  run         Runs task in project
  shell       Start a shell in the pixi environment of the project
  global      Global is the main entry point for the part of pixi that executes on the global(system) level
  auth        Login to prefix.dev or anaconda.org servers to access private channels
  install     Install all dependencies
  task        Command management in project
  info        Information about the system and project
  upload      Upload a package to a prefix.dev channel
  search      Search a package, output will list the latest version of package
  project     Modify the project configuration file through the command line
  remove      Remove the dependency from the project
  help        Print this message or the help of the given subcommand(s)

Options:
  -v, --verbose...     More output per occurrence
  -q, --quiet...       Less output per occurrence
      --color <COLOR>  Whether the log needs to be colored [default: auto] [possible values: always, never, auto]
  -h, --help           Print help
  -V, --version        Print version
```

## Install the class pixi environment

Navigate to the `python-pixi-environment` subdirectory in PowerShell or the terminal. Run the following command

```bash
pixi run install
```

If the class pixi environment was successfully installed you should see

```text
Successful testing of pixi environment for gw1774
```

in the last line of the information output to the screen during the environment installation process.
