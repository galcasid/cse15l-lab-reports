# Installing VScode
* The first step to using Java on your computer and remotely connecting for this class is to download VScode. For me, I already have this downloaded, but for those who haven't, you will want to visit [https://code.visualstudio.com/](https://code.visualstudio.com/) and download the correct version depending on the operating system you're using.
![Image](vscodehome.png)
* After downloading, opening up the application, and picking the display of your choice, it should take you to a page that looks like this. Mine is bright because I chose the light mode, but many tend to go for the dark mode. Either way, seeing this page means that you have successfully installed VScode, and can now move onto the next step. 
![Image](vscodescreenshot.png)

# Remotely Connecting
* Trying to remotely connect for the first time was, in my experience, a very lengthy and tiring process that required a lot of patience. Know that following through step by step can still lead to some errors, and that it's ok because it happens to all of us! Just remember to have patience and ask for help if you need it. 
![Image](newTerminal.png)
* Once you do this, a terminal should pop up at the bottom of the screen. In the terminal, type in:
```
ssh cs15lsp23bu@ieng6.ucsd.edu
```
* and press return (but be sure to replace cs15lsp23bu with your own username!)
* For Windows users, before this step, you will need to install git for windows which can be found here: [https://gitforwindows.org/](https://gitforwindows.org/) 
* After pressing enter, you will see a lot of text, but look for where it says (yes/no/[fingerprint])?. If you see this, just like when typing your username into the terminal earlier, you'll want to type in:
```
yes
```
* and then again pressing return.
* Once you see your terminal output the screenshot below (but with your username), you have successfully remotely connected!
![Image](remotelyconnecting.png)

# Trying Some Commands
* So you've successfully opened a terminal and remotely connected, so now it's time to explore and learn some commands!
* You can try typing in: cd, ls, pwd
* log out of the remote server by ctrl d
![Image](testingcommands.png)
