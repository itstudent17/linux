# Linux Mint 22

Knowledge base about Linux Mint 22 (Cinnamon Edition)

## System Updates

`sudo apt update`

`sudo apt upgrade`

## Git

Install the [latest available version](https://git-scm.com/downloads/linux) of git

`sudo add-apt-repository ppa:git-core/ppa`

`sudo apt update`

`sudo apt install git`

Generate an SSH key and add it to the Gitlab / Github / Bitbucket account settings to be able to clone repos via SSH

`ssh-keygen`

`cat cat ~/.ssh/id_ed25519.pub`

Clone a repository, go into a repository folder and set your credentials:

`git config --local user.name itstudent17`

`git config --local user.email itstudent17@outlook.com`

## NVM

Use install & update script from the [NVM Github page](https://github.com/nvm-sh/nvm)

`curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash`

or

`wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash`

Then install, list and use appropriate node version

`nvm install <stable | 20 | carbon>`

`nvm ls`

`nvm use <stable | 20 | carbon>`

`nvm alias default <stable | 20 | carbon>`

## Chrome

Download and install .deb package from the official website (https://itsfoss.com/install-chrome-linux-mint/)

`sudo dpkg -i ~/Downloads/google-chrome-stable_current_amd64.deb`

## VS Code

[Download](https://code.visualstudio.com/) and install .deb package from the official website

`sudo dpkg -i ~/Downloads/code_1.95.3-1731513102_amd64.deb`

### settings

* Auto Save: onFocusChange

* Format on Save: true

### extensions

* Prettier - Code formatter (edit settings.json after installation)

* ESLint

* [Simple React Snippets](https://marketplace.visualstudio.com/items?itemName=burkeholland.simple-react-snippets) (Burke Holland)

* Live Server (Ritwick Dey)

## PHPStorm / WebStorm

- go to WebStrom Other versions and download a WebStorm-2023.3.8.tar.gz for 2023.3.8 version.
- unzip the archive and go to the ./bin folder
- give the webstorm.sh script rights for execution `chmod +x ./webstorm.sh`
- run the .sh script via `./webstorm.sh`

1. disable updates
2. turn off new UI
3. eslint -> Run eslint --fix on save
4. Tools -> Create desktop Entry... (creates a desktop entry to add a Webstorm shortcut into Programs)

## Telegram

Go to the [official website](https://telegram.org/) and download archive, unzip it and doubleclick Telegram file

## OS Commands and Hotkeys

| Command |    Description     |
| :------ | :----------------: |
| history | show last commands |
| clear   |   clear terminal   |
| chmod +x shell.sh  |   give shell script excecutable rights |

| Hotkey           |         Description          |
| :--------------- | :--------------------------: |
| Ctrl + Alt + T   |     launch new terminal      |
| Ctrl + Shift + T | new tab in existing terminal |
| Ctrl + Alt + D | hide all windows |
| PrintScreen | Take screenshot with options  |
| Shift + PrintScreen | Take screenshot of all the screen  |

## Customise System Settings

### Keyboard layout

System Settings - Keyboard - Layouts - + Add language - Choose language - Options to change switching to another layout - (Mint)

System Settings - Keyboard Shortcuts - View and Customize Shortcuts - Typing - Switch to next Input Source (Ubuntu)

### VPN

Network Settings - Click Plus at the bottom - Import from file... and choose a VPN configuration file - Enter login and password

## Other info

In Ubuntu programs (Chromium, Telegram, etc.) can be installed via Snap Store App

---

# Create React App

## npx

`npx create-react-app <project-name> --template typescript`

`npx create-react-app . --template typescript`

## yarn

`yarn create-react app <project-name> --template typescript`

`yarn create-react app . --template typescript`

## vite

`npx create vite@latest`


