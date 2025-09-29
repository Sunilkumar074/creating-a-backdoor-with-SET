# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="938" height="834" alt="image" src="https://github.com/user-attachments/assets/21253856-ebbb-4078-a6f5-61b36e41a91b" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="957" height="720" alt="image" src="https://github.com/user-attachments/assets/0c5282b2-792f-40d1-a536-7cd52de019a6" />
<img width="851" height="777" alt="image" src="https://github.com/user-attachments/assets/4b092420-6016-42ef-b668-abcc2840664d" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="663" height="343" alt="image" src="https://github.com/user-attachments/assets/ef91abbb-e02d-440c-811f-ba16f407f2b9" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="843" height="199" alt="image" src="https://github.com/user-attachments/assets/989326f4-6f84-468d-9271-1184f9fcfa9f" />


**6. Send the generated link to the victim.**
<img width="1278" height="842" alt="image" src="https://github.com/user-attachments/assets/76ea6d3b-7772-44bf-8c4c-6df3d90ea7c1" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="945" height="427" alt="image" src="https://github.com/user-attachments/assets/2c257fb3-bbd2-45c3-839a-09462d18c477" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
