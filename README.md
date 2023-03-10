# All The Stuff I Use

## Base Tools
- [chocolatey](https://chocolatey.org/install) - package manager (apk/npm/nuget/apt-get) for Windows, use LLVM setup instructions
- [Git SCM](https://git-scm.com/downloads) - git command line plus bash
- [cmder](https://cmder.app) - console emulator for Windows
- [neovim](https://neovim.io) - modern vim, see neovim folder for config
- [Agent Ransack](https://www.mythicsoft.com/agentransack) - search tool for windows filesystem
- [Docker](https://www.docker.com) - containers
- [Visual Studio Code](https://code.visualstudio.com) - IDE

## Programming Languages and Runtimes
- [node.js](https://nodejs.org) - javascript runtime
- [rust](https://www.rust-lang.org)
- [java](https://www.oracle.com/java/technologies/downloads)

## Neovim
Neovim is my preferred console text editor.  I'm currently using a configuration inspired by the Primeagen, see: [0 to LSP](https://www.youtube.com/watch?v=w7i4amO_zaE)

### Installation

1. make sure that git and nvim are downloaded and installed
2. install packer per the Windows instructions here: [packer quickstart](https://github.com/wbthomason/packer.nvim#quickstart)
3. the best installation if you want to use neovim in both vscode and cmder is to split the configs/plugins
    - windows config directory:  ```~/AppData/Local/nvim```
    - windows data directory: ```~/AppData/Local/nvim-data```
    - cmder config directory: ```$XDG_CONFIG_HOME/nvim```
    - cmder data directory: ```$XDG_DATA_HOME/nvim-data```
4. copy the contents of the nvim config of your choice into the correct directory, see above
5. any config that uses packer must clone packer into the right directory, see [packer quickstart](https://github.com/wbthomason/packer.nvim#quickstart)
    - be sure to run: ```nvim --headless -c 'autocmd User PackerComplete quitall' -c 'PackerSync'```
7. update ```~/.bash_profile``` with the following
    - ```alias vim=nvim```
8. launch nvim, if an LSP is installed it will start installing language plugins

[treesitter Windows support](https://github.com/nvim-treesitter/nvim-treesitter/wiki/Windows-support)
[cmder git-bash](https://gist.github.com/nickautomatic/02ccb76292f7f8d9767e)

The setup that worked for me on Windows 10/11 was to use LLVM/clang for a c compiler and git-bash in the terminal.  For some reason, cmder bash just never worked with nvim.

One of the cmder/conemu keybinds that doesn't play nice out of the box is C-w which can be remapped to C+S-w.

