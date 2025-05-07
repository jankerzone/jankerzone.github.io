---
layout: post
title:  "[Kumpulan] Sintak Terminal Linux Untuk Saya Sendiri"
date:   2025-05-07 09:00:00 +0530
comments: true
---


> Saking bodohnya saya menggunakan terminal Linux, maka saya bikinkan
> untuk diri saya sendiri khususnya, dan rekan-rekan yang kebetulan
> mampir kesini, beberapa perintah yang sering digunakan dalam mengelola
> VPS.

![ilustrasi](https://miro.medium.com/v2/resize:fit:1050/format:webp/0*3WgriVmfY3ULMbxm.png)

### Daemon
	php -q /etc/sentora/panel/bin/daemon.php

### Setting SMTP via TSL LetsEncrypt
> [https://www.svennd.be/setting-up-postfix-tsl-with-lets-encrypt/](https://www.svennd.be/setting-up-postfix-tsl-with-lets-encrypt/)

### Virtual Host for webmail
	</VirtualHost>
	# Configuration for WebMail - webmail.yoursite.tld
	<VirtualHost *:80>
	ServerAdmin webmaster@domain.com
	DocumentRoot "/etc/sentora/panel/etc/apps/webmail/"
	ServerName webmail.domain.com
	AddType application/x-httpd-php .php3 .php
	<Directory />
	Options +FollowSymLinks -Indexes
	 AllowOverride All
	 Require all granted
	</Directory>

### Mail
> [http://sharadchhetri.com/2013/03/06/how-to-change-smtp-port-number-25-in-postfix/](http://sharadchhetri.com/2013/03/06/how-to-change-smtp-port-number-25-in-postfix/)

### Setting Client
![enter image description here](https://miro.medium.com/v2/resize:fit:1252/format:webp/0*ckuuzm6Kw2672Pv8.png)
![enter image description here](https://miro.medium.com/v2/resize:fit:1262/format:webp/0*JVjlDqT5Vz13iSC1.png)

	chown -R apache:apache [url]
### dan
chmod +x [url]

### Remove Bulk/Folder
	rm -rf [path]

### Melakukan diff-ing

	diff -u file1.csv file2.csv > diff.txt

### Install Netstat

	sudo yum install net-tools

### Menampilkan netstat

	netstat -plutn | grep [port]

### Melakukan Curl sebuah web

	curl -gkvL [full url]

### Start / Restart Apache dan MariaDB

	service mariadb/httpd start/restart

### Check Hardisk via SSH

	# df -h atau df -k

### Check size folder dan file

	sudo du -h /folder/ | sort -rh | head -5

### Log MariaDB

	/var/log/mariadb/mariadb.log

### Archieve / zip / tar / gz

	tar cvzf kompresan.tar.gz /home/folder

### Ekstrak / zip / tar / gz

	tar -xvf kompresan.tar
### Setting Permision dan Owner pada Wordpress
	chown www-data:www-data  -R * # Jadiin apache ownernya  
	find . -type d -exec chmod 755 {} \;   
	find . -type f -exec chmod 644 {} \; #jadiin semua folder/files kebaca username, kecuali wp-content dia harus dibaca juga sama apachechown <username>:<username>  -R * # Let your useraccount be owner  
	chown www-data:www-data wp-content # Let apache be owner of wp-contentchmod -R 775 wp-content/

### Baca-baca dulu soal Cron dan Crontab
> https://www.digitalocean.com/community/tutorials/how-to-use-cron-to-automate-tasks-on-a-vps?source=post_page-----8590154d0ecc---------------------------------------
### Cek apakah Port sudah listening apa belum
	sudo netstat -plunt
### Belajar Membuka dan Menutup Port Server

> [https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-using-firewalld-on-centos-7](https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-using-firewalld-on-centos-7?source=post_page-----8590154d0ecc---------------------------------------#setting-rules-for-your-applications)
### Instalasi OpenVPN

	wget https://git.io/vpn -O openvpn-install.sh
---
	sudo chmod +x openvpn-install.sh  
	sudo bash openvpn-install.sh

ikuti langkah-langkah instalasi

### Rename File

	cp file_lama file_baru

### **Youtube-dl**

Install at Ubuntu

	sudo apt purge youtube-dl   
	sudo pip3 install youtube-dl  
	hash youtube-dl

Ketika mendapatkan Forbidden

	youtube-dl --rm-cache-dir

### Download MP3 format

> youtube-dl -x --audio-format mp3 https://www.youtube.com/watch?v=dQw4w9WgXcQ

### **Youtube-dl alternatif**

	python3 -m pip install -U yt-dlp

Download berdasarkan format

	yt-dlp --list-formats link-youtube  
	  
	yt-dlp -f 22 link-youtube

### Dump mySQL

	$ mysqldump -u [username] -p [database_name] > [backup_file_name].sql

### Restore mySQL

	$ mysql -u [username] -p [database_name] < [backup_name].sql

### **Pulling git without entering passphare**

	ssh-add ~/.ssh/id_rsa
  