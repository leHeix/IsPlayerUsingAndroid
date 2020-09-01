# IsPlayerAndroid
Check if a player is using Android.

## Note
* **Using in OnPlayerConnect is likely to return that the player is always using Android as how the include is done.**
* Client checks are done by RPCs and depend on the client. PacketLoss MIGHT make the user to not receive the RPC thus showing it as an Android user.
* New SA-MP Android versions may have a default response to RPC_ClientCheck, making this include useless.
* This can also be used to detect users who have NOPed the ClientCheck RPC.

## Installation
1. Include this in your gamemode/filterscript.
 
## Usage 
```pawn
public OnPlayerSpawn( playerid )
{
    if(IsPlayerAndroid(playerid))
        SendClientMessage(playerid, "You're connected from an Android version");

    return 1;
}
```
