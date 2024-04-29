# Windows Server Setup - With Active Directory
Setting up a new Hyper-V instance of Windows Server, With Active Directory. A Windows 10 Client and Clients for the Active Directory.

1. I am using Hyper-V features on a Windows 10 Laptop in order to perform the steps in this Lab.

2. If you have not enabled Hyper-V features previously, please enable them in Windows Settings -- "Turn Windows Features On or Off".

3. Once Hyper-v is enabled, please download ISO files for Windows Server 2022 & Windows 10 from Microsoft Evaluation Center.

4. Install both ISOs as seperate VMS using Hyper-V. Specific guidelines for VM configuration depends upon your specific system. For my setup, I used 2048mb of Memory and 4 Virtual Processors. My Hard Drive size starts at 40GB but its dynamic (expandable). 

5. Lets Begin With Windows Server Installation. Attach the Windows Server ISO to the VM via the Media --> DVD Drive attachment feature on Hyper-V.

6. Install Windows Server. ![Screenshot 2024-04-29 160207](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/cda62217-d34a-47d5-ba69-8549514b3b81)


7. Create Administrator Password as prompted.

8. Once Administrator password is created, the login screen with appear. Please Login as Administrator.

9. Once logged in for first time, you should see the Server Manager GUI. Please create a checkpoint. ![Screenshot 2024-04-29 171117](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/397a5309-f13a-4b03-90f1-38c6448e5cc2) 
![Screenshot 2024-04-29 162631](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/ba9f1fda-5d16-4733-ae4e-2c5a4037c752)


10. 

