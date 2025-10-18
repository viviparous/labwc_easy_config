#clone the repository, change to the directory
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
cp -R  home_config/foot/ ~/.config/
cp -R  home_themes/zox1/ ~/.themes/

#run labwc
labwc

#bash_aliases.txt contains the function "dirf" as a wrapper for pushd/popd/dirs
dirf -h: 

0 => list entries (cmdnum)
3 => choose dir (cmdnum)
5 => add curr dir (cmdnum)
7 => add named dir (cmdnum,dir)
9 => switch to dir num (cmdnum,num)


