# ShotText

This tool gives users the ability to take a screenshot and copy to the clipboard the text content of the screenshot. Works on Windows, macOS, and most modern Linux distros.

![ShotText Demo](https://i.imgur.com/Z0Ng13S.gif)

## Use

Running `shottext.py` with `python`/`python3` will open an overlay over the screen, where a rectangle can be drawn over the portion of the screen containing the text the user wishes to copy.

An optional command line argument can specify the language. For example, `python shottext.py eng+fra` will use English as the primary language and French as the secondary language. The default is `eng` (English). Make sure that the appropriate data files for Tesseract are installed for other languages. A list of all supported languages can be found [here](https://github.com/tesseract-ocr/tesseract/blob/master/doc/tesseract.1.asc#languages-and-scripts).

It is recommended to attach a global hotkey to this tool so you can run it without opening a console and typing in the command.

On **Windows**, one can accomplish this by using an [AutoHotkey](https://www.autohotkey.com/) script; `shottext.ahk` contains a sample AHK script that can be used.  
On **Ubuntu**, open the Keyboard Settings, which shows you all the Gnome shortcuts. At the bottom there is a `+` button to add your own shortcuts. Click it and set the command to `/usr/bin/python3 <path-to-shottext.py>`. In case you are using a virtual environment, the `python3` path above should point to the environment's `python3` instead of the global `python3`.  
The process on other operating systems can be found by searching how to run a shell command with a keyboard shortcut.

## Installation

- Install [Python 3](https://www.python.org/downloads/)
- Clone this repository... `git clone https://github.com/Anmol-Sri/ShotText.git`
- ...and `cd` into it `cd ShotText`
- Install the required packages with `pip install -r requirements.txt`
- Install [Google's Tesseract OCR Engine](https://github.com/tesseract-ocr/tesseract), and ensure that `tesseract` can be reached from the command line by adding the directory to your system path. In Linux it can be done by typing ` sudo apt-get install tesseract-ocr ` in the terminal.
- `python3 shottext.py `

Linux users: If the text shows up correctly in the notification, but you cannot paste it, install `xclip` (e.g. with `sudo apt install xclip`).

## Description of Packages Used

- Pyperclip : Pyperclip is a cross-platform Python module for copy and paste clipboard functions.
- Pytesseract : Python-tesseract is an optical character recognition (OCR) tool for python. That is, it will recognize and “read” the text embedded in images.
- PIL : Python Imaging Library (abbreviated as PIL) is a free and open-source additional library for the Python programming language that adds support for  opening, manipulating, and saving many different image file formats.
- PyQt5 : Qt is set of cross-platform C++ libraries that implement high-level APIs for accessing many aspects of modern desktop and mobile systems.
