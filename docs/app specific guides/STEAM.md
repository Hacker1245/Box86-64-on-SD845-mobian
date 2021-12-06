# STEAM

Installing steam is straight forward as mostly you need to download deb file from Valve server, extract it and run binary. Probably some libs will be missing, so you need to use steps from troubleshooting guide. Bookworm don't have some of them, but it should run ok anyway.

At this moment only installing and starting apps in small mode works. If you want to use more steam functionality, I recommend to use steamcmd.

For just installing Steam use this command: 

```
cd ~; mkdir steam; cd steam; wget http://media.steampowered.com/client/installer/steam.deb; ar x steam.deb; tar xf data.tar.xz; STEAMOS=1 ./usr/lib/steam/bin_steam.sh
```

And than run it with command below:

```
STEAMOS=1 setarch -L linux32 ~/steam/usr/lib/steam/bin_steam.sh
```

Wihout steamcmd to remove game files, delete game directory from `~/.steam/steam/steamapps/common/`

If I'll have a time, I'll update it with steamcmd part.