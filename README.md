# 📁 Shared Folder Between Host and Windows VM

### 🧠 Description  
This project demonstrates how to share a folder between a Windows 10 Virtual Machine (guest) and the host PC. It simulates a real-world file sharing setup — useful in help desk, sysadmin, and SOC environments when transferring logs, scripts, or other files between machines on the same network.

---

### 🛠 Tools Used  
- VirtualBox  
- Windows 10 VM  
- File Sharing (SMB)  
- Command Prompt (ipconfig)

---

### 📂 Steps Taken

1. **Created a test folder** on the Windows 10 VM desktop  
   - Named it `sharedtest` and gave full permissions to `Everyone` (read/write)

2. **Enabled sharing:**
   - Right-clicked the folder → Properties → Sharing → Advanced Sharing → Checked "Share this folder"

3. **Found VM IP address:**
   - Ran `ipconfig` inside VM
   - Got IP address

4. **Accessed folder from host PC:**  
   - Pressed `Windows + R`  
   - Typed: `\\192.***.*.*\sharedtest`  
   - Successfully connected and viewed the VM’s shared folder from the main computer

---

### 🔐 Key Notes  

- This only works when both the VM and host PC are on the same **local network**
- Used **Bridged Adapter** in VirtualBox so the VM could pull a unique IP from the router  
- Ensured proper folder sharing permissions (`Everyone`, full control)  
- This simulates how IT pros access user machines on the same domain or network

---

### ✅ Outcome  
Successfully created and accessed a shared folder between the host and guest machine using SMB and IP-based access. A fundamental skill in troubleshooting, log collection, and remote support environments.

---

### 💼 Real-World Use Cases  
- Pull logs from a user’s machine  
- Share installation scripts or software remotely  
- Transfer evidence in a cybersecurity lab  
