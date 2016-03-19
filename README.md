# Sublime setup for JavaScript/Node Development

Sublime Text is the greatest text editor that is very easy to hate. I should know: I hated it for years. And the reason is: it is very barebone and super-confusing to get a nice setup, unless somebody mentors you. Well, somebody did eventually show me how to get started and I quickly fell in love. In order to help others get over the initial steep setup curve - I created this repo.

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
    > cp "*-settings" "$ST3U/"
    > # Start Sublime

    ```

To install terminal integration, put the following in your `~/.bash_profile` or `~/.profile`:

```
alias subl='open -a /Applications/Sublime\ Text.app'
```
