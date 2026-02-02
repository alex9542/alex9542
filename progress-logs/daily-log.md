# 🛡️ Learning & Progress Log
*A chronological record of my journey into ethical hacking.*

---

### 📅 February 2026
#### Entry 1: Investigating Mobile Device Vulnerabilities
- **Focus:** Gaining experience and identifying device weaknesses.
- **Environment:** Kali Linux VM running on **QEMU/KVM** (Host: Garuda Linux Dr460nized).

**Step 1: Initial Discovery Scan**
- **Action:** Executed a full TCP SYN scan on my phone's local IPv4 address.
- **Command Used:** 
  `sudo nmap -p- -sS -T4 -Pn 192.168.1.174`
- **Scan Screenshot:** ![Nmap Scan Results](./full-nmap-scan-on-phone-ipv4.png)
- **Analysis:** I ran a full TCP SYN scan on my phone’s IPv4 on my home Wi‑Fi. Most ports were closed or filtered, showing active blocking. Two TCP ports were open: **1716/tcp (xmsg/KDE Connect)**, and **46888/tcp**, which Nmap identified as an unknown service. This helped me understand how devices filter traffic and limit exposed services on a local network.

**Step 2: Service Version Investigation**
- **Action:** Ran a targeted version scan (`-sV`) on the unknown port (46888) to get more data.
- **Command Used:** 
  `sudo nmap -p 46888 -sV 192.168.1.174`
- **Scan Screenshot:** ![Nmap Version Results](./nmap-version-scan-46888.png)
- **Analysis:** I ran an `-sV` scan to figure out that unknown port. The results showed "OAFP" and my phone's model, which turns out to be a built-in **Oppo discovery service** for things like Oppo Share. This helped me understand how to find more info on a service when [Nmap](https://nmap.org) doesn't label it automatically.

---

### 📅 Next Steps
- [ ] Continue the **[TryHackMe: Jr. Penetration Tester Path](https://tryhackme.com)**.
- [ ] Research the **OAFP protocol** to see if it has any known public exploits.


