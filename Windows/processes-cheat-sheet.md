# 🧾 Windows Processes Cheat Sheet

Quick reference for common Windows processes and their functions. Useful for detection engineering, incident response, and malware analysis.

---

## 🔧 Core System Processes

| Process Name          | Description                                         |
|-----------------------|-----------------------------------------------------|
| `System`              | Kernel-level operations.                            |
| `System Idle Process` | Shows unused CPU time (not an actual process).      |
| `smss.exe`            | Session Manager – initializes sessions.             |
| `csrss.exe`           | Client/Server Runtime – manages windows and console.|
| `wininit.exe`         | Starts `services.exe` and `lsass.exe`.              |
| `services.exe`        | Controls system services.                           |
| `lsass.exe`           | Handles user authentication, local security.        |
| `winlogon.exe`        | Manages user logon and logoff.                      |
| `svchost.exe`         | Hosts Windows services (can run multiple times).    |

---

## 🧑‍💻 User Session & Interface

| Process Name   | Description                                   |
|----------------|-----------------------------------------------|
| `explorer.exe` | File Explorer, taskbar, desktop.              |
| `dwm.exe`      | Desktop Window Manager – visual effects.      |
| `conhost.exe`  | Console Host – runs with `cmd.exe`, `powershell.exe`. |
| `ctfmon.exe`   | Input services (IME, language bar).           |
| `LogonUI.exe`  | Handles the login screen.                     |
| `fontdrvhost.exe` | Font rendering in user sessions.           |
| `taskhostw.exe` | Executes scheduled tasks.                    |
| `taskmgr.exe`   | Opens Task Manager.                          |

---

## 🔐 Security-Related

| Process Name      | Description                               |
|-------------------|-------------------------------------------|
| `MsMpEng.exe`     | Microsoft Defender Antivirus engine.      |
| `NisSrv.exe`      | Defender’s Network Inspection Service.    |
| `smartscreen.exe` | Windows SmartScreen for app filtering.    |

---

## 🌐 Networking & RDP

| Process Name | Description                          |
|--------------|--------------------------------------|
| `rdpclip.exe` | Clipboard sync for RDP.             |
| `mstsc.exe`   | Remote Desktop Connection.          |
| `lsm.exe`     | Local Session Manager (RDP sessions). |

---

## 🪟 Modern Shell & UWP Apps

| Process Name                  | Description                      |
|-------------------------------|----------------------------------|
| `ShellExperienceHost.exe`     | Controls Start menu, taskbar.    |
| `SearchUI.exe` / `SearchApp.exe` | Cortana or Windows search.   |
| `RuntimeBroker.exe`           | Manages app permissions.         |
| `dllhost.exe`                 | COM Surrogate – loads COM DLLs.  |

---

## ⚙️ Common Utilities

| Process Name               | Description                               |
|----------------------------|-------------------------------------------|
| `WmiPrvSE.exe`             | WMI Provider – used in monitoring tools.  |
| `msdtc.exe`                | Microsoft Distributed Transaction Coordinator. |
| `OneDrive.exe`             | OneDrive client.                          |
| `notepad.exe`, `calc.exe`  | Classic apps.                             |

---

