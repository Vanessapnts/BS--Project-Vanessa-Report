# Report

## Project and Learning Journal

Computer Architecture and Systems

A report requested by<i> Conor McGinn </i>

## Introduction

The purpose of this report is to present the steps of the process of installing and configuring a virtual machine hosting a LAMP stack using Virtualbox. The main three stages are:

-	<b> Installing and configuring a virtual machine (Linux Ubuntu) using the program Virtualbox.
-	Deployment of a LAMP stack on Ubuntu Server. </b>
      – Installing Apache Web-Server.
      - MySQL.
      - PHP and Modules.
-	<b> Content Management System -  Installing and testing the hosted website. </b>


## Installing and configuring the virtual machine

First step was to download the Virtualbox. A <b>VirtualBox </b>is a software virtualization package that installs on an operating system as an application. Virtualbox allows additional operating systems to be installed on it. It can be found on (https://www.virtualbox.org/wiki/Downloads). (Image below)

   ![002](https://cloud.githubusercontent.com/assets/25640511/25554593/dfbcb228-2cc8-11e7-996d-9171fd9435a5.png)


Second step was to download a copy of the Ubuntu Server OS 16.10. It can be found on (http://releases.ubuntu.com/16.10/).
Download the Server Install image. (Picture below)

   ![1](https://cloud.githubusercontent.com/assets/25640511/25501789/da7a8332-2b8b-11e7-83e7-f3d9096d1e6a.png)

After downloading and installing the virtualbox the following steps were followed:

   ![2](https://cloud.githubusercontent.com/assets/25640511/25501788/da761cde-2b8b-11e7-80c9-6e24047e6cb3.png)
    
  - A virtual machine was created to install the guest OS (32 Bit Ubuntu Linux Server) using Virtualbox. To create we applied the following specifications:

   - <b> Memory Size </b>: 2048mb
   
   ![3](https://cloud.githubusercontent.com/assets/25640511/25501713/916d657e-2b8b-11e7-9cf7-56ffd324e1a5.png)
   
   - <b> Virutal Hard Disk </b> - Create a virtual hard disk now.
   

   ![4](https://cloud.githubusercontent.com/assets/25640511/25501714/91716b1a-2b8b-11e7-9a95-26cfba41e437.png)

   - <b> VDI </b> - Virtualbox Disk Image
   
   
   ![5](https://cloud.githubusercontent.com/assets/25640511/25501715/91744060-2b8b-11e7-89d5-7d2942012370.png)
   
   - <b> Dynamically Allocated </b> - Storage on physical hard disk
   
   
   ![6](https://cloud.githubusercontent.com/assets/25640511/25501716/919d1724-2b8b-11e7-945e-ed524e0d69c6.png)
   
   - <b> 20gb </b> - Create Virtual Hard Disk Size
   
   
   ![7](https://cloud.githubusercontent.com/assets/25640511/25501717/919e7876-2b8b-11e7-845e-6e2d036651f6.png)
   

After following the previous steps, it was necessary to mount the image .iso (Ubuntu Server) that we downloaded previously.
As shown in the image below, I selected the virtual CD drive by selecting the file Ubuntu image.

   ![8](https://cloud.githubusercontent.com/assets/25640511/25501718/919ef5bc-2b8b-11e7-92c5-9731f87f1d8e.png)


Subsequent to have mounted the .iso power on my virtual machine and the Ubuntu installed file the virtual machine boot up. 

  ![12](https://cloud.githubusercontent.com/assets/25640511/25501704/91430ebe-2b8b-11e7-8ea3-4e82a02778fe.png)
  

Some simple settings had to be made, such as language selection, automatic keyboard identification, region, and timezone and others. 

   After these simples configuration was setup, I created a username and password. Even though this was a simple step it was very important to write down and save the username and password as without them all the work would be lost. A good password it's composed of minimum of seven characters mixing with numbers and symbols and using uppercase and lowercase letters. 
   
   Also there was an option to encrypt my disk, if this option was selected I would have needed to use a password fo access it every time the virtual disk was boot up on the Virtualbox. 
   
   When I finished this part of the process and confirmed changes to the disk, the installation started.
   
   This part of the process took around 15 minutes. On this stage I did not set up a proxy and chose automatic security updates. I only installed the base package and installed the GRUB bootloader (GRUB 'GRand Unified Bootloader' is a boot loader package that supports multiple operating systems on a computer) then the installations was finished.
   
   The machine rebooted and then prompted my username and password, that I had created before.
   
   This was the installation and configuration of Ubuntu Server.
   
   In the end I took a snapshot of my machine to save all the changes I've made so far. Because I could recover the machine at the this point if something went wrong in the next steps. Also means that I have a fresh install image of Ubuntu Server to use so I would not have to go through the install process again if I wanted a identical machine.
   
## Deployment of a LAMP stack on Ubuntu Server

   <b>A Web server</b> is a system that delivers content or services to end users over the Internet. A Web server consists of a physical server, server operating system (OS) and software used to facilitate HTTP communication.
   
  <b> LAMP stack</b> is a group of open source software used to get web servers up and running. The acronym stands for Linux, Apache,  MySQL, and PHP. Since the virtual private server is already running Ubuntu.
   
<b>-   Apache Web-Server </b>

Apache is the most widely used web server software.

I first installed the Apache Web-Server ussing the command: <b> sudo apt-get install apache2 apache2-utils </b>

Then I changed the setting so the Apache2 Web-Server could start up at system boot, for this I used the systemctl enable command: 
<b> sudo systemtcl enable apache2 </b>. To Apache start the service I entered the command: <b> sudo systemctl start apache2 </b>

To confirm that my Apache server was running, I checked the network adapter settings making my VM visible from my host. I chaged the settings on my virtual network adapter, I set up port fowarding with my host to make it accesible from the host. Then I did the fallowing steps: <b> Settings - Network - Advanced - Por - Fowarding </b>, so I wrote "Name: <i> Apache </i>/ Protocol:<i> TCP</i>/ Host Port:<i> 80</i> /Guest Port:<i> 80 </i>. (iamge below)


![15](https://cloud.githubusercontent.com/assets/25640511/25501703/9142bdec-2b8b-11e7-9440-4e286553a15b.png)


After this I was able to access the default apache homepage on http://localhost on my browser. (image below)


![16](https://cloud.githubusercontent.com/assets/25640511/25501705/9143ff7c-2b8b-11e7-9a3e-1b8a8aa39185.png)


When I finished all those previosly steps configuring my local Apache Web-Server, I was able to host a basic webpage. 

<b>-   MySQL </b>

MySQL is an open source Database program. Different of the Apache MySQL is responsable of moden websites to maintain database that allows user to login, saving input to websites and etc.

To install my MySQL database server I used the command: <b> sudo apt-get install mysql-client mysql-server</b>

It's very important to keep the database secure, even though in my case I am not configuring a website for a production environment, to see how security would be configured I used the command: <b>sudo mysql_secure_installation </b>

![17](https://cloud.githubusercontent.com/assets/25640511/25501707/91589fe0-2b8b-11e7-8649-fde1d01d3928.png)


If I was working for a production environment a strong password would be necessary, in this case in my testing environment I chose setting which made my environment easier to run. When I changed the root password I saved it so I could remember after. I chose <b> Yes </b> to reload privilege tables, so all the changes was upoload.

<b>-  PHP and Modules </b>

PHP (PHP: Hypertext Preprocessor) is a widely used open source general purpose scripting language that is especially suited for web development and can be embedded into HTML. PHP allows web developers to create dynamic, interactive websites.

To install PHP and the modules I used the command: 
<b>sudo apt-get install php7.0 php7.0-mysql libapache2-mod-php7.0 php7.0-cli php7.0-cgi php7.0-gd

 After this command finished run I needed to test that PHP was working, so I created a <i>info php</i> file in my <i>var/www/html</i>  directory. I created that file and oppened it text editor VI to inserted some basic PHP code. I used the command:
 <b>sudo vi /var/wwww/html/info.php </b>
 
 This oppened a new file called <i> info.php.</i> Then I used the code : 
 <b>
 
 **< ?php
 
 phpinfo();
 
 ?>**
 </b>
 
 <i>PS: The code above with no space and no * </i>
 
 I pressed ESC after finish then I used the command <b> :wq</b> and saved my file and closed VI.(image below)
 
 
 ![21](https://cloud.githubusercontent.com/assets/25640511/25501709/915bb392-2b8b-11e7-8379-788a477f7fc5.png)

Then I oppened in my browser the address <b>localhost/info.php</b> and the image below appeared.

![23](https://cloud.githubusercontent.com/assets/25640511/25501710/915e840a-2b8b-11e7-80d8-3dc0f6045380.png)

That image above shows that my php was installed correctly and it was working perfectly.


## Content Management System


