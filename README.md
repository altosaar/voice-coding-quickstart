It was very difficult and confusing for me to set this up the first time, so I hope this helps someone else save time.

There are so many helpful resources that I needed to get this to work:
- Help from @LexiconCode on properly installing natlink and getting a minimal working example to test the system end-to-end (see https://github.com/dictation-toolbox/dragonfly/pull/351/commits/cbe2d25a16a778474e5b5291605272b9d2c0d645)
- Lots of help from @wolfmanstout (see https://handsfreecoding.org/) on how to get started

## Installation
- Windows 10
- Install Dragon NaturallySpeaking. You might be able to get a copy through your school's or employer's disability office or leave management office. 
- Install natlink by following the exact instructions: https://github.com/dictation-toolbox/natlink (may need to uninstall all other versions of python and ensure they are removed from the PATH environment variable in Windows, before installing the 32-bit version of python 3.8 using the official download: https://www.python.org/downloads/)
- Python 3.8, 32-bit installs to `C:\Users\jaan\AppData\Local\Programs\Python\Python38-32\python.exe`; may need to add this to the PATH variable by editing environment variables in Windows
- Configure natlink: run `python C:\Users\jaan\Dropbox\projects\natlink\src\natlinkpy\ConfigureNatlink\start_configurenatlink.py` and enable the UserDirectory; select the location as this repo:
 <img src="https://user-images.githubusercontent.com/5317244/124948678-e7d28780-dfde-11eb-9094-87ab9c930235.png" width="300">
- Install dragonfly: https://github.com/dictation-toolbox/dragonfly/ 
- Restart dragon

## Minimal working example 
Natlink allows dragonfly to communicate with Dragon NaturallySpeaking. 

A simple example rule is in `_dragonfly_example_rule.py`. To test whether this is working, simply say "hotel" and the rule should translate this to "hotels are not cheap".

## Editing text

- Start with the grammar defined in `_multiedit.py`. 
- In Visual Studio Code, you can set line numbers to "relative", making it easier to go up and down. 



