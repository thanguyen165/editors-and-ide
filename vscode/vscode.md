# INSTALL AND PREPARE VISUAL STUDIO CODE
## Table of contents
1. [What is VISUAL STUDIO CODE?](#What_is_VSCODE?)
2. [Install VS CODE](#Install_VS_CODE)
3. [Start VS Code](#Start_VS_Code)
4. [Install extensions](#Install_extensions)
5. [Shortcuts for VS Code](#Shortcuts_for_VS_Code)
6. [Install GNU-GCC](#Install_GNU_GCC)
7. [Install Python](#Install_Python)

## 1. What is VISUAL STUDIO CODE? <a name="What_is_VSCODE?"></a>
Visual Studio Code (VS Code) is one of the most popular **text editor**, allows us to work with a lot of language. **VS CODE IS NOT AN IDE**.\
Check VS Code official website [here](https://code.visualstudio.com/).

## 2. Install VS CODE <a name="Install_VS_CODE"></a>
Run this command:
```
sudo apt-get install code
```
Or just download from [VS Code official website](https://code.visualstudio.com/).
## 3. Start VS Code: <a name="Start_VS_Code"></a>
* In Linux:
Open terminal and do:
```
code hello.py
```
* In Windows:
Open Powershell and do:
```
code hello.py
```
* Or just open it with GUI.

## 4. Install extensions <a name="Install_extensions"></a>
I suggest these extensions:
1. [Code Runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) (by Jun Han).
2. [Bracket Pair Colorization Toggler](https://marketplace.visualstudio.com/items?itemName=dzhavat.bracket-pair-toggler) (by Dzhavat Ushev) to colorise the respective brackets.
3. [C/C++ Extension Pack](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools-extension-pack) (by Microsoft) if you work with [C/C++](https://en.cppreference.com/w/).
4. [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python) (by Microsoft) if you work with [Python](https://www.python.org/).
5. [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) (by Ritwick Dey) if you work with web-development.
You don't have to reload page to see updates. Just save html files and the page will be automatically reloaded.
6. [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag) (by Jub Han) if you work with web-development.
7. [WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) (by Microsoft) if you wok with [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/install).\
Check [here](https://x-team.com/blog/best-vscode-extensions/) for more suggestions.

## 5. Shortcuts for VS Code <a name="Shortcuts_for_VS_Code"></a>
See [VS Code shortcuts](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf).

## 6. Install [GNU-GCC](https://gcc.gnu.org/) for C/C++ <a name="Install_GNU_GCC"></a>
### 6.1 Install GNU-GCC
Run these commands, one by one:
```
sudo apt update
```
```
sudo apt install build-essential
```
You might want to see [what is the difference between apt and apt-get](https://askubuntu.com/questions/445384/what-is-the-difference-between-apt-and-apt-get).

### 6.2 Verify installation
Verify that the GCC compiler is successfully installed by running the following command that prints the GCC version:
```
gcc --version
```
### 6.3 Hello World program
```
code helloWorld.c
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
## 7. Install [Python](https://www.python.org/downloads/) <a name="Install_Python"></a>
### 7.1 Install Python
Run these commands, one by one:
```
sudo apt update
```
```
sudo apt-get install python3.6
```
You might want to see [what is the difference between apt and apt-get](https://askubuntu.com/questions/445384/what-is-the-difference-between-apt-and-apt-get).

### 7.2 Verify installation
Verify that Python is successfully installed by running the following command that prints the Python version:
```
python --version
```
### 7.3 Hello World program
```
code helloWorld.py
```
```
print("Hello World")
```
Save the file and Execute that file with:
```
python helloWorld.py
```
