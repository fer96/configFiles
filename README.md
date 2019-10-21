# Configuration files

A simple repository to set a nice terminal for MacOS in a simple and fastest way

## Previous requirements

+	Install [Homebrew](https://brew.sh/) (open-source software package management system)
```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
+ Install [Sublime Text](https://www.sublimetext.com/3)

## Step by step

1. Install _MyZSH_
```sh
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```
2. Clone a sample of .zshrc file 
```sh
git clone https://github.com/bhilburn/powerlevel9k.git ~/.oh-my-zsh/custom/themes/powerlevel9k
```
3. Open .zshrc file and edit it like this
```sh
# If you come from bash you might have to change your $PATH.
#export PATH=$HOME/bin:/usr/local/bin:$PATH

# Path to your oh-my-zsh installation.
export ZSH="/Users/<your_user>/.oh-my-zsh"

# THEME
ZSH_THEME="powerlevel9k/powerlevel9k"

#PLUGINGS
plugins=(
        git
)

source $ZSH/oh-my-zsh.sh

# User configuration

POWERLEVEL9K_LEFT_PROMPT_ELEMENTS=(dir rbenv vcs)
POWERLEVEL9K_RIGHT_PROMPT_ELEMENTS=(status time)
POWERLEVEL9K_PROMPT_ON_NEWLINE=true

## Add a space in the first prompt
#POWERLEVEL9K_MULTILINE_FIRST_PROMPT_PREFIX="%f"# Visual customisation of the second prompt line
local user_symbol="$"
if [[ $(print -P "%#") =~ "#" ]]; then
    user_symbol = "#"
fi
POWERLEVEL9K_MULTILINE_LAST_PROMPT_PREFIX="%{%B%F{black}%K{yellow}%} $user_symbol%{%b%f%k%F{yellow}%} %{%f%}"

# SUBLIME
# This is an alias optional
alias sublime="open -a /Applications/Sublime\ Text.app"
```
4. Open terminal preferences and (cmd + ,)
5. Go to profiles
6. Select add profile
7. Import _darkTheme.terminal_ profile
8. Select _darkTheme_ as your default theme
9. Close and open the terminal to see the changes