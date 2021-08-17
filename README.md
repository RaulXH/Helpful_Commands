# Helpful Commands
<p align="center"><img src="https://camo.githubusercontent.com/c9e94f489280055c51bbe3a177755b34132ba88b34cb949beac1ffc0a1790367/68747470733a2f2f692e696d6775722e636f6d2f384975594c526c2e6a7067" alt="ICON" align="center" border="1" width="800" height="auto"></p>

# _Official website_
```
https://f-droid.org/en/packages/com.termux/
```
![](https://badges.pufler.dev/visits/RaulXH/Helpful_Commands?style=flat-square&logo=Github) ![](https://img.shields.io/github/stars/RaulXH/Helpful_Commands?style=flat-square&logo=Github)  ![](https://img.shields.io/badge/Commads-Termux-blue?style=flat-square&logo=Github)
# root
#
```
pkg install proot 

echo -e 'alias root="proot -w $PWD -0 $BASH"' >> $PREFIX/etc/profile

```
* *_Open a new session_* 
* run: *_root_*
# Password generator
```
pkg install pwgen
```
* _use pwgen --help_
* _Create a function_
```
echo '
GenKey()
{
    A=$(pw``gen -s -C 20 -n10)                                    
    printf "\n\e[7;50;33m You Generate Password\e[0m: \e[0;50;37m$A\n\n\e[0m"                                          
}
' >> ~/.bashrc
source ~/.bashrc
```
* call the function: $~ _GenKey_
* view
![Screenshot_20210516_215725](https://user-images.githubusercontent.com/77165035/118427076-062c9e80-b692-11eb-8eac-7c8a9d72e22a.jpg)
# Backup to the $HOME repositories
* Quick backup of your Termux repositories.  quickly
* For more information: https://wiki.termux.com/wiki/Backing_up_Termux
* be located inside $ HOME
```
cd $HOME
```
* Execute the following command inside a variable:
```
BACKUP=$(ls -l $HOME | awk '/^d/ && !/storage/ {print $NF}' | xargs )
```
* Next step | Save the backup in the INTERNAL MEMORY
```
tar -zcf /sdcard/Backup-Termux.tar.gz $BACKUP
```
* RESTORE the backup created
```
termux-setup-storage
```
```
tar -zxf /sdcard/Backup-termux.tar.gz --recursive-unlink --preserve-permissions

```
# view 
<a href="https://asciinema.org/a/icY1qz37rKbWoLxTQrQ77CX0M" target="_blank"><img src="https://asciinema.org/a/icY1qz37rKbWoLxTQrQ77CX0M.svg" /></a>
* done!  It is easy
# Quick file sharing
```
echo '
transfer()
{
    [[ -z $1 ]] || [[ ! -f $1 ]] && printf "\n[ Error ]\n\n" && return 1;
        curl --progress-bar --upload-file "$1" https://transfer.sh/$(basename "$1") | tee /dev/null; echo
}' >> ~/.bashrc
source ~/.bashrc
```
# View
[![asciicast](https://asciinema.org/a/mCE5fshrrIQ5Swrd9s6QHbm9t.svg)](https://asciinema.org/a/mCE5fshrrIQ5Swrd9s6QHbm9t)
# More will come!
