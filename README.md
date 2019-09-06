# Perlbrew - a build system for Sublime Text that utilizes the "Perlbrew" Perl version manager!

More to come....

THIS PROJECT IS NOT YET READY FOR USE!


## Installation

Install the package using [Package Control][].
The package's name is <kbd>Perlbrew</kbd>.

Perlbrew was made for **Sublime Text 3**.

[Package Control]: https://packagecontrol.io/

If you do not have Perlbrew installed on your machine, you may 
manually install it by following the instructions at 
[https://perlbrew.pl/](https://perlbrew.pl/), or by running the following command:
```
\curl -L https://install.perlbrew.pl | bash

Or, if your system does not have curl but something else:

# Linux
\wget -O - https://install.perlbrew.pl | bash

# FreeBSD
\fetch -o- https://install.perlbrew.pl | sh
```

If you have Perl installed on your system, you may also try :
```
sudo cpan App::perlbrew
perlbrew init
```


## Getting Started

If you have Perlbrew already installed, you should be able to start 
using Perlbrew without any additional configuration.

If you do not already have Perlbrew installed, you should first run 
the `Install Perlbrew` command before using any other commands in this
module.

Various commands, for configuring and utilizing Perlbrew and the associated Perl versions, are made available through the command palette.

When you install this module, two new build systems will be added to 
the *Tools → Build System* menu, one labeled "<kbd>Perlbrew</kbd>" and other 
simply labeled "<kbd>Perl</kbd>".

The "<kbd>Perlbrew</kbd>" build system will use the currently selected 
Perlbrew version, while the "<kbd>Perl</kbd>" build system will 
attempt to use your system Perl if you have one.

For more information, visit [the Sublime Perlbrew wiki][wiki].

[wiki]: https://github.com/faelin/SublimePerlbrew/wiki


## Features Overview

- Build Systems:

  - <kbd>Perlbrew</kbd> – utilizes the Perlbrew installation of Perl 
  currently active in Sublime.

  - <kbd>Perl</kbd> – utilizes the default Perl indicated by the Shell

- New Commands:
  - <kbd>Install Perlbrew</kbd> — attempts to install a new instance 
  of Perlbrew if it is not already installed.

  *NOTE:* this may modify your $PATH and/or other system variables as 
  per the Perlbrew documentation.

  - <kbd>Perlbrew: Switch To Version</kbd> — allow you to select from the currently installed versions of Perl that Perlbrew is aware of.

  After selecting a Perl version, the <kbd>Perlbrew</kbd> build system
  will use this Perl until a new version is selected.

  - <kbd>Perlbrew: Install Perl</kbd> — lists the currently available 
  Perl versions, and will attempt to install the selected version 
  using Perlbrew.

  - <kbd>Perlbrew: Uninstall Perl</kbd> — lists the currently 
  installed  Perl versions, and will attempt to remove the selected 
  version using Perlbrew.

  - <kbd>Perlbrew: Install Module</kbd> — installs a specified module 
  for the currently selected version of Perl, using <kbd>cpanm</kbd> 
  via Perlbrew.

  If the "Sync Modules" setting is enabled in your user settings, 
  Sublime Perlbrew will automatically attempt to clone new modules to 
  each installed instance of Perl as they are pulled down.

  - <kbd>Perlbrew: Uninstall Module</kbd> — lists the currently 
  installed modules for your current Perl version, and will attempt to 
  uninstall the selected module.

  If the "Sync Modules" setting is enabled in your user settings, 
  Sublime Perlbrew will automatically attempt to remove the selected 
  module from each installed instance of Perl.

  - <kbd>Perlbrew: Uninstall Module (once)</kbd> — as above, but the 
  "Sync Modules" setting is ignored, so that the selected module will 
  only be removed from the active Perlbrew Perl installation.

  *NOTE:* this command is only available when the "Sync Modules" 
  setting is set to <kbd>true</kbd>.

  - <kbd>Perlbrew: Clone Modules</kbd> — copies all installed modules from one Perl version to another.

  This tools is especially useful if you are testing a particular Perl 
  script in several environments, and wish to have your dependencies 
  availabe in multiple installed Perl versions.
