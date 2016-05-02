## Running the Binary (Windows-only)

The simplest way to use PyKeylogger on Windows is to use the binary distribution.

* Get the binary package (instructions). \*
* If you got the executable installer, just run it and it will install PyKeylogger to wherever you specify.
* If you got the zip archive, unzip the archive, and put the contents anywhere you want (as long as they are all together in the same directory, of course)
* To start logging keys, just run pykeylogger.exe (if you used the installer, you can start it from the start menu shortcut). You can rename the exe to anything you want before running it, if you don't want "pykeylogger.exe" showing up in your task list.
* Default log location is the directory "logs" within the pykeylogger directory. Default master password is blank. To customize this, and other defaults, use the control panel. (For more detail, see docs/usage_instructions.)

* Information is outdated, the easiest way to the binary is to compile from source.

Library | Library Description | Library Version | OS | PyKeylogger Version | Comments
--------|---------------------|-----------------|----|---------------------|---------
Python  | The python language interpreter | 2.4.x |All | 0.8.0
Python | The python language interpreter | >= 2.4.x | All | >= 0.8.1 | Use the official python distribution from python.org, to minimize potential problems.
Python Imaging Library (PIL) | Image processing, used for image capture functionality. | >=1.1.6 | All | >=1.0.0 | Earlier versions may work, but no guarantees.
ConfigObj | Flexible .ini file parsing | >=4.5.2 | All | >= 0.8.0 | Get archive with both configobj.py and validate.py. To install ConfigObj:Unzip the contents of the archiveOpen a command prompt and 'cd' to the directory where you unzippedRun "python setup.py install" |
pyHook | Wraps the Windows API to capture mouse and keyboard events. | 1.5.1 | Windows | All |
py2exe | Builds windows executable out of python source. | 0.6.8 (Use 0.6.6 if you use pyHook version earlier than 1.5.1) | Windows | >= 0.8.0 | Optional, use only if you want to freeze your own executable out of source.
PyWin32 | Provide access to the Windows API. | >= 212 | Windows | All | Previously known as "win32all extensions"
python-xlib | Interfaces with the X server API, used to capture mouse and keyboard events. | >= 0.14 | Linux | >= 1.0.0 |
pygtk | Python GTK binding, used to quickly capture full-screen screenshots. | | Linux | >= 1.2.0 | Usually included in the default install.
pyHook | Wraps the Windows API to capture mouse and keyboard events. | 1.5.1 | Windows | All |
py2exe | Builds windows executable out of python source. | 0.6.8 (Use 0.6.6 if you use pyHook version earlier than 1.5.1) | Windows | >= 0.8.0 | Optional, use only if you want to freeze your own executable out of source.
PyWin32 | Provide access to the Windows API. | >= 212 | Windows | All | Previously known as "win32all extensions"
python-xlib | Interfaces with the X server API, used to capture mouse and keyboard events. | >= 0.14 | Linux | >= 1.0.0 |
pygtk | Python GTK binding, used to quickly capture full-screen screenshots. | | Linux | >= 1.2.0 | Usually included in the default install.
