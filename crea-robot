#!/bin/bash
# -*- ENCODING: UTF-8 -*-
echo -e "\e[33mEste procedimiento creara un archivo robots.txt con el siguiente texto:\e[39m
User-agent: *
Disallow: /"
#REVISAMOS QUE EL ARCHIVO EXISTA SI: AVISA QUE SE VA A SOBREESCRIBIR / NO:LO ESCRIBE
if [ -f ./robots.txt ];
then
    #AVISAMOS SI REALMETE SE QUIERE SOBREESCRIBIR
    while true; do
        read -r -p "El archivo robots.txt ya existe seguro deseas sobrescribirlo?  Yes or no? " response
        if [[ $response =~ ^([yY][eE][sS]|[yY])$ ]]
        then
            echo "User-agent: *
Disallow: /">robots.txt
            echo -e "\e[33mTu archivo robots.txt se ha sobreescrito\e[39m"
            exit 0
        else
            echo -e "\e[32mTu archivo robots.txt se mantiene como estaba\e[39m"
            exit 0
        fi
    done
else
    echo -e "\e[323mTu archivo robots.txt se ha creado con exito\e[39m"
    echo "User-agent: *
Disallow: /">robots.txt
fi

exit
