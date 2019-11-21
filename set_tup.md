# Hack the box gives some basic steps to make sure you connect. My plan is to expand those a little further. 

## Install software for managing virtual machines, such as VirtualBox, VMWare Workstation, etc.

  I am using virtualbox (URL https://www.virtualbox.org/wiki/Downloads)

## Create a Linux virtual machine. You can use a pre-made pentesting OS such as Kali Linux/Parrot Linux, or build your own toolkit from scratch. We do not recommend using Windows as your primary attack environment.
 
 In my case, I am using Kali Linux on Mac. (URL to Kali Download https://www.kali.org/downloads/, for mac use the Kali Linux XFCE 64-Bit)  
 
 ## Once you have both VirtualBox and the Kali Linux downloaded. 

Very useful URL for this is https://null-byte.wonderhowto.com/how-to/mac-for-hackers-install-kali-linux-as-virtual-machine-0174250/

## Download your connection pack, it should be your_username.ovpn

## Run openvpn your_username.ovpn in terminal from Kali Linux.
  This step was tricky for me. 
  
 From virtualbox, click your Kali box -> Settings -> Shared Folders -> add path (to your machine's downloads so you can find the ovpn file later) -> give it full access
 
 Then on Kali -> open File Manager ->  on the left side you should see something along the lines of File System and under another path to Downloads (for me its called sf_Downloads, you should see your Downloads from your actual computer) -> verify that the ovpn file is there.
 
 From Kali, open terminal -> navigate to the folder path (for me its /media/sf_Downloads) -> run command `sudo apt-get install openvpn` -> and then run your file ` openvpn --config xcortez.ovpn`
