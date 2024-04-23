[![Build Status](https://gitlab.gnome.org/GNOME/gnome-control-center/badges/main/pipeline.svg)](https://gitlab.gnome.org/GNOME/gnome-control-center/pipelines)
[![Coverage report](https://gitlab.gnome.org/GNOME/gnome-control-center/badges/main/coverage.svg)](https://gnome.pages.gitlab.gnome.org/gnome-control-center/)
[![License](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://gitlab.gnome.org/GNOME/gnome-control-center/blob/main/COPYING)

GNOME Settings
====================

GNOME Settings is GNOME's main interface for configuration of various aspects of your desktop.

If you are looking for usage tips and instructions, you can find it at the [User Documentation](https://help.gnome.org/users/gnome-help/stable/prefs.html) (translated in various languages).

## Reporting Issues

Before reporting any bugs or opening feature requests, [read the communication guidelines](https://gitlab.gnome.org/GNOME/gnome-control-center/blob/main/docs/CODE_OF_CONDUCT.md#communication-guidelines).

Report issues to the [GNOME issue tracking system](https://gitlab.gnome.org/GNOME/gnome-control-center/issues).

## Feature Requests

For feature requests or conceptual changes, please start a topic on [GNOME Discourse](https://discourse.gnome.org/tags/settings).

## Contributing

See [`docs/CONTRIBUTING.md`](docs/CONTRIBUTING.md) for details on the contribution process, and [`docs/CODING_STYLE.md`](docs/CODING_STYLE.md)
for the coding style guidelines.

Visit the [Settings development wiki](https://gitlab.gnome.org/GNOME/gnome-control-center/-/wikis/home) for more information.


## Setup gnome-control-center			
            
*Prerequisite:	<br />	
Ubuntu 23.10 (Mantic Minotaur) is installed			
            
*Setup development environment:		<br />	
1.) Extract/Clone the code repo from the following link:	<br />		
https://github.com/Josef-Ouano/gnome-control-center/042324_gnomeSetup		
            
2.) Setup the environment			<br />	
*Change directory		<br />		
cd gnome-control-center			
            
*Extract APN_Gnome45_Setup.zip		<br />	
unzip  APN_Gnome45_Setup.zip			
            
*Copy subprojects folder to		<br />	
cd APN_Gnome45_Setup			<br />	
cp -rvf subprojects ..<br />				
            
*Install dependencies:			<br />	
Run update and upgrade on Ubuntu first:		<br />	
sudo apt-get update && apt-get upgrade			
            
a.) Run the gnome dependecny install script gnome45_dep_install.sh	<br />			
sudo bash ./gnome45_dep_install.sh			
            
b.) You can also install the dependencies manually			<br />	
sudo apt install meson build-essential -y &&			<br />	
sudo apt install libpulse-dev -y &&			<br />	
sudo apt install libglib2.0-dev -y &&		<br />	
sudo apt install cmake -y &&			<br />	
sudo apt install libxkbcommon-dev -y &&	<br />			
sudo apt install libcairo2-dev -y &&	<br />			
sudo apt-get install -y libxml2-dev -y &&<br />			
sudo apt-get install libwayland-bin -y &&<br />				
sudo apt-get install libxrandr-dev -y &&<br />				
sudo apt-get install libxi-dev -y &&	<br />			
sudo apt-get install libxcursor-dev -y &&<br />				
sudo apt-get install libxdamage-dev -y &&<br />				
sudo apt-get install libxinerama-dev -y &&<br />				
sudo apt-get install python3-dev -y &&		<br />		
sudo apt-get install flex -y &&			<br />	
sudo apt-get install bison -y &&		<br />		
sudo apt-get install gettext -y &&		<br />	
sudo apt install libcurl4-openssl-dev -y &&<br />				
sudo apt-get install libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio -y &&			<br />	
sudo apt install libyaml-dev -y &&		<br />		
sudo apt-get install libstemmer-dev -y &&<br />				
sudo apt-get install itstool -y &&		<br />		
sudo apt-get install xsltproc -y &&		<br />		
sudo apt-get install libaccountsservice-dev -y &&		<br />		
sudo apt-get install libcolord-dev -y &&			<br />	
sudo apt-get install libgnome-desktop-4-dev -y &&		<br />		
sudo apt-get install libgnome-bg-4-dev -y &&		<br />		
sudo apt-get install libgnome-rr-4-dev -y &&		<br />		
sudo apt-get install -y gnome-settings-daemon-dev -y &&		<br />		
sudo apt-get install libgoa-1.0-dev -y &&			<br />	
sudo apt-get install libupower-glib-dev -y &&		<br />		
sudo apt-get install libgcr-3-dev -y &&			<br />	
sudo apt-get install libpwquality-dev -y &&			<br />	
sudo apt-get install libcups2-dev -y &&			<br />	
sudo apt-get install libibus-1.0-dev -y &&		<br />		
sudo apt-get install libmm-glib-dev -y &&		<br />		
sudo apt-get install libnm-dev -y &&			<br />	
sudo apt-get install libnma-gtk4-dev -y &&			<br />	
sudo apt-get install libgnome-bluetooth-ui-3.0-dev -y &&	<br />			
sudo apt-get install libwacom-dev -y &&			<br />	
sudo apt-get install libcolord-gtk4-dev -y &&			<br />	
sudo apt-get install libudisks2-dev -y &&			<br />	
sudo apt-get install libgtop2-dev -y &&			<br />	
sudo apt-get install libgoa-backend-1.0-dev -y &&	<br />			
sudo apt-get install libsmbclient-dev -y &&		<br />		
sudo apt-get install libsecret-1-dev -y &&		<br />		
sudo apt-get install gnutls-bin -y &&			<br />	
sudo apt-get install gnutls-dev -y &&			<br />	
sudo apt-get install libgsound-dev -y &&		<br />		
sudo apt-get install libkrb5-dev -y &&			<br />	
sudo apt-get install gperf -y &&			<br />	
sudo apt-get install libjson-glib-dev -y &&		<br />		
sudo apt-get install libsoup-3.0-dev &&			
            
*Setup build directory		<br />		
meson setup builddir			
            
3.) Build the project & install		<br />		
sudo ninja -C builddir			<br />	
sudo ninja -C builddir install			
            
4.) Test project			<br />	
(If editing an existing APN) Go to Settings-> Mobile Network-> Access Point Names-> Click on the "gear" icon in APN item selected	<br />			
(If Adding an existing APN) Go to Settings-> Mobile Network-> Access Point Names-> Click on "+" icon to add APN			<br />	
An APN dialog box will appear. Please refer to pic below.			
		
