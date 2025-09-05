# 🕵️ Windows Forensics Cheat Sheet  

### Quick reference for common Windows forensic artifacts.  

---

## 🖥️ System Info & Accounts  

- **OS Version**  
  `SOFTWARE\Microsoft\Windows NT\CurrentVersion`  

- **Current Control Set**  
  - `HKLM\SYSTEM\CurrentControlSet`
  
  - `SYSTEM\Select\Current`
  
  - `SYSTEM\Select\LastKnownGood`  

- **Computer Name**  
  `SYSTEM\CurrentControlSet\Control\ComputerName\ComputerName`  

- **Time Zone Information**  
  `SYSTEM\CurrentControlSet\Control\TimeZoneInformation`  

- **Network Interfaces & Past Networks**  
  `SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\Interfaces`  

- **Autostart Programs (Autoruns)**  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Run`  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\RunOnce`  
  - `SOFTWARE\Microsoft\Windows\CurrentVersion\RunOnce`  
  - `SOFTWARE\Microsoft\Windows\CurrentVersion\policies\Explorer\Run`  
  - `SOFTWARE\Microsoft\Windows\CurrentVersion\Run`  

- **SAM Hive & User Info**  
  `SAM\Domains\Account\Users`  

---

## 📂 User Activity  

- **Recent Files**  
  `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\RecentDocs`  

- **Office Recent Files**  
  - `NTUSER.DAT\Software\Microsoft\Office\VERSION`  
  - `NTUSER.DAT\Software\Microsoft\Office\VERSION\UserMRU\LiveID_####\FileMRU`  

- **ShellBags (Folder Views)**  
  - `USRCLASS.DAT\Local Settings\Software\Microsoft\Windows\Shell\Bags`  
  - `USRCLASS.DAT\Local Settings\Software\Microsoft\Windows\Shell\BagMRU`  
  - `NTUSER.DAT\Software\Microsoft\Windows\Shell\BagMRU`  
  - `NTUSER.DAT\Software\Microsoft\Windows\Shell\Bags`  

- **Open/Save & LastVisited Dialog MRUs**  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\OpenSavePIDlMRU`  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\ComDlg32\LastVisitedPidlMRU`  

- **Windows Explorer Address/Search Bars**  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\TypedPaths`  
  - `NTUSER.DAT\Software\Microsoft\Windows\CurrentVersion\Explorer\WordWheelQuery`  

---

## ⚙️ Execution Evidence  

- **UserAssist (Program Execution Tracking)**  
  `NTUSER.DAT\Software\Microsoft\Windows\Currentversion\Explorer\UserAssist\{GUID}\Count`  

- **ShimCache (AppCompatCache)**  
  `SYSTEM\CurrentControlSet\Control\Session Manager\AppCompatCache`  

- **AmCache**  
  `Amcache.hve\Root\File\{Volume GUID}\`  

- **BAM/DAM (Background Activity Monitor / Desktop Activity Monitor)**  
  - `SYSTEM\CurrentControlSet\Services\bam\UserSettings\{SID}`  
  - `SYSTEM\CurrentControlSet\Services\dam\UserSettings\{SID}`  

---

## 💽 External / USB Device Forensics  

- **Device Identification**  
  - `SYSTEM\CurrentControlSet\Enum\USBSTOR`  
  - `SYSTEM\CurrentControlSet\Enum\USB`  

- **First/Last Connection Times**  
  `SYSTEM\CurrentControlSet\Enum\USBSTOR\Ven_Prod_Version\USBSerial#\Properties\{83da6326-97a6-4088-9453-a19231573b29}\####`  
  - `0064 = First connection`  
  - `0066 = Last connection`  
  - `0067 = Last removal`  

- **USB Device Volume Name**  
  `SOFTWARE\Microsoft\Windows Portable Devices\Devices`  

---
