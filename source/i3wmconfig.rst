
**i3wm Install and Configuration**
######################################

1. Apps and Tools
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

2 Pacman and Yay
==================
2.1 Pacman
************

::

    $ sudo pacman-mirrors --country China
    $ sudo pacman -Syyu

2.2 Yay
*********

::

    $ sudo pacman -S yay base-devel
    $ yay -Syyu


3 Network & Wifi
=================
wifi:

::

    $ yay -S network-manager-applet
    $ yay -S nm-connection-editor

or tools to configure network / wifi:

:: 

    nmcli
    nmtui


4 Display Configuration
=========================

4.1 Modify Display Configuration
**********************************

::

    $ cvt 1920 1080 60

    # copy output and add the mode
    $ xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync

    # add the mode to Display
    $ xrandr --addmode Virtual1 1920x1080_60


4.1.1 Dual Display
+++++++++++++++++++

::

    # clone mode:
    $ xrandr --output Virtual1 --same-as HDMI-2 --mode 1920x1080_60

    # extension mode:
    $ xrandr --output Virtual1 --left-of HDMI-2 --auto

    # multi Display
    $ xrandr --output Virtual1 --primary --auto --output HDMI-1 --auto --left-of HDMI-2

Reference: \ `xrand display configuration <https://www.dazhuanlan.com/2020/01/30/5e320494cf9cf>`_


5 Misc Tools
==============

5.1 Screen shot tools
***********************
    * mate-screenshot
    * flameshot (good)



.. note::

    sample of note section.

