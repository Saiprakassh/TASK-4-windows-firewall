# 🔒 Task 4 – Setup and Use a Firewall on Windows

## 📌 Objective
The goal of this task is to configure and test basic firewall rules to block specific network traffic.  
In this example, we blocked **Telnet** traffic on port **23**, which is insecure and should be disabled.

---

## 🛠 Tools Used
- **Windows Defender Firewall with Advanced Security** (GUI)
- Windows 11
- `.wfw` Firewall Policy Export for documentation

---

## 📋 Steps Performed

### 1️⃣ Open Windows Defender Firewall with Advanced Security
- Press `Win + R`, type `wf.msc`, and press Enter.

### 2️⃣ Create a New Inbound Rule
- Click **Inbound Rules** → **New Rule…**

### 3️⃣ Select Rule Type
- Choose **Port** → Controls connections for TCP or UDP ports.

### 4️⃣ Choose Protocol and Port
- Protocol: **TCP**
- Specific local ports: **23** (Telnet)

### 5️⃣ Choose Action
- **Block the connection**

### 6️⃣ Apply Profile
- Applied to **Domain**, **Private**, and **Public** profiles.

### 7️⃣ Name the Rule
- Rule Name: `block Telnet port 23`

### 8️⃣ Export Firewall Policy
- From the **Action** menu, select **Export Policy** and save as `firewall-config.wfw`.
- Policy export confirmation appeared.

---

## 📸 Screenshots
1. Rule type selection (Port)  
2. TCP protocol & port 23 configuration  
3. Block connection action  
4. Profile selection (Domain, Private, Public)  
5. Naming the rule  
6. Exporting the firewall policy  
7. Export success confirmation

---

## 📂 Repository Contents
- **README.md** – task documentation
- **firewall-config.wfw** – exported firewall configuration
- **Screenshots** – images showing the steps

---

## 📖 Understanding the Task

- **Why block port 23?**  
  Telnet sends all data, including passwords, in plain text. This makes it vulnerable to interception. Secure alternatives like SSH (port 22) should be used.

- **Inbound vs. Outbound rules:**  
  - **Inbound**: Controls traffic coming **into** your system.  
  - **Outbound**: Controls traffic going **out** from your system.

- **Firewall role:**  
  A firewall filters traffic based on defined rules, helping to prevent unauthorized access.

---

## ✅ Outcome
Successfully created a firewall rule blocking inbound TCP connections on port 23 (Telnet) for all profiles and exported the configuration.
