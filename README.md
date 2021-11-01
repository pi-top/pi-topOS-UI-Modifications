# pi-topOS UI Modifications

This package provides various UI modifications for pi-topOS. This is derived from https://github.com/RPi-Distro/raspberrypi-ui-mods.

Notable additional changes:
* Change to `LXDE-pt` session name
* VNC config (`/etc/vnc/config.d/common.custom`):
  * Disable tray icon
  * Add virtual 1920x1080 resolution for VNC
* Auto-start resolution handling
  * `autorandr` dependency includes auto-start of default profile
  * `/etc/xdg/autorandr/default`
    * Symlinking `default` to `common` here set this as the default profile
      * `common` = largest common resolution
* Auto-start drop shadow behaviour (`/etc/xdg/autostart/compton.desktop`)
* Custom start menu (`/etc/xdg/lxpanel/LXDE-pt/panels/panel`)
* Custom logout program ([`pt-os-quit-options`](https://github.com/pi-top/pi-topOS-Start-Menu-Quit-Options)) (`/etc/xdg/lxpanel/LXDE-pt/config`)
* Custom desktop appearance/behaviour
  * `/etc/xdg/lxsession/LXDE-pt/desktop.conf`
    * Adapta theme
    * pi-topOS Icon Theme
  * `/etc/xdg/pcmanfm/LXDE-pt/desktop-items-{0,1}.conf`
  * `/etc/xdg/pcmanfm/LXDE-pt/pcmanfm.conf`
* Custom 'help' section in start menu
  * `/etc/xdg/menus/lxde-pt-applications.menu`
  * `/usr/share/pt-os-ui-overrides/desktop-directories/lxde-help.directory`
* Custom handling of 'print screen' for handling
  * `/etc/xdg/openbox/lxde-pt-rc.xml`
    * Specifies key binding to 'Print Screen' button
  * `/usr/bin/pt-scrot`
    * `scrot` or `raspi2png`, depending on display driver
* Adapta theme for notification appearance (`/etc/xdg/xfce4/xfconf/xfce-perchannel-xml/xfce4-notifyd.xml`)
* Custom wallpapers (`/usr/share/backgrounds/pi-top/{pink,teal,yellow}.png`)
* Additional start menu entries (`/usr/share/pt-os-ui-overrides`)
* Add onboard on-screen keyboard and custom config for window positioning
  * `/usr/share/onboard/onboard-defaults.conf`
* Custom terminal UI (`/usr/share/pt-os-ui-overrides/lxterminal.conf`)
