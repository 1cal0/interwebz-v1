# interwebz-v1
original src was posted on https://hackvshack.net/threads/interwebz-fixed-for-csgo-2023.13212/
this version has fixed crashes and removed unused features, uses original src for iwebz v1

---

### what changed vs the original
- fixed crashes (null checks on things that used to instacrash on some setups)
- removed unused / broken features so the build is cleaner
- ported properly from css to csgo so it actually runs

### included
- aimbot (smooth, silent, psilent, trigger, knife, autoshoot, autopistol, nospread)
- esp (box, health, name, head, visibility checks)
- chams (fullbright, ignorez, asus/wireframe, nosky, nohands)
- misc (bhop, strafe, fakelag, anti-aim, no-recoil)
- in-game menu with cfg save/load

### configs
- saved to `C:\iwebz\` as `<name>.cfg`
- configs are stored locally, no server needed, og src relied on a php webserver

### building
- compile the project as an x86 dll and inject into csgo alongside the sdk headers

### files
- `CAimbot.cpp` - aiming / nospread logic
- `CESP.cpp` - visual esp
- `Surface.cpp` - chams + paint traverse hook
- `CDraw.cpp` - text / box drawing (per-frame text is allocation-free)
- `client.cpp` - create move / movement hooks
- `menu.cpp` - in-game menu + hacks
- `CVARS.cpp` - cvar + config path handling
- `DllMain.cpp` - attach / detach
