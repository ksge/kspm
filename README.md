# kspm
Kiss Strip Poker Maker
a step by step tool to realize your own strip poker game!

this project is discontinued and included into kiss strip poker https://github.com/ksge/ksp

what you need: 

- windows => 10 or debian => 10, a good text editor such as geany https://www.geany.org/ and of course Kiss Strip Poker Maker archive.

- if you are using debian install: 
	sudo apt install -y gcc libncurses-dev libgpm-dev libx11-dev libxext-dev libxpm-dev libxrandr-dev libxrender-dev libgl1-mesa-dev libffi-dev libtinfo5 libvlc-dev vlc
	sudo apt install python3-pip
	pip install pygame
	pip install pyinstaller
	sudo apt install python3-tk

- if you are using windows:
	install python (tested version: 3.9) from https://www.python.org/
	upgrade pip from a windows prompt: C:\Users\*\AppData\Local\Programs\Python\Python39\python.exe -m pip install --upgrade pip
	install pygame from a windows prompt: C:\Users\*\AppData\Local\Programs\Python\Python39\Scripts\pip.exe install pygame
	install pyinstaller from a windows prompt: C:\Users\*\AppData\Local\Programs\Python\Python39\Scripts\pip.exe install pyinstaller
	

1- unpack Kiss Strip Poker Maker archive

2- create clips (.mkv), name in the right way and copy all inside the core folder, check https://github.com/ksge/ksge for more informations on about how to name clips

3- fill in the signature-settings.txt file. very important: keep it carefully as it contains the key you will use to encrypt the videos and more. tip: if your game is not intended for monetization just set the C6 varibale (number of demo stages) = to number of total stages. otherwise set the right setting and have also care to set the variables intended for monetization

4- copy and paste in the right location the code of signature-settings.txt into kspc.bas and ksge-utils.bas

5- run compile-kspc-ksge-utils-runme.bat (.sh if you are using linux)

6- run the just compiled ksge-utils and launch option 9- count clips to check that clips are named without errors, correct any errors if necessary

7- use again ksge-utils to encrypt you clips with option 1- video file encrypter

8- use again ksge-utils, now with option 6- generate single md5sum hash of encrypted *.cpt clips files and kspc ; copy and paste the two md5sum inside signature-settings.txt (shash = ... , kspca = ....) and then inside ksge.bas

9- run compile-ksge.bat (.sh if you are using linux)

10- edit pokerview.py and pokermodel.py filling the right model name and stages (must be equal to signature-settings pay attention to capital letters)

11- edit compile-py and fill it for your environment (user name and python version) and then run it

11- if you want you can personalize song.ogg, graphics and message inside poker-end.py. You can also add a readme/credits txt file of course

12- copy runme.exe (runme if on linux) inside game folder, if you want you can rename runme with model name or what you want

13- try your game

14- if you want to distribute it simply create a zip file with all the game folder, if you want to monetize, have care to remove source codes (.bas , .py), ksge-utils binary and of course key.cpt. if you want to monetazie don't forget to set C6 varibale (number of demo stages)


--------------------------------------------------------------
how monetization works?
end user can use the automatic integrated bitcoin payment (beta) or contact directly the game maker using mail for manual procedure.
you can also use ksge-utils option 41- activation file generation 4 no hw limits to send the key.cpt file to the user.  
