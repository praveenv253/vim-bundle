vim-bundle
==========

The bundle subdirectory of my .vim folder. It contains the pathogen modules I
use as git submodules.

Set up as follows:

1. Clone the primary repository and set it up as your .vim folder
    ```
    cd
    git clone https://github.com/praveenv253/dotvim.git .vim
    ```

2. Create a symbolic link for .vimrc
    ```
    ln -s .vim/vimrc .vimrc
    ```

3. Copy the file for powerline fonts
    ```
    mkdir -p .fonts
    cd .fonts
    ln -s ~/.vim/DejaVuSansMono-Powerline.ttf
    ```

4. Clone the bundle repository
    ```
    cd ~/.vim
    git clone https://github.com/praveenv253/vim-bundle bundle
    ```

5. Set up the bundle submodules
    ```
    cd ~/.vim/bundle
    git submodule init
    git submodule update
    ```

That's it!

Notes
-----
* taglist is not a submodule, because the one at
  [vim scripts](http://www.vim.org/scripts/script.php?script_id=273) is way
  ahead of its [git mirror](https://github.com/vim-scripts/taglist.vim) at the
  time of this writing.
* [vim-powerline](https://github.com/Lokaltog/vim-powerline) is going to be
  replaced by [powerline](https://github.com/powerline/powerline). So this
  needs to be changed in the near future. Further, patched fonts need to be
  installed to fully make use of vim-powerline, as described above.
