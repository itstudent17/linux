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

`cat ~/.ssh/id_ed25519.pub`

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

* [ES7+ React/Redux/React-Nati](https://github.com/r5n-labs/vscode-react-javascript-snippets/blob/HEAD/docs/Snippets.md) (dsznajder)

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

Wallpapers are stored in /usr/share/backgrounds

---

# Create React App

## npx

`npx create-react-app <project-name> --template typescript`

`npx create-react-app . --template typescript`

`npm install`

`npm start` / `npm run start`

## yarn

`yarn create react-app <project-name> --template typescript`

`yarn create react-app . --template typescript`

`yarn` or `yarn install`

`yarn start`

Created by npm or yarn the app starts at  `http://localhost:3000`

# Vite

`npm create vite@latest my-app --template` for npm / `yarn create vite my-app --template` for yarn

`cd my-app`

`npm i` / `yarn install` / `yarn`

`npm run dev` / `yarn start`

---

`rm -rf node_modules`

`npm cache clean --force`

`yarn cache clean`

# Bitbucket

Add an ssh key: [https://bitbucket.org/account/settings/ssh-keys/](https://bitbucket.org/account/settings/ssh-keys/)

In order to delete a repo in Butbucket follow the steps: go to the repository page, choose **Repository settings** on the left sidebar, then **General / Repository details**, **Manage repository** to the right, **Delete**

I order to delete the whole project you need to delete all repositories in the project first. After deleting all enclosed repositories delete the project itself as you delete a separate repository.

---

# Markdown

`**some text**` to make text bold

`---` adds horizontal line

`# ## ### ...` for headings

`[text](url)` for links 

`![alt text](filename)` for images

`*`, `+`, `-` for bullets


---

# Youtubers

[Codevolution (Wishvas)](https://www.youtube.com/@Codevolution/playlists)

[PurpleSchool | Anton Larichev](https://www.youtube.com/@PurpleSchool/playlists)

Антон Ларичев

[Михаил Непомнящий](https://www.youtube.com/@mishanep)

[Github](https://github.com/michey85)

# React

CSS files are imported by their address: `import "./index.css";` 

Images are imported like objects/components: `import { logo } "./logo.svg";` 

# React Developer Interviews

[15 questions](https://github.com/evgenii-studitskikh/react-ru-interview-questions)

[100 questions](https://github.com/AndrewMosh/react_interview_cheatsheet)

# Windows

| Command |    Description     |
| :------ | :----------------: |
| Win + R | regedit |
| Win + Shift  + S | make screenshot |
| Win + R | record video |

## Software

MPC-HC Player

[https://github.com/clsid2/mpc-hc/releases](https://github.com/clsid2/mpc-hc/releases)

[Speed settings](https://www.youtube.com/watch?v=Nu6skiGa3c8)

![Воспроизведение - Шаг скорости](https://github.com/user-attachments/assets/e2c7ccaf-5514-41c9-9201-a475c156e7d5)

![Вывод - Рендер аудио](https://github.com/user-attachments/assets/eaed1336-8943-4885-b857-53bb371ef85e)


# Interviews

Microfrontends, Feature Sliced Design,


React Patterns:

* render props
* container / presentational components
* Hight Order components (React.memo(), React.forwardRef())
* Reducer
* Observer (Mobx)


"Рендер-пропсы" (render props) - это паттерн в React, который позволяет передавать компоненту функцию через пропсы, которая затем используется для определения, что компонент должен отрисовать



