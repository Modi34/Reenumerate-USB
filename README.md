# Reenumerate-USB

![](https://i.imgur.com/yZ3IlPu.png)

Sometimes I need to unplug a usb device and plug it again.
This workflow does it via reenumerate binary copied from USB Prober.app 

Main reason why I need it is [my shuttle express](http://forums.contourdesign.com/viewtopic.php?f=4&t=8479&p=15032&hilit=mac+os#p15032) - it does not work on system startup.
I also had the same issue with 3d conexion space mouse and wacom touch driver

if you want to run it on system startup you can use this bash script:
``./reenumerate -v -l "0x$(ioreg -p IOUSB -w0 | sed -n 's/.*ShuttleXpress@\([^ ]*\).*/\1/p')"``

USB Prober.app can be downloaded from https://developer.apple.com/download/more/
