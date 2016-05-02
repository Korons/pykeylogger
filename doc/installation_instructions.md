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

After all the needed dependencies are installed, download and unzip the PyKeylogger source zip archive, double click the keylogger.pyw file (or run "python keylogger.pyw" from a terminal), and it will run in the background, logging your keys.

# Some Linux notes

* You may be able to find a lot of these libraries in the repositories for your distro. Look for packages named python-configobj, python-xlib, python-imaging, python-gtk2, and of course, python. Just make sure you have the right versions of these in your repos - which you would, if you're running a relatively recent distro.
* You may also have to enable the 'record' extension on your X server (if it's not enabled by default). To do that, edit your /etc/X11/xorg.conf, and in Section "Module" add the line Load "record". Restart X for changes to take effect.
* Note that Xorg > 1.5 has a broken record module... Hopefully will be fixed soon, but for now refer to these links for more info. It seems that it is fixed as of the Xorg that ships with Ubuntu Lucid.

# Create Windows executables

To create your own Windows executables, open a terminal (command prompt), cd to the directory where you have extracted the PyKeylogger source, and run

```python setup.py py2exe```

(Note: if you haven't included the python install directory in your PATH, you will have to specify the full path to the python executable in your command. Instead of just 'python', it will be something like C:\Python26\python.exe.) This will create a subdirectory named "dist" with the binaries and all supporting libraries.

To create your own installer, you have to get NSIS (Nullsoft Scriptable Install System, then use it to build the installer from the "pykeylogger_install_script.nsi" file that comes with the source distribution of PyKeylogger. Note that the .nsi looks for the built binaries in "./pykeylogger-[version]" directory, so you have to rename the "dist" subdirectory that was created by py2exe so that NSIS can find it.

Default log location is the directory "logs" within the pykeylogger directory. Default master password is blank. To customize this, and other defaults, use the control panel. (For more detail, see Usage Instructions.)
