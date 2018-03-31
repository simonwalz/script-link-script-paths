# link script paths

Let's organise our shell script files in git repositories. Wait, we don't
want to add all these git repositories to the search path.

This tool links script files into one directory. So we only have to add this
single directory to the path.

## Usage

Run this script in a location with a lot of (git) subfolders containing
shell scripts. The shell scripts with execution bit are linked to
the given target directory.

```sh
cd ~/my_scripts/
link-script-path [-d] TARGET_DIR
```

##### Options
`-d` = Debug mode. Do not perform any actions.


##### Target directory
The given target directory shall added to the path environment.
Add to your `.bashrc`:
```sh
PATH="${PATH}:~/my_scripts"
```

Or use a global script dir as target.

