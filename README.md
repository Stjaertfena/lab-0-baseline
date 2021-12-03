# Lab 0 - Baseline
![Tools](./docs/tools.jpeg)
Photo by <a href="https://unsplash.com/@carlevarino?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Cesar Carlevarino Aragon</a> on <a href="https://unsplash.com/s/photos/tools?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

## Purpose & Goal
- Make sure all relevant Git tools are working on your machine
  - [Git > v2.34.0][1]
  - [gitk](http://git-scm.com/docs/gitk)
  - [git-gui](http://git-scm.com/docs/git-gui)
- Verify auto complete for Git CLI is working
- Have [SSH connectivity][2] with GitHub
- Verify local Git config is set up

## Expectations
- Work on your own machine, but feel free to help each other out

## The assignment
### Installing Git (gitk + git-gui)
1. Verify if Git is installed or not, and if you are running the latest version using:
```
$ git --version
git version 2.34.1
```
If you see above output you are all good and can continue to the next section. Other wise, you first need to install Git by downloading it from [here][1].

1. Follow

### Configuring CLI auto complete
1. Verify if your Git CLI auto complete is already working by typing `git sw` in your terminal and hit **_tab_** – if everything is working it should automatically complete you command to `git switch`.

1. If this is not the case you need to enable auto complete for your particular system, whether it's `bash`, `zsh`, `Windows Console`, `Windows Powershell`, or `Cygwin`.

### Configuring your local Git config
With both Git and auto complete working it's time to make sure you have some basic configuration in place. With Git there are three different places configuration can be set:
- `$(prefix)/etc/gitconfig` (System-wide configuration file)
- `~/.gitconfig` (User specific configuration file, a.k.a "global" config)
- `.git/config` (Repository specific configuration file)

Configuration is read by Git top down, with last value found taking precedence over values read earlier.

In this case we're interested in verifying your "global" config, which is applicable across all Git projects on your machine.

1. Read the configurations already present using:
```
$ git config --list --global
```
1. Make sure the following attributes are set.
```
user.name=Alexis Määttä Vinkler
user.email=alexis@flatwave.se
init.defaultbranch=main
```
If not, set them up accordingly:
```
$ git config --global user.name "Donald Duck"
$ git config --global user.email "donald.duck@duckburg.com"
$ git config --global init.defaultBranch "main"
```
1. Verify through step 1 that all settings now looks as expected.

### Settings up SSH connectivity with GitHub
- Follow [this][2] manual for install instructions

[1]: http://git-scm.com/downloads "Git"
[2]: (https://docs.github.com/en/authentication/connecting-to-github-with-ssh "SSH"
