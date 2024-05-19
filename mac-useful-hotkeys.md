# OSX Hotkeys list

Please refer to the extensive list of all [keyboard shortcuts](https://support.apple.com/en-gb/HT201236)

| Combo | Definition|
|-|-|
|`ctrl+cmd+Q` | desktop - Lock screen |
|`ctrl+cmd+F` | desktop - enter/exit full screen |
|`cmd+tab` | desktop - cycle through open apps |
|`cmd+space` | desktop - open spotlight search |
|`cmd+mission-control` |  desktop - Show desktop|
|`shift+cmd+5` |  desktop - take screenshot |
|`shift+cmd+4` |  desktop - take more awesome screenshot |
|`fn + F3`| mission control|
|-|-|
|`opt+cmd+d` | dock - show/hide dock |
|-|-|
| [FINDER]-> `shift+cmd+g` | finder - when opening finder, this opens Go-To-Folder dialog window in Finder to allow pasting file path |
|`opt+ctrl+p|finder - see entire path at bottom of window|
|`cmd+shift+.`|finder - see hidden files in finder|
|`opt+cmd+del` | finder - delete file/folder permanently |
|`cmd+shift+.` | finder - show hidden files |


# Visual studio Mac hotkeys

Please refer to the extensive list of all [keyboard shortcuts](https://docs.microsoft.com/en-us/visualstudio/mac/keyboard-shortcuts?view=vsmac-2019)


| Combo | Definition|
|-|-|
|`cmd+.` | open global symbol search |
|`cmd+d` | Go to type, property, field, var etc declaration|
|`shift+cmd+p` | command search (opens in global search window) |
|`shift+cmd+r` | Find all references |
|`shift+cmd+f` | Open Find in Solution window |
| - | - |
|`cmd+r` | rename |
|`cmd+/` | toggle line comments |
|`ctrl+i` | Format Document |
|`ctrl+space` | invoke intellisense: auto-complete, suggestions etc |
|`opt+enter` | invoke suggestions menu (auto-import, code fixes etc) |
| - | - |
|`cmd+B` | Build |
|`ctrl+cmd+B` | Build all |
|`cmd+enter` | run with debug |
|`opt+cmd+enter` | run without debug |


# Visual studio Code hotkeys

| Combo | Definition|
|-|-|
|`cmd+p` | open code command picker |
| `shift+opt+[mouse select]`| invoke multiline select|
| `ctrl+` `| show/hide terminal |


# Chrome hotkeys

Refer to [Devtools-shortcuts](https://developers.google.com/web/tools/chrome-devtools/shortcuts)

| Combo | Definition|
|-|-|
|`shft+cmd+C  OR F12` | open dev tools inspector |
|`cmd+p` | open global file search |



# Show hidden files in all folders

make hidden files and folders visible requires you to use Terminal.

    Open Terminal
    Run the following script:
    $ defaults write com.apple.Finder AppleShowAllFiles true
    $ killall Finder

# Find where a command is installed
example to locate the func runtime:

```
> which func
/usr/local/bin/func
```

or for dotnet

```
> which dotnet
/usr/local/share/dotnet/dotnet
```

# Install .pkg file from terminal

```
sudo installer -pkg dotnet-sdk-3.1.101-osx-x64.pkg -target /
```

# Finder Show POSIX File path always - Shows the file path with the slashes

```
defaults write com.apple.finder _FXShowPosixPathInTitle -bool YES
Killall Finder
```