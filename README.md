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
* Execute the following command inside a variable:
```
BACKUP=$(ls -l $HOME | awk '/^d/ && !/storage/ {print $NF}' | xargs )
```
* Next step | Save the backup in the INTERNAL MEMORY
```
tar -zcf /sdcard/Backup-Termux.tar.gz $BACKUP
```
* restore the backup created
```
tar -zxf /sdcard/Backup-termux.tar.gz --recursive-unlink --preserve-permissions
```
* done!  It is easy
# More will come!
