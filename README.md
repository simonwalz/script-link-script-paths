# link script paths

Let's organise our shell script files in git repositories. Wait, we don't
want to add all these git repositories to the search path.

This tool links script files into one directory, so we only need to add this
single directory to the path.

## Usage

Run this script in a location with a lot of (git) subfolders containing
shell scripts. The shell scripts with execution bit are linked to
the given target directory.

```sh
cd ~/my_scripts/
link-script-paths [-d] TARGET_DIR
```

##### Options
`-d` = Debug mode. Do not perform any actions.


##### Target directory
The given target directory shall be added to the search path environment.
Add to your `.bashrc`:
```sh
PATH="${PATH}:~/.bin"
```

Or use a global script dir as target.

#### Installation

* Create a target directory as described above or use an existing directory, e.g. `/usr/local/bin`
* Create a directory for all your git script repositories. Let's name it `~/documents/shell-scripts/`
* Clone this repository:
```sh
git clone https://github.com/simonwalz/script-link-script-paths.git
```
* Clone other script repositories:
```sh
git clone https://github.com/simonwalz/git2.git
git clone https://github.com/simonwalz/screen-session.git
git clone https://github.com/simonwalz/exifrename.git
git clone https://github.com/simonwalz/script-git-find-repos.git
git clone https://github.com/simonwalz/script-git-backup.git
```
* Run link-script-paths:
```sh
cd ~/documents/shell-scripts
script-link-script-paths/link-script-paths ~/.bin
```

## Other recommended scripts

##### git
* [script-git-find-repos](https://github.com/simonwalz/script-git-find-repos):  A script to list status of all repositories located in subdirectories.
* [script-git-backup](https://github.com/simonwalz/script-git-backup): Various scripts to backup git repositories (github, gitlab, gitolite).
* [git2](https://github.com/simonwalz/git2): Handle multiple git repositories in one directory.

##### screen
* [screen-save](https://github.com/simonwalz/screen-save): A tool to make screen sessions persistent = survive system reboot.

#### images
* [exifrename](https://github.com/simonwalz/exifrename): A perl script to rename pictures with their EXIF CreateData entry.
