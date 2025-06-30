# 🔥 Cybersecurity Internship – Task 4

## 📌 Task Title:
**Firewall Configuration and Traffic Filtering using UFW (Linux)**

---

## 🧠 Objective:
The aim of this task was to understand how firewalls manage inbound and outbound network traffic. I used the **Uncomplicated Firewall (UFW)** on a Linux machine to practice adding, removing, and verifying rules. This exercise demonstrated the importance of firewall rule order and traffic control.

---

## 🛠️ Tools Used:
- **Operating System:** Ubuntu Linux (or Kali)
- **Firewall Tool:** UFW (Uncomplicated Firewall)
- **Commands Executed via Terminal**

---

## 🧪 Experiment Steps:

### 🧩 Step 1: Check Firewall Status
```bash
sudo ufw status
```
### 🧩 Step 2: Enable UFW

To enable the Uncomplicated Firewall (UFW) on a Linux system, use the following command:

```bash
sudo ufw enable
```
### 🧩 Step 3: List Current Rules
```bash
sudo ufw status numbered
```
### 🧩 Step 4: Block Inbound Telnet (Port 23)
```bash
sudo ufw deny 23
```
📌 This blocks incoming traffic on port 23 to prevent insecure Telnet usage.
### 🧩 Step 5: Allow SSH Access (Port 22)
```bash
sudo ufw allow 22
```
📌 Ensures remote administration access remains open.
### 🧩 Step 6: Verify Updated Rules
```bash
sudo ufw status
```

**Expected Output:**

    To                         Action      From
    --                         ------      ----
    22                         ALLOW       Anywhere
    23                         DENY        Anywhere

### 🧩 Step 7: Remove Test Rule
```bash
sudo ufw delete deny 23
```
---

### 📸 Screenshot Included:

- `firewall.png` – Firewall configuration steps
----

### 🔐 Security Takeaways:

- Port 23 (Telnet) is often blocked because it’s insecure (unencrypted text communication).
- Allowing only necessary ports (like 22 for SSH) reduces the attack surface.
- UFW makes firewall management beginner-friendly, using simple command syntax.

### 🧠 Concepts Learned:

- What is a firewall and how it filters traffic
- UFW command structure for adding/removing rules
- The difference between inbound and outbound rules
- Importance of blocking unused and insecure ports
- How rule order can affect traffic flow
---
### 🙋‍♂️ Author:

Name: Prangshu Das

Role: Cybersecurity Intern @The ELevate Labs

Task Date: 23rd June 2025
