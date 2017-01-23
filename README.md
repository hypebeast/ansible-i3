# ansible-i3

Ansible role to install and configure i3 on Ubuntu.


## Features

This Ansible role installs the following components:

  * [i3](https://i3wm.org/) the tiling window manager with a custom config.
  * [j4-dmenu-desktop](https://github.com/enkore/j4-dmenu-desktop) a fast desktop menu
  * [rofi](https://davedavenport.github.io/rofi/): A window switcher, run dialog and dmenu replacement
  * [quickswitch-i3](https://github.com/proxypoke/quickswitch-for-i3) a python utility to quickly change to and locate windows in i3.
  * [compton](https://github.com/chjj/compton) a compositor for X11.
  * [conky](https://github.com/brndnmtthws/conky) a Light-weight system monitor for X with custom theme.
  * [dunst](http://www.knopwob.org/dunst/): lightweight and customizable notification daemon
  * [lightdm](https://www.freedesktop.org/wiki/Software/LightDM/) with custom theme.



## Usage

To install use:

```
ansible-playbook playbook.yml -i hosts -e action=install

```


## Vagrant

To test the installation run:

```
vagrant up
```


## TODO

  * [j4-make-config](https://github.com/okraits/j4-make-config)
  * Status line for i3
    * [j4status](https://j4status.j4tools.org/) and [j4status-plugins](https://j4status.j4tools.org/j4status-plugins/) and [i3blocks](https://github.com/vivien/i3blocks)
    * or [i3pystatus](https://github.com/enkore/i3pystatus)
    * or [py3status](https://github.com/ultrabug/py3status)
