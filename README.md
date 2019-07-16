# osc-plugin-install_script [![Build Status](https://travis-ci.org/openSUSE/osc-plugin-install.svg?branch=master)](https://travis-ci.org/openSUSE/osc-plugin-install)

Plugin to make package installation easier.


## Usage

This osc plugin extends osc with the subcommand 'osc install'.
The main effort of this plugin is to free the end-user of the sometimes tedious
task to look up the correct repository URL to be used with zypper.
Dependencies are resolved across projects, just as the online one-click mechanism
would do.
The plugin can also guess the best matching platform for your system.

Example usage:

```
osc co PROJ PACK ; cd PACK
do osc build ; vi ... ; osc ci ; osc results
osc in
```


## Contribute

This project lives in https://github.com/openSUSE/osc-plugin-install

Feel free to add issues in github or send pull requests.

TODOs and ideas are tracked in the file `TODO` as well as github issues.


### Testing

Probably the easiest way to test is to ensure that the plugin is not installed
by any system package and then symlink the plugin file into ~/.osc-plugins and
call example commands, for example:

```
ln -s $PWD/osc-install.py ~/.osc-plugins/
osc in bash
```


### Rules for commits

* Please make sure to test your changes

* For git commit messages use the rules stated on
  [How to Write a Git Commit Message](http://chris.beams.io/posts/git-commit/) as
  a reference

If this is too much hassle for you feel free to provide incomplete pull
requests for consideration or create an issue with a code change proposal.

## License

This project is licensed under the GPLv2 or GPLv3 license, see LICENSE file
for details.

