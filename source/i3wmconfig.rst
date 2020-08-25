
**i3wm Install and Configuration**
######################################


1. Display Configuration
========================

1.1. Modify Display Configuration
**********************************

::

    $ cvt 1920 1080 60

    # copy output and add the mode
    $xrandr --newmode "1920x1080_60.00" 173.00 1920 2048 2248 2576 1080 1083 1088 1120 -hsync +vsync

    # add the mode to Display
    $xrandr --addmode Virtual1 1920x1080_60


1.2. Dual Display
******************

::

    #clone mode:
    $xrandr --output Virtual1 --same-as HDMI-2 --mode 1920x1080_60

    #extension mode:
    $xrandr --output Virtual1 --left-of HDMI-2 --auto

    #multi Display
    $xrandr --output Virtual1 --primary --auto --output HDMI-1 --auto --left-of HDMI-2

Reference: \ `xrand display configuration <https://www.dazhuanlan.com/2020/01/30/5e320494cf9cf>`_


.. note::

    sample of note section.

1.2.1 Third level title
++++++++++++++++++++++++
* List1
* List2
    * sublist
    * sublist


- List3
- List4
    - sublist
    - sublist


#. sequence List
#. sequence List
#. sequence List
    #. sequence sublist
    #. sequence ssublist


anchor link:
    sample: \ `xrand display configuration <https://www.dazhuanlan.com/2020/01/30/5e320494cf9cf>`_


1.2.1.1 Fourth Level title
===========================



