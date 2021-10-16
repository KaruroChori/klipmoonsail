# klipmoonsail

intended to build and run dockerized klipper, moonraker and fluid (mainsail on the original branch) on raspi (which has direct usb connection to your 3d printer).
Still, it will work on any system and I have it on my server.

1) edit buildstart.sh script and make sure mainsail version is correct; a separate buildstart.alt.sh has been added for fluidd.
2) put your klipper config to runtime/config as printer.cfg (beware of resent changes in klipper, which renders all old menu customizations broken). There is sample config file for AnetA8 included for reference if needed.
3) run ```./buildstart.sh init``` which will clone klipper and moonraker and download mainsail release, build docker images and run klipper for the first time interactively, so you can configure and flash the printer according to klipper docs (up to flashing)
4) run ```buildstart.sh run``` to run 

now klipper, moonraker and fluid are running in docker (hopefully) and you can connect to your raspi:8080 with web browser.

to stop, use "./buildstart.sh stop"
to restart, "./buildstart.sh restart"

issues, PRs, stars :) welcome.
