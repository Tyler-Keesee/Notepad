# Notepad

A Windows-oriented PyQt6 text editor.

## Windows 11: exact setup (PowerShell)

Requires Git and Python 3.11+ with the standard Tcl/Tk and GUI support. Run **one command at a time**:

```powershell
git --version
```

```powershell
python --version
```

```powershell
git clone https://github.com/Tyler-Keesee/Notepad.git
```

```powershell
Set-Location .\Notepad
```

```powershell
python -m venv .venv
```

```powershell
.\.venv\Scripts\python.exe -m pip install --upgrade pip
```

```powershell
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

```powershell
.\.venv\Scripts\python.exe -m compileall -q main.py
```

```powershell
.\.venv\Scripts\python.exe main.py
```

A desktop editor window should appear. No venv activation is required: all commands use the project's Python executable directly. The repository currently has no automated GUI integration tests, so installation and syntax checks do not prove every editor feature works.

**Troubleshooting:** If the Qt GUI does not open, use a regular Windows desktop session and inspect the first traceback. Python 3.14 compatibility of every dependency is not confirmed; for an older project, Python 3.11 is a conservative fallback. Do not run the editor as Administrator just to fix an installation problem.
