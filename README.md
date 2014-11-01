zomboid-startup-script
======================

Project Zomboid Server Service Script for Linux (e.g. Ubuntu).
It will start your server as a service, which will automatically start on boot, and allows for easy start/save/restart/stop.

Preconditions:
- You have created a user named "steam" that has installed project zomboid.
- Steam is installed in "/home/steam/Steam".
- You have screen installed (apt-get install screen).

Installation:
- copy zomboid-server to "/etc/init.d/zomboid-server".
- enter "sudo update-rc.d zomboid-server defaults".
- start server using "service zomboid-server start" or "/etc/init.d/zomboid-server start".

Tips:
- Create a cronjob that saves every minute using "crontab -e" and add line: "*/1 * * * * service zomboid-server save".
- Connect to the running server via console using "screen -r", and detach from the screen using "Ctrl+A, ... D". Read "man screen" for further information about screen.