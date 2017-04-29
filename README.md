# Report

## Project and Learning Journal

Computer Architecture and Systems

A report requested by Conor McGinn 

## Introduction

The purpose of this report is to present the steps of the process of installing and configuring a virtual machine hosting a LAMP stack using Virtualbox. The main three stages are:

-	Installing and configuring a virtual machine (Linux Ubuntu) using the program Virtualbox.
-	Deployment of a LAMP stack on Ubuntu Server – Installing Apache Web-Server, MySQL and PHP and Modules.
-	Content Management System -  Installing and testing the hosted website.

## Installing and configuring the virtual machine

First step was to download the Virtualbox. A VirtualBox is a software virtualization package that installs on an operating system as an application. Virtualbox allows additional operating systems to be installed on it. It can be found on https://www.virtualbox.org/wiki/Downloads. (Image below)

![002](https://cloud.githubusercontent.com/assets/25640511/25554593/dfbcb228-2cc8-11e7-996d-9171fd9435a5.png)

Second step was to download a copy of the Ubuntu Server OS 16.10. It can be found on http://releases.ubuntu.com/16.10/.
Download the Server Install image. (Picture below)

![1](https://cloud.githubusercontent.com/assets/25640511/25501789/da7a8332-2b8b-11e7-83e7-f3d9096d1e6a.png)

After downloading and installing the virtualbox the following steps were followed:

![2](https://cloud.githubusercontent.com/assets/25640511/25501788/da761cde-2b8b-11e7-80c9-6e24047e6cb3.png)

- A virtual machine was created to install the guest OS (32 Bit Ubuntu Linux Server) using Virtualbox. To create we applied the following specifications:

   - Memory Size: 2048mb
   
   ![3](https://cloud.githubusercontent.com/assets/25640511/25501713/916d657e-2b8b-11e7-9cf7-56ffd324e1a5.png)
   
   - Virutal Har Disk- Create a virtual hard disk now.

   ![4](https://cloud.githubusercontent.com/assets/25640511/25501714/91716b1a-2b8b-11e7-9a95-26cfba41e437.png)

   - VDI - Virtualbox Disk Image
   
   ![5](https://cloud.githubusercontent.com/assets/25640511/25501715/91744060-2b8b-11e7-89d5-7d2942012370.png)
   
   - Dynamically Allocated - Storage on physical hard disk
   
   ![6](https://cloud.githubusercontent.com/assets/25640511/25501716/919d1724-2b8b-11e7-945e-ed524e0d69c6.png)
   
   - 20gb - Create Virtual Hard Disk Size
   
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

