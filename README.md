<h1 align="center">Better Warden</h1>

<p align="center">
	<img src="http://i.imgur.com/WXfuF5Y.png" width="572px"><br/>
	<a href="https://travis-ci.org/condolent/Better-Warden">
		<img src="https://travis-ci.org/condolent/Better-Warden.svg?branch=master">
	</a>
	<a href="https://github.com/condolent/Better-Warden/wiki">
		<img src="https://img.shields.io/badge/Plugin-Wiki-orange.svg?style=flat">
	</a>
	<a href="https://github.com/condolent/Better-Warden/releases">
		<img src="https://img.shields.io/github/release/condolent/better-warden.svg">
	</a>
	<a href="https://github.com/condolent/Better-Warden/releases">
		<img src="https://img.shields.io/github/downloads/condolent/better-warden/total.svg">
	</a>
	<a href="https://github.com/condolent/Better-Warden/issues">
		<img src="https://img.shields.io/github/issues-raw/condolent/better-warden.svg">
	</a>
	<a href="https://forums.alliedmods.net/showthread.php?p=2541919#post2541919">
		<img src="https://img.shields.io/badge/SM-Thread-lightgrey.svg?style=flat">
	</a>
	<a href="https://github.com/condolent/Better-Warden/blob/master/LICENSE">
		<img src="https://img.shields.io/badge/License-GPL3-red.svg?style=flat">
	</a>
</p>
<p align="center">
	<sup><strong>An improved and more advanced warden plugin with a custom menu for CS:GO jailbreak servers!</strong></sup>
<p>

## Repository Index
* [Installation](#installation)
* [Dependencies](#dependencies)
* [Features](#features)
* [CVars](#cvars)
* [Commands](https://github.com/condolent/Better-Warden/wiki/Commands)
* [API](#api)
* [Translations](#translations)

## Installation
1. [Download the plugin package](https://github.com/condolent/Better-Warden/releases)
2. In the `SERVER FILES` folder, drag all of its' content to your servers root folder (`csgo`)
3. Everything in the `FASTDL` folder should be uploaded to your FastDL webserver
4. Restart your server or change map
5. Make your desired changes in the two configs located in `csgo/cfg/BetterWarden` folder
6. Change map, restart server or reload both `betterwarden.smx` and `cmenu.smx` for changes to apply
7. Done!

## Dependencies
* [SmartJailDoors](https://forums.alliedmods.net/showthread.php?t=264100) _by Kailo_

## Features
The major function this plugin offers is that the warden can choose special event days to play out for the round. Each day has some special server rules & features that applies in order to make it much more fun for the players!  
1. Hide and Seek
2. Freeday
3. Warday
4. Gravity Freeday

There's also some other functions in the menu that the warden can take advantage of in order to make the game more comfortable.  
Some of the other entries in the menu include:  
1. Toggle noblock
2. Weapons menu, allowing the warden to spawn in the selected weapon to himself
3. Give a specific player(s) freeday, marked with beacons

## CVars
### BetterWarden
| ConVar      | Default | Description   |
|:----------- |:-------:|:------------- |
|`sm_warden_version`|**0.3**|Current version running. Debugging purposes only! Do NOT change this!|
|`sm_warden_admin`|**b**|The flag used for admin commands.|
|`sm_warden_noblock`|**1**|Give the warden the ability to toggle noblock via sm_noblock? 1 = Enable. 0 = Disable.|
|`sm_warden_cellscmd`|**1**|Give the warden ability to toggle cell-doors via sm_open? Cell doors on every map needs to be setup with SmartJailDoors for this to work! 1 = Enable. 0 = Disable.|
|`sm_warden_same_twice`|**0**|Prevent the same warden from becoming warden next round instantly? This should only be used on populated servers for obvious reasons. 1 = Enable. 0 = Disable.|
|`sm_warden_stats`|**1**|Have a hint message up during the round with information about who's warden, how many players there are etc. 1 = Enable. 0 = Disable.|
|`sm_warden_colorR`|**33**|The Red value of the color the warden gets.|
|`sm_warden_colorG`|**114**|The Green value of the color the warden gets.|
|`sm_warden_colorB`|**255**|The Blue value of the color the warden gets.|
|`sm_warden_icon`|**1**|Have an icon above the wardens' head? 1 = Enable. 0 = Disable.|
|`sm_warden_icon_path`|**decals/BetterWarden/warden**|The path to the icon. Do not include file extensions!|

### CMenu
| ConVar      | Default | Description   |
|:----------- |:-------:|:------------- |
|`sm_cmenu_version`|**0.2**|Current version running. Debugging purposes only! Do NOT change this!|
|`sm_cmenu_hns`|**1**|Add an option for Hide and Seek in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_hns_godmode`|**1**|Makes CT's invulnerable against attacks from T's during HnS to prevent rebels. 0 = Disable. 1 = Enable.|
|`sm_cmenu_hns_rounds`|**2**|How many times is HnS allowed per map? Set to 0 for unlimited.|
|`sm_cmenu_freeday`|**1**|Add an option for a freeday in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_freeday_rounds`|**2**|How many times is a Freeday allowed per map? Set to 0 for unlimited.|
|`sm_cmenu_warday`|**1**|Add an option for Warday in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_warday_rounds`|**1**|How many times is a Warday allowed per map? Set to 0 for unlimited.|
|`sm_cmenu_gravity`|**1**|Add an option for a gravity freeday in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_gravity_team`|**2**|Which team should get a special gravity on Gravity Freedays? 0 = All teams. 1 = Counter-Terrorists. 2 = Terorrists.|
|`sm_cmenu_gravity_strength`|**0.5**|What should the gravity be set to on Gravity Freedays?|
|`sm_cmenu_gravity_rounds`|**1**|How many times is a Gravity Freeday allowed per map? Set to 0 for unlimited.|
|`sm_cmenu_noblock`|**1**|_sm_warden_noblock needs to be set to 1 for this to work!_ Add an option for toggling noblock in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_auto_open`|**1**|Automatically open the menu when a user becomes warden? 0 = Disable. 1 = Enable.|
|`sm_cmenu_weapons`|**1**|Add an option for giving the warden a list of weapons via the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_restricted_freeday`|**1**|Add an option for a restricted freeday in the menu? This event uses the same configuration as a normal freeday. 0 = Disable. 1 = Enable.|
|`sm_cmenu_player_freeday`|**1**|Add an option for giving a specific player a freeday in the menu? 0 = Disable. 1 = Enable.|
|`sm_cmenu_doors`|**1**|sm_warden_cellscmd needs to be set to 1 for this to work! Add an option for opening doors via the menu. 0 = Disable. 1 = Enable|

## API
### Betterwarden
```sourcepawn
/*
* 
* INCLUDE FOR THE SOURCEMOD PLUGIN; BETTER WARDEN
* https://github.com/condolent/Better-Warden
* 
*/
#if defined bwardenincluded
 #endinput
#endif
#define bwardenincluded
#define VERSION "0.4"

#define a ADMFLAG_RESERVATION
#define b ADMFLAG_GENERIC
#define c ADMFLAG_KICK
#define d ADMFLAG_BAN
#define e ADMFLAG_UNBAN
#define f ADMFLAG_SLAY
#define g ADMFLAG_CHANGEMAP
#define h ADMFLAG_CONVARS
#define i ADMFLAG_CONFIG
#define j ADMFLAG_CHAT
#define k ADMFLAG_VOTE
#define l ADMFLAG_PASSWORD
#define m ADMFLAG_RCON
#define n ADMFLAG_CHEATS
#define z ADMFLAG_ROOT
#define o ADMFLAG_CUSTOM1
#define p ADMFLAG_CUSTOM2
#define q ADMFLAG_CUSTOM3
#define r ADMFLAG_CUSTOM4
#define s ADMFLAG_CUSTOM5
#define t ADMFLAG_CUSTOM6

/**
* Called when the current warden dies.
*
* @param client index
*/
forward void OnWardenDeath(int client);

/**
* Called when a player becomes warden.
*
* @param client index
*/
forward void OnWardenCreated(int client);

/**
* Called when an admin sets a warden.
*
* @param admin client index
* @param client index
*/
forward void OnWardenCreatedByAdmin(int admin, int client);

/**
* Called when the current warden disconnects.
*
* @param client index
*/
forward void OnWardenDisconnect(int client);

/**
* Called when the current warden retires by himself.
*
* @param client index
*/
forward void OnWardenRetire(int client);

/**
* Called when an admin removes the current warden.
*
* @param client index
*/
forward void OnAdminRemoveWarden(int admin, int warden);

/**
* Checks if the given client is currently warden.
*
* @param client index
* @return true if yes
*/
native bool IsClientWarden(int client);

/**
* Checks is there currently is a warden.
*
* @return true if yes
*/
native bool WardenExists();

/**
* Makes the given client warden for the round.
*
* @param client index
* @return true if successful
*/
native bool SetWarden(int client);

/**
* Remove the current warden.
*
* @return true if successful
*/
native bool RemoveWarden();

/**
* Fetch the current wardens' client index
*
* @return client index
*/
native bool GetCurrentWarden();

/**
* Gets the amount of alive players in the specified team.
*
* @param team index
* @return the alive count
*/
native bool GetTeamAliveClientCount(int teamIndex);

/**
* Checks if the client is a Better Warden admin.
*
* @param client index
* @return true if yes
*/
native bool IsClientWardenAdmin(int client);

/**
* Checks several parameters to see if the specified client is a valid user.
*
* @param client index
* @param Allow bots? (False)
* @param Allow dead? (False)
* @return true if valid
*/
stock bool IsValidClient(int client, bool bAllowBots = false, bool bAllowDead = false)
{
	if(!(1 <= client <= MaxClients) || !IsClientInGame(client) || (IsFakeClient(client) && !bAllowBots) || IsClientSourceTV(client) || IsClientReplay(client) || (!bAllowDead && !IsPlayerAlive(client)))
	{
		return false;
	}
	return true;
}

/**
* Precaches and prepares models for download. Used for icons!
*
* @param path to model
*/
stock void PrecacheModelAnyDownload(char[] sModel)
{
	char sBuffer[256];
	Format(sBuffer, sizeof(sBuffer), "materials/%s.vmt", sModel);
	AddFileToDownloadsTable(sBuffer);
	PrecacheModel(sBuffer, true);
	Format(sBuffer, sizeof(sBuffer), "materials/%s.vtf", sModel);
	AddFileToDownloadsTable(sBuffer);
	PrecacheModel(sBuffer, true);
}
```
### CMenu
```sourcepawn
/*
* https://github.com/condolent/Better-Warden
*/

#if defined cmenuincluded
 #endinput
#endif
#define cmenuincluded

/**
* Called when a warden opens the warden menu. Also called when a player becomes a warden if sm_cmenu_auto_open is set to 1.
*
* @param client index of the one opening the menu
*/
forward void OnCMenuOpened(int client);

/**
* Called when an event day is created.
*/
forward void OnEventDayCreated();

/**
* Called when an event day is aborted.
*/
forward void OnEventDayAborted();

/**
* Called when Hide and Seek is won.
*/
forward void OnHnsOver();

/**
* Check if there is a event day currently active.
* 
* @return     true if yes
*/
native bool IsEventDayActive();

/**
* Check if a Hide and Seek game is running.
*
* @return     true if yes
*/
native bool IsHnsActive();

/**
* Check if a Gravity Freeday is running.
*
* @return     true if yes
*/
native bool IsGravFreedayActive();

/**
* Check if a warday is running.
*
* @return     true if yes
*/
native bool IsWarActive();

/**
* Check if a freeday is running.
*
* @return     true if yes
*/
native bool IsFreedayActive();

/**
* Check if the specified client already has a freeday.
*
* @param     client index
* @return     true if yes
*/
native bool ClientHasFreeday(int client);

/**
* Give a client a freeday
*
* @param      client index
* @return     true if successful
*/
native bool GiveClientFreeday(int client);

/**
* Remove a client's freeday
*
* @param      client index
* @return     true if successful
*/
native bool RemoveClientFreeday(int client);

/**
* Sets a beacon on a client. Just like the one in the SM Admin Menu.
*
* @param client index
* @param state of the beacon.
* @return true if successful
*/
native bool SetClientBeacon(int client, bool beaconState);
```

## Translations
* English ✓
* Swedish ✓
* French × _(Some are done)_
* Russian ×
