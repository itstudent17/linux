# Linux Mint 22

Knowledge base about Linux Mint 22 (Cinnamon Edition)

Ubuntu 22.04 LTS (Jammy Jellyfish) отличается от Ubuntu 20.04.5 LTS (Focal Fossa) прежде всего обновлением версии рабочего окружения GNOME до 42й версии.

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

### Git commands

Dealing with branches:

| Command |    Description     |
| :------ | :----------------: |
| `git branch` | displays local branches |
| `git branch -r` | displays remote branches |
| `git branch --all` | displays both local and remote branches |
| `git checkout {branch-name}` | checkout into an existing branch |
| `git checkout -b {new-branch-name}` | create a new branch and checkout into it |
| `git checkout {branch-name} origin/{branch-name}` | checkout a remote branch |
| `git branch -m {new-branch-name}` | rename local branch |
| `git branch -D {branch-name}` | delete local branch |


Delete all local branches except **master**: `git branch | grep -v master | xargs git branch -D`

Dealing with commits:

| Command |    Description     |
| :------ | :----------------: |
| `git log` | show last commits |
| `git reset --hard HEAD~n` | reset last n local commits |

Dealing with repos:

| Command |    Description     |
| :------- | :---------------: |
| `git clone` | clone a repo |
| `git fetch origin` | update local repository |

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

Best VPN Chrome extension so far is **Free VPN Proxy - 1VPN** (Free VPN Proxy - VPNLY is good as well)

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

#### Simple React Snippets

`sfc` creates an arrow function / component

#### ES7+ React/Redux/React-Native snippets

`rafce` creates functional component with default export and React import

`nfn` creates an arrow function


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

`sudo apt purge <program>` removes a program

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

CRA is a utility to create React app boilerplate. Since February 14, 2005 is officially depricated. There is no way to install boilerplate for specific React version; we have to adapt boilerplate to particular React version mannually. Firstly, create latest React version boilerplate, then remove node-modules and package-lock.json, and edit package.json for the desired React version. Finally, install new packages and start your application. 

## npm / npx

`npx create-react-app <project-name> --template typescript`

`npx create-react-app . --template typescript`

`npm install`

`npm start` / `npm run start`

`npm i styled-components` install as dependency (dependencies block in package.json)

`npm i --save-dev @types/styled-components` install types for a tool as a devDependency (devDependencies in package.json); present only in development

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

`npm run dev` / `yarn dev`

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

Put your code inside bacticks to hightlight it with grey. Use ``` before and after your code to create a block of code

---

# Youtubers

[Codevolution (Wishvas)](https://www.youtube.com/@Codevolution/playlists)

[Net Ninja](https://www.youtube.com/@NetNinja/playlists)

[https://github.com/iamshaunjp](https://github.com/iamshaunjp)

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

# Operation Systems

In order to create a bootable USB disk for Linux Mint / Ubuntu download and install **rufus**, **set FAT32 as file system**

<img width="428" height="594" alt="image" src="https://github.com/user-attachments/assets/c27a1634-5d8e-435a-8806-79b332800a13" />


# Windows

| Command |    Description     |
| :------ | :----------------: |
| Win + R | regedit |
| Win + Alt + R | record video (Xbox Game Bar) |
| Win + Shift  + S | make screenshot |

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


### APIs

[The Star Wars API](https://swapi.dev/)

# React

[The official docs](https://react.dev/learn/react-developer-tools)

# What I don`t know

debounce / trottle 

Types of authorization. How to implement JWT token authorization?


Feature flags and how to implement them?

Scaffolding project in






