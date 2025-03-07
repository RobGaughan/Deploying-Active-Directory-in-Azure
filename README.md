# Deploying-Active-Directory-in-Azure

### 3. Install Active Directory 
First we must RDP into Domain-Controller-1 to do that we need to find its public IP address

We can find the IP address by navigating to: 
 - Virtual Machines --> Domain-Controller-1 --> Networking --> Network settings
   
![image](https://github.com/user-attachments/assets/36c65ae5-cd40-42f9-ae4a-7f5e4c3c7b91)

- Next we will RDP in using Remote Desktop Connection using the public IP 
   - The login credential will be Username: LabADMIN Password: LabPassword123 from earlier

![image](https://github.com/user-attachments/assets/e2ed221a-4c8e-44bc-b203-4bfc1720ae35)

- When you connect you should be met with this screen
   -To begin installing Active Directory click on "add roles and files"
  
![418238521-7925871f-0282-4e5b-a517-ed33bbcd5fc4](https://github.com/user-attachments/assets/00bd1956-3a31-4375-ae36-3b3b285224c9)

- Next we will be met with the activation wizard we can click next on all prompt until we get to the "Server roles" secction

![image](https://github.com/user-attachments/assets/1dbe9ded-acb3-4b01-824a-4d1160ee089f)


 - On the "Server roles" section:
    -  check the highlighted "Active Directory Domain Services" box
    -  accept any addtional prompts and hit next until you get to "Confirmation"

![image](https://github.com/user-attachments/assets/e87b07f4-50f5-466b-9f5f-048fe84dc7e8)

 - Check the "Restart the destination server automatically if required" and click install
   
![image](https://github.com/user-attachments/assets/d28d5c80-7f28-455a-afe5-39b30ec4b33a)

- Now we must promote this VM to domain controller to do that
   - Select the flag icon on the top right of the screen and click on "Promote this server to a domain controller"

![image](https://github.com/user-attachments/assets/b0fe3318-9eee-4a6e-843f-86179d20f2f5)

- Enter "exampledomain.com" into the root domain name

![image](https://github.com/user-attachments/assets/9659ddb9-675e-4da1-98bf-c6e1529ff0bd)


- Next choose a password for the Dirrectory Services Restore Mode
   - I used: LabPassword123 to keep lab passwords consistent

![image](https://github.com/user-attachments/assets/e2aba41f-d5a8-4205-92d8-6dc92a67031e)

- uncheck "Create DNS delegation" when met with this prompt

![image](https://github.com/user-attachments/assets/5475c2e7-8c06-4af0-a8de-ee18385c9231)

- Click next until you get to Prerequisites Check and click install
   - After installtion the VM will restart and you will loose the RDP connection momentarily
      
![image](https://github.com/user-attachments/assets/c9b03c31-f37f-48c9-8f51-f09bb620aff4)


Navigate to "Active Directory Users and Computers"
![image](https://github.com/user-attachments/assets/9160b08c-b74d-4eae-b0f9-de710c241e13)

Create a new Organizational Unit (OU) 
![image](https://github.com/user-attachments/assets/71306999-945f-490e-bde8-6553a049b98a)


