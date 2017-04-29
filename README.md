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

First step was to download the Virtualbox. A VirtualBox is a software virtualization package that installs on an operating system as an application. It allows additional operating systems to be installed on it and can be found on https://www.virtualbox.org/wiki/Downloads. (Image below)

![002](https://cloud.githubusercontent.com/assets/25640511/25554593/dfbcb228-2cc8-11e7-996d-9171fd9435a5.png)

Second step was to download a copy of the Ubuntu Server OS 16.10. It can be found on http://releases.ubuntu.com/16.10/.

Download the Server Install image. (Picture below)

![1](https://cloud.githubusercontent.com/assets/25640511/25501789/da7a8332-2b8b-11e7-83e7-f3d9096d1e6a.png)

After downloading and installing the virtualbox the following steps were followed:

- A virtual machine was created to install the guest OS using Virtualbox applying the following specifications:

   32 Bit Ubuntu Linux Server (that we download the image)

![2](https://cloud.githubusercontent.com/assets/25640511/25501788/da761cde-2b8b-11e7-80c9-6e24047e6cb3.png)




Using VM VirtualBox create a machine for hosting our 32 Bit Ubuntu Linux server. 
You will need to select the size and type of drive you use as well as the memory you will assign to your machine. I recommend the following settings:
 • Memory Size: 2048mb 
• Virtual Hard Disk: VDI, dynamically allocated, 20gb 
You will then need to mount the .iso image (Ubuntu Install File) you downloaded/copied earlier and proceed. You can access the virtual CD drive by accessing the settings for the virtual machine and looking in the Storage settings.

