#!/bin/bash
echo "Vvedite chislo ot kotorogo poshitat` factorial"
read counter
factorial=1
if [ $counter -lt 0 ]       
then
    echo "Vvedite polojitel`noe chislo ili nol`"
else
    while [ $counter -gt 0 ] # 
    do
        factorial=$(($factorial*$counter))
        counter=$(($counter - 1))
    done
    echo $factorial
fi
exit 0
