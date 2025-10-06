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
<img width="1386" height="792" alt="1" src="https://github.com/user-attachments/assets/a0a08466-8934-4add-9af9-634dfa8877b7" />

**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method  
```
<img width="1388" height="792" alt="2" src="https://github.com/user-attachments/assets/7d990c8c-4207-48bb-8812-8d2ecce366cb" />
<img width="1386" height="795" alt="3" src="https://github.com/user-attachments/assets/c7961fca-76a5-4bba-ad26-6059077abadc" />


**3. Enter your IP address as the attacker server.**
**4. Choose:**
```bash
2) Site Cloner
```
<img width="1390" height="791" alt="4" src="https://github.com/user-attachments/assets/fa670c28-8885-4e29-b3ce-0b9b63ff12c1" />

**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="1385" height="797" alt="5" src="https://github.com/user-attachments/assets/16e938a1-df46-4998-88c7-bec404b95648" />


**6. Send the generated link to the victim.**
<img width="1392" height="792" alt="6" src="https://github.com/user-attachments/assets/a4c81fe9-40f7-472b-a559-a47675579123" />


**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```
<img width="1376" height="382" alt="7" src="https://github.com/user-attachments/assets/848c0588-eab7-4d32-b927-baf6c5f1abfd" />



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
