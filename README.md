# 🔐 Folder Locker for Windows Home

Are you worried about how and where to save your personal files and photos securely on your laptop—without using external apps or websites? This project provides a simple batch script that lets you lock and unlock folders with a password, using only built-in Windows features. Perfect for Windows Home users who want offline privacy and control.

---

## 📁 What’s Included

| **File Name**       | **Description**                                                                 |
|---------------------|----------------------------------------------------------------------------------|
| `locker.bat`        | Ready-to-use batch file that locks/unlocks folders                              |
| `locker code.txt`   | Source code for the batch script, useful for customization or learning          |

---

## 🧰 How It Works

This script uses a clever trick: it renames your folder to mimic the Windows Control Panel using a special CLSID. This makes the folder inaccessible through normal browsing. It also hides the folder using system attributes. To unlock it, you enter a password in Command Prompt.

---

## ⚠️ Important Warning

<p style="color:red;"><strong>🚨 Be sure to set your password before using the script, and remember it carefully. If you forget the password, you will not be able to unlock your folder!</strong></p>

---

## 🛠️ Setup Instructions

### Step 1: Download the Files
- Clone this repository or download the ZIP.
- Extract the contents to a safe location on your laptop (e.g., `Documents\FolderLocker`).

### Step 2: Set Your Password
- Open `locker code.txt` in Notepad.
- Find the line:
  ```batch
  if NOT %pass%==YOUR_PASSWORD goto FAIL
  ```
- Replace `YOUR_PASSWORD` with your desired password. Example:
  ```batch
  if NOT %pass%==MySecret123 goto FAIL
  ```
- Save the file as `locker.bat` (if you're editing the code manually).

> ✅ Tip: Do **not** share this file with others unless you’ve removed or changed the password.

### Step 3: Place the Script
- Move `locker.bat` to the location where you want to create the locked folder.
- Double-click `locker.bat` to run it.

---

## 🔐 Using the Locker

| **Action**        | **What Happens**                                                                 |
|-------------------|----------------------------------------------------------------------------------|
| First Run         | Creates a folder named `Locker`                                                  |
| Lock Folder       | Prompts for confirmation, then hides and disguises the folder                    |
| Unlock Folder     | Prompts for password, then restores visibility and access                        |

### Locking the Folder
- Run `locker.bat`
- You’ll be asked:
  ```
  Are you sure you want to lock the folder? (Y/N)
  ```
- Type `Y` and press Enter
- The folder will disappear—it’s now hidden and disguised as the Control Panel

### Unlocking the Folder
- Run `locker.bat`
- You’ll be prompted:
  ```
  Enter password to unlock folder:
  ```
- Type your password and press Enter
- If correct, the folder will reappear as `Locker`

---

## ⚠️ Important Notes

- This script is **not encrypted**—it only hides the folder and restricts access via disguise.
- Anyone who opens the `.bat` file can see or change the password.
- For stronger protection, consider using encryption tools like VeraCrypt or BitLocker (not available on Windows Home).

---

## 🧪 Tested On

| **Operating System** | **Status**       |
|----------------------|------------------|
| Windows 10 Home      | ✅ Fully working |
| Windows 11 Home      | ✅ Fully working |

No admin rights or third-party software required.

---

## 📄 License

This project is licensed under the **MIT License**. You’re free to use, modify, and share it with proper attribution.

---

## 🙌 Credits

Created by **Vedhanth-P** — for learners, tinkerers, and anyone who loves simple, offline solutions.
