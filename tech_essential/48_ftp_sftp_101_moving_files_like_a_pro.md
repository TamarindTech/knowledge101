# **📂 FTP/SFTP 101: Moving Files Like a Pro**

**💡 What Are FTP and SFTP?**

Both **FTP (File Transfer Protocol)** and **SFTP (SSH File Transfer Protocol)** are used to **transfer files** between your computer and a **remote server**, such as a web host or a cloud server.

“It’s like drag-and-drop, but over the internet.”

|**Protocol**|**What It Stands For**|**Secure?**|**Port**|**Common Use**|
| :- | :- | :- | :- | :- |
|FTP|File Transfer Protocol|❌ No|21|Uploading to a web server|
|SFTP|SSH File Transfer Protocol|✅ Yes|22|Secure server file access|

**📦 When Do You Use FTP or SFTP?**

- Upload a website to a server
- Download log files from a remote machine
- Transfer backup files between servers
- Access files from a remote development environment

**🔒 Why Use SFTP Over FTP?**

|**Feature**|**FTP**|**SFTP**|
| :- | :- | :- |
|Encrypted Connection|❌ No|✅ Yes|
|Username/Password|✅ Required|✅ Required|
|File Integrity|❌ Weak|✅ Strong|
|Authentication|Basic|Supports SSH keys|

Always use **SFTP** unless your server only supports legacy FTP.

**🧠 How FTP/SFTP Works**

1. You use a **client** (like FileZilla or command-line)
1. Connect to a **server** using IP/domain + credentials
1. You browse, upload, download, rename, or delete files
1. Changes happen **directly on the remote server**

**🛠️ FTP/SFTP Clients You Can Use**

|**Tool**|**Type**|**Use Case**|
| :- | :- | :- |
|**FileZilla**|GUI app|Easy drag-and-drop interface|
|**Cyberduck**|GUI app|Mac-friendly file manager|
|**WinSCP**|GUI + script|Good for automated transfers on Windows|
|**Terminal**|Command-line|For pros, scripting, automation|

**

**📂 Common FTP/SFTP Commands (CLI)**

\# Connect using SFTP

sftp username@yourserver.com

\# List files

ls

\# Change directory

cd /var/www

\# Upload file

put index.html

\# Download file

get backup.zip

\# Exit session

bye

**

**🔐 SFTP with SSH Keys (for Extra Security)**

Instead of using just a password, you can use a **private/public key pair**:

1. Generate a key:\
   ssh-keygen -t ed25519
1. Copy your public key to the server:\
   ssh-copy-id user@host
1. Connect without typing a password:\
   sftp user@host

This is safer and script-friendly.

**⚠️ Common FTP/SFTP Errors**

|**Error**|**Cause**|
| :- | :- |
|“Connection Refused”|Wrong port, firewall block|
|“Permission Denied”|Invalid username, password, or file access|
|“Timeout”|Server too slow, wrong IP/domain|
|“Can’t Change Directory”|Invalid path or restricted access|

✅ Check your credentials, paths, and ensure the server is up.

**🧪 Try It Yourself (Safe Practice)**

- Set up an SFTP server using a cloud VM (e.g. DigitalOcean, EC2)
- Use FileZilla to connect using sftp://your-ip
- Transfer test files like hello.txt

**

**🧰 Automation & DevOps Use Cases**

- 🔁 Sync code to servers
- 📦 Transfer CI/CD build artifacts
- 🔐 Secure backups
- 🤖 Script file uploads using cron jobs or CI tools

**🧠 Key Concepts to Remember**

|**Term**|**Meaning**|
| :- | :- |
|**FTP**|Basic, insecure file transfer protocol|
|**SFTP**|Secure file transfer via SSH|
|**SSH**|Encrypted shell access|
|**Client**|Your local software|
|**Server**|The remote machine or host|

**📚 Learn More**

- 📘 *“The Linux Command Line”* by William Shotts
- 🌐 [FileZilla Docs](https://wiki.filezilla-project.org/)
- 🔐 [SFTP Server Setup Guide (DigitalOcean)](https://www.digitalocean.com/community/tutorials/how-to-enable-sftp-without-shell-access)
- 📹 YouTube: “SFTP vs FTP – Explained in 5 Minutes”

**

**💬 Final Thought**

“FTP moves your files. SFTP moves them **safely**.”

Once you understand how FTP/SFTP works, you'll have the power to:

- Deploy websites
- Automate backups
- Collaborate with remote teams



