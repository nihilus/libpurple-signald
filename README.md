# purple-signald-ttl

This is a forked version of the [signald plugin for pidgin (purple-signald)](https://github.com/hoehermann/libpurple-signald). In contrast to the original version, this fork 

* does not require a new registration of the user (i.e. mobil number) but is based on linking to the signal app via QR code and
* starts the underlying [signald daemon](https://git.callpipe.com/finn/signald) by itself

Following software must be installed:

* [signald](https://git.callpipe.com/finn/signald), see its documentation for its installation  
  **Important:** The command `signald` has to available within the program directories listed in the `$PATH` variable.
* *qrencode*, a tool for creating QR codes from strings. On Debian/Ubuntu, just use  
  `sudo apt install qrencode`
* *feh*, a lightweight immage viewer for displaying the QR code for linking. On Debian/Ubuntu, just use  
  `sudo apt install feh`

The plugin in this version is tested on Debian 10 (Buster) but should also run on other linux distros. Windows and MacOS are not supported. Sorry guys, I do not want to support non-free software.


##Original Readme

**This is the original readme file of the signald plugin.**

A libpurple/Pidgin plugin for [signald](https://git.callpipe.com/finn/signald) (signal, formerly textsecure).

signald is written by Finn Herzfeld.

I never wrote code for use in Pidgin before. EionRobb's [purple-discord](https://github.com/EionRobb/purple-discord) sources were of great help. 

Tested on Ubuntu 18.04.

### Known Issues

There have been reports of incoming offline-messages getting lost. As far as I observed, they are not lost but delayed and delivered after a restart of signald.

### Features

* Receive messages
* Send messages
* Receive files
* Receive images
* Send images
* Receive buddy list from server

Note: When signald is being run as a system service, downloaded files may not be accessible directly to the user. Do not forget to add yourself to the `signald` group.

![Instant Message](/instant_message.png?raw=true "Instant Message Screenshot")

### Missing Features

* signald configuration (i.e. initial number registration)
* Synchronizing messages sent from another device
* Deleting buddies from the server
* Updating contact details
* Contact colors
* Expiring messages
* Messages with quotes
* Proper group chats (right now you can send and receive group messages, but you cannot tell which one of the group members is answering)

![Group Chat](/groupchat.png?raw=true "Group Chat Screenshot")

