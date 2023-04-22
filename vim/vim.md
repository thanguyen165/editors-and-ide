# INSTALL AND PREPARE VIM
This is for [Linux](https://ubuntu.com/). For [Windows](https://www.microsoft.com/en-us/windows), I don't know.
## 1. INSTALL VIM
Run this command:
```
sudo apt-get install vim
```
## 2. Config Vim:
See [How to config Vim](https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/).
## 3. Install NVM (Node Version Manager)
### 3.1 Install NVM
* Open terminal and run:
 ```
 curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
 ```
* If you use **Linux**, exit current terminal and open the new one again before continuing.
### 3.2 Verrify Installation
To verify that NVM has been installed, do:
```
nvm --version
```
## 4. Install nodeJs:
To download and install last version of node, do
```
nvm install node
```
If you want to choose the specific version:
```
nvm install 18.0.4
```
Check the avaliable version by:
```
nvmls-remote
```
Check the current version:
```
node --version
```
See [How to install NVM and nodeJs](https://github.com/nvm-sh/nvm) for more information.
## 5. Install autocomplete extension: [coc.nvim](https://github.com/neoclide/coc.nvim)
Put these lines into ```vimrc``` file you made in **Step 2**:
```
call plug#begin()

Plug 'neoclide/coc.nvim', {'branch': 'release'}

call plug#end()
```
There we go!
## 6. Install what you need!
### 6.1 For Web-development:
```
:CocInstall coc-tsserver coc-json coc-html coc-css
```
### 6.2 For [python3](https://www.python.org/)
```
:CocInstall coc-pyright
```
### 6.3 For [C++](https://en.cppreference.com/w/)
```
:CocInstall clangd
```
## 7. Vim commands
See [Vim commands](https://phoenixnap.com/kb/vim-commands-cheat-sheet).
