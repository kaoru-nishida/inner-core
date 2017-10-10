# INNER CORE (1.0.1.3 BETA) 

Inner Core is a full-fledged development environment for mods and games with them, giving opportunities that are as close to a modem as possible, and far exceeding everything that was before. 

This project is designed to breathe life into the dying generation of mods on MCPE, improve them and give rise to new ones. I sincerely hope that this will happen. 


Here are the main advantages: 

- Inner Core is separate from MCPE completely independent application containing its own MCPE, which allows not only to not put any additional software, but also not to delete the version of MCPE from which you play. Even worlds with mods are stored separately from vanilla worlds.

- The mods under Inner Core are fully compatible and will not conflict, the API is built in such a way that it is very easy to make mods interact with each other. This allows you to create complex assemblies of dozens of mods. 

- It's extremely easy to transfer the mods from the old Core Engine because CE has been saved as the main kind of API for mods under Inner Core, which will result in a rapid transfer of developing mods. 

- The API kernel written in c ++ and java, multithreading, adapting API for frequent mod needs, as well as the ability to compile mods in java-bytecode allows to reach new heights in speed.

- New features in all areas, especially in the graphical component of mods, which now allows you to create any desired appearance of in-game objects. The old API modules were also greatly improved and new ones were introduced, but due to the stable version API will develop much faster. 

- The GUI API makes it incredibly easy to create any required interface, including its main feature is the simple creation of a dynamic interface that works in stable 40-60 fps.

- A complex and variable structure of mods, an assembly file, several kinds of APIs and types of executable files will allow creating the most convenient structure for mods, which plays an important role. Own development environment, adapted for Inner Core allows you to develop a fashion from a PC and download and run them via USB. 

Inner Core is a complete replacement for BlockLauncher, which for a long time existed as the only modding option and was extremely poorly implemented and had an awfully inconvenient API, which entailed many unpleasant consequences. Now this is the end. 


## CHANGELOG: 
Other fixes: 
- Fixed some recipe and icon in the workbench, fixed a bug where sometimes it was impossible to select a specific recipe.
- Fixed a bug due to which the vanilla tools did not break. 
- Fixed no damage and effects from tools and weapons that are added by mods. 
- Fixed API ArmorRegistry module. 
- The MobRegistry module is still poorly debugged and it is not advisable to use it. 
- Fixed a lot of non-working API methods, added those that were forgotten, but existed, new ones were introduced. 
- Optimized the spawn of particles, corrected the flight when spawning a large number of particles from the flow. Added a method that allows you to create particles at any distance from the player. 

## Fix flights and stability:
- Fixed a bug causing random flights in the world, but not the fact that it caused you departures and they will be lost. Also, this fix should remove friezes and slightly stabilize the work. 
- Fixed bug, sometimes causing a crash when creating animations (models). 
- Fixed a bug that probably could crash immediately after launch. 
- Now when you crash due to unsuccessful loading of native code, the error will be written to the log. 
- The pocket style of the interface is forced, because The classic for many evoked departures. 
- Fixed crash when breaking a custom block without the drop function in the survival. 

## INSTALLATION: 
1. Read the system requirements and warning.
2. Download (attached file) and install the application (for installation, rename it to the .apk extension, it is not necessary to delete MCPE) 
3. If desired, perform a test run without mods. 

To install the mods, you need to unpack the archive with the mod in the games / com.mojang / mods folder, the subsequent launch of Inner Core will immediately load this mod. The old mods under Core Engine that are in the same folder are ignored. 

## SYSTEM REQUIREMENTS: 
Inner Core requires the architecture of the processor armv7 and Android not lower than 4.4.2, it also requires at least 300MB of free space on the card and 200MB of RAM. This is the vast majority of Android devices, but there are units that do not meet these requirements, to which I offer my deepest apologies. 

## A WARNING:
This is a beta version of this product, although it passed a 2-week PTA (Closed Beta Test) on devices with completely different characteristics and versions of the system, and stability was achieved at all, bugs will be and this is fact, because the project is huge. Read more about this here - https://vk.com/wall-129680450_4068 

## DOCUMENTATION: 
I will try not to repeat past mistakes and in the near future I will be working on documentation, not new features that only increase the number of files 6?
