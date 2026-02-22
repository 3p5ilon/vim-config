# Vim Config for CP

Vim configuration for competitive programming in C++, using [Vim-Plug](https://github.com/junegunn/vim-plug).

## Requirements

This setup uses [`bits/stdc++.h`](https://raw.githubusercontent.com/gcc-mirror/gcc/master/libstdc++-v3/include/precompiled/stdc++.h), which is part of GCC's C++ standard library.

On macOS, install GCC via Homebrew:

```bash
brew install gcc
```

The header is typically located at:

```text
/opt/homebrew/Cellar/gcc/<version>/include/c++/<version>/bits/stdc++.h
```

## Installation

1. Clone this repo:

```bash
git clone https://github.com/3p5ilon/cpvim.git
cd cpvim
```

2. Copy vimrc to your home directory:

```bash
cp .vimrc ~/.vimrc
```

3. Install [vim-plug](https://github.com/junegunn/vim-plug) (plugin manager):

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

4. Install plugins:

```bash
vim +PlugInstall +qall
# Or run :PlugInstall inside Vim
```

5. Add [jellybeans](https://github.com/nanotech/jellybeans.vim) colorscheme:

You can use your favorite color scheme – just change `colorscheme` in `.vimrc`.

```bash
mkdir -p ~/.vim/colors
curl -o ~/.vim/colors/jellybeans.vim https://raw.githubusercontent.com/nanotech/jellybeans.vim/master/colors/jellybeans.vim
```

6. Add custom C++ snippets:

After step 4,`~/.vim` will be created with the plugin structure. Then add your custom snippets:

```bash
mkdir -p ~/.vim/UltiSnips
cp .vim/UltiSnips/cpp.snippets ~/.vim/UltiSnips/
```

Your `~/.vim` folder should look like this:

![.vim folder](.vim.png)
