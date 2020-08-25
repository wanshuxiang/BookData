
**i3wm Install and Configuration**
######################################

1. Installation
=================
App and Tools needed:
    #. i3wm (i3-gaps)
    #. tmux
    #. nvim
    #. polybar
    #. compton (picom)
    #. ranger
    #. rofi
    #. feh (backgroupd) + variety

Opetional for optimization:
    * screenkey (good tool)
    * alacritty (terminal)
    * fish (terminal)
    * simplescreenrecorder
    * lxappearance (change theme)

Chinese Imput Method
    - fcitx / fcitx-im / fcitx-configtool
    - fcitx-sunpinyin (fcitx-sogoupinyin, ...etc)
    - adding following lines to ~/.xprofile

    ::

        export GTK_IM_MODULE=fcitx
        export QT_IM_MODULE=fcitx
        export XMODIFIERS="@im=fcitx"

1.1 Pacman and Yay
*******************
1.1.1 Pacman
+++++++++++++

::

    $ sudo pacman-mirrors --country China
    $ sudo pacman -Syyu

1.1.2 Yay
+++++++++++

::

    $ sudo pacman -S yay base-devel
    $ yay -Syyu


1.2 Network Wifi
******************
wifi:

::

    $ yay -s network-manager-applet

or tools to configure network / wifi:

:: 

    nmcli
    nmtui




2. Display Configuration
========================

2.1 Modify Display Configuration
**********************************

::

    $ cvt 1920 1080 60

    # copy output and add the mode
    $ xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync

    # add the mode to Display
    $ xrandr --addmode Virtual1 1920x1080_60


2.2. Dual Display
******************

::

    # clone mode:
    $ xrandr --output Virtual1 --same-as HDMI-2 --mode 1920x1080_60

    # extension mode:
    $ xrandr --output Virtual1 --left-of HDMI-2 --auto

    # multi Display
    $ xrandr --output Virtual1 --primary --auto --output HDMI-1 --auto --left-of HDMI-2

Reference: \ `xrand display configuration <https://www.dazhuanlan.com/2020/01/30/5e320494cf9cf>`_


.. note::

    sample of note section.

