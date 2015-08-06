# CmderRemaster
A simple remaster the cmder to run on Windows 10

![Cmder Screenshot](http://i.imgur.com/4KDpa7J.png)

## Why use it

The main advantage of Cmder is portability. It is designed to be totally self-contained with no external dependencies, that is makes it great for **USB Sticks** or **Dropbox**. So you can carry your console, aliases and binaries (like wget, curl and git) with you anywhere.

## Installation

1. Download the latest release
2. Extract
3. (optional) Place your own executable files into the `bin` folder to be injected into your PATH.
4. Run cmder

*(There will be a version with installer)*

## Integration

So you've experimented with cmder a little and want to give it a shot in a more permanent home;

### Shortcut to open Cmder in a chosen folder

1. Open a terminal as an Administrator
2. Navigate to the directory you have placed Cmder
3. Execute `.\cmder.exe /REGISTER ALL`  
   _If you get a message "Access Denied" ensure you are executing the command in an **Administrator** prompt._

In a file explorer window right click in or on a directory to see "Cmder Here" in the context menu.

## Keyboard shortcuts

### Tab manipulation

* `Ctrl + t` : new tab dialog (maybe you want to open cmd as admin?)
* `Ctrl + w` : close tab
* `Ctrl + d` : close tab (if pressed on empty command)
* `Shift + alt + number` : fast new tab: `1` - CMD, `2` - Powershell `*` - More to come
* `Alt + enter`: Fullscreen

### Shell

* `Shift + Up` : Traverse up in directory structure (lovely feature!)
* `End, Home, Ctrl` : Traversing text with as usual on Windows
* `Ctrl + r` : History search
* `Shift + mouse` : Select and copy text from buffer

(Some shortcuts are not yet documented, thought they exist, please add them here)

## Features

### Aliases
You can define simple aliases with command `alias name=command`.

For example there is one defined for you `alias e.=explorer .`

All aliases will be saved in `/config/aliases` file

### SSH Agent

To start SSH agent simply call `agent`, which is in the `bin` folder.

If you want to run SSH agent on startup, uncomment the line in `/vendor/init.bat`so it says `@call "%CMDER_ROOT%/bin/agent.cmd"`.

## Todo

1. Git Bash
2. Check for clink and git before injecting them (Sort of done)

## License

All software included is bundled with own license

The MIT License (MIT)

Copyright (c) 2015 Samuel Vasko
Copyright (c) 2015 Bruno Moreno(remaster)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
