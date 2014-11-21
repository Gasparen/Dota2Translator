![Dota 2 Translator](http://i.imgur.com/9yz2hyY.png)

## Introduction

This is my try at getting Dota 2 Translator(https://github.com/patriksletmo/Dota2Translator) to work on my system (linux 17 qiana). As of now it works by intercepting the networktraffic, just like the original, quering google translate for a translation and printing that to a console (so it's nowhere close to beeing as flashy as the original as of now). 

## Building From Source

Loads of dependencies at the moment and I havn't tried to make this portable yet so here's the installation sequence:

1. Install libpcap:
   apt-get install flex
   apt-get install bison
   apt-get install libpcap-dev
   
   At this point the ldev.c test should be able to compile (gcc -ldev.c -lpcap)

2. Install [pylibpcap](http://sourceforge.net/projects/pylibpcap/):
   Download, unpack and install with "python ./setup.py install"

3. Now main.py should be runnable

## Notes
Root access is needed during installation (duh) and run the program, otherwise you won't be able to grap packages.

The program needs to be started from a console (as the translations are written there), so dual monitors is quite needed at the moment.