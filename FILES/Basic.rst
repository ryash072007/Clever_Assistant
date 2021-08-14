$project
========

This package allows you to make virtual assistants easier!

Features
--------

- delete folder contents keeping specific files.
- shift files from a folder to another folder
- create hotkeys to open apps
- make custom macros that run on pressing hotkeys
- seach the internet
- speech to text support

Installation
------------

Install Clever_Assistant using:
..code-block:: python
   pip install Clever_Assistant
   
Usage
-----
ALWAYS remember to put '\\' to prevent error. EG: 'C:\\folder'
..code-block:: python
   from Clever_Assistant import *
   #delete all files except the one's specified from a folder
   del_all_keep_file(file_names: list, folder_path: str) #file_names has to have the extension, eg: file.txt
   
   #Shift files out of a folder to another
   shift_out_and_where(folder_path: str, other_folder_path: str)
   
   #create shortcut to open an app or start a file from its folder_path
   create_shortcut_for_app(hotkey: str, app_to_open: str)
   #hotkey example: 'ctrl/alt/shift + ctrl/alt/shift + Letter/Number'
   #app_to_open: location - 'c:\\location'
   #app_to_open: location - 'generic name of file'

   #run a function on pressing a hotkey
   run_func_on_hotkey(function, hotkey: str, args)
   #function is the function to be executed
   #hotkey example: 'ctrl/alt/shift + ctrl/alt/shift + Letter/Number'
   #args is the argument to be passed to the function, ONLY ONE argument is accepted

   #search the internet
   search_web(query, tld)
   #returns string
   #query is the string to search
   #tld is not neccesary, tld is the extension, defaults to 'com'

   #speach to text
   speachToText = S2t()
   speech = speachToText.listen()
   #returns string
   

License
-------

The project is licensed under the MIT license.
