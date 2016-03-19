# sublime
My Sublime settings

# Installation on OS-X

1. Install Sublime Text 3
1. Install Package Control: https://packagecontrol.io/installation
1. Install configs that will install the packages I recommend:

    ```console
    > cd ~/
    > git clone https://github.com/inadarei/sublime.git
    > cd sublime
    > # Stop Sublime Text
    > export ST3U="$HOME/Library/Application Support/Sublime Text 3/Packages/User"
    > rm "$ST3U/Preferences.sublime-settings"
    > cp "Package Control.sublime-settings" "$ST3U/Package Control.sublime-settings"  
    > cp "Preferences.sublime-settings" "$ST3U/Preferences.sublime-settings"
    > # Start Sublime Text
    ```

To install terminal integration, put the following in your `~/.bash_profile` or `~/.profile`:

```
alias subl='open -a /Applications/Sublime\ Text.app'
```
