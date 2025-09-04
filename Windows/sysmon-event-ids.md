# 🛡️ Sysmon Event ID Cheat Sheet

**Source**: Sysmon logs are located at:  
`Applications and Services Logs/Microsoft/Windows/Sysmon/Operational`

This cheatsheet helps defenders quickly map Sysmon Event IDs to their security use cases.

---

## 🔐 1. Process & Execution Events

| Event ID | Description        | Use Case |
|----------|-------------------|----------|
| **1**    | Process Create    | Detect suspicious processes (command line, hashes, parent process). |
| **5**    | Process Terminated | Track when a process ends. |
| **10**   | Process Access    | Detect credential dumping (e.g., LSASS memory access). |
| **25**   | Process Tampering | Detect code injection / hollowing attempts. |

---

## 📂 2. File & Image Events

| Event ID | Description              | Use Case |
|----------|--------------------------|----------|
| **2**    | File Creation Time Changed | Detect timestomping (anti-forensics). |
| **11**   | File Created             | Monitor dropped payloads, malware writing files. |
| **23**   | File Deleted             | Track malware deleting itself or logs. |
| **7**    | Image Loaded (DLL Load)  | Detect unsigned DLLs, malicious DLL injection. |
| **26**   | File Executed via Mapped Section | Detect fileless malware execution. |

---

## 🌐 3. Network & IPC (Lateral Movement)

| Event ID | Description            | Use Case |
|----------|------------------------|----------|
| **3**    | Network Connection     | See which process opened a connection (IP, port, process). |
| **17**   | Named Pipe Created     | Malware C2 channel detection. |
| **18**   | Named Pipe Connected   | Detect lateral movement / persistence via named pipes. |
| **22**   | DNS Query              | Detect suspicious domains (malware C2, phishing). |

---

## 🗝️ 4. Registry & WMI Persistence

| Event ID | Description                | Use Case |
|----------|----------------------------|----------|
| **12**   | Registry Object Created/Deleted | Persistence keys detection. |
| **13**   | Registry Value Set         | Detect autorun or service modifications. |
| **14**   | Registry Key/Value Renamed | Detect registry tampering. |
| **19**   | WMI Event Filter           | Detect WMI persistence. |
| **20**   | WMI Event Consumer         | Detect malicious consumers. |
| **21**   | WMI Event Binding          | Link filters and consumers → persistence. |

---

## ⚙️ 5. Driver & System Integrity

| Event ID | Description           | Use Case |
|----------|-----------------------|----------|
| **6**    | Driver Loaded         | Detect unsigned / suspicious drivers. |
| **15**   | File Stream Created   | Detect ADS (Alternate Data Streams) persistence. |
| **27**   | File Block Executable | Blocked execution of untrusted files. |
| **28**   | File Block Shredding  | Prevents destruction of evidence. |

---

## 🚨 6. Other Suspicious Activities

| Event ID | Description               | Use Case |
|----------|---------------------------|----------|
| **8**    | CreateRemoteThread        | Detect process injection (classic malware technique). |
| **9**    | Raw Access Read           | Detect tools reading raw disk (e.g., Mimikatz, forensic evasion). |
| **16**   | Sysmon Configuration Change | Detect tampering with Sysmon itself. |
| **24**   | Clipboard Change          | Detect sensitive data exfiltration via clipboard. |

---

