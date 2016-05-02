# PyKeylogger

PyKeylogger is a free open source keylogger written in the python programming language, available under the terms of the GNU General Public License. I threw it together one day after not being able to find a simple and trustworthy (as measured by the availability of source code) keylogger for windows, and it sort of snowballed from there. It is currently available for Windows (NT/2000 and up), and Linux (using Xlib, so won't work on the console).

It is primarily designed for personal backup purposes, rather than stealth keylogging. Thus, it does not make explicit attempts to hide its presence from the operating system or the user. That said, the only way it is visible is that the process name shows up in the task list, so it is not immediately apparent that there is a keylogger on the system. However, since it also makes periodic writes to disk, and since it openly hooks well-known windows APIs (SetWindowsHookEx), any keylogger detector worth its salt will be able to sniff it out. (The fact that there are almost no anti-malware detectors worth their salt is a completely separate issue.) So basically, it doesn't exactly advertise itself, but doesn't hide itself either.

The main goal is to create a "universal backup solution" for everything you type. We have all at one time or another accidentally closed that word or notepad file without saving. We have all lost form data on the web after it failed to submit properly. Not even mentioning the ever-present threat of computer crash. PyKeylogger logs everything you type, so you can recover the text of anything you type in any application. Simple and elegant, don't you think? :)

Since PyKeylogger is available as a simple python source file (well, a few simple source files), there are no trust issues with using it - you can just look at the source yourself and make sure that it does exactly what you need it to, and nothing more. (Especially not sending your info to someone else without your knowledge.) If you think you can trust me, and/or if you are not interested in getting all those packages to run the source file (see instructions), there is also a binary distribution available for windows.

If you think that you can contribute to the project in any way, feel free to jump in.

## Major Features

* Log all keystrokes to disk, to a delimited data file
* Automatically archive logfiles to dated zips
* Automatic log rotation
* Automatically send zipped log archives to specified email address[es] (works with any SMTP server, including GMail and Yahoo Mail secure SMTP servers)
* Automatically upload zipped log archives to a specified FTP server.
* Takes a partial screenshot, centered at the location of every mouse click.
* Takes a full screenshot at fixed time intervals, if the computer is not idle.
* Automatically flush write buffer to disk, to minimize data loss in the event of a crash
* Very customizable, through configuration with a .ini text file
* GUI (graphical) control panel for settings and actions (this is now the recommended way to change settings)
* Password protection of control panel
* Passwords are obfuscated in the configuration file, to prevent casual snooping
* Automatically delete log files older than specified age

## Licensing

* PyKeylogger itself is licensed under GPL v3 or later.
* The pyxhook module contributed by Tim Alexander is licensed under GPL v2 or later.
* The PyKeylogger icon is a remix of the icons from the Tango Desktop Project, and is thereby licensed under the Creative Commons Attribution Share-Alike license v 2.5

A number of libraries are used by PyKeylogger, and their license terms are listed here for your convenience.

* Python itself is under the Python Software Foundation License (PSFL).
* Python Imaging Library (PIL) is under the MIT license.
* py2exe is under the MIT license.
* ConfigObj is under the BSD license.
* pyHook is under the MIT license
* PyWin32 (formerly known as win32all extensions) is under the PSFL
* python-xlib is under the GPL v2 or later.
* Pmw GUI toolkit is under the MIT License.
* PyGTK is licensed under the LGPL 2.1 or later.
