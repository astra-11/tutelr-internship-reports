# 🛠 CHAPS – Windows Configuration Hardening Assessment

This report documents my hands-on assessment of Windows security configurations using the **CHAPS (Configuration Hardening Assessment PowerShell Script)** tool. The goal was to identify security weaknesses on a system where traditional policy tools can't be installed.

---

## 📌 Objective

To audit Windows configuration hardening using a standalone PowerShell script and recommend remediations based on the findings.

---

## 🧰 Tools Used

- CHAPS PowerShell Script
- PowerSploit
- Windows Command Prompt
- Python HTTP Server (for local hosting)

---

## 🧪 Steps Performed

1. Setup local web server to host CHAPS and PowerSploit.
2. Executed the script via PowerShell with bypass execution policy.
3. Collected results on system settings like:
   - BitLocker status
   - PowerShell logging
   - Credential Guard
   - Remote access policies
4. Identified insecure defaults and misconfigurations.

---

## 🔍 Key Findings

- BitLocker was not enabled.
- PowerShell auditing settings were disabled.
- Cached logon count was high (10).
- Credential Guard & Device Guard checks failed.
- RDP was not explicitly disabled.

---

## ✅ Recommended Remediations

- Enable BitLocker on OS volume.
- Configure PowerShell Module & Script Logging.
- Set CachedLogonsCount to 0 or 1.
- Enable Credential Guard if supported.
- Disable RDP access unless required.

---

## 💡 What I Learned

- Real-world use of auditing scripts without additional installations
- Importance of secure defaults in enterprise environments
- Manual execution and delivery of PowerShell-based assessments

