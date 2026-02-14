# 🔐 Learning Remote Access: Connecting Kali Linux to macOS with SSH

> A hands-on homelab project demonstrating secure remote access using SSH between Kali Linux and macOS.

---

## ⚠️ Disclaimer

This project was conducted **for educational purposes only** inside a private home lab environment using machines I personally own and control.

⚠️ Do **not** attempt to access systems you do not have explicit permission to use.

---

## 📚 Project Overview

This lab demonstrates how to:

- Enable SSH access on macOS
- Identify a machine’s local IP address
- Establish an SSH connection from Kali Linux
- Verify remote session access
- Securely close the connection

This project builds foundational skills in:

- Remote system administration
- Secure networking
- Linux command-line usage
- Cybersecurity fundamentals

---

## 🧠 What Is SSH?

**SSH (Secure Shell)** is a secure network protocol that allows encrypted communication between two systems over a network.

It is commonly used for:

- Remote server administration  
- Cloud infrastructure management  
- Secure file transfers  
- DevOps workflows  
- Cybersecurity operations  

SSH encrypts all traffic, protecting credentials and commands from interception.

---

## 🖥️ Lab Environment

| Role | System |
|------|--------|
| Host Machine | Kali Linux (VMware Workstation Pro) |
| Target Machine | macOS (MacBook Pro) |
| Network | Local Home Wi-Fi |
| Tool Used | OpenSSH (built into both systems) |

---

# 🔎 Step-By-Step Walkthrough

---

## Step 1 — Enable Remote Login on macOS

On the Mac:

1. Open **System Settings / System Preferences**
2. Navigate to **Sharing**
3. Enable **Remote Login**
4. Allow access for your macOS user account

This activates the SSH server on macOS.

---

## Step 2 — Find the Mac’s Local IP Address

Open Terminal on macOS and run:

```bash
ipconfig getifaddr en0
```

This returns the local IP address (example: `192.168.1.15`).

> Note: If using Ethernet instead of Wi-Fi, the interface may differ.

---

## Step 3 — Connect from Kali Linux

On Kali Linux, open the terminal and run:

```bash
ssh username@192.168.1.15
```

Replace:

- `username` → Your macOS account name  
- `192.168.1.15` → The IP address found in Step 2  

If connecting for the first time, you’ll see a fingerprint prompt:

```
Are you sure you want to continue connecting (yes/no)?
```

Type:

```
yes
```

Then enter your macOS password.

> 🔒 Password input will not display characters — this is normal.

---

## Step 4 — Verify Remote Access

Once connected, run:

```bash
whoami
hostname
pwd
```

These confirm:

- The user you are logged in as
- The machine you are connected to
- Your current working directory

You are now executing commands remotely on macOS from Kali Linux.

---

## Step 5 — Close the SSH Session

To securely exit:

```bash
exit
```

For additional security:

- Return to macOS
- Disable **Remote Login** if no longer needed

---

# 🔐 What Happens During SSH?

When initiating the SSH connection:

1. Kali Linux sends a connection request.
2. macOS responds with its public key fingerprint.
3. An encrypted tunnel is established.
4. Authentication is performed.
5. A secure remote shell session begins.

All traffic is encrypted.

---

# 📸 Proof of Concept

The original lab documentation includes redacted screenshots demonstrating:

- Successful SSH login
- Remote command execution
- Secure disconnection

All sensitive information was removed prior to publication.

---

# 🧩 Skills Demonstrated

- Linux CLI proficiency  
- Network configuration basics  
- Understanding encrypted protocols  
- Remote authentication  
- Documentation and lab reporting  

---

# 🚀 Future Expansions

Planned follow-up projects:

- SSH into Windows virtual machines  
- Configure SSH key-based authentication  
- Use SCP / SFTP for secure file transfer  
- Deploy a cloud VM and connect remotely  
- Expand into penetration testing labs  

---

# 📌 Key Takeaways

✔ SSH is a foundational networking skill  
✔ Remote access can be safely practiced in a homelab  
✔ Encryption protects authentication credentials  
✔ Documentation strengthens technical portfolios  

---

# 🏁 Conclusion

This project served as a practical introduction to remote access and secure system administration.

By building and documenting this lab, I strengthened my understanding of:

- Network communication
- Linux terminal workflows
- Secure authentication principles
- Responsible cybersecurity practices

---

## 👤 Author

Daniel Horan  
Aspiring Cybersecurity Professional | Homelab Builder | Continuous Learner  

---


