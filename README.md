
Skip to content

    BinaryBrother
    MuMuPlayerDebloat

Repository navigation

    Code
    Issues
    Pull requests
    Agents
    Actions
    Projects
    Wiki
    Security and quality
    Insights
    Settings

Files
tT

    BlcokAdsMumu.bat
    README.md

    MuMuPlayerDebloat

/
in
main

Indent mode
Indent size
Line wrap mode
Editing README.md file contents
  1
  2
  3
  4
  5
  6
  7
  8
  9
 10
 11
 12
 13
 14
 15
 16
 17
 18
 19
 20
 21
 22
 23
 24
 25
 26
 27
 28
 29
 30
 31
 32
 33
 34
 35
 36
 37
 38
 39
 40
 41
 42
 43
 44
 45
 46
 47
 48
 49
 50
 51
 52
 53
 54
 55
 56
 57
 58
 59
 60
 61
 62
 63
 64
 65
 66
 67
 68
 69
 70
# MuMuPlayer 6 Android 15 Debloat
I've made a YouTube video for anyone who wants to watch it https://www.youtube.com/watch?v=1wchUkN2Jjc 
But I'll list the steps here, too.

# Emulator Settings
In the MuMuPlayer Launcher

1.) Click the 3-dots next to the target Android 15 Virtual Device

2.) Select Device Settings

3.) Choose the Developer options section.

4.) Enable Root

5.) Change Disk sharing to Writable system disk.

6.) Close Settings

7.) Launch target Android device running Android 15.

# Android 15 Process
In Android 15

1.) Start downloading Chrome, by clicking on it.

2.) Go to Settings and Search "Private DNS"

3.) Change the value from Automatic to 
77aead.dns.nextdns.io
This will block most system ads.

4.) Go back to Chrome and search for Root Explorer apk and click the first link.
We need this app to modify the system partition.
It doesn't really matter how you get the APK, it's just the File Manager that seems to work for me.

5.) Next, we need to use KernelSU to give Root Explorer root privileges.
So Open KernelSU.

6.) Click the Superuser category on the left-hand side of the screen.

7.) Click Root Explorer

8.) Enabled Superuser, but this isn't enough to delete files in the system partition just yet.

9.) Change "Groups" to root.

10.) Click App Profile and Select Custom

11.) Click Capabilities and give Root Explorer every seen permission. I'm sure only a few of these are needed, but I don't know which ones specifically, so I select them all. And be sure to click "Confirm".

12.) Verify that Capabilities is propagated with permissions and close KernelSU

13.) Open Root Explorer

14.) Scroll down and select the "system" partition.

15.) Then find the "priv-app" folder and enter it.

16.) Hold-click on com.mumu.acc_overseas to begin selection.
Also select 
com.mumu.store_overseas
com.netease.mumu.cloner.

17.) After having selected all 3, click the trash-bin icon at the top right-hand corner of the screen to delete all three folders.

But, as you can see... We still get ads on Device Boot. With MuMu Store removed, accidentally clicking them won't prompt downloads, but who wants to look at these ads every boot?

Finally, close the Android 15 instance and download this IP blocking script. You can view the contents and see that the only thing it's doing is blocking IP addresses.
https://github.com/BinaryBrother/MuMuPlayerDebloat/raw/refs/heads/main/BlockAdsMumu.bat
