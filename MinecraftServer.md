# How to host a minecraft server on an android device

## Last updated: 01-19-2019

#### Written by 8_N3Z

---

- Prerequisites: Youll need to download 3 Apps

  AnLinux - [Download](https://play.google.com/store/apps/details?id=exa.lnx.a)


    Termux - [Download](https://play.google.com/store/apps/details?id=com.termux)

    Hacker's Keyboard - [Download](https://play.google.com/store/apps/details?id=org.pocketworkstation.pckeyboard)

---

- Download all the apps needed,Linked above

1.  Open Anlinux
2.  Tap Choose, then pick which linux version you would like to use, will be the same no matter which is used
3.  Tap copy and then you back button to close out the ad
4.  Tap launch
5.  Termux should've opened, so tap and hold until you can paste after which just push your enter key and wait for linux to install
6.  After its done the last line will tell you how to start running linux in my case i run `./start-ubuntu.sh`
7.  Then make sure everything's updated by running `apt-get update`
8.  now we need java so run `apt-get install openjdk-8-jdk` it will prompt you in a moment if you want to use up space just put `y` and tap enter
9.  now we need to make a folder for the server, run `mkdir [foldername]`
10. then go into folder by running `cd [foldername]`
11. now to actually download the server run `wget https://s3.amazonaws.com/Minecraft.Download/versions/[YOURMINECRAFTVERSION]/minecraft_server.[YOURMINECRAFTVERSION].jar`
    Example for minecraft 1.12.2: `wget https://s3.amazonaws.com/Minecraft.Download/versions/1.12.2/minecraft_server.1.12.2.jar`
12. now for simplicity's sake we want to change the jar name to something shorter so we will copy it and change it to server.jar by running `cp minecraft_server.1.12.2.jar server.jar`
13. now we will run the server once `java -Xmx1G -jar server.jar nogui`
14. Now you'll get a message telling you to accept the eula so we need to get a text editor installed, run `apt-get install nano`
15. then you'll just open it by running `nano eula.txt`
16. Once in here you will need to change false to true, this is where the keyboard will help since it has arrow keys
17. then tap Ctrl+x then tap y and enter that will exit and save
18. run the server once more `java -Xmx1G -jar server.jar nogui`
19. After you see the servers done loading you can connect, you'll need the internal ip which can be found under settings-> wifi then tapping on your wifi clicking advance options
20. boot minecraft on your pc, click multiplayer, click direct connect, type in the ip and connect
