Title :- Firewall -Linux

----

# **1. Title**

**Linux Firewall Practice – UFW 

---

# **2. Objective**

- Learn and practice Linux firewall configuration.
    
- Understand how to allow, block, and monitor network traffic.
    
- Test inbound/outbound connection filtering.
    
- Analyze logs to verify firewall actions.
    


---

# **3. Environment & Setup**

- **Host System:** Windows 10
    
- **Practice VM:** Kali Linux 
    
- **Network Mode:** NAT 
    
    
- **Firewall Tools Used:**
    
    - `ufw` 

---

# **4. Date & Time**

- **Start:** 10-12-2025  13:31 IST
    
- **End:** 


# **5.Command Executed**

 - **Enable the Firewall**: sudo ufw enable
 - **Allow Specific Ports:** sudo ufw allow [port]/tcp
	 - example: sudo  ufw allow 20/tcp
 - **Block Specific Ports**: sudo ufw deny [port]
	 - example: sudo ufw deny 23
- **Allow Specific IP:** sudo ufw allow from [IP]
- **Deny Specific IP:** sudo ufw deny from[IP]
- **Check Rules Of firewall**: sudo ufw status numbered
- **Delete Firewall Rules:** sudo ufw delete[number]
	- example: sudo ufw delete 3

# **6. Results 

- Port 22 allowed successfully
    
- Port 23 blocked
    
- IP 192.168.56.102 denied
    
- Web traffic on port 80 allowed properly
    
- Firewall logs show dropped packets


# **7.Output**:


![[Firewall -1.png]]![[Firewall-2.png]]![[Firewall-3.png]]