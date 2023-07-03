## Emuladores Recomendados

| Consola   | Emulador                                      | Compatibilidad    | Notas |
| ---       | ---                                           | ---               |  ---  |
| Gamecube  | [Dolphin](https://es.dolphin-emu.org/?cr=es)  | [Dolphin Compat](https://es.dolphin-emu.org/compat/)
| Wii       | [Dolphin](https://es.dolphin-emu.org/?cr=es)  | [Dolphin Compat](https://es.dolphin-emu.org/compat/)
| Wii U     | [CEMU](https://cemu.info/#download)           | [Cemu Compat](http://compat.cemu.info/)
| Switch    | [Yuzu](https://yuzu-emu.org/)                 | [Yuzu Compat](https://yuzu-emu.org/game/)
|           | [Ryujinx](https://ryujinx.org/)               | [Github Issues](https://github.com/Ryujinx/Ryujinx-Games-List/issues) |
|           | [Skyline for Android](https://skyline-emu.one/)
| DS        | [MelonDS](https://github.com/Arisotura/melonDS/releases) |        | Fork de DeSmuME



### Otros emuladores
| Consola   | Emulador                                      | Estado / Notas    |
| ---       | ---                                           | ---               |
| DS        | [DeSmuME](https://desmume.org/)               | MelonDS es su continuación (más o menos).
| 3DS       | [Citra](https://citra-emu.org/)               | Desarrollo abandonado en favor de Yuzu. No especialmente completo.
|           | [Mikage](https://mikage.app/time-to-renew-3ds-emulation/) ([Youtube](https://www.youtube.com/@MikageEmu)) | Desarrollo a puerta cerrada, por ahora (Abril/23) sin publicarse.
| PS4/5     | [Kyty](https://github.com/InoriRus/Kyty)      | Proyecto no publicado, no es útil por ahora (Abril/23).


## Info sobre emuladores
- [Emugen](https://emulation.gametechwiki.com/index.php/Main_Page) y [FAQ](https://emulation.gametechwiki.com/index.php/General_problems_FAQ)
- [Emugen: Emulators on Windows](https://emulation.gametechwiki.com/index.php/Emulators_on_Windows)
- [Emugen: Emulators on Android](https://emulation.gametechwiki.com/index.php/Emulators_on_Android)


## Archivos necesarios
- [Emulator Files - Emugen](https://emulation.gametechwiki.com/index.php/Emulator_files)
- [Switch Firmware - No oficial](https://darthsternie.net/switch-firmwares/)
- [PS3 Firmware - Oficial](https://www.playstation.com/es-es/support/hardware/ps3/system-software/)


## Comprimir ROMS / Ahorrar espacio
- Nintendo GameCube
    - ``.rvz`` solo para emulador. Convertir desde Dolphin.
    - ``.ciso`` funciona con consolas. Usar [GameCube Backup Manager](https://github.com/AxionDrak/GameCube-Backup-Manager) cuando [añada soporte](https://github.com/AxionDrak/GameCube-Backup-Manager/issues/117) o [Wimm's ISO Tools](https://wit.wiimm.de/).
- Nintendo Wii
    - ``.rvz`` solo para emulador. Convertir desde Dolphin.
    - ``.wbfs`` funciona con consolas. Usar [Wii Backup Manager](https://wiibackupmanager.co.uk/downloads.html) o [Wimm's ISO Tools](https://wit.wiimm.de/).
- Playstation 2 
    - ``.zso`` funciona con consolas. Usar [este script de python](https://github.com/ps2homebrew/Open-PS2-Loader/blob/master/pc/ziso.py) (requiere python + pip + modulo lz4).
- Xbox 360
    - ``Games on Demand - GoD`` funciona con consolas. Usar [ISO2GOD](https://digiex.net/threads/iso2god-v1-3-6-download-convert-xbox-360-xgd3-isos-to-gods-games-on-demand.9502/)
