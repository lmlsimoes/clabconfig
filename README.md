# clabconfig

install using: 
sudo docker run --rm -v $(pwd):/workspace ghcr.io/oras-project/oras:v0.12.0 pull ghcr.io/lmlsimoes/clabconfig:latest


clabconfig.run is a program to help setup containerlab topologies using srlinux (made in dart by an amateur in its free time 😊). Please expect to find some errors in the program execution as I didn’t test all corner cases… 

The idea is for a University student or anyone without much knowledge on Containerlab and SRLinux to be able to jump start with a working setup of a leaf and spine SRLinux virtual deployment, and work their way back.

It provides the possibility to create a leaf/spine topology file automatically, editing a json formatted file which you can export by running “clabconfig.run -e appsettings.json”. The file name “appsettings.json” is just an example. You can use whatever filename you choose. If existing the program will ask you if you want to overwrite it.  
After updating the appsettings.json file with your personalized parameters, you can import it by running “clabconfig.run -i appsettings.json”.

You also have an automatic mode which runs the program with the default parameters. To do so, just run “containerlab.run -a” (which basically is the same as running “containerlab.run -e appsettings.json -i appsettings.json”. It will generate a folder with a topology file with a baseline configuration and an updated topology file with all the options by default, including the configuration files for the automatically generated topology, launch, test and destroy scripts, topology tree representations, etc.
Have fun and if you have some ideas for improvement, please share. 
