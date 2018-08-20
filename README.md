# Installing-Oh-My-Zsh-On-Windows-10
The best way I've found to installing git, ZSH and 'OH My Zsh' on windows 10

1:
First you need to turn developer mode on by going to the following:
setting > update & security > for developers > click to turn 'Developer mode' on

2:
Now you need to turn some features on by going to:
control panel > Programs >  turn windows features on or of > then you need to scroll down to where it says "Windows Substystem for Linux" click to turn it on then press 'OK' then reebot you machine.

3:
Now serach for bash and click enter it should show a message say "Windows Subsystem for linux has no installed distrobutions" or something like that which is fine where about top take care of that

4:
Go to the microsofrt store and search for ubuntu and install it (You may have to login to the store)
Once it's done launch it then create a username and password it can be anything

5:
Now time to update your packages and files. Type the following:

sudo apt update

after that when going to upgrade (this take a while) so type the following:

sudo apt upgrade

6:
Now here comes the fun part... get HYPER.
literally go to: https://hyper.is/ and download the software then open it.

7:
Once hyper is open click on the top right menu then Edit > Preferences

8:
Scroll down to where it says :
"// Bash on Windows
    // - Example: `C:\\Windows\\System32\\bash.exe`
    //
    // PowerShell on Windows
    // - Example: `C:\\WINDOWS\\System32\\WindowsPowerShell\\v1.0\\powershell.exe`
    shell:'',

9:
As you can see the shell is empty it is not defined so between the '' quotation marks paste the following:
C:\\Windows\\System32\\bash.exe

is should look like this:

 shell: `C:\\Windows\\System32\\bash.exe`,

Make sure to save then close the file then restart hyper.

10:
Last stage!

run these 3 commands one by one :

sudo apt-get update

sudo apt-get upgrade

sudo apt-get install curl

sudo apt-get install git

sudo apt-get install zsh

Then run:
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

11:
Now lets set it to our default
Open bash terminal using bash command and use nano ~/.bashrc to open .bashrc config file.

Warning: Do not change Linux files using Windows apps and tools

In start of that file add following command:

bash -c zsh
