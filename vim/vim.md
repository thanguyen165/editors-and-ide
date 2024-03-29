# INSTALL AND PREPARE VIM

This is written for [Linux](https://ubuntu.com/).

## 1. What is Vim?

Check Vim official repository [here](https://github.com/vim/vim).

## 2. INSTALL VIM

Run this command:
```console
sudo apt-get install vim
```
## 3. Config Vim:

See [How to config Vim](https://www.freecodecamp.org/news/vimrc-configuration-guide-customize-your-vim-editor/).

## 4. Vim commands

See [Vim commands](https://phoenixnap.com/kb/vim-commands-cheat-sheet).

## 5. Install NVM (Node Version Manager)
### 5.1 Install NVM

* Open terminal and run:
 ```console
 curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
 ```
* If you use **Linux**, exit current terminal and open the new one again before continuing.

### 5.2 Verrify installation

To verify that NVM has been installed, do:
```console
nvm --version
```
## 6. Install nodeJs:

To download and install last version of node, do
```console
nvm install node
```
If you want to choose the specific version:
```console
nvm install 18.16.0
```
Check the avaliable versions by:
```console
nvm ls-remote
```
Check the current version:
```console
node --version
```
See [How to install NVM and nodeJs](https://github.com/nvm-sh/nvm) for more information.

## 7. Install Vim plug manager

Check at [junegunn/vim-plug](https://github.com/junegunn/vim-plug)

Run this command
```console
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

## 8. Install autocomplete extension: [coc.nvim](https://github.com/neoclide/coc.nvim)

Put these lines into ```~/.vimrc``` file you made in **Step 2**:
```
call plug#begin()

Plug 'neoclide/coc.nvim', {'branch': 'release'}

call plug#end()
```

Then start Vim and run this command
```
:PlugInstall
```

```coc.nvim``` is installed now.

Put these lines into ```~/.vimrc``` file for autocomplete selection (by [stackoverflow](https://stackoverflow.com/questions/67370086/how-to-remap-coc-nvim-autocomplete-key))

```
inoremap <silent><expr> <tab> pumvisible() ? coc#_select_confirm() : "\<C-g>u\<TAB>"
inoremap <silent><expr> <cr> "\<c-g>u\<CR>"
```


There we go!

## 9. Install autocomplete extension respect to each language
### 9.1 For Web-development:

```console
:CocInstall coc-tsserver coc-json coc-html coc-css
```

### 9.2 For [python3](https://www.python.org/):

```console
:CocInstall coc-pyright
```

### 9.3 For [C/C++](https://en.cppreference.com/w/):

```console
:CocInstall clangd
```

## 10. Install [GNU-GCC](https://gcc.gnu.org/) for C/C++
### 10.1 Install GNU-GCC
Run these commands, one by one:
```console
sudo apt update
```
```console
sudo apt install build-essential
```
You might want to see [what is the difference between apt and apt-get](https://askubuntu.com/questions/445384/what-is-the-difference-between-apt-and-apt-get).

### 10.2 Verrify installation

Verify that the GCC compiler is successfully installed by running the following command that prints the GCC version:
```console
gcc --version
```
### 10.3 Hello World program

```console
vim helloWorld.c
```
```c
#include<stdio.h>

int main() {
    printf("Hello World!\n");
    return 0;
}
```
Save the file and compile it into an executable:
```console
gcc hello.c -o hello
```
**Note**: Compile ```C``` files with ```gcc```, and ```C++``` files with ```g++```. \
Execute that file with:
```console
./hello
```

<!-- code highlight:
https://github.com/github/linguist/blob/master/lib/linguist/languages.yml -->
