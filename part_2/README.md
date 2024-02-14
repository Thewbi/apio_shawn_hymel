# Tutorial 2 - https://www.youtube.com/watch?v=gtkQ84Euyww

## Installation of the toolchain

1. Install python
1. pip install -U apio
1. python -m pip install apio==0.8.4
1. pip install apio
1. run a quick test: 'apio --version' has to print the version
1. apio install --all
1. apio install drivers

## Enable the ftdi drivers

1. Plug in the IceStick
1. Open a cmd terminal with administrator priviledges
1. apio drivers --ftdi-enable
1. Zadig will open	
1. In Zadig > Option > List all devices
1. From the drop down list, select Dual-RS232 HSI (Interface 0)
1. In the spinner box that the green arrow points to, select libusbK (v3.0.7.0)
1. Click replace driver. After installing, quit Zadig and close the Administrator Cmd terminal.
1. apio system --lsftdi

## Run a predefined example for the ICEstick provided by apio

1. cd dev
1. mkdir apio
1. cd apio
1. apio examples -d icestick\leds
1. cd icestick
1. cd leds
1. apio init --board icestick
1. apio verify
1. apio sim
1. apio build
1. apio upload

All the user-leds (four red, one green in the middle) should light up constantly.