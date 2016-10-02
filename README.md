# Vagrant with Wordpress

This is an easy to use Vagrant box that includes all setup needed for Wordpress. See below on the list of items included on this box.

  - Ubuntu 12.04
  - PHP 5
  - Nginx
  - MySQL
  - PHP5-Fpm
  - PHP MyAdmin
  - Wordpress Single Site with Postman using Gmail SMTP

### Pre-Requisite

User should already have

* [Virtualbox]
* [Vagrant] 

### Installation

Once you have the above pre-requisite installed you can follow the instructions below

Clone this repository
```sh
$ git clone https://github.com/vbernabe/vagrant-wordpress.git vagrant-wordpress
```

Download vagrant-wordpress.box
```sh
$ cd vagrant-wordpress
$ wget https://www.dropbox.com/s/1e6onzt27cva42c/vagrant-wordpress.box?dl=0
```

Add vagrant-wordpress box to local vagrant 

```sh
$ vagrant box add vagrant-wordpress vagrant-wordpress.box
```

Set your Wordpress local URI
```sh
$ sudo vi /etc/hosts
Add this line: 
192.168.33.44 	wordpress.local.com
```
For Windows /etc/hosts equivalent is under \WINDOWS\system32\drivers\etc make sure that your are updating as Super User.

Start your vagrant box
```sh
$ vagrant up
```

**Done!**

### Managing your Vagrant Wordpress box

To access your vagrant
```sh
$ vagrant ssh
```

To stop vagrant
```sh
$ vagrant halt
```

For Windows Users you need to install PuTTy to manage Vagrant

> Other vagrant commands: https://www.vagrantup.com/docs/cli/

#### Access Wordpress Admin

> Go to your browser and access http://wordpress.local.com/wp-admin

#### Access Wordpress

> Go to your browser and access http://wordpress.local.com

#### Access PHP MyAdmin

> Go to your browser and access http://wordpress.local.com:8888/

### Misc Stuff
* VM User Pass
  * Username: vagrant
  * Password: vagrant

* MySql User Pass
  * Username: root
  * Password: password123

* IP and Port
  * 192.168.33.44:80/wp-admin - wordpress
  * 192.168.33.44:8888 - phpmyadmin

* Hostname
  * 192.158.33.44 - wordpress.local.com

* Wordpress User Pass
  * Username: wp-user-workshop
  * Password: password123

* Gmail
  * Username: wpuserworkshop@gmail.com

License
----

MIT


**Free Software, Hell Yeah!**

[//]: # (These are reference links used in the body of this note and get stripped out when the markdown processor does its job. There is no need to format nicely because it shouldn't be seen. Thanks SO - http://stackoverflow.com/questions/4823468/store-comments-in-markdown-syntax)


   [virtualbox]: <https://www.virtualbox.org/wiki/Downloads>
   [vagrant]: <https://www.vagrantup.com/downloads.html>

