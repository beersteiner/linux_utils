#!/bin/bash

# script to open terminals in a variety of common configurations
# 1=top left, 2=top right, 3=bottom left, 4=bottom right
# 12=top wide, 24=right tall, etc. (14 or 23 are invalid!)
# usefule command: xwininfo -id $(xprop -root | awk '/_NET_ACTIVE_WINDOW\(WINDOW\)/{print $NF}')

W=100
WW=203
H=28
HH=59
L=70
R=190
T=30
B=90

for w in "$@"
do
    case "$w" in
        1)
            gnome-terminal --geometry "$W"x"$H"+"$L"+"$T"
            ;;
        2)
            gnome-terminal --geometry "$W"x"$H"-"$R"+"$T"
            ;;
        3)
            gnome-terminal --geometry "$W"x"$H"+"$L"-"$B"
            ;;
        4)
            gnome-terminal --geometry "$W"x"$H"-"$R"-"$B"
            ;;
        12)
            gnome-terminal --geometry "$WW"x"$H"+"$L"+"$T"
            ;;
        13)
            gnome-terminal --geometry "$W"x"$HH"+"$L"+"$T"
            ;;
        24)
            gnome-terminal --geometry "$W"x"$HH"-"$R"+"$T"
            ;;
        34)
            gnome-terminal --geometry "$WW"x"$H"+"$L"-"$B"
            ;;
        1234)
            gnome-terminal --geometry "$WW"x"$HH"+"$L"+"$T"
            ;;
        *)
            echo 'Configuration "$w" not valid!'
            ;;
        esac
done
