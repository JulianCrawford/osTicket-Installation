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
 
 
 Here we will install MySQL as typical setup and from there we will choose standard configuration
 
 ![image](https://user-images.githubusercontent.com/130851140/235475964-f5ea9b4d-3fbd-4065-a721-ab6c32ea47cb.png)
 
 You will then create your password and complete the download shown below.
 ![image](https://user-images.githubusercontent.com/130851140/235476390-0038276d-ee41-4710-b20f-c7e253912207.png)

 On our Virtual Machine we will open up IIS as admin and register PHP within IIS
 
 ![image](https://user-images.githubusercontent.com/130851140/235479141-526927fb-382a-4604-9934-fcbc6186a9e7.png)

 ![image](https://user-images.githubusercontent.com/130851140/235479229-f0cf35d1-2315-47f1-94ba-c5efb7b51c97.png)
 
 The PHP files we downloaded will be use in IIS to register new PHP verison then we will stop and start the IIS manager again.
 
 ![image](https://user-images.githubusercontent.com/130851140/235480494-66d62b6f-c99a-41b2-9cc0-6ffdebfc098f.png)
 
 On this next step we will download the osTicket zip file and within the zip we will extract the Upload file into the inetpub folder wwwroot in C: drive and rename file to osTicket
 
 ![image](https://user-images.githubusercontent.com/130851140/235482808-261b78a9-e5a9-48b0-9ac7-793fabafe7e3.png)
 
 ![image](https://user-images.githubusercontent.com/130851140/235483324-37080984-da6d-418f-ba29-ad734294e027.png)

You should be able to see the osTicket file within you IIS manager under Sites>Default. On the right it will be a Http named Browse 80 you can click on and will bring up osTicket Installer

![image](https://user-images.githubusercontent.com/130851140/235484448-e4963cfb-a3fa-4d7b-b1fe-ae60693f1706.png)

![image](https://user-images.githubusercontent.com/130851140/235485145-1b75dd84-55c3-470f-ad31-ef1abb076a74.png)

Now we will need to enable some PHP extensions within the IIS manager under the PHP manager and the extensions we will be enabling with be circled in the picture below

![image](https://user-images.githubusercontent.com/130851140/235486511-a2111c86-ae55-4653-bf58-3f16acdfef5a.png)


![image](https://user-images.githubusercontent.com/130851140/235486342-2dd704f6-65aa-4d48-bb99-d888875e50a9.png)

once you enable the extensions you should then refresh your browser with osTicket installer see the changes

![image](https://user-images.githubusercontent.com/130851140/235486986-1114f32f-0275-4b48-adb3-c0b218e18935.png)

Once that is handle we will go into C:\inetpub\wwwroot\osTicket\include rename file ost-sampleconfig.php to ost-config.php and remove all permissions and make new permissions for everyone->all

![image](https://user-images.githubusercontent.com/130851140/235488845-286538d3-6543-4f15-91b5-478ca5556842.png)

![image](https://user-images.githubusercontent.com/130851140/235489185-33098c23-9378-4eb7-93d6-f3ab3c5c7575.png)

Continue in the browser you have osTicket Installer in and hit continue and put in you helpdesk name and email (To recieve customer request)

![image](https://user-images.githubusercontent.com/130851140/235514477-5e031057-4861-4aeb-96fe-a317f9524161.png)

Now we will download the last file and that is heidiSQL and create a new session username and password

![image](https://user-images.githubusercontent.com/130851140/235515097-edbfe0f0-7971-412f-a808-5478c0d6b180.png)

![image](https://user-images.githubusercontent.com/130851140/235524482-376238f2-97e0-464d-9baf-4413692157a5.png)

Create a new database and name it osTicket then complete the rest of the setup in osTicket Installer

![image](https://user-images.githubusercontent.com/130851140/235524836-1506b877-badd-4943-8ded-0170052d7a89.png)

![image](https://user-images.githubusercontent.com/130851140/235525599-0fb82959-fc78-4d78-8b72-8a6e846b270a.png)

once you've completed filing out all the information you are ready to start osTicket 

![image](https://user-images.githubusercontent.com/130851140/235525813-e0a26169-4a4d-4231-a351-225120496797.png)


























