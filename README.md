===========================================
🔐 iOS Binary Security Checker (otool-based)
===========================================

This tool automates essential static security checks on iOS binaries using `otool`. It's designed for iOS penetration testers, reverse engineers, and mobile app security professionals who want a quick assessment of binary-level hardening and risk exposure.

---------------------
📌 Key Security Checks
---------------------
The script performs the following assessments:

1. Linked Libraries
2. PIE (Position Independent Executable)
3. Stack Canary Protection
4. ARC (Automatic Reference Counting)
5. Binary Encryption Status (FairPlay DRM)
6. NX (No-Execute Bit / DEP)
7. RPATH Usage (Dylib Hijacking Risk)
8. Debug Symbols
9. Objective-C Class & Method Names
10. Weak Hashing Algorithms (e.g., MD5, SHA-1)
11. Deprecated/Banned APIs (e.g., gets, strcpy)
12. Weak Random Functions (e.g., rand)
13. Unsafe Memory Functions (e.g., malloc, memcpy)

-----------------------
⚙️ How to Use the Script
-----------------------

1️⃣ Save the script to a file named `otool_checker.sh`

```bash
nano otool_checker.sh
Paste the full script content, then save and exit using:

objectivec
Copy
Edit
CTRL + X → Y → Enter
2️⃣ Make the script executable:

bash
Copy
Edit
chmod +x otool_checker.sh
3️⃣ Run the script with your iOS binary as the argument:

bash
Copy
Edit
./otool_checker.sh <binary_file>
Example:

bash
Copy
Edit
./otool_checker.sh MyAppBinary
✅ Requirements & Notes
Works on macOS with otool available by default.

Designed for static analysis only — no code execution is performed.

Suitable for both stripped and unstripped binaries.

📂 Use Cases
iOS Application Security Audits

Reverse Engineering Pre-Checks

CI/CD Pipeline Binary Hardening Validation

Red Team Static Recon