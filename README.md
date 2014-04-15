getting-started-with-irc
========================

Getting Started with IRC

For now, this lesson is just a README explaining how to get set up with IRC. But later we could make it into a slideshow.

*Documentation in progress.*

What is IRC? Why use it?
========================

IRC stands for [Internet Relay Chat](http://en.wikipedia.org/wiki/Internet_Relay_Chat) which is a type of chat software that is popular in the open source community. Lots of OpenStreetMap users and open source mappers like to use IRC, so it's a great way to keep your finger on the pulse of the open geo community.

Which IRC channels should I follow?
========================

irc://irc.freenode.net/#maptime of course!

Some suggestions:

- irc://irc.oftc.net/osm
- irc://irc.oftc.net/osm-dev
- irc://irc.oftc.net/hot
- irc://irc.oftc.net/osm-us
- irc://irc.oftc.net/osm-ca
- irc://irc.oftc.net/osm-diversity
- irc://irc.oftc.net/publiclab
- irc://irc.freenode.org/openstreetmap
- irc://irc.freenode.org/mapbox
- irc://irc.freenode.org/leaflet
- irc://irc.freenode.org/mapnik
- irc://irc.freenode.org/qgis
- irc://irc.freenode.org/postgis
- irc://irc.freenode.org/osgeo

Connecting to IRC via the web
========================

Normally people use an IRC client to connect to IRC chat rooms. But you want to connect more quickly without a lot of set up, you can use the web for the IRC server you want to connect to. For example: http://webchat.freenode.net/ and http://www.oftc.net/WebChat/


## Mac OSX Clients

### Adium

Download [Adium](https://adium.im/), which is an open source chat client that can connect to IRC (and other chat protocols, such as AIM, Twitter, Windows Messenger, etc).

#### Scripting Adium with AppleScript

If you follow a lot of chat rooms, it's a pain to connect to them all every time you log in. So I use some AppleScript to tell Adium which channels to connect to.

Most of it I stole from here: http://kb.mit.edu/confluence/display/mitcontrib/Configure+Adium+to+automatically+join+Group+Chat+rooms+on+startup

Copy the following scripts to some folder on your computer.

Freenode script `adium-group-chat-freenode.scpt`:

```
	tell application "Adium"
		GetURL "irc://irc.freenode.org/openstreetmap"
		GetURL "irc://irc.freenode.org/mapbox"
		GetURL "irc://irc.freenode.org/leaflet"
		GetURL "irc://irc.freenode.org/mapnik"
		GetURL "irc://irc.freenode.org/qgis"
		GetURL "irc://irc.freenode.org/postgis"
		GetURL "irc://irc.freenode.org/cugos"
		GetURL "irc://irc.freenode.org/osgeo"
		GetURL "irc://irc.freenode.org/maptime"
	end tell
```

oftc script `adium-group-chat-oftc.scpt`:

```
	tell application "Adium"
		GetURL "irc://irc.oftc.net/osm"
		GetURL "irc://irc.oftc.net/osm-dev"
		GetURL "irc://irc.oftc.net/hot"
		GetURL "irc://irc.oftc.net/osm-us"
		GetURL "irc://irc.oftc.net/osm-ca"
		GetURL "irc://irc.oftc.net/osm-diversity"
		GetURL "irc://irc.oftc.net/publiclab"
	end tell

```

Script to call the other scripts `adium-group-chat.scpt`:

```

run script ("/Users/alan/Dropbox/bin/adium-group-chat-freenode.scpt" as POSIX file)
run script ("/Users/alan/Dropbox/bin/adium-group-chat-oftc.scpt" as POSIX file)

```

(Replace the path with the path to wherever you save those scripts).

Finally, in _Adium > Preferences... > Events_, go to the "You Connect" event, add the action "Run an AppleScript" and Browse for the location of `adium-group-chat.scpt`.

### Limechat

Limechat is a free IRC client for Mac OSX. It allows you to connect to multiple servers and automatically join channels on startup.

http://limechat.net/mac/

### Textual

Textual is a paid IRC client for Mac OSX (it also has a free trial version). It's very similiar to Limechat but has more features and is still being actively updated and maintained.

http://www.codeux.com/textual/


Registering your username on IRC hosts
===================
This is important. Some info to start with here: http://freenode.net/faq.shtml#userregistration
