# Backup OS Image

 
> Basic principle: Make a mirror image of the IPC（You need to prepare another hard disk larger than 100g）
> Statement: To prevent the user from installing other drivers in IPC or destroying the system configuration during software, which will result in the inability to run the autopilot and start the driver, the original system can be restored through the backup image (the original image of the system has been attached to the U disk). Users can also back up their own system image, and can use the hard disk to save the image of IPC.
> References：<https://www.youtube.com/watch?v=8-7w5zwD9M4>

##  To create a backup system image, follow these steps:
1.Insert the USB drive and press F12 during startup (a wired keyboard can be used for this operation) to enter the flashing startup interface.
![alt 第一步](images/lQLPJwDCetAopwbNBD3NCGmwBeApK3fykssEPgo_EcB8AQ_2153_1085.png)
2.Use hard disk for mirroring（select first）
![alt](images/lQLPJwospArGKAbNBG7NCEqwTvJWVkqz2FsEPgo_GgCFAQ_2122_1134.png)
3.Select the Chinese interface (you can also choose other languages)
![alt](images/lQLPJwdL8ziBiAbNBG_NCAewb7ZWChcktagEPgo_GcCyAQ_2055_1135.png)
4.Keep
![alt](images/5.png)
5.Start Clonezilla(frist)
![alt](images/8.png)
6.Save image file to hard disk
![alt](images/6.png)
7.Select the first one when using a hard disk
![alt](images/10.png)
8.Insert hard drive
![alt](images/0.png)
9.When the hard disk is recognized，ctrl+c
![alt](images/l9.png)
10.Select the hard drive just mounted
![alt](images/E.png)
11.Select the first
![alt](images/E09png.png)
12.Select the directory to save
![alt](images/63.png)
13.Done Enter
![alt](images/D2.png)
14.Default the first option(Beginner)
![alt](images/76AE.png)
15.Savedisk 
![alt](images/94D879.png)
16.Name the file 
![alt](images/DC2EF.png)
17.Compress storage in zip(zip)  
![alt](images/720q90g.jpg)  
18.Default the first   
![alt](images/hh.jpg)  
19.Default the first  
![alt](images/f.jpg)  
20.Default the first  
![alt](images/g.jpg)  
21.Select——poweroff  
![alt](images/k.jpg)   
22.Start copying   
![alt](images/l.jpg)   
23.Wait for the automatic shutdown to complete

**Note**: 1. You need to prepare a hard disk to store your image.
2.The U disk is used as a boot disk, and the user needs to provide a hard disk when it needs to save its own image. Do not make any modifications, add or save other files on the U disk, so as not to damage the environment of the startup disk.
 