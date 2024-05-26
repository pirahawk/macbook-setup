# Mac Install List

## Important locations

* `/usr/local/bin`: Locally installed Software that a normal user may run.
* `/usr/local/sbin`: Locally installed programs for system administration.
* `/bin`: User Utilities fundamental to both single user and multi-user environments. (Such as `bash` `zsh`, `mv`, `cp`, `rm` etc.)
* `/usr/bin`: Common utilities, programming tools and applications. (Contains vital execs such as `grep`, `curl`, `java`, `javac` `ssh` etc.)
* `/sbin` : System programs and administration utilities fundamental to both single-user and multi-user environments. (Contains vital execs such as `md5`, `shutdown`, `ping`, `mount-[filesystem]`, `unmount` etc.). I think these sort of commands would require `su` permissions.
* `/usr/sbin`: System daemons & system utilities (executed by users). I don’t think I would use the tools in here regularly as they have ones like `chown`, `chroot`, `httpd` etc.

>Note: Typically you should aim to install to `usr/local/bin` & `usr/local/sbin` (if required) as these will not mess any of the other files up.

Also look at the path `~/Library/`. Some interesting things stored at that location.


## Setups

### ZSH Shell and zsh profiles on OSX

* Since OSX uses the zsh shell by default, learn about .zsh profiles from [this article](https://www.freecodecamp.org/news/how-do-zsh-configuration-files-work/#:~:text=zprofile%20file%20(versus%20~%2F.,feel%20of%20the%20interactive%20terminal.)
* The advice from the article states that on OSX you want to clearly write to the `~/.zprofile` as its best suited for interactive/non-interactive login shells.
* the zsh shell is located by default in `/bin/zsh`. You can also run the bash shell from `/bin/bash/`
*

### HomeBrew

* Installed from [HomeBrew](https://brew.sh)
* Good [video](https://www.youtube.com/watch?v=whcbOuZ07Iw) to watch.

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Remember to run the next steps:

```
==> Next steps:
- Run these two commands in your terminal to add Homebrew to your PATH:
    (echo; echo 'eval "$(/opt/homebrew/bin/brew shellenv)"') >> /Users/pirantata/.zprofile
    eval "$(/opt/homebrew/bin/brew shellenv)"
- Run brew help to get started
- Further documentation:
    https://docs.brew.sh

```

Where is the Homebrew installed? Can get this information via the following command:
```
> brew --prefix
```


Where are packages in the HomeBrew Cellar located?: 
* See this location on machine `/opt/homebrew/bin`
	* This in turn links to `/opt/homebrew/Cellar` which is the Brew Cellar. Things are symlinked from here.
	* There is also `/opt/homebrew/Caskroom` etc etc.


Update homebrew
```
> brew update
```


If you want to know how brew went about installing a formula (I.e. package) the see below in the case of installing `jq`. This will tell you what was installed and what was symlinked etc.
```
> brew info jq
```

If you want to know which `tap` repositories homebrew is currently using go:
```
>brew tap
```

## Installs


### Direct From Source

| Install-Name | Install-Instruction |
|-|-|
| nodejs | Installed using `NVM` as per instructions on https://nodejs.org/en/download/package-manager  . This means that you will now use `nvm` to upgrade nodejs versions |
| dotnet | Install direct from website |


### Using Homebrew

|Package-Name | Package-Install-Instruction |
|-|-|
| jq | `brew install jq` |
| git | `brew install git` |
| python | `brew install python@3.10` |
| azure-cli | `brew update && brew install azure-cli` |

### Other installs

| Install-Name | Install-Instruction |
|-|-|
| Rosetta 2 | Install using `softwareupdate --install-rosetta`. Required for docker destop |
| Docker Desktop | Installed using .dmg downloaded directly from site |
| Visual Studio Code | Installed using .dmg downloaded directly from site |
| Github Desktop | Installed using .dmg downloaded directly from site |

## Nuget

All global nuget package installs are located at `~/.nuget/packages` on osx.

