# Linux NCDC Setup Guide

This guide is designed to help users of Linux systems connect to the campus DC++ infrastructure using **NCDC**, a terminal-based DC++ client.             

**IMPORTANT NOTE FOR LINUX USERS:** NCDC relies heavily on keyboard shortcuts. Wherever the macOS guide mentions the "Option" key, you must use the **Alt** key instead.      

## 1. Installation

Since NCDC is available in most official repositories, you can install it directly via your distribution's package manager.        

For Arch-based distributions (like Manjaro):     
```bash
sudo pacman -S ncdc
# or if using an AUR helper: yay -S ncdc
# For Debian/Ubuntu-based distributions:
sudo apt install ncdc
```
if ncdc isn't an already availaible package for your distro, follow this tutorial for installation: [link](https://dev.yorhel.nl/ncdc/install)     
## 2. Initial Application Setup
NCDC is now ready to use. Open your terminal and type:      
```bash
ncdc
```
The main NCDC terminal interface will initialize.          
### Locating Your Downloads
Your working directory is set to /home/your-name/.ncdc. This is a hidden directory containing a folder called dl, which holds all the content you will eventually download from the hub.     

Since this is the first time NCDC is being used, you should run a few commands inside the interface to set up your profile:      
- /set nick yourNickname — Sets your nickname to whatever you want it to be.    
- /set active true — Makes your status active.       
- /set desc hello world — Sets your description.     

## 3. Directory Sharing and Connection 
You need to share at least 1 GB of content to access and download files on the hubs.     
### Step 1: Link Your Share Folder   
Once you’ve gathered your files in a directory, make that folder usable for sharing by entering:     
```bash
/share "folder-name" /home/your-name/your-folder-address
```
### Step 2: Set Your Download Location
Since you want to share whatever you download, it is a good idea to set your download directory to be the same as your shared folder:      
```bash
/set download_dir /home/your-name/your-folder-address
```
### Step 3: Connect to the Hub
With your sharing set up, you can now access the network! Enter the following command to connect to an active hub:       
```bash
/open Sandhub sandhub.aten2005.dev
```

## 4. Interface Navigation and Usage
The main hub screen will open in a new tab (e.g., tab #2).   
### Tab Management
- **Switching Tabs:** Press Alt + [Tab Number].      
- **Closing Tabs:** Press Alt + C.

### Accessing Users and Downloading
1. To see a list of all users, use: /userlist       
2. Use the arrow keys to navigate, and press the 'B' (Shift + B) key to view the folders of a user.    
3. Within a user’s folder structure, you can use the arrow keys to navigate and see all the items they have shared.     
4. To download an item, press the d key. You should get a message which says that the item has been added to the download queue.     

### Monitoring the Queue
To check out the download queue, return to the main hub tab and type /queue in the command line (or you can just press Alt + Q). It should open another window.      
In the queue, you can check on the progress of the download. If you want to cancel the download, press the d key while highlighting the item in the queue.    

### Searching
To search for an item, use the command:     
```bash
/search what you want
```
This will open in a new tab once again, and there you can navigate (similar to how you navigate through a user's files), and download whatever content you want.       

## 5. Maintenance and Community Support
- To update your shared items, so that what’s in the folder is reflected and available to other users, use: /refresh      
- To chat with another user, use: /pm username. It will open in a new window.        
- You can use /disconnect to disconnect from the hub.     
- Join the [Whatsapp](placeholder)   
- Check [Active Hubs](https://swd.bits-hyderabad.ac.in/dcpphub_status/)    
