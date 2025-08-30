# 🖥️ Lecture 2: Setting Up Kali Linux & VirtualBox Networking

## ❓ Overview

In this lecture, we learned how to set up **Kali Linux on VirtualBox** and explored different **network adapter modes** that control how our virtual machine connects to the internet and the host machine.
We also discussed **IP ranges**, the working of the **NAT adapter**, and explored **Kali Linux tools** safely inside a VM.

---

## 🔧 Key Concepts

### **Types of Network Adapters in VirtualBox**

* 🌐 **NAT Adapter (Network Address Translation)** → Creates a private subnet for VMs, while still allowing internet access.
* 🔗 **Bridged Adapter** → VM acts like a separate device on the same network as the host.
* 🏠 **Internal Network** → VMs can talk to each other only (no internet, no host).
* 💻 **Host-Only Adapter** → VM can talk only with the host machine (no internet).
* ⚙️ **Generic Driver / NAT Network** → Advanced custom configurations.

---

## 📡 NAT Adapter Explained

**Scenario Example**

* Router (Access Point): `192.168.56.1.1`
* PC: `192.168.56.1.11`
* Phone: `192.168.56.1.12`
* CCTV: `192.168.56.1.101`

➡️ When VM uses a **NAT adapter**:

* NAT creates a new subnet (e.g., `192.168.56.2.x`)
* VM gets IP `192.168.56.2.11`
* Same internet is shared, but **VM is isolated inside its own subnet**.

📝 **Key Point:** NAT allows internet access to the VM but hides it behind the host machine.

---

## 🗂️ Task Assigned by Mentor

📄 **One-Page Summary Document**

* Create a **pictorial diagram** showing:

  * Normal home network (router → devices).
  * Network with **NAT adapter** (router → PC → VM with new subnet).
* Use **Google Drawings** or similar (not AI/YouTube).
* Goal → Learn how to search and create diagrams independently.

---

## 🐧 Exploring Kali Linux in VirtualBox

Once Kali Linux is installed:

* Open the **terminal** and try commands:

  * `ifconfig` or `ip a` → Check VM’s IP address.
  * Compare with Windows host (`ipconfig`).
* Notice subnet difference (proof of NAT).
* Explore pre-installed tools (don’t use yet):

  * 🛰️ `nmap`
  * 🕵️ `wireshark`
  * 🎯 `metasploit`
  * 🌐 `burpsuite`

💡 VM can always be reset/re-imported into VirtualBox if something breaks — host system stays safe.

---

## 🧠 Mentor Tip

📖 "Create visuals for complex concepts. A diagram explains in seconds what words may take paragraphs to describe."

---

✅ **End of Notes for Lecture 2**

---
