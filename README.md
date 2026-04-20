<h1>Azure-SOC-SIEM and Honeypot</h1>

<h2>Description</h2>
I set up a basic home SOC in Azure from scratch. Using a free Azure subscription, I will walk through creating a virtual machine (VM), opening it to the internet as a honeypot, and forwarding logs to a central repository. We then integrate Microsoft Sentinel to analyze real-world attack data.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Azure Virtual Machine</b> 
- <b>Log Repository using Log Analytics Workspace</b>
- <b>KQL</b>
- <b>Azure Sentinel</b>

First we create a resource group<img width="901" height="484" alt="image" src="https://github.com/user-attachments/assets/7e67ebaf-09e9-4ff8-a542-36008c0d0b6c" />

Next we create a virtual network that our virtual machine will connect to<img width="914" height="722" alt="image" src="https://github.com/user-attachments/assets/9df0f268-7ea9-4d94-aa8d-d318ebc50c1f" />

<img width="653" height="846" alt="image" src="https://github.com/user-attachments/assets/c7eb6c20-1ea8-43d0-ad42-98c9089f5399" />

Go to resource groups to validate Vnet was created
<img width="1200" height="383" alt="image" src="https://github.com/user-attachments/assets/d4167208-e6ec-447f-84aa-f96496e4a125" />
Create Virtual Machine for the honeypot
<img width="949" height="726" alt="image" src="https://github.com/user-attachments/assets/1c341923-0eec-4de3-97cc-20315d161d5f" />


Edit rules for Virtual machine to be exsposed to public internet for honepot<img width="512" height="388" alt="image" src="https://github.com/user-attachments/assets/bb385448-6965-4bda-95a5-8918e7145a18" />

<img width="770" height="512" alt="image" src="https://github.com/user-attachments/assets/791fe919-e217-4dfc-83b3-db1adc80d3a1" />

Launched Virtual Machine and changed Firewall settings
<img width="981" height="622" alt="image" src="https://github.com/user-attachments/assets/ae761c04-4097-42fe-9b6d-ae2a4e72fd4e" />

Relaunched VM with failed log ion attempts in Event Viewer
<img width="1200" height="619" alt="image" src="https://github.com/user-attachments/assets/3d15431a-fcbe-4dae-8c89-a08ba9114301" />

<img width="819" height="708" alt="image" src="https://github.com/user-attachments/assets/1e26da73-5fd6-436a-b3f2-7c84759c791c" />

Created and Queried the results
<img width="751" height="685" alt="image" src="https://github.com/user-attachments/assets/6932fc98-b2f0-41d5-a29a-b7e10f654406" />

<img width="1243" height="815" alt="image" src="https://github.com/user-attachments/assets/47d2d662-c298-45e1-a2f7-323fcc53d9b0" />

Then edited the Attack Map
<img width="1277" height="794" alt="image" src="https://github.com/user-attachments/assets/057ed738-26f7-4068-9f76-973af3d8fde8" />

<img width="1072" height="688" alt="image" src="https://github.com/user-attachments/assets/18f91531-ca5d-4f3b-8e32-e3e9b86e6823" />
