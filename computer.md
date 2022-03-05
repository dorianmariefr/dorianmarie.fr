---
title: How I Use My Computer
layout: default
indexed: true
---

<a href="/img/menubar.png"><img src="/img/menubar.png" alt="Menu bar" /></a>

## Menu bar

### Apple icon

<a href="/img/menubar/apple.png"><img src="/img/menubar/apple.png" alt="Apple icon" /></a>

I use a Macbook Air as my personal laptop, with macOS.

I could remove this icon by hiding the menu bar for instance but it's
important, it lets me access my system information, my storage space,
all all the settings mainly.

### Application menu

<a href="/img/menubar/menu.png"><img src="/img/menubar/menu.png" alt="Application Menu" /></a>

It's not a coincidence that this is the Terminal, that's where I spend
most of my time when I'm not on Chrome, and that's where I write code
which is my main activity.

I don't use the menu very often, I would say I either go to the Preferences
or go to Help and search for what I'm trying to do.

If I would use something regularly I would make a shortcut for it.

Shortcuts in macOS are based on menu item labels and using search in Help will
locate the menu item visually for me, very nice.

### Tray icons

<a href="/img/menubar/tray.png"><img src="/img/menubar/tray.png" alt="Tray icons" /></a>

All those tray icons start when my Mac starts. By default I just let the icons be and let them do their job.

- **Cloudflare WARP**: A free and simple VPN that lets me use the internet always over
  secure connections
  - I will occasionnaly switch WARP on and off when the internet is not working, not sure why, didn't investigate
- **Redis.app**: I find it works better than having a backround service, here I can visually see when redis is running
  - Redis is a database I use for caching, background jobs, and websockets through Action Cable in my Ruby on Rails appas
- **Postgres.app**: Same as Redis.app, better than a background service because I see when it's running, I can see the version. I will rarely use Postico to see the tables and data inside the database
  - Postgres (short for PostgreSQL) is a database that works very well, is reliable and has a lot of features including search
- **Music**: I listen to music on Apple Music now, switched from Spotify a few days ago and it works well and is much nicer. I like to be surrounded by well-designed apps, I think it influences my own design and taste.
- **Spectable**: I use it for shotcuts like Command+Option+Right to put a window on the right half of my screen (often of Terminal), Command+Option+Left to put a window on the left half of my screen (rare), Command+Option+f for doing a full-screen (without switching to macOS full screen that hides the menu bar) (often for Chrome)
- **KeepingYouAwake**: It keeps my Mac awake while I listen to music or download files. Kind of an issue sometimes because it seems like it keeps the Mac awake when the lid is closed
- **Bluetooth**: Great when it works to connect speakers
- **Sound**: I use the keyboard shortcuts to adjust the volume but this works too
- **Wifi**: Connect to the internet over Wifi, pretty useful
- **Battery**: Should look at it more
- **Controls**: Never use that
- **Date and time**: Pretty useful

## Destkop

<a href="/img/desktop.png"><img src="/img/desktop.png" alt="Desktop" /></a>

I use the desktop mainly for temporary screenshots and when saving files from
Chrome (e.g. kind of downloading).

## Chrome

<a href="/img/chrome.png"><img src="/img/chrome.png" alt="Chrome" /></a>

I try to have as few tabs open as possible and quit Chrome when I'm not using it
(true for all apps expect Finder that I can't quit).

I have a new tab page I made as an extension (available in Chrome Web Store) that has
a blank title, blank favicon and black background matching Chrome and macOS dark
theme.

My default search engine is Google because that's what works best by far.

I don't use the share URL or favorites.

I use Dashlane for passwords and secure notes, works well.

Then in extensions I have:

- **React Developer Tools**: To debug React apps
- **Stylish**: To customize a few websites, mainly the login button of Cloudflare
- **uBlock**: To block ads, trackers, bad search results, etc.

I don't really use the reading list.

I'm logged in with my main account: dorian@dorianmarie.fr

Then I go to the settings to change language (test language auto-detection), or to reset permissions or clear cookies/cache for websites.

I sometimes go to some chrome:// urls like chrome://net-internals to fix HTTPS on localhost.

## Files

<a href="/img/home.png"><img src="/img/home.png" alt="Home" /></a>

I have an `~/src` folder with my code.

I started a `~/TODO.md`, usually I have one per-project but trying something new with the top items from Paul Graham's TODO list.

I use `~/Applications` to uninstall applications.

I use `~/Documents` to store my Sketch files mainly.

I look at `~/Downloads` often.

I added `dorianmariefr` which my home directory for easier file access because you can't
go to the parent directory easily in Finder.

I added `~/Music` to look at my music files.

## Mail

<a href="/img/mail.png"><img src="/img/mail.png" alt="Mail" /></a>

I started with Hotmail, then GMail classic UI, then GMail web 2.0 UI, then Inbox, then GMail, then Hey, then GMail, then Superhuman, and now on Apple Mail, liking it so far.

I added Command+E for Archiving and Command+Enter for sending emails kinda like Superhuman.

I use Inbox Zero as you can see.

## Music

<a href="/img/music.png"><img src="/img/music.png" alt="Music" /></a>

I listen to music quite a lot and have many artists.

## Terminal

<a href="/img/terminal.png"><img src="/img/terminal.png" alt="Terminal" /></a>

And after I put it on the right of the screen:

<a href="/img/terminal-right.png"><img src="/img/terminal-right.png" alt="Terminal Right" /></a>

I use the Terminal with:

- **fish**: for the shell because of the auto-completion
- **vim**: for text editing because it's so fast and no need for a new window to manage
- **ruby**, **rails**, **node**, **yarn**, etc. many many dev tools
