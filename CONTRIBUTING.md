# Contributing to the unofficial CurseForgeBadge
Thank you for investing your time in contributing to our project! Changes you make here will be reflected on [cf.way2muchnoise.eu](https://cf.way2muchnoise.eu/).

<br />

## Table of Contents
### [Getting started](#Getting-started)
#### &ensp; [Getting an API key from CurseForge](#Getting-an-API-key-from-CurseForge)
### [Setting up the development environment](#Setting-up-the-development-environment)
#### &ensp; [Python](#Python)
#### &ensp; [Setting your environment variables](#Setting-your-environment-variables)
### [Running CurseForgeBadge](#Running-CurseForgeBadge)
### [Ok, I set up my workspace! Now what?](#Ok%2C-I-set-up-my-workspace%21-Now-what%3F)

<br />

## Getting started

### Getting an API key from CurseForge
In order to get started you'll need to create an account and [generate a key](https://console.curseforge.com/) to use CurseForge's API services.
CurseForgeBadge uses this to poll information about mods and users from the official website.

You can create an account and get a key here: https://console.curseforge.com/

![CurseForge Console](https://user-images.githubusercontent.com/19243263/202071016-c7a6bed7-bc32-4c0e-a056-28e6b582ad61.png)

<br />

### Setting up the development environment

#### Python
You'll need the latest release of Python installed in order to run CurseForgeBadge. You can get it here: https://www.python.org/downloads/

Once Python is installed, open up the command console and type `pip install` for each dependency listed in [requirements.txt](./requirements.txt).
For instance, flask would be installed by typing `pip install flask` and pressing enter.

#### Setting your environment variables
In order for CurseForgeBadge to use your CurseForge account info you'll have to set some environment variables.
This is different depending on the operating system you're using. If you know how to set environment variables already then you may opt to set them with your preferred method instead.

#### Windows
On the console type `setx CURSEFORGE_API_USER USERNAME`, replacing `USERNAME` with your display name for [console.curseforge.com](https://console.curseforge.com/).

Next type in `setx CURSEFORGE_API_KEY KEY`, replacing `KEY` with the key you generated on [console.curseforge.com](https://console.curseforge.com/).

IMPORTANT: If you are using PowerShell, insert a backtick character ( \` ) in front of every $ character in the key. A key of `$b$30$4LotsOfNumbers` would be set with the command ``setx CURSEFORGE_API_KEY `$b`$30`$4LotsOfNumbers``.
If you do not do this then it will save incorrectly and not work!

![PowerShell Env Vars](https://user-images.githubusercontent.com/19243263/202071217-028456b6-3e5c-4d48-b8e5-6d02375b0e7d.png)

#### MacOS
Open `~/.bash_profile` or `/etc/bashrc` with your favorite text editor.
The latter file will affect all users and will require administrative privileges whereas the former file will only affect your account, but not require administrative privileges. If those files don't exist then you can also try editing `~/.bash_login`, `~/.profile`, or `/etc/profile`.

Add the lines `export CURSEFORGE_API_USER="USERNAME"` and `export CURSEFORGE_API_KEY="KEY"` to your file, replacing `USERNAME` with your CurseForge display name and `KEY` with the key you generated on [console.curseforge.com](https://console.curseforge.com/).

Restart any terminals you have open so the changes can take effect.

#### Linux
Open `.bashrc` or `/etc/environment` with your favorite text editor.
The latter file will affect all users and will require administrative privileges whereas the former file will only affect your account, but not require administrative privileges.

Add the lines `export CURSEFORGE_API_USER="USERNAME"` and `export CURSEFORGE_API_KEY="KEY"` to your file, replacing `USERNAME` with your CurseForge display name and `KEY` with the key you generated on [console.curseforge.com](https://console.curseforge.com/).

Restart any terminals you have open so the changes can take effect.

<br />

## Running CurseForgeBadge
Clone the project to a folder of your choice and then open it up. Once you're there you may double-click `CurseForgeBadge.py` to run the server locally or run it on the command line with `python CurseForgeBadge.py`.
The server will be hosted on all available IPs on your computer. You can check if it is working by navigating to `localhost/jei.svg` on your browser.
If you get a 500 error then you likely gave the wrong authentication information or the environment variables were saved incorrectly.

![CurseForgeBadge Runtime](https://user-images.githubusercontent.com/19243263/202071157-d360ac5b-6a98-43a4-8c5d-54f687c62442.png)

<br />

## Ok, I set up my workspace! Now what?
You can change the code and see what it does! You can also check out the github [issues](https://github.com/way2muchnoise/CurseForgeBadge-Unofficial/issues) to get inspiration,
and once your code is to your liking you may submit a [pull request](https://github.com/way2muchnoise/CurseForgeBadge-Unofficial/pulls) to have it reviewed to be added to the server.
