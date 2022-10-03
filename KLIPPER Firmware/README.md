# Klipper Firmware
* Work in progress, will update as I go
## Need to follow [this](https://klipperscreen.readthedocs.io/en/latest/Hardware/?h=ori#screen-rotation) to get the klipper screen rotation and touchscreen matrix setup correctly.</br>
`sudo nano /usr/share/X11/xorg.conf.d/90-monitor.conf`</br>
Section "Monitor"</br>
    Identifier "HDMI-1"</br>
    Option "Rotate" "right"</br>
    Option "PreferredMode" "800x400"</br>
EndSection</br>
`sudo service KlipperScreen restart`</br>
`DISPLAY=:0 xinput`</br>
`DISPLAY=:0 xinput set-prop "BIQU BTT-HDMI5" 'Coordinate Transformation Matrix' 0 1 0 -1 0 1 0 0 1`</br>
`sudo service KlipperScreen restart`</br>
## Need to follow [this](https://github.com/bigtreetech/CB1/issues/44#issuecomment-1264733456) to get the gpio pins working if you get an parsing error.
