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

10. Change Name of Server - Computer.

11. Go to settings, under System Information. Click on "Rename This PC". Rename the PC with the consideration that this will be your Domain Controller. A User Friendly / Easily Remembered name is suggested. ![Screenshot 2024-04-29 171618](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/53148a24-c14e-48d5-9a0e-dbcc5f59633c) 
![Screenshot 2024-04-29 171700](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/e91637a0-4775-49f8-872d-e5d7f79148e8)

12. Restart PC. 
![Screenshot 2024-04-29 171721](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/72c75437-1508-4f60-ba5e-06ff04651b62)

13. Verfiy System Name Change. ![Screenshot 2024-04-29 172254](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/946a54ee-43f2-4026-bbc1-ca1ae5a9fc21)

14. Promote The Server To Domain Controller.

15. Select Add Roles and Features in right corner of Server Manager GUI. 
![Screenshot 2024-04-29 172522](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/0430e615-ec36-45d4-afe2-50556b090425)

16. Select Role Based or Feature Based Installation. 
![Screenshot 2024-04-29 172559](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/634ff8ba-8317-445f-9ae7-a2a0481ac30a)

17. Select your server, You should see the name you used to rename your Server - PC. ![Screenshot 2024-04-29 172616](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/25188da3-a046-425b-a12a-5d4b5df95ff7)

18. Select Active Directory Domain Services. This feature requires the installation on a few other features, which will automatically install with the Active Directory Domain Services feature installation. 
![Screenshot 2024-04-29 172644](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/95f3852a-6719-435a-8168-7120fe8b5e2d)

19. Click next until you see feature installation confirmation. ![Screenshot 2024-04-29 172800](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/e3f98361-72f9-4670-af3f-8a2d80894b3e)

20. Install Active Directory Services. ![Screenshot 2024-04-29 172822](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/fda698db-482e-44b5-9a3f-fc46287d7ba3)

21. 




