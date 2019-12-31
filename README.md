# fortune_study_guide
Use fortune, lolcat, and custom strfiles for adhoc learning.

## Getting Started
### Mac Instructions
Install fortune, lolcat, and cowsay using Homebrew.  Only fortune is needed but the asthetics of having Lolcat and Cowsay make it better.
*  [https://en.wikipedia.org/wiki/Fortune_(Unix)](https://en.wikipedia.org/wiki/Fortune_(Unix))
*  [https://github.com/busyloop/lolcat](https://github.com/busyloop/lolcat)
*  [https://github.com/tnalpgge/rank-amateur-cowsay](https://github.com/tnalpgge/rank-amateur-cowsay)
```console
$ brew install fortune
$ brew install lolcat
$ brew install cowsay
```
### Linux Instructions
TODO - I need to take the time to document it but you should be able to piece together what you need from the Mac instructions.


## Fortune Files
### Creation
Here is a rough explanation of how to create a custom file and then the dat file from it.  [http://bradthemad.org/tech/notes/fortune_makefile.php](http://bradthemad.org/tech/notes/fortune_makefile.php)  
TODO - First one was a collection from random googling and flashcard sites.  
TODO - For right now I'm just giving a crap about the Security+ fortune file.  In time I'll need to add other fortune files.
### Installation Of Fortune File
I install them locally to ~/.fortune since the intention is to have specific cert ones for focus.  You could install this wherever you want, you just need to remember that for the .bash_profile step.
```console
$ mkdir ~/.fortune
$ cp ./study_guides/SY0_501.fortune ~/.fortune/
$ strfile ~/.fortune/SY0_501.fortune
```


## Testing
![Screenshot](/images/screenshot.png)
```console
$ fortune ~/.fortune/SY0_501.fortune | cowsay -f $(shuf -n 1 -e $(cowsay -l | tail -n +2)) | lolcat
```


## Profile Setup
TODO - Non-bash instructions?
```console
$ cp ~/.bash_profile ~/.bash_profile.backup.$$
$ echo 'fortune ~/.fortune/SY0_501.fortune | cowsay -f $(shuf -n 1 -e $(cowsay -l | tail -n +2)) | lolcat' >> ~/.bash_profile
```

