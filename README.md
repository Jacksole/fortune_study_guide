# fortune_study_guide
Use fortune, lolcat, and custom strfiles for adhoc learning.

## Getting Started
### Mac Instructions
1. Install fortune using Homebrew.  [https://en.wikipedia.org/wiki/Fortune_(Unix)](https://en.wikipedia.org/wiki/Fortune_(Unix))
```console
$ brew install fortune
```
1. Install lolcat using Homebrew.  This is not needed but I appreciate the eye catching color to draw my attention when the terminal opens up.  [https://github.com/busyloop/lolcat](https://github.com/busyloop/lolcat) 
```console
$ brew install lolcat
```
1. Install cowsay using Homebrew.  This also isn't needed but I wanted to the parts to visually catch my eye.[https://github.com/tnalpgge/rank-amateur-cowsay](https://github.com/tnalpgge/rank-amateur-cowsay)
```console
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
$ cp SY0_501.fortune ~/.fortune/
$ strfile ~/.fortune/SY0_501.fortune
```

## Testing
TODO - Screenshot
```console
$ fortune ~/.fortune/SY0_501.fortune | cowsay -f $(shuf -n 1 -e $(cowsay -l | tail -n +2)) | lolcat
```

## Profile Setup
TODO - Non-bash instructions?
```console
$ cp ~/.bash_profile ~/.bash_profile.backup.$$
$ echo 'fortune ~/.fortune/SY0_501.fortune | cowsay -f $(shuf -n 1 -e $(cowsay -l | tail -n +2)) | lolcat' >> ~/.bash_profile
```

Now everytime you fire up a terminal you should have some random keyword to memorize for the SY0-501 test.  As I add new fortunes I'll update it here.

