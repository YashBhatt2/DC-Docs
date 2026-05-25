# macOS NCDC Setup Guide

This guide is designed for macOS users to connect to the campus DC++ infrastructure using **NCDC**, a lightweight, terminal-based DC++ client.

---

## 1. Installation

### Step 1: Install Homebrew
Homebrew is a package management system required to simplify software installation on macOS. Open your Terminal application and execute the following command:   

```bash
/bin/bash -c "$(curl -fsSL [https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh](https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh))"
```
For more detailed information on [Homebrew](https://brew.sh/).    

### Step 2: Install NCDC
Once Homebrew installation finishes successfully, run the following command in your terminal to install NCDC:    

```bash
brew install ncdc
```

### Step 3: Configure the Option Key (Crucial Layout Step)
Because NCDC relies heavily on terminal shortcuts, you must configure your Option key to act as a modifier key:      
1. Open the macOS Terminal app.     
2. Navigate to Settings -> Profiles -> Keyboard.      
3. Locate the checkbox labeled "Use Option as meta key" and check it to enable the behavior.     

## 2. Initial Application Setup
Launch the application by opening your terminal and typing:     
```bash 
ncdc
```
Upon successful installation, the main NCDC terminal interface will initialize.       

### Locating Your Downloads
Your default configuration and working files are saved in a hidden folder located at /Users/your-name/.ncdc. All completed downloads will be stored  inside the dl subdirectory here: /Users/your-name/.ncdc/dl.    
To view this hidden folder in Finder:      
1. Open your Finder application and go to your home directory (/Users/your-name).      
2. Press Command + Shift + Dot (.) on your keyboard to reveal hidden files.        

### Configuration Commands
The first time you run NCDC, execute these baseline commands inside the application interface to set up your environment:   
- ```text  /set nick yourNickname``` - Sets your community username.    
- ```text /set active true``` - Configures your network status to active mode.   
- ```text /set desc hello world``` - Sets your public user description.    

## 3. Directory Sharing and Connection. 

### Step 1: Link Your Share Folder
Gather your files into a dedicated folder, then map it to NCDC by running:     
```bash
/share "folder-name" /Users/your-name/your-folder-address
```

### Step 2: Set Your Download Location
To automatically reshare your completed downloads to the community, point your download path to the exact same folder location:     
```bash
/set download_dir /Users/your-name/your-folder-address
```

### Step 3: Connect to the Hub
With your sharing targets mapped, execute the following command to connect directly to the active campus infrastructure:    
```bash
/open Sandhub sandhub.aten2005.dev
```     

## 4. Interface Navigation and Usage
### Tab Management
When a connection opens, the main hub feed will instantiate in a new terminal tab (e.g., tab #2).    
- **Switching Tabs:** Press Option + [Tab Number] (e.g., Option + 2).   
- **Closing Tabs:** Navigate to the active tab and press Option + C.     

### User Directory and Downloading    
1. Type /userlist inside the hub tab to view all connected peers.       
2. Navigate the roster using your Arrow Keys.       
3. Press Shift + B (capital B) on a highlighted user to browse their shared folder layout.    
4. Use the arrow keys to browse their files, and press the d key to add any target item to your download queue.    

### Monitoring Downloads
- Open your download queue window by typing /queue or pressing Option + Q.    
- To cancel an active download, highlight the file within the queue window and press the d key.     
- Review a complete file transfer demonstration via this instructional reference [link](https://drive.google.com/file/d/1eCJK9Lf3dDfo19oFDNjZ6JhtRu936oyt/view?usp=sharing.)           

### Searching Files
To query files across the entire hub network, run:
```bash
/search name_of_the_thing_u_wanna_search
```
This initializes your results layout inside a dedicated tab. Navigate and queue items here using the standard navigation controls.      

## 5. Maintenance and Community Support     
### Key Commands
- /refresh — Forces a re-indexing update of your shared directory folder layout to mirror new files to other peers.      
- /pm username — Opens a private chat session window with a selected peer.      
- /disconnect — Gracefully disconnects your connection from the current hub infrastructure.     

## Support Links
Join the [whatsapp](https://chat.whatsapp.com/G1WxkIIK9R5HYKVyDL9lV2)        
[Check For Active Hubs](https://swd.bits-hyderabad.ac.in/dcpphub_status/)         
