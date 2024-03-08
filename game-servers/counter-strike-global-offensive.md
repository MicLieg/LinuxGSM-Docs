# Counter-Strike: Global Offensive

## **Server Resources**

**Official Server Resources**

* [CS:GO Dedicated server Wiki](https://developer.valvesoftware.com/wiki/Counter-Strike:\_Global\_Offensive\_Dedicated\_Servers)
* [CS:GO Server Workshop setup Wiki](https://developer.valvesoftware.com/wiki/CSGO\_Workshop\_For\_Server\_Operators)
* [CS:GO Server Known Issues Wiki](https://developer.valvesoftware.com/wiki/CSGO\_Game\_Mode\_Commands)
* [CS:GO Game Modes](https://developer.valvesoftware.com/wiki/CS:GO\_Game\_Modes)

## **Game Modes**

CS:GO features various game modes, which can be played on your server. To make setting up your server a bit easier, the following table sums up the configuration required in your server's [LinuxGSM config](../configuration/linuxgsm-config.md) for the various game modes. If you want more detailed and up-to-date information, take a look at Valve's wiki: [CS:GO Game Modes](https://developer.valvesoftware.com/wiki/CS:GO\_Game\_Modes). Up-to-date information about mapgroups can be found in the file `serverfiles/csgo/gamemodes.txt`.

| \[Game Modes]                     | gametype | gamemode | gamemodeflags | skirmishid | mapgroup (you can mix these across all Game Modes except Danger Zone, but use only one)                                                                             |
| --------------------------------- | -------- | -------- | ------------- | ---------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Arms Race                         | 1        | 0        | 0             | 0          | mg\_armsrace                                                                                                                                                        |
| Boom! Headshot!                   | 1        | 2        | 0             | 6          | mg\_skirmish\_headshots                                                                                                                                             |
| Classic Casual                    | 0        | 0        | 0             | 0          | mg\_casualsigma, mg\_casualdelta                                                                                                                                    |
| Classic Competitive (Default)     | 0        | 1        | 0             | 0          | mg\_active, mg\_reserves, mg\_hostage, mg\_de\_dust2, ...                                                                                                           |
| Classic Competitive (Short Match) | 0        | 1        | 32            | 0          | mg\_active, mg\_reserves, mg\_hostage, mg\_de\_dust2, ...                                                                                                           |
| Danger Zone                       | 6        | 0        | 0             | 0          | mg\_dz\_blacksite (map: dz\_blacksite), mg\_dz\_sirocco (map: dz\_sirocco)                                                                                          |
| Deathmatch (Default)              | 1        | 2        | 0             | 0          | mg\_deathmatch                                                                                                                                                      |
| Deathmatch (Free For All)         | 1        | 2        | 32            | 0          | mg\_deathmatch                                                                                                                                                      |
| Deathmatch (Team vs Team)         | 1        | 2        | 4             | 0          | mg\_deathmatch                                                                                                                                                      |
| Demolition                        | 1        | 1        | 0             | 0          | mg\_demolition                                                                                                                                                      |
| Flying Scoutsman                  | 0        | 0        | 0             | 3          | mg\_skirmish\_flyingscoutsman                                                                                                                                       |
| Hunter-Gatherers                  | 1        | 2        | 0             | 7          | mg\_skirmish\_huntergatherers                                                                                                                                       |
| Retakes                           | 0        | 0        | 0             | 12         | mg\_skirmish\_retakes                                                                                                                                               |
| Stab Stab Zap                     | 0        | 0        | 0             | 1          | mg\_skirmish\_stabstabzap                                                                                                                                           |
| Trigger Discipline                | 0        | 0        | 0             | 4          | mg\_skirmish\_triggerdiscipline                                                                                                                                     |
| Wingman                           | 0        | 2        | 0             | 0          | mg\_de\_prime, mg\_de\_blagai, mg\_de\_vertigo, mg\_de\_inferno, mg\_de\_overpass, mg\_de\_cbble, mg\_de\_train, mg\_de\_shortnuke, mg\_de\_shortdust, mg\_de\_lake |

When adjusting the `mapgroup`, don't forget to also set `defaultmap` to a map contained in the same mapgroup.

If players are respawning in random locations on custom maps, set `mp_randomspawn` to 0.

If players are being banned for dying too much, such as on minigames maps, as a workaround set `mp_autokick` to 0. **Warning, this disables AFK and Teamkilling kicks as well.**

## **Server Guides**

[Install Sourcemod on CS:GO Server](../guides/sourcemod-csgo-server.md)

## **Setting for a 128 Tick Server**

Add to the following to the config `lgsm/config-lgsm/csgoserver/csgoserver.cfg` :

`tickrate="128"`

AS well it is needed to add a few options to the game config (default in: `serverfiles/csgo/cfg/csgoserver.cfg` )

```bash
sv_mincmdrate 128
sv_minupdaterate 128
```

This will as well force the client to use the 128 tickrate

## Workshop

For CSGO, edit these lines in your [LinuxGSM config](../configuration/linuxgsm-config.md)

```bash
wsapikey="YOUR_STEAM_API_KEY"
wscollectionid="YOUR_COLLECTION_ID"
wsstartmap="
```

## **Server Tips**

If players are respawning in random locations on custom maps, set mp\_randomspawn to 0.

If players are being banned for dying too much, such as on minigames maps, as a workaround set mp\_autokick to 0. **Warning, this disables AFK and Teamkilling kicks as well.**
