 ![osticket-logo700x208](https://user-images.githubusercontent.com/130851140/234125060-38a61c7a-9607-427e-818d-db129b76f1fe.png)


# osTicket - Installation

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. Here you will find some of the things that were needed to install osTicket to my Windows 10 Microsoft Azure virtual machine.

<h2>Environments and Technologies Used</h2>
  
  - Microsoft Azure (Virtual Machine/Compute)
  - Remote Desktop
  - Internet Information Services(IIS)
  - osTicket

<h2>Operating Systems Used </h2>

   - Windows 10(21H2)
  
<h2>List of Prerequisites</h2>
  
   - osTicket Installation Files
   - Remote Desktop Connection
   - Completing osTicket browser installation
   - Directory creating 

<h2>Installation Steps</h2>

To begin we will open up the Azure Virtual Machine through remote desktop connection. From there we will start the installation of the files we will use for osTicket.

![image](https://user-images.githubusercontent.com/130851140/234133944-5b950dd6-0079-4059-b3e7-dab91b3d48ff.png)



Once you are in your Virtual Machine(VM) we will make sure to enable/install IIS with CGI. After that we will move on to installing PHP Manager for IIS and Rewrite Module. 

![image](https://user-images.githubusercontent.com/130851140/234135236-8e3b141b-cb27-448f-bc3c-74d7a9faea6d.png)

 ![image](https://user-images.githubusercontent.com/130851140/234135946-c896da74-8264-46b1-b24a-8fc0ac1e151b.png)
 ![image](https://user-images.githubusercontent.com/130851140/234136158-416bc8ba-ff44-4eb5-9416-d0e1ad30da98.png)
 
 
 
 When those files are completely downloaded we will need to create a directory called PHP(C:\PHP) for the files we will begin to download.
 
 ![image](https://user-images.githubusercontent.com/130851140/234137531-3d0fe4b1-d18c-423b-a9fa-be7c1b14d478.png)
 
 
 Next step we will begin to download the VC redist file.
 
 
 ![image](https://user-images.githubusercontent.com/130851140/235475115-6bfe47da-40d7-4132-aff8-40fdc1e79b00.png)
 
 
 Here we will install MySQL
 
 ![image](https://user-images.githubusercontent.com/130851140/235475964-f5ea9b4d-3fbd-4065-a721-ab6c32ea47cb.png)
 
 Within this download you will create your password to use when setting up osTicket.
 ![image](https://user-images.githubusercontent.com/130851140/235476390-0038276d-ee41-4710-b20f-c7e253912207.png)

 
 









