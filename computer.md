---
title: How I Use My Computer
layout: default
indexed: true
---

I'm going to show you how I use my computer.

<figure>
  <a href="/img/menubar.png"><img src="/img/menubar.png" alt="Menu bar" /></a>
  <figcaption>Screenshot of my computer</figcaption>
</figure>

## Menu bar

### Apple icon

<figure>
  <a href="/img/menubar/apple.png"><img src="/img/menubar/apple.png" alt="Apple icon" /></a>
  <figcaption>Apple icon on the top-left of the screen</figcaption>
</figure>

I use a Macbook Air as my personal laptop, with macOS.

I use it to access my system information, my storage space,
all all the settings mainly.

### Application menu

<figure>
  <a href="/img/menubar/menu.png"><img src="/img/menubar/menu.png" alt="Application Menu" /></a>
  <figcaption>Menu on the top-left of the screen next to the Apple icon</figcaption>
</figure>

It's not a coincidence that this is the Terminal, that's where I spend
most of my time when I'm not on Chrome, and that's where I write code.

I don't use the menu very often, I would say I either go to the Preferences
or go to Help and search for what I'm trying to do.

If I would use something regularly I would make a shortcut for it. (like Archive, Send and Reply in Mail.app)

Shortcuts in macOS are based on menu item labels and using search in Help will
locate the menu item visually for me, very nice.

### Tray icons

<figure>
  <a href="/img/menubar/tray.png"><img src="/img/menubar/tray.png" alt="Tray icons" /></a>
  <figcaption>Tray icons on the top-right of the screen</figcaption>
</figure>

All those tray icons start when my Mac starts. By default I just let the icons be and let them do their job.

- **Cloudflare WARP**: A free and simple VPN that lets me use the internet always over
  secure connections
- **Redis.app**: I find it works better than having a backround service, here I can visually see when redis is running
- **Postgres.app**: Same as Redis.app, better than a background service because I see when it's running, I can see the version. I will rarely use Postico to see the tables and data inside the database
- **Music**: I listen to music on Apple Music now, switched from Spotify a few days ago and it works well and is much nicer. I like to be surrounded by well-designed apps, I think it influences my own taste for great design.
- **Spectable**: I use it for shortcuts like Command+Option+Right to put a window on the right half of my screen (often for Terminal), Command+Option+Left to put a window on the left half of my screen (rare), Command+Option+F for doing a full-screen (without switching to macOS full screen that hides the menu bar) (often for Chrome)
- **KeepingYouAwake**: It keeps my Mac awake while I listen to music or download files
- **Bluetooth**: Great to connect to speakers
- **Sound**: I use the keyboard shortcuts instead of the tray icon's menu
- **Wifi**: Connect to the internet over Wifi, pretty useful
- **Battery**: Very useful to know when to charge my computer
- **Controls**: I do not use "Do not disturd" and other items in this menu, I prefer the keyboard shortcuts
- **Date and time**: Pretty useful

## Destkop

<figure>
  <a href="/img/desktop.png"><img src="/img/desktop.png" alt="Desktop" /></a>
  <figcaption>A file on my desktop</figcaption>
</figure>

I use the desktop mainly for temporary screenshots and when saving files from
Chrome (e.g. kind of downloading).

## Chrome

<figure>
  <a href="/img/chrome.png"><img src="/img/chrome.png" alt="Chrome" /></a>
  <figcaption>Google Chrome new tab page</figcaption>
</figure>

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

I sometimes go to some chrome:// urls like chrome://net-internals to fix HTTPS on localhost because I had an environment with HSTS for localhost and others with HTTP-only. Next time I will use a separate local domain.

## Files

<figure>
  <a href="/img/home.png"><img src="/img/home.png" alt="Home" /></a>
  <figcaption>Finder's in home directory, e.g. <code>/Users/dorianmariefr/</code></figcaption>
</figure>

I have an `~/src` folder with my code.

I started a `~/TODO.md`, usually I have one per-project but trying something new with the top items from Paul Graham's TODO list.

I use `~/Applications` to uninstall applications.

I use `~/Documents` to store my Sketch files mainly.

I look at `~/Downloads` often.

I added `dorianmariefr` which my home directory for easier file access because you can't
go to the parent directory easily in Finder.

I added `~/Music` to look at my music files.

## Mail

<figure>
  <a href="/img/mail.png"><img src="/img/mail.png" alt="Mail" /></a>
  <figcaption>Mail.app also named Apple Mail</figcaption>
</figure>

I started with Hotmail, then GMail classic UI, then GMail web 2.0 UI, then Inbox, then GMail, then Hey, then GMail, then Superhuman, and now on Apple Mail, liking it so far.

I added Command+E for Archiving and Command+Enter for sending emails kinda like Superhuman.

I use Inbox Zero as you can see.

## Music

<figure>
  <a href="/img/music.png"><img src="/img/music.png" alt="Music" /></a>
  <figcaption>Music.app also named Apple Music</figcaption>
</figure>

I listen to music quite a lot and have many artists.

## Terminal

<figure>
  <a href="/img/terminal.png"><img src="/img/terminal.png" alt="Terminal" /></a>
  <figcaption>Terminal.app default window</figcaption>
</figure>

<figure>
  <a href="/img/terminal-right.png"><img src="/img/terminal-right.png" alt="Terminal Right" /></a>
  <figcaption>Terminal.app once I put it on the right of the screen</figcaption>
</figure>

I use the Terminal with:

- **fish**: for the shell because of the auto-completion
- **vim**: for text editing because it's so fast and no need for a new window to manage
- **ruby**, **rails**, **node**, **yarn**, etc. many many dev tools

## Applications

- **AdBlock.app**: Ad blocker on Safari
- **Dashlane.app**: I use the Chrome Extension but this could come handy
- **Docker.app**: Sometimes I need containers to run rubygems.org or test a Dockerfile for CircleCI
- **Google Chrome.app**: I especially love the Dev Tools and the simplicity in general
- **KeepingYouAwake.app**: Keeping my Mac awake
- **Numbers.app**: To view CSV and generate some CSV
- **Postgres.app**: To manage the PostgreSQL background process
- **Postico.app**: To manage PostgreSQL databases and tables
- **Redis.app**: To manage the Redis background process
- **Safari.app**: Useful to debug websites that don't work on iOS
- **Sketch.app**: I design a lot of small things with it, mainly for websites
- **Spectacle.app**: Windows management shortcuts
- **Xcode.app**: Useful to develop iOS apps but very slow
- **YubiKey Manager.app**: Manage my yubikeys
- **zoom.us.app**: I prefer Google Meet but a lot of people use Zoom

## Websites

- **[Hacker News](https://news.ycombinator.com/)**: Interesting articles and comments
- **localhost:4000**: Making this website (jekyll)
- **localhost:3000**: Making rails websites
- **[talent.io](https://www.talent.io)**: Website that matches programmers with companies
- **[Reddit](https://www.reddit.com)**: /r/ruby, /r/rails for ruby related content, /r/iphone, /r/apple for apple related content, also /r/github and /r/stripe. Sometimes looking at /r/all
- **[Twitter](https://twitter.com)**: Mostly interesting and ruby-related content
- **[WhatsApp](https://web.whatsapp.com)**: I have my WhatsApp, my calls and texts go through my computer so it's easier to manage them
- **[Cloudflare](https://www.cloudflare.com)**: Manage my DNS mainly
- **[Y Combinator](https://www.ycombinator.com)**: Startup School, Jobs and great content

## Tools

### Vim

Here is my `.vimrc`:

```vim
set tabstop=2
set shiftwidth=2
set expandtab
set autoindent
set nobackup
set nowritebackup
set noswapfile
set nocompatible
set shell=/bin/bash
set viminfo='20,<1000
set backspace=indent,eol,start
set whichwrap+=<,>,[,]

set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

Plugin 'gmarik/vundle'
Plugin 'bogado/file-line'
Plugin 'yuezk/vim-js'
Plugin 'maxmellon/vim-jsx-pretty'
Plugin 'tpope/vim-rails'
Plugin 'slim-template/vim-slim'

call vundle#end()

filetype plugin indent on
syntax on

fun! TrimWhitespace()
    let l:save = winsaveview()
    keeppatterns %s/\s\+$//e
    call winrestview(l:save)
endfun

autocmd BufWritePre * :call TrimWhitespace()

" Go to the last cursor location when a file is opened, unless this is a
" git commit (in which case it's annoying)
au BufReadPost *
    \ if line("'\"") > 0 && line("'\"") <= line("$") && &filetype != "gitcommit" |
        \ execute("normal `\"") |
    \ endif
```

### Git

Here is my `.gitconfig`:

```ruby
[user]
  email = dorian@dorianmarie.fr
  name = Dorian Marié
[alias]
  co = checkout
  cm = commit
  cmm = commit -m
  dfs = diff --staged
  s = status
  r = reset
  df = diff
  b = branch
  lg = log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit
  cp = cherry-pick
[push]
  default = current
[core]
  excludesfile = /Users/dorianmariefr/.gitignore_global
[init]
  defaultBranch = master
[pull]
  rebase = false
```

## Questions? Comments? Feedback?

Send me an email at [dorian@dorianmarie.fr](mailto:dorian@dorianmarie.fr)
and/or [on Twitter (@dorianmariefr)](https://twitter.com/dorianmariefr).
