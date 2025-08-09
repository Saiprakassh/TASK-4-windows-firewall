# TASK-4-windows-firewall
# 🔒 Firewall Configuration – Block Telnet Port 23 (Windows Defender Firewall)

## 📌 Objective
Configure **Windows Defender Firewall** to block inbound traffic on **TCP port 23** (Telnet) for all network profiles, export the configuration policy, and verify successful rule creation.

---

## 🛠 Tools Used
- **Windows 11**  
- **Windows Defender Firewall with Advanced Security**

---

## 📖 Steps Performed

### 1️⃣ Open Windows Defender Firewall with Advanced Security
- Press `Windows + S` → Search for **Windows Defender Firewall with Advanced Security** → Open it.

---

### 2️⃣ Create a New Inbound Rule
1. In the **Actions** panel → Click **New Rule…**
2. Select **Port** → Click **Next**.

---

### 3️⃣ Configure Protocol and Port
1. Select **TCP**.
2. Choose **Specific local ports** → Enter **23** → Click **Next**.

---

### 4️⃣ Define the Action
- Select **Block the connection** → Click **Next**.

---

### 5️⃣ Choose Profiles
- Select **Domain**, **Private**, and **Public** → Click **Next**.

---

### 6️⃣ Name the Rule
- Name: `block Telnet port 23`
- Click **Finish**.

---

### 7️⃣ Export Firewall Policy
1. Go to **Action** → **Export Policy…**
2. Save the `.wfw` file (this stores your firewall configuration).
3. Confirmation: **Policy successfully exported**.

---

## 📂 Deliverables
- **Screenshots**: Rule creation steps and export confirmation.
- **Exported Policy File**: `firewall-config.wfw`

---

## 🎯 Outcome
- Inbound TCP traffic on **port 23 (Telnet)** is blocked across all network profiles.
- The firewall policy was successfully exported for backup/sharing.

---

## 🔍 Key Concepts Learned
- Creating and managing inbound firewall rules.
- Blocking unsafe legacy protocols like Telnet.
- Exporting firewall configurations for backup or deployment.

---

## 💡 Why Block Port 23?
Telnet uses plaintext transmission without encryption, making it vulnerable to **password sniffing** and **MITM attacks**. Blocking this port prevents insecure remote login attempts.

---

## 📷 Reference Screenshots
1. **Select Rule Type** → Port  
2. **Protocol & Ports** → TCP, Port 23  
3. **Action** → Block the connection  
4. **Profiles** → Domain, Private, Public  
5. **Rule Name** → block Telnet port 23  
6. **Policy Export** confirmation
