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

21. Once Active Directory Domain Services Feature is successfully installed, you will see a caution flag near the top of the screen inside of the Server Manager GUI. You will use this flag to set your server - PC as the domain controller. 
![Screenshot 2024-04-29 173524](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/67a00fc6-12ce-44e5-ada2-cba10ec17137)

22. Under Select Deployment Operation, Select Add A New Forest. Create a domain name for your server. Domain name should end in .local for this project. ![Screenshot 2024-04-29 173648](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/578c0ca8-3c35-400d-b551-0e4f4a4b0837)

23. Under Domain Controller Options, Select the Forest and Domain functional level. This determines the lowest version of Windows Server that can be used with your AD Forest. Next, set your DSRM password. 
![Screenshot 2024-04-29 173727](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/10bf77ae-483a-4809-9410-d366b31d7aea)

24. Click next until you reach the Installation confirmation windows.
  
25. Confirm installation and install. Server - PC will reboot once install is successful. ![Screenshot 2024-04-29 174040](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/91d6ab6d-1874-4459-bee4-bea8c7c6149f)

26. Once Server - PC restarts, you will notice is is now connected to your domain, you will see the name below the credential entry space. ![Screenshot 2024-04-29 174735](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/85efb6c6-97a7-4b7b-ade7-04859819cf12)

27. Once logged in as Administrator, Go to the Server Manager GUI. Under tools, select Active Directory Users and Computers. ![Screenshot 2024-04-29 175214](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/b21b39a8-6be6-47cd-853c-95fe72fb168e)

28. Once inside of the Active Directory Users and Computers tool, click the link down arrow, and using the User option arrow, select New, and then User.  ![Screenshot 2024-04-29 175313](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/d3682a65-3a05-485d-afa1-5562d32dd376)

29. Add User information, create a username and click next. Create a temporary password. Choose the option "Change password at next login", so that the user may set their own password. Click next to confirm user information and click "Finish". ![Screenshot 2024-04-29 175341](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/e0fa4f1d-41c0-490c-8a30-0e17167bfa71) 
![Screenshot 2024-04-29 175420](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/8ee490ed-1a4a-49bd-8074-de288e6204a5)
![Screenshot 2024-04-29 175436](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/a3809617-862a-4c26-9b96-afbc6bdd53c3)


30. Verify User by clicking user in Active Directory Users and Computers tool. ![Screenshot 2024-04-29 175453](https://github.com/kendal-in-tech/Server-Setup---Active-Directory-/assets/168005414/2b00dc0f-6496-4328-b88c-15d9e19f0c06)

31. 




