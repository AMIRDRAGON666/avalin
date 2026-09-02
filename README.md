i'm web creators and mesege to my gmail acount for Collaboration
🔒 Hide-folder – Ultra Shield Pro
Advanced File & Folder Hider for Windows (Pure Python 3 | No External Libraries)
Hide-folder (also known as Ultra Shield Pro) is an enterprise-grade security tool built entirely in pure Python 3 with no external dependencies. It lets you hide folders, files, and even embed secret files inside images (PNG, JPEG, BMP) — all while remaining invisible from Windows Explorer, Control Panel, and file search tools.

✨ Key Features
Feature	Description
🔐 Ultra Stealth Folder Hiding	Folders become invisible from Windows Explorer, Control Panel, and search (even with "Show Hidden Files" enabled)
🖼️ Image-Based Stealth Hiding	Hide any file inside an image — the image looks completely normal, but the secret file is recoverable
📁 List Hidden Folders & Images	Scan your system to find all ultra-hidden folders and images containing secret files
🔓 Ultra Unhide	Restore visibility to hidden folders instantly
📤 Extract Files from Images	Recover hidden files from image containers
🔐 File Name Encryption	Encrypt filenames using Base64 + Hex encoding for extra secrecy
🗂️ Directory Navigation	Change working directory within the tool
🗝️ Enterprise Password Security	Password protected with PBKDF2-HMAC-SHA256 (10,000 iterations), 3-attempt lockout, and salt-based encryption
🎨 Professional Terminal Interface	Colorful output, matrix startup effect, and clean menu system
🧠 How It Works
1. Ultra Stealth Folder Hiding
Uses Windows API (ctypes.windll.kernel32) to set file attributes:

0x02 – Hidden attribute
0x04 – System attribute
Combined with attrib +h +s to make folders invisible even when "Show Hidden Files" is enabled.

2. Image-Based Stealth Hiding
Reads the original file and encodes it in Base64
Appends metadata (filename, size, timestamp) + encoded data to the end of an image file
Saves as a .image_secret file and applies ultra stealth hiding
The image looks normal but contains recoverable secret data
3. Password Security
Uses PBKDF2-HMAC-SHA256 with random 32-byte salt
10,000 hashing iterations for brute-force protection
Password stored in ~/.ultra_shield_pro_config.json with enterprise encryption
3-attempt limit before system lockout
4. File Name Encryption
Converts filename to hex → then Base64
Prefixes with ULTRA_ENC_
Automatically applies ultra stealth hiding to encrypted file
🚀 Usage
Run the script (requires Python 3 on Windows):
python Hide-folder.py
Set your password (first run, minimum 8 characters)

Choose from the main menu:

Hide/unhide folders
Hide files inside images
Extract files from images
List hidden folders/images
Encrypt filenames
Change password
⚠️ Important Notes
Windows only – Uses ctypes.windll (Windows API), incompatible with Linux/Mac
Requires Administrator privileges for some features
Files hidden with ultra stealth are not visible in standard Windows interfaces
Image-hided files are recoverable but require the tool to extract
🛡️ Security Level
Security Feature	Value
Encryption Algorithm	PBKDF2-HMAC-SHA256 (256-bit)
Password Hashing	Salt-based, 10,000 iterations
Stealth Method	Hidden + System attributes + filename encryption
External Dependencies	None – 100% pure Python
📦 Requirements
Python 3.6+
Windows 10/11
Administrator privileges (recommended)
🤝 Contributing
Feel free to submit issues, enhancements, or pull requests!

⚖️ License
This project is for educational and security research purposes only. Use responsibly.

Hide-folder – Where stealth meets enterprise security in pure Python. 🚀
