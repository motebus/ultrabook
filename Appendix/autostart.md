# autostart

## Create a .desktop File
 Open a terminal, and execute the following commands to create an autostart directory (if one does not already exist) and edit a .desktop file for our clock example:

    mkdir /home/jujue/.config/autostart
    nano /home/jujue/.config/autostart/smartscreen.desktop

 Copy in the following text into the clock.desktop file. Feel free to change the Name and Exec variables to your particular application.

    [Desktop Entry]
    Type=Application
    Name=smartscreen
    Exec=smartscreen
    
 ## Reboot
 Save and exit with ctrl + x, followed by y when prompted to save, and then enter. Reboot with:

    sudo reboot
