# INSTALL AND PREPARE VIM
This is written for [Linux](https://ubuntu.com/).
## 1. What is Vim?
Check Vim official repository  [here](https://github.com/vim/vim).

## 2. INSTALL VIM
Run this command:
```
sudo apt-get install vim
```
## 3. Config Vim:
See [How to config Vim](https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/).

## 4. Vim commands
See [Vim commands](https://phoenixnap.com/kb/vim-commands-cheat-sheet).

## 5. Install NVM (Node Version Manager)
### 5.1 Install NVM
* Open terminal and run:
 ```
 curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
 ```
* If you use **Linux**, exit current terminal and open the new one again before continuing.
### 5.2 Verrify installation
To verify that NVM has been installed, do:
```
nvm --version
```
## 6. Install nodeJs:
To download and install last version of node, do
```
nvm install node
```
If you want to choose the specific version:
```
nvm install 18.16.0
```
Check the avaliable versions by:
```
nvm ls-remote
```
Check the current version:
```
node --version
```
See [How to install NVM and nodeJs](https://github.com/nvm-sh/nvm) for more information.
## 7. Install autocomplete extension: [coc.nvim](https://github.com/neoclide/coc.nvim)
Put these lines into ```vimrc``` file you made in **Step 2**:
```
call plug#begin()

Plug 'neoclide/coc.nvim', {'branch': 'release'}

call plug#end()
```
There we go!
## 8. Install autocomplete extension respect to each language
### 8.1 For Web-development:
```
:CocInstall coc-tsserver coc-json coc-html coc-css
```
### 8.2 For [python3](https://www.python.org/):
```
:CocInstall coc-pyright
```
### 8.3 For [C/C++](https://en.cppreference.com/w/):
```
:CocInstall clangd
```

## 9. Install [GNU-GCC](https://gcc.gnu.org/) for C/C++
### 9.1 Install GNU-GCC
Run these commands, one by one:
```
sudo apt update
```
```
sudo apt install build-essential
```
You might want to see [what is the difference between apt and apt-get](https://askubuntu.com/questions/445384/what-is-the-difference-between-apt-and-apt-get).

### 9.2 Verrify installation
Verify that the GCC compiler is successfully installed by running the following command that prints the GCC version:
```
gcc --version
```
### 9.3 Hello World program
```
vim helloWorld.c
```
```
#include<stdio.h>

int main() {
    printf("Hello World!\n");
    return 0;
}
```
Save the file and compile it into an executable:
```
gcc hello.c -o hello
```
**Note**: Compile ```C``` files with ```gcc```, and ```C++``` files with ```g++```. \
Execute that file with:
```
./hello
```
