```
smss.exe (Session Manager Subsystem)
│
├──> Session 0 (System Session)
│ ├── csrss.exe (Client/Server Runtime Subsystem)
│ ├── wininit.exe (Windows Initialization Process)
│ │ ├── services.exe (Service Control Manager)
│ │ │   └── svchost.exe (Host Process for Windows Services)
│ │ ├── lsass.exe (Local Security Authority Subsystem Service)
│ │ └── lsm.exe (Local Session Manager - handles RDP sessions)
│
└──> Session 1 (First User Session - Interactive Logon)
| ├── csrss.exe (Client/Server Runtime for user session)
| ├── winlogon.exe (Windows Logon Manager)
│ | └── LogonUI.exe (Logon Screen UI)
| |
| └── User Shell Initialization
|   ├── explorer.exe (Windows Explorer - desktop, taskbar, start menu)
|   ├── dwm.exe (Desktop Window Manager - GUI rendering)
|   ├── ctfmon.exe (Language/IME services)
|   ├── RuntimeBroker.exe (Manages UWP app permissions)
|   ├── ShellExperienceHost.exe (Modern UI / Start Menu control)
|   ├── SearchUI.exe / SearchApp.exe (Cortana or Windows search)
|   ├── OneDrive.exe (OneDrive sync client, if enabled)
|   └── taskhostw.exe (Host for scheduled/COM tasks)
```
