
**Install z-shell on your Linux**
#####################################


1. Install ZSH binary
======================

::

    #FreeBSD
    $ sudo pkg install zsh 

    # Ubuntu
    $ sudo apt install zsh

    # ArchLinux
    $ pacman -S zsh

    # Manjaro
    # yay -S zsh


2. Use oh-my-zsh for ease
===========================

modify /etc/hosts to add line:  "199.232.28.133	raw.githubusercontent.com"

::

    # run command to get existing good oh-my-zsh configuration.
    $ sh -c "$(wget https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"


3. Add Plugins
===================

3.1 zsh-autosuggestions
+++++++++++++++++++++++++++

::

    $ git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions

3.2 zsh-syntax-highlighting
+++++++++++++++++++++++++++++

::

    $ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

4. Modify .zshrc
====================

::

    plugins=(git
        zsh-syntax-highlighting
        zsh-autosuggestions)

::

    # shell prompt: 
    export PS1='%(?.%F{green}.%F{red})%n@%m:%~%# %f'

    # source highlighting
    source ~/.oh-my-zsh/custom/plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh


