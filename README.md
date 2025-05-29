### 🛡️ John the Ripper: The Basics

**Room:** [John the Ripper: The Basics — TryHackMe](https://tryhackme.com/room/johntheripperbasics)  
**Status:** ✅ Completed  
**Date:** *29 May 2025*

---

### 🎯 Objective  
Learn how to use John the Ripper (Jumbo version), a fast and flexible hash-cracking tool. The room covers cracking various types of hashes and password-protected files using different modes and tools in the John suite.

---

### 🗝️ Key Concepts  
- **Hash** — A fixed-length value created from input data using a hash algorithm (e.g. MD5, SHA1).
- **One-way Function** — Hashing is designed to be easy to compute but hard to reverse.
- **Dictionary Attack** — Trying common passwords from a list to crack hashed passwords.
- **NTLM (NTHash)** — Hash format used by Windows to store passwords.
- **/etc/shadow** — Linux file storing user password hashes; must be combined with `/etc/passwd` using `unshadow`.
- **Single Crack Mode** — John generates passwords based on usernames and GECOS fields.
- **Custom Rules** — User-defined rules for password mangling in `john.conf`.
- **zip2john / rar2john / ssh2john** — Convert file formats (ZIP, RAR, SSH keys) into hash formats John can crack.

---

### 🛠️ Tools Used  
- **John the Ripper (Jumbo)** — Main tool used for cracking various hash types.  
- **rockyou.txt** — Common password wordlist used for dictionary attacks.  
- **unshadow** — Combines `/etc/passwd` and `/etc/shadow` for cracking Linux passwords.  
- **zip2john / rar2john / ssh2john** — Convert protected files into hash formats for cracking.  
- **hash-identifier** — Helps identify hash formats.

---

### ⚠️ Challenges Faced  
- Understanding when to use `--format=` vs relying on auto-detection took some trial and error.  
- Figuring out when file formats needed tweaking (e.g., adding usernames for single crack mode).  
- It took me a while to get the hang of using word mangling rules in the right order.

---

### 🧠 What I Learned  
- John the Ripper supports more than just hashes – it can crack ZIP, RAR, and SSH key passwords.  
- Knowing the hash type makes cracking faster and more reliable.  
- Word mangling and custom rules are powerful when you know common patterns (e.g. `Password123!`).  
- Cracking /etc/shadow requires combining with /etc/passwd using `unshadow`.  
- Single crack mode is smart at guessing based on names and user info.

---

### 🌐 Real-World Application:  
> On penetration tests, John the Ripper is often used to crack weak passwords from dumped hashes. Tools like `zip2john` and `ssh2john` are useful for handling real-life password-protected files during post-exploitation.

---

### 💭 Reflections:  
- This room was long but practical. It covered a wide range of real-life uses for John.  
- Custom rules and single crack mode were especially interesting – they show how attackers can take advantage of human patterns.  
