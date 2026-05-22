# Windows DC++ Setup Guide

## 1. Download and Firewall Configuration
1. Download the DC++ client installer from the official source [link](https://dcplusplus.sourceforge.io/download.html).          
2. Launch the application for the first time. If prompted by a Windows Security Alert regarding Windows Defender Firewall, check both **Private networks** and **Public networks**, then click **Allow access**.        

*Crucial Firewall Fix*
    If you cannot connect or search after completing the setup, an external antivirus firewall (such as McAfee) or Windows Firewall is likely blocking the client. Disable any third-party antivirus firewalls and manually verify that DC++ is added to both the inbound and outbound program exception rules within Windows Defender Firewall.            

---

## 2. Mandatory Client Settings
The client should automatically open the settings menu upon the first launch. Configure the following parameters precisely across these specific categories:    

### Personal Information
* **Nick:** Set your unique username.    
* **Line speed (upload):** Change this value to `1000` MB/s.    
* **Away mode settings:** Uncheck "Enable away mode when the Windows session is locked". Set the field for "Enable away mode after..." to `0` minutes of inactivity to disable it.     

### Connectivity
* Uncheck the first available checkbox under this section, which states "Let DC++ determine the best connectivity settings". This completely disables automatic connectivity setup.     

### Sharing
* Select the local folder on your storage drive that you want to share with the hub.      
* **Warning:** Do not share personal or system Windows files under any circumstances.            
* **File Indexing & Refreshing:** Added files will only reflect on the hub after the client finishes hashing them. You can track this background process via `View -> Indexing progress`. If you modify the contents of your shared folder and they do not show up, manually force an update via `File -> Refresh file list`.       

### Downloads     
* Set your default download directory path to match the exact same directory chosen in your Sharing settings. This ensures any completed file downloads are immediately reshared to the community.     

### Advanced     
* Uncheck the setting: "Register with Windows to handle magnet...".      
* Check the setting: "Start DC++ when Windows starts".     
* Check the setting: "Add finished files to share instantly (if shared)".     

---

## 3. Connecting to Campus Hubs    
Once settings are applied and file indexing completes, connect to the active campus infrastructure using these steps:       

1. Click on `File -> Quick connect` from the top menu or use the keyboard shortcut `Ctrl + Q`.       
2. Enter the target hub's IP address and connect.      

### [Active Hub Addresses](https://swd.bits-hyderabad.ac.in/dcpphub_status/)      

### Community Links
* Join the local hub community WhatsApp group for support and file requests: [Whatsapp](https://chat.whatsapp.com/G1WxkIIK9R5HYKVYDL9IV2).    

---

## 4. Hardware and Speed Optimization
To achieve gigabit local network transfer speeds and bypass basic connection limitations, verify your physical layer connection:     

* **Ethernet Cable Spec:** Ensure you are using a minimum specification of a **Cat5e** ethernet cable. The specification rating is printed directly on the outer sleeve of the cable.      
* **Type-C Adapters:** If your laptop lacks an RJ45 port and requires a Type-C ethernet adapter, confirm that your hardware explicitly supports `1000/1000 Mbps` gigabit transfer rates. Cheap hardware adapters are frequently capped at `100/100 Mbps` hardware limits.      
* **Verifying Link Speed:** In Windows, open `Settings -> Network and Internet -> Properties (of your Ethernet adapter)`. Confirm that the entry for **Link speed (Receive/Transmit)** reads exactly `1000/1000 (Mbps)`.      

---

## 5. Usage and Troubleshooting (FAQ)

### How do I locate files?
Click the magnifying glass icon located in the main system toolbar or press `Ctrl + S` on your keyboard to open the search utility. Download the files you need, and ensure they remain in your shared folder to distribute them to other peers.     

### Q. I see a red bar on my client icon. What is wrong?
This indicates a connection failure. Re-verify that all properties match the exact criteria specified in Section 2. If the problem persists, review the Windows Firewall exceptions detailed in Section 1 to ensure inbound/outbound blocks are fully lifted, then attempt to reconnect.       

### Q. Why are my download speeds capped or extremely slow?
Your connection is hitting a bottleneck below gigabit performance. Re-verify your hardware pipeline using the metrics outlined in Section 4 (Checking for suboptimal ethernet cables, sub-par Type-C adapters, or a network interface card negotiated down to 100 Mbps limits).     