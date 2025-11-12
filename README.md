Smart File Organizer (Python GUI App)
Overview:

Smart File Organizer is a simple and intuitive desktop application built with Python and Tkinter that automatically sorts and organizes your files into folders based on their types.
It’s perfect for anyone who downloads or stores a lot of files and wants a clean, clutter-free workspace — with just one click.

Features:

User-friendly graphical interface (GUI)
Automatically detects file types and organizes them into folders
Works on Windows, macOS, and Linux
Built with Python’s built-in libraries — no external dependencies required
Optional EXE version for easy use without installing Python

How It Works:

Open the app

Click “Select Folder”

Choose the folder you want to organize

The app automatically creates folders (like Images, Documents, Videos, etc.) and moves your files accordingly.

Example:

Before Running:

Downloads/
│── photo1.jpg
│── notes.txt
│── video.mp4
│── resume.pdf


After Running:

Downloads/
│── Images/
│   └── photo1.jpg
│── Videos/
│   └── video.mp4
│── Documents/
│   └── resume.pdf
│── Text/
│   └── notes.txt

Technologies Used:

Python 3+

Tkinter (GUI Framework)

os, shutil (File Handling)

Installation:
Option 1 – Run from Python

Download or clone this repository

Open a terminal and run:

python file_organizer.py

Option 2 – Run as an App (EXE)

If you want to use it like a desktop app (no Python required):

Download the .exe file from the dist folder

Double-click it to launch the app

Choose any folder — it will organize your files instantly

Code Example:

Here’s a short snippet of the core logic:

for filename in os.listdir(folder_path):
    file_ext = os.path.splitext(filename)[1].lower()
    for folder_name, extensions in FILE_TYPES.items():
        if file_ext in extensions:
            target_folder = os.path.join(folder_path, folder_name)
            os.makedirs(target_folder, exist_ok=True)
            shutil.move(file_path, os.path.join(target_folder, filename))

Future Improvements:

Add drag-and-drop functionality

Support for more file types

Dark/Light mode switch

Save preferred folder paths


Author:

Nkosinathi Maqutyana
Python Developer | Automation Enthusiast

Tags

#Python #Automation #Tkinter #DesktopApp #Productivity #FileManagement

License

This project is open-source — you’re free to use, modify, and share it with credit.