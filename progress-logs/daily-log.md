# 🛡️ Learning & Progress Log
*A chronological record of my journey into ethical hacking.*

---

### 📅 February 2024
#### Entry 1: First Network Scan & Analysis
- **Focus:** Gaining experience and identifying device weaknesses.
- **Environment:** Kali Linux VM running on **QEMU/KVM** (Host: Garuda Linux Dr460nized).
- **Action:** Executed a full TCP SYN scan on my phone's local IPv4 address.
- **Command Used:** 
  `sudo nmap -p- -sS -T4 -Pn 192.168.1.174`

**Scan Screenshot:**
![Nmap Scan Results](./your-screenshot-filename.png)

**My Analysis:**
> I ran a full TCP SYN scan on my phone’s IPv4 on my home Wi‑Fi. Most ports were closed or filtered, showing active blocking. Two TCP ports were open: **1716/tcp (xmsg/KDE Connect)**, and **46888/tcp**, which Nmap identified as an unknown service likely opened by an app. This helped me understand how devices filter traffic and limit exposed services on a local network.

---

### 📅 Next Steps
- [ ] Continue **TryHackMe: Jr. Penetration Tester Path**
