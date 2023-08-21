# RuntimeError: Failed to resolve Python.Runtime.Loader.Initialize

RuntimeError: Failed to resolve Python.Runtime.Loader.Initialize from C:\Users\sam\Downloads\customerSearch (2)\temeats\pythonnet\runtime\Python.Runtime.dll site:stackoverflow.com

add this to your projects folder (only needed) as requirements.txt
ruquired are clr, pythonet

```python

Flask==2.2.0
pywebview
setuptools
packaging
clr-loader==0.1.7
pythonnet==3.0.0a2
```

#

Make sure pyinstaller is installed, make sure python path directed properly in 'pyvenv.cfg'

how my pyinstaller command line looks like:

```batch
pyinstaller --noconfirm --name "temeats"  --onedir --windowed --clean --hidden-import=clr --paths "C:\Users\dower\OneDrive\pywebviewEVERYTHIGN\testingFlask\customerTable\venv\Lib\site-packages" "C:\Users\dower\OneDrive\pywebviewEVERYTHIGN\testingFlask\customerTable\main.py"
```



error may look like:

Traceback (most recent call last): File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\main.py, line 56, in <module> File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\webview\__init__.py, line 154, in start File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\webview\guilib.py, line 119, in initialize File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\webview\guilib.py, line 71, in try_import File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\webview\guilib.py, line 60, in import_winforms File <frozen importlib._bootstrap>, line 1027, in _find_and_load File <frozen importlib._bootstrap>, line 1006, in _find_and_load_unlocked File <frozen importlib._bootstrap>, line 688, in _load_unlocked File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\webview\platforms\winforms.py, line 12, in <module webview.platforms.winforms> File <frozen importlib._bootstrap>, line 1027, in _find_and_load File <frozen importlib._bootstrap>, line 1006, in _find_and_load_unlocked File <frozen importlib._bootstrap>, line 688, in _load_unlocked File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\clr.py, line 6, in <module clr> File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\pythonnet\__init__.py, line 141, in load File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\clr_loader\types.py, line 94, in get_function File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\clr_loader\types.py, line 58, in __init__ File C:\Users\sam\DOWNLO~1\MAIN~1.DIS\clr_loader\netfx.py, line 47, in _get_callable RuntimeError: Failed to resolve Python.Runtime.Loader.Initialize from C:\Users\sam\DOWNLO~1\MAIN~1.DIS\pythonnet\runtime\Python.Runtime.dll
