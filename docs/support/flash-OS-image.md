# Flash-OS-image

> Basic principle：Flash the system backup image to IPC
> Statement：When the industrial computer system is damaged, missing files make it impossible to run the autopilot, or the system cannot be entered due to a black screen, you can use a U disk to restore the industrial computer system and restore the factory settings.
> References：<https://www.youtube.com/watch?v=YEFt2LPSYMk>

## According to the following steps
1.Insert the USB drive and press F12 during startup (a wired keyboard can be used for this operation) to enter the flashing startup interface.
![alt 第一步](images/lQLPJwDCetAopwbNBD3NCGmwBeApK3fykssEPgo_EcB8AQ_2153_1085.png)
2.Select the second option when using a USB flash drive to restore the image
![alt 第二步](images/006.jpg)
3.Select the Chinese interface (you can also choose other languages)
![alt](images/lQLPJwdL8ziBiAbNBG_NCAewb7ZWChcktagEPgo_GcCyAQ_2055_1135.png)
4.Keep
![alt](images/5.png)
5.Start Clonezilla(frist)
![alt](images/8.png)
6.The image comes from the USB drive
![alt](images/6.png) 
7.Read to U disk(dev/sdb)
![alt](images/35.jpg) 
8.ctrl+c
![alt](images/l9.png) 
9.Select U disk when inserting
![alt](images/36.jpg) 
10.Select the image file in the U disk
![alt](images/15.png) 
11.Default the first option(Beginner)
![alt](images/16.png)
12.Select the third option to restore the image of the U disk to the industrial computer
![alt](images/37.jpg) 
13.Select the image name that needs to be restored    
![alt](images/38.jpg)  
14.System Disk Location
![alt](images/23.png) 
15.Check before restore
![alt](images/24.png)
16.select——poweroff
![alt](images/25.png)
17.Waiting to read mirror
![alt](images/26.png)
18.Enter y
![alt](images/20.png)
19.Wait for the flash (about 10 minutes) 
![alt](images/21.png) 
20.The system automatically shuts down - flashing has been completed

**Note**： This U disk is only recommended to restore the image, do not make any modification, add or save other files, so as not to damage the environment of the startup disk.



