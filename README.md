# Sublime Setup for JS/Node Devs

[Sublime Text](https://www.sublimetext.com/) is the greatest text editor that is very easy to hate. I should know: I hated it for years. And the reason is: it is super barebone/unappearlin out of the box. And it is super-confusing to get a nice setup, unless somebody shows you the ropes. Well, [somebody](https://github.com/gogasan) did eventually show me how to get started and I quickly fell in love with Sublime. In order to help others get over the initial steep setup curve - I created this repo.

# Installation on OS-X

1. Install Sublime Text 3
1. Install Package Control: https://packagecontrol.io/installation
1. Restart Sublime 
2. Install configs that will install the packages I recommend:

    ```console
    > cd ~/
    > git clone https://github.com/inadarei/sublime.git
    > cd sublime
    > # Stop Sublime Text
    > export ST3U="$HOME/Library/Application Support/Sublime Text 3/Packages/User"
    > test -f "$ST3U/Preferences.sublime-settings" && rm "$ST3U/Preferences.sublime-settings"
    > cp "Package Control.sublime-settings" "$ST3U/Package Control.sublime-settings"  
    > # Start Sublime Text
    > # Show Sublime's Console by clicking `Ctrl + ``. Wait until every missing package is installed. 
    > # You may get some annoying alerts. 
    > # Stop Sublime
    > cd "$HOME/Library/Application Support/Sublime Text 3/Packages/tern_for_sublime"
    > npm install && cd -
    > cp -R colour-schemes/* "$ST3U"
    > cp *-settings "$ST3U/"
    > # Start Sublime
    ```

### Terminal Integration 

To install terminal integration, put the following in your `~/.bash_profile` or `~/.profile`:

```
alias subl='open -a /Applications/Sublime\ Text.app'
```

### More Information

1. To find more awesome packages you may enjoy: https://packagecontrol.io/
2. To install a package: `Cmd+Shift+P` and then type: `Install Package` + Enter + package name
3. To remove a package: `Cmd+Shift+P` and then type: `Remove Package` + Enter + package name
4. If you are like me and love seeing open files on the sidebar, instead of tab bar:
    - View -> SideBar -> Show Open Files
    - View -> Hide Tabs
