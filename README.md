# Helpful Commands
<p align="center"><img src="https://camo.githubusercontent.com/c9e94f489280055c51bbe3a177755b34132ba88b34cb949beac1ffc0a1790367/68747470733a2f2f692e696d6775722e636f6d2f384975594c526c2e6a7067" alt="ICON" align="center" border="1" width="800" height="auto"></p>

![](https://badges.pufler.dev/visits/RaulXH/Helpful_Commands) ![](https://img.shields.io/github/RaulXH/Helpful_Commands)
# root
#
```
pkg install proot 

echo -e 'alias root="proot -0 -$PWD ~ $BASH"' >> $PREFIX/etc/profile

```
* *_Open a new session_* 
* Execute: *_root_*
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
# More will come!
