# Python Windows Service Boilerplate

This is a simple boilerplate for a Windows Service using Python. The code is based on this blog post:
<https://metallapan.se/post/windows-service-pywin32-pyinstaller/>

```cmd
# Create venv:
python -m venv .venv

# Activate venv:
.\.venv\Scripts\activate

# Prerequisites:
pip3 install pywin32 pyinstaller

# Build:
pyinstaller.exe --onefile --runtime-tmpdir=. --hidden-import win32timezone myservice.py

# With Administrator privilges
# Install:
dist\myservice.exe install

# Start:
dist\myservice.exe start

# Install with autostart:
dist\myservice.exe --startup delayed install

# Debug:
dist\myservice.exe debug

# Stop:
dist\myservice.exe stop

# Uninstall:
dist\myservice.exe remove
```