# Mpv-play

A cli wrapper around mpv with convenience functions for adding more items to the playlist and skipping around the playlist.
Written purely in POSIX-compliant shell

## Purpose
mpv is a great minimalist video and audio player with arguably better performance and compatibility than vlc, but for my use it has 2 main flaws:
1. Not being able to easily add files after the instance has been created
1. Not being able to skip around the playlist easily. 

This is especially painful with audio files. 
This program uses mpv's ipc server protocol to communicate with the running instance, so users can add files to the playlist, skip around the playlist and remove entries from the playlist. Since it's written in POSIX shell it is easil extensible however you want. 

## Caveats
The main caveat with mpv-play is that pausing and playing are done through the command line. So to pause you need to issue ```mpv-play -P``` rather than just pressing your hotkey if you were normally using mpv. I map the play and pause commands to hotkeys to get around this, but if you aren't comfortable with setting hotkeys you will have to use the command line to pause and resume

