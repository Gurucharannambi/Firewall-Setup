#Setup and Use a Firewall

## 📌 Objective

The objective of this task is to configure and test basic firewall rules on a system to allow or block network traffic and to understand how firewalls filter traffic to enhance system security.

---

## 🛠 Tools and Technologies Used

* **Operating System:** Windows 10 / Windows 11
* **Firewall:** Windows Defender Firewall
* **Testing Tools:** Telnet Client / PowerShell

---

## ⚙️ System Configuration

* Firewall configured using **Advanced Security Settings**
* Inbound traffic rules tested on specific TCP ports

---

## 🚀 Procedure

### 1️⃣ Open Firewall Configuration

* Open **Control Panel**
* Navigate to **Windows Defender Firewall**
* Click **Advanced settings**
* Select **Inbound Rules**

---

### 2️⃣ Create a Rule to Block Telnet (Port 23)

* Click **New Rule**
* Rule Type: **Port**
* Protocol: **TCP**
* Specific Local Port: **23**
* Action: **Block the connection**
* Apply to **Domain, Private, and Public**
* Rule Name: `Block Telnet Port 23`

---

### 3️⃣ Test the Firewall Rule

Run the following command in **Command Prompt**:

```cmd
telnet localhost 23
```

**Output:**

```
Connecting To localhost...
Could not open connection to the host, on port 23: Connect failed
```

✅ This confirms that the firewall successfully blocked inbound traffic on port 23.

---

### 4️⃣ Allow Secure Traffic (Port 22 – SSH)

* Created a new inbound rule
* Allowed **TCP port 22**
* Ensures secure remote access is permitted

---

### 5️⃣ Remove Test Rule (Optional)

* Navigated to **Inbound Rules**
* Deleted the Telnet block rule to restore system state

---

## 🧪 Commands Used

```cmd
telnet localhost 23
```

```powershell
Test-NetConnection localhost -Port 23
```

---

## 🔍 Observations

* Firewall rules effectively control network traffic.
* Blocked ports deny unauthorized access.
* Allowed ports permit secure and required services.

---

## 🔐 Summary: How Firewall Filters Traffic

A firewall filters traffic by inspecting incoming and outgoing data packets and comparing them against predefined security rules based on port numbers, protocols, IP addresses, and traffic direction. Traffic that matches an allow rule is permitted, while traffic matching a block rule is denied, thereby protecting the system from unauthorized network access.

---

## ✅ Conclusion

This task successfully demonstrated the configuration and testing of firewall rules. Blocking and allowing specific ports verified how firewalls protect systems by filtering network traffic based on defined security policies.

