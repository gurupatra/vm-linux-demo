#Pre-Requisites
Download & Install Virtual Box https://www.virtualbox.org/wiki/Downloads
Download & Install Vagrant https://www.vagrantup.com/
Download(if you don't have git alredy) & Install Git https://git-scm.com/download/win

#Enable virtualisation of CPU.
If VT-x is disabled in the BIOS for all CPU modes (VERR_VMX_MSR_ALL_VMX_DISABLED),
Access you BIOS setup via your latops BIOS Key (F2, F12 or F10) and then enable Virtualisation.
If not sure about your BIOS Setup Keys in Windows 10, go to 

Settings --> Recovery  --> Advance Startup
Select Troubleshoot --> UFEI Firmware Update

This will show you the Function Key for BIOS Settings.

In BIOS settings, look for Virtualisation option, Enable, Save and Exit.


#clone the code repo.

$git clone 
$cd virtual-machine-demo
$vagrant up

will take few minutes to download the virtual box - Ubuntu 18.04 LTS 64-bit.

Once started, ssh to the guest VM (Virtual Machine) - Linux machine

$vagrant ssh

You can try out all linux/Unix (except a few!) commands and practice shell scripting. 

#Installing Software in the gues OS.
Any additional software you want to run in the guest Linux Machine, you can use the
apt package manager to install.

For example to install apache web server on the VM you can
$sudo apt-get update 
$sudo apt-get install appache2

You can logout from the VM simply type logout on the ssh terminal

#Stopping the VM
You can stop the VM from the Virtual Box --> Machine --> Power Off

#Disposing the VM
You can dispose off the VM, when no lnger needed
$vagrant destroy

Note - you can bring the VM back up using the vagrant up command.

#Further Learning

https://learn.hashicorp.com/tutorials/vagrant/getting-started-networking?in=vagrant/getting-started

You can try other Linux distributions:
     CentOS7 - https://app.vagrantup.com/centos/boxes/7
     Fedora - https://app.vagrantup.com/generic/boxes/fedora28
     
from Hashicorp's Vagrant Cloud https://app.vagrantup.com/boxes/search?provider=virtualbox

#Advanced Learning
   Networking
   