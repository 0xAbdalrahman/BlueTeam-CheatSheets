# 📝 Windows Event IDs Cheat Sheet

This cheat sheet covers the most common Windows Security Event IDs used in SOC, Incident Response, and Threat Hunting.

---

## 🔑 1. Authentication & Logon Events

| Event ID | Description                                    |
| -------- | ---------------------------------------------- |
| **4624** | Successful Logon                               |
| **4625** | Failed Logon                                   |
| **4634** | Logoff                                         |
| **4648** | Logon using explicit credentials               |
| **4672** | Special Privilege Logon (Admins, SYSTEM, etc.) |
| **4776** | Credential validation attempt                  |
| **4768** | Kerberos TGT Request (AS-REQ)                  |
| **4769** | Kerberos Service Ticket Request (TGS-REQ)      |
| **4771** | Kerberos pre-authentication failed             |
| **4740** | Account Lockout                                |

---

## 👤 2. Account & Privilege Escalation Events

| Event ID | Description                                       |
| -------- | ------------------------------------------------- |
| **4720** | User Account Created                              |
| **4722** | User Account Enabled                              |
| **4725** | User Account Disabled                             |
| **4726** | User Account Deleted                              |
| **4738** | User Account Changed                              |
| **4756** | User added to an Admin Group                      |
| **4757** | User removed from an Admin Group                  |
| **4673** | A privileged service was called                   |
| **4674** | An operation was performed on a privileged object |

---

## ⚙️ 3. Process Creation & Execution

| Event ID | Description                           |
| -------- | ------------------------------------- |
| **4688** | A new process has been created         |
| **4689** | A process has exited                   |
| **4697** | Service installed                      |
| **7030** | Service marked as interactive (persistence) |
| **7045** | A service was installed in the system  |

---

## 🛡️ 4. Security & Group Policy Changes

| Event ID | Description                             |
| -------- | --------------------------------------- |
| **1102** | Security Log Cleared (log tampering)    |
| **4719** | System audit policy changed             |
| **4732** | User added to a security group          |
| **4733** | User removed from a security group      |
| **4735** | Security group modified                 |
| **4737** | Local group modified                    |
| **4764** | Group deleted                           |

---

## 🌐 5. Network Events & Lateral Movement

| Event ID | Description                                       |
| -------- | ------------------------------------------------- |
| **5140** | A network share was accessed                      |
| **5145** | A network share object was checked                |
| **5156** | Allowed network connection                        |
| **5157** | Blocked network connection                        |
| **4649** | A replay attack was detected                      |
| **4769** | Kerberos TGS ticket request (Pass-the-Ticket)     |
| **4776** | NTLM authentication (NTLM relay detection)        |

---

## 🕒 6. Malware, Persistence & Suspicious Activities

| Event ID | Description                           |
| -------- | ------------------------------------- |
| **4698** | Scheduled Task Created                |
| **4699** | Scheduled Task Deleted                 |
| **4700** | Scheduled Task Enabled                 |
| **4701** | Scheduled Task Disabled                |
| **4713** | Kerberos policy changed                |
| **7022** | Service hang detected                  |
| **7040** | Startup type of a service was changed |

---

## 📂 7. File & Object Access Events

| Event ID | Description                           |
| -------- | ------------------------------------- |
| **4656** | File access attempt                   |
| **4663** | File or object accessed               |
| **4660** | Object deleted                        |
| **4661** | Handle requested for an object        |
| **4670** | Permissions on an object were changed |

---

## 🛡️ 8. Windows Defender & Security Alerts

| Event ID | Description                           |
| -------- | ------------------------------------- |
| **1116** | Malware detected and action taken     |
| **1117** | Malware detected but no action taken  |
| **1118** | Malware removed                       |
| **5007** | Windows Defender settings modified    |

---

🔎 **Tip:** Prioritize these events for detection rules, as they often indicate malicious or suspicious activity.
