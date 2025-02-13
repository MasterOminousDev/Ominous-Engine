

![Ominous Engine Logo](OminousEngineLogo.png)


## Kade Engine Stuff (Not for Ominous Engine)

[![AppVeyor](https://img.shields.io/appveyor/build/KadeDev/Kade-Engine-Windows?label=windows%20build)](https://ci.appveyor.com/project/KadeDev/kade-engine-windows/branch/master/artifacts) [![AppVeyor](https://img.shields.io/appveyor/build/KadeDev/Kade-Engine-Macos?label=macOS%20build)](https://ci.appveyor.com/project/KadeDev/kade-engine-macos/branch/master/artifacts)  [![AppVeyor](https://img.shields.io/appveyor/build/KadeDev/Kade-Engine-Linux?label=linux%20build)](https://ci.appveyor.com/project/KadeDev/kade-engine-linux/branch/master/artifacts) [![AppVeyor](https://img.shields.io/appveyor/build/daniel11420/KadeEngineWeb?label=html5&20build)](https://ci.appveyor.com/project/daniel11420/KadeEngineWeb) [![Discord](https://img.shields.io/discord/808039740464300104?label=discord)](https://discord.gg/MG6GQFh52U) [![GitHub issues](https://img.shields.io/github/issues/KadeDev/Kade-Engine)](https://github.com/KadeDev/Kade-Engine/issues) [![GitHub pull requests](https://img.shields.io/github/issues-pr/KadeDev/Kade-Engine)](https://github.com/KadeDev/Kade-Engine/pulls) []() []()

![GitHub commits since latest release (by date)](https://img.shields.io/github/commits-since/KadeDev/Kade-Engine/latest) ![GitHub repo size](https://img.shields.io/github/repo-size/KadeDev/Kade-Engine) ![Lines of code](https://img.shields.io/tokei/lines/github/KadeDev/Kade-Engine) ![Supported platforms](https://img.shields.io/badge/supported%20platforms-windows%2C%20macOS%2C%20linux%2C%20html5-blue) ![GitHub all releases](https://img.shields.io/github/downloads/KadeDev/Kade-Engine/total) ![GitHub](https://img.shields.io/github/license/KadeDev/Kade-Engine) ![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/KadeDev/Kade-Engine?include_prereleases&label=latest%20version) 

## Engine Information

### If you want to contribute Ominous Engine read [this](https://github.com/MasterOminousDev/Ominous-Engine/blob/stable/CONTRIBUTING.md) first.
### If you want to build Ominous Engine read [this](https://github.com/MasterOminousDev/Ominous-Engine/blob/stable/docs/building.md) or continue reading


# Friday Night Funkin'

This is the repository for Friday Night Funkin: Ominous Engine, a reworked engine made for a game originally made for Ludum Dare 47 "Stuck In a Loop".

Play the Ludum Dare prototype here: https://ninja-muffin24.itch.io/friday-night-funkin
Play the Newgrounds one here: https://www.newgrounds.com/portal/view/770371
Support the project on the itch.io page: https://ninja-muffin24.itch.io/funkin

IF YOU MAKE A MOD AND DISTRIBUTE A MODIFIED / RECOMPILED VERSION, YOU MUST OPEN SOURCE YOUR MOD AS WELL

## Ominous Engine

Always remember that this is a **mod** for FNF. You can call it a **engine** though i don't really mind.


## Credits / shoutouts

- [ninjamuffin99](https://twitter.com/ninja_muffin99) - Programmer for FNF
- [PhantomArcade3K](https://twitter.com/phantomarcade3k) and [Evilsk8r](https://twitter.com/evilsk8r) - Art for FNF
- [Kawaisprite](https://twitter.com/kawaisprite) - Musician for FNF
- [KadeDev](https://github.com/KadeDev) - code (that i borrowed for the first update)
- [MasterOminousDev (me!)](https://github.com/MasterOminousDev) - the idiot that made the engine (I made everything) (especially i added a code)

This game was made with love to Newgrounds and its community.

## Build instructions

THESE INSTRUCTIONS ARE FOR COMPILING THE GAME'S SOURCE CODE!!!

IF YOU WANT TO JUST DOWNLOAD AND INSTALL AND PLAY FNF OR OMINOUS ENGINE NORMALLY, GO TO ITCH.IO TO DOWNLOAD THE GAME FOR PC, MAC, AND LINUX!!

https://ninja-muffin24.itch.io/funkin
https://ominousdeveloper.itch.io/funkin (In-development)

IF YOU WANT TO COMPILE THE GAME YOURSELF, READ `building.md` OR CONTINUE READING!!!

### Installing the Required Programs

First, you need to install Haxe and HaxeFlixel. I'm still working on the engine but too lazy to write and keep updated with that setup (which is pretty simple). 
1. [Install Haxe 4.1.5](https://haxe.org/download/version/4.1.5/) (Download 4.1.5 instead of 4.2.0 because 4.2.0 is broken and is not working with gits properly...)
2. [Install HaxeFlixel](https://haxeflixel.com/documentation/install-haxeflixel/) after downloading Haxe

Other installations you'd need are the additional libraries, a fully updated list will be in `Project.xml` in the project root. Currently, these are all of the things you need to install:
```
flixel
flixel-addons
flixel-ui
hscript
newgrounds
```
So for each of those type `haxelib install [library]` so for example `haxelib install newgrounds`

You'll also need to install a couple things that involve Gits. To do this, you need to do a few things first.
1. Download [git-scm](https://git-scm.com/downloads). Works for Windows, Mac, and Linux, just select your build.
2. Follow instructions to install the application properly.
3. Run `haxelib git polymod https://github.com/MasterOminousDev/polymod.git` to install Polymod.
4. Run `haxelib git discord_rpc https://github.com/MasterOminousDev/linc_discord-rpc` to install Discord RPC.

You should have everything ready for compiling the game! Follow the guide below to continue!

At the moment, you can optionally fix the transition bug in songs with zoomed-out cameras.
- Run `haxelib git flixel-addons https://github.com/MasterOminousDev/flixel-addons` in the terminal/command-prompt.



### Compiling game
NOTE: If you see any messages relating to deprecated packages, ignore them. They're just warnings that don't affect compiling

Once you have all those installed, it's pretty easy to compile the game. You just need to run `lime test html5 -debug` in the root of the project to build and run the HTML5 version. (command prompt navigation guide can be found here: [https://ninjamuffin99.newgrounds.com/news/post/1090480](https://ninjamuffin99.newgrounds.com/news/post/1090480))
To run it from your desktop (Windows, Mac, Linux) it can be a bit more involved. For Linux, you only need to open a terminal in the project directory and run `lime test linux -debug` and then run the executable file in export/release/linux/bin. For Windows, you need to install Visual Studio Community 2019. While installing VSC, don't click on any of the options to install workloads. Instead, go to the individual components tab and choose the following:

* MSVC v142 - VS 2019 C++ x64/x86 build tools
* Windows SDK (10.0.17763.0)

Once that is done you can open up a command line in the project's directory and run `lime test windows -debug`. Once that command finishes (it takes forever even on a higher end PC), you can run FNF from the .exe file under export\release\windows\bin
As for Mac, 'lime test mac -debug' should work, if not the internet surely has a guide on how to compile Haxe stuff for Mac.

### Additional guides

- [Command line basics](https://ninjamuffin99.newgrounds.com/news/post/1090480)

### Important Information

Check the docs folder for information

Read `building.md` to compile, it has all the information that you need for compiling the game, and more!



### Play the game on android

For Ominous Engine on android, go to the `android` branch 

I know that the original fnf android code will pop up, that's because i will start doing android port when I finish PC Port

















