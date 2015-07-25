###IT12045068##
###P.G.A Jayashanka##

----------


# Creating an Amazon EBS-Backed Linux AMI #
------------------------------------------
## To create an AMI from a snapshot using the console ##

###1. Open the Amazon EC2 console. ###

![image01](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xfa1/v/t1.0-9/p206x206/11781788_1015552078455568_2456774802937957973_n.jpg?oh=cd0193f1c1d126c575518d2617d83039&oe=5611E40C)

###2. Connect to the instance and customize it. ###
![image02](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/11753646_1015552091788900_3495671941288495264_n.jpg?oh=46044d6ed7ba3c089a14ee4f6173952d&oe=564702E1)
![image03](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xft1/v/t1.0-9/11751730_1015552108455565_1955859198425532307_n.jpg?oh=71670f548663404fa2990cb854108426&oe=564EE68E)
![image04](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/11745624_1015552118455564_6828412941350619873_n.jpg?oh=a39273beae8812296b50f0e21ea9e7a4&oe=56425AE6)
### 3. In the navigation pane, click Instances and select your instance. Click Actions, select Image, and then click Create Image. ###
![image05](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xft1/v/t1.0-9/11781737_1015552138455562_3385975731934689162_n.jpg?oh=1077ea796ada2469aa4c8e65531b43eb&oe=56557291)

### 4. In the Create Image dialog box, specify the following, and then click Create Image. ###
1. A unique name for the image.
2. A description of the image, up to 255 characters.
3. By default, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. Select No reboot if you don't want your instance to be shut down.
![image06](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xpa1/v/t1.0-9/11800514_1015552148455561_5909054935621316956_n.jpg?oh=ea1d7c33570413de07f36048e94d0da3&oe=565653A3)
![image06](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xtp1/v/t1.0-9/11702775_1015552168455559_5856235546841110529_n.jpg?oh=41df7888355e1020684f27a3da39cbc4&oe=5651D8BF)

### 5. Click AMIs in the navigation pane to view the status of your AMI. While the new AMI is being created, its status is pending. This process typically takes a few minutes	to finish, and then the status of your AMI is available. ###
![image07](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xaf1/v/t1.0-9/11760041_1015552181788891_5783027233434951491_n.jpg?oh=3de1881d14b4e20c79eecb258534a6e5&oe=5653C021)

## Creating a Linux AMI from a Snapshot ##

###1. In the navigation pane, under Elastic Block Store, choose Snapshots. ###
![image08](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xaf1/v/t1.0-9/11781698_1015552198455556_7199600608507131261_n.jpg?oh=28f3cbec5079c576892f449833854890&oe=56470EF6)
### 2. Choose the snapshot, and then choose Create Image from the Actions list. ###
![image08](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xft1/v/t1.0-9/11745485_1015552228455553_7576222398320958923_n.jpg?oh=13d0b0fdd4a5fb68a03343164ff10e81&oe=5644CE54)

![image09](https://scontent-cdg2-1.xx.fbcdn.net/hphotos-xpt1/v/t1.0-9/11709639_1015552225122220_7021234515318013258_n.jpg?oh=52f8a460efd2614e78e68ad4883368b4&oe=56489BD6)




