#tar -kxvf topic_labwc_config.tar.gz
cd topic_labwc_config/

cat labwc-install-list.txt 

sudo -v
grep -vP "^#" labwc-install-list.txt | while read LL; do $LL ; done

mkdir ~/.config
mkdir ~/.themes

#this config affords
#ctrl+alt+larrow , ctrl+alt+rarrow to switch desktops
#alt+tab for window list
#alt-F3 to show bemenu; run terminal application "foot" ; run "firefox" 
#defined in autostart: background colour, screen blanking

cp -R  home_config/labwc/ ~/.config/
cp -R  home_themes/zox1/ ~/.themes/

#run labwc
labwc

