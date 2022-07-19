# iTerm2 Mac Settings
This a list of notes, tools, and themes used for my iTerm setup on macbook pro.

## Themes Used
    - Dracula
    - Material-Design

## Install/Setup Notes
*Credit to Chamika Kasun for the awesome instructions / writeup*

**1. Install Homebrew for Mac**
```bash
> /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

**2. Install ZSH (through Homebrew)**
```bash
> brew install zsh
```

**3. Install "Oh My Zsh" framework**
 - Using curl:
    ```bash
    > sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```

 - Using wget:
    ```bash
    > sh -c "$(wget https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
    ```

**4. Install Powerlevel10k theme**
   1. Font: `https://github.com/romkatv/powerlevel10k#meslo-nerd-font-patched-for-powerlevel10k`
        
   2. P10k for Oh-My-Zsh plugin manager:
        ```bash
        > git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
        ```
    1. Edit ".zshrc" file
        ```bash
        > nano ~/.zshrc
        ```
        Change `ZSH_THEME` to add `"powerlevel10k/powerlevel10k"`
    2. Save and restart terminal session
    3. Run p10k configure
        ```bash
        > p10k configure
        ```

**5. Install Autosuggestions**
   1. Clone repo into `$ZSH_CUSTOM/plugins`
        ```bash
        > git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
        ```
    2. Add plugin into the zsh plugins list
       1. `> nano ~/.zshrc`
       2. Find the `plugins=()`
       3. Add `zsh-autosuggestions`
       4. Should look like this: `plugins=(zsh-autosuggestions OTHER_PLUGINS_HERE)`
    3. Restart terminal session
   
**6. Install Syntax Highlighting**
   1. Clone the git repo
        ```bash
        > git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
        ```
    1. Add source of script to `.zshrc`
        ```bash
        > echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
        ```
    2. Restart terminal session