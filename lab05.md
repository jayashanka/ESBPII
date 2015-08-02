###ESBPII Lab 05 - Setting up owncloud
###IT12045068 		-      P.G.A Jayashanka

----------

#Setting up owncloud
##Create Local YUM repository on CentOS 7
###1. Create repository Source using mounting the DVD on the directory:
![image1](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/11836782_1019712211372888_3702307192261099354_n.jpg?oh=8412fe1f514fa96dc51828e1e346fc93&oe=5644186F)

###2. Configuration file:
Create the new repo file called cdrom.repo under /etc/repos.d directory
![image2](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xpt1/v/t1.0-9/11817056_1019712231372886_7824551852049468705_n.jpg?oh=1fb7e0d9ffba06711e4c77a6b1dd6fcc&oe=563E7B9C)
###3. Installation:
![image3](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtp1/v/t1.0-9/11267855_1019712291372880_3690279807049907932_n.jpg?oh=a5e026f86b7f8c041fe3b17915f14caf&oe=5646CC0D)

#Install OwnCloud on CentOS
###1. Prerequisite packages:
#####Owncloud based on PHP and database combination, database can be SQLite, MySQL, Oracle or PostgreSQL. So install PHP, Apache web server and MySQL server on CentOS. For demo purpose installed both SQLite and MySQL on CentOS.
![image4](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xpt1/v/t1.0-9/11828550_1019712321372877_1313186086773379497_n.jpg?oh=aa11480fecf662973007592341ac8804&oe=565CA926)
![image5](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/11214098_1019712421372867_662206482780963309_n.jpg?oh=edea21872f96bd0cd0c06dd6936702f9&oe=564FEDCE)
#####Set SELinux to allow OwnCloud to write the data.
![image6](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/11796178_1019712441372865_218698657814802947_n.jpg?oh=bface40a6cc3c35e066fcf416b296483&oe=564B78B5)
#####Allow apache in firewall.
![image7](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xfa1/v/t1.0-9/11825875_1019712474706195_1658718726253161145_n.jpg?oh=0259235c08fe6b328a5daa0faaee1241&oe=56530C76)

#####Start Apache and MariaDB, Auto start the service at system start-up.Auto start the service at system start-up.
![image8](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/11141160_1019712491372860_825961006082329970_n.jpg?oh=b9938f989815ffb521db84098e371931&oe=564CC940)

###2. Download and Setup:
#####Extract the archive.
![image9](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xta1/v/t1.0-9/11212788_1019712578039518_161770762881294379_n.jpg?oh=f4813fbbcf35dbe96c894f286177a47c&oe=56595CC0)
#####Allow the web server to read and write the files on cloud directory.
![image10](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xpa1/v/t1.0-9/11226542_1019712631372846_948755307239713366_n.jpg?oh=266651f504e4a1967d7aca27c95361fc&oe=5654F786)
###3. Create Database:
#####Execute the "mysql_secure_installation" command to start MySQL configuration for the first time.
![image11](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtp1/v/t1.0-9/11143581_1019712654706177_578913706074972118_n.jpg?oh=0cc8b24bc3e42e12fd973b34e795ba0b&oe=5643BFF5)
#####login to MySQL server.
![image12](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/11828768_1019712728039503_8892484816703332692_n.jpg?oh=fbb5745b6c3d00572ea4cebe24b99118&oe=564B29B7)
#####Create database called “clouddb”.
![image13](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtp1/v/t1.0-9/11800396_1019712741372835_3759016841428011583_n.jpg?oh=00569264241d72516ad8c9be86c789d3&oe=56526E8A)
#####Allow “clouddbuser” to access the “clouddb” database on localhost with predefined password.
![image14](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xat1/v/t1.0-9/11229307_1019712758039500_5503460869002675842_n.jpg?oh=4ae25a9eb1b52c9c8dea349a40526133&oe=564635C7)
###4. Configure Apache server:
#####While configuring Apache web server, it is recommended that to enable .htaccess to get a enhanced security features, by default .htaccess is disabled in Apache server. To enable it, open your virtual host file and make AllowOverride is set to All.
![image15](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xtf1/v/t1.0-9/11811332_1019712774706165_6496531102891109123_n.jpg?oh=958f330f8a5a291a6e70edee6f7c262c&oe=56542216)
![image16](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/11828799_1019712814706161_1481901003035239441_n.jpg?oh=edcc3421db96468ec562de2ae48f5397&oe=5659EAA7)
#####restart all services related to Apache server.
![image17](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xfp1/v/t1.0-9/11781605_1019712834706159_5615613695190385750_n.jpg?oh=8ffea78676c0554c0a4ba190dbb411b1&oe=564339FD)
###5. Configure ownCloud:
#####Open up web browser, point a URL to http://your-ip-address/owncloud. Browser will automatically take to ownCloud setup page where it must be configured before going to live. Enter admin user name, password, data folder location and database details.
![image18](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xft1/v/t1.0-9/11817243_1019712924706150_2772695362658438253_n.jpg?oh=486c54b9bd146603f45eed6507f26432&oe=5638A15D)
#####Home page will look like this, can start uploading the contents using upload button.
![image19](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xpf1/v/t1.0-9/11817037_1019712871372822_7580176986573930073_n.jpg?oh=326ed19bd9afc1abb6d05bfee44ce563&oe=5645378A)
![image20](https://scontent-bru2-1.xx.fbcdn.net/hphotos-xaf1/v/t1.0-9/11822355_1019712894706153_5486638253898918229_n.jpg?oh=5b483b5e714df8e2d98fbf26859d5b60&oe=5647C867)

----------
