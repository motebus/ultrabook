## **setup RPi autorun**  
1.  make autostart DIR  
    `mkdir /home/pi/.config/autostart`  

2.  create new file as xxx.desktop  
    #### RPi auto run program  
    1.  xxx.desktop file content is  
        ```
        [Desktop Entry]
        Name=example
        Comment=My Python Program
        Exec=python /home/pi/example.py
        Icon=/home/pi/example.png
        Terminal=false
        MultipleArgs=false
        Type=Application
        Categories=Application;Development;
        StartupNotify=true
        ```  

    2.  if program have snap, EXEC also can key in snap package name  
        example:  
        ```
        [Desktop Entry]  
        Name=smartscreen  
        Comment=smartscreen  
        Exec=smartscreen  
        Icon=/home/pi/smartscreen.png  
        Terminal=false  
        MultipleArgs=false  
        Type=Application  
        Categories=Application;Development;  
        StartupNotify=true  
        ```    

    #### RPi auto run Web  
    1.  modify EXEC `x-www-browser --start-fullscreen <url>`  
        example:  
        ```
        [Desktop Entry]
        Name=ioc-view
        Comment=ioc-view
        Exec=x-www-browser --start-fullscreen http://boss.ypcloud.com:8083/
        Icon=/home/pi/ioc.png
        Terminal=false
        MultipleArgs=false
        Type=Application
        Categories=Application;Development;
        StartupNotify=true
        ```  

3.  `touch /home/pi/.config/autostart/xxx.desktop`  

4.  `vim /home/pi/.config/autostart/xxx.desktop`  

5.  .desktop file can use `#` annotate EXEC, so xxx.desktop will not be execute.  

## **reference:**  
[開機自動執行python程式](https://medium.com/@yanweiliu/raspberry-pi%E5%AD%B8%E7%BF%92%E7%AD%86%E8%A8%98-%E5%8D%81-%E9%96%8B%E6%A9%9F%E8%87%AA%E5%8B%95%E5%9F%B7%E8%A1%8Cpython%E7%A8%8B%E5%BC%8F-69a936709c0c)  
