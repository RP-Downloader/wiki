---
description: Other Optional Settings That Can Be Edited
---

# Other Settings

### Resourcepack-Command:

This setting is used to change the command players will use to download the resource pack (If Send-Resourcepack-On-Join is set to false)

{% code title="Line 3 | Settings.yml" %}
```yaml
#The command that will be used is put here 
#(NOTE: the command must be a single word, it cant be "Pack Download" or "rpd download" ect)
#Default Setting: rp
Resourcepack-Command: rp
#wether or not the command should be case sensitive
#if set to true, if your command to download is rp
#the player cant type /Rp, /rP, /RP, etc, etc to execute the command
#Default Setting: false
Command-Case-Sensitive: false
```
{% endcode %}

### Send-Resourcepack-On-Join:

This setting can be set to true to send a pack request, asking the player to download the pack, when they connect to the server.&#x20;

{% hint style="info" %}
**By default**, this is set to **false** but if you are running a server that requires the use of a resource pack, this can be used along with Conditional Commands to force the player to accept the pack by kicking them if they decline.&#x20;
{% endhint %}

{% code title="Line 5 | Settings.yml" %}
```yaml
#When enabled players with the permission RPD.Bypass.Join 
#will not be sent the pack request when joining the server
#(This Wont Do Anything If "Send-Resourcepack-On-Join" is set to False)
Use-Join-Bypass-Permission: false
#This setting can be set to true to send a pack request, 
#asking the player to download the pack, when they connect to the server. 
Send-Resourcepack-On-Join: false
```
{% endcode %}

### Conditional Commands:

conditional commands can be enabled to execute commands from the console when the player accepts, declines, downloads or fails to download the pack. Using the placeholder **%player%** will be replaced with the players username. and using the placeholder **%UUID%** will return the players UUID.

{% code title="Line 7 | Settings.yml" %}
```yaml
#Run after accepting the pack
Accepted-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
#Run after declining the pack
Declined-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
#Run after the successfuly download the pack
Successfuly-Downloaded-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
#Run if there was an error during the download process
Failed-Download-Command:
  Enabled: false
  Command: tell %PLAYER% Your uuid is %UUID%
```
{% endcode %}

### Messages:

This is where you can toggle the messages sent by resource pack downloader.&#x20;

{% tabs %}
{% tab title="Line 19 | Settings.yml" %}
```yaml
Messages:
#Changing these to false will 
#disable the message from Messages.yml being sent to the player.
  Enable-Accepted-Message: true
  Enable-Declined-Message: true
  Enable-Successfuly-Downloaded-Message: true
  Enable-Failed-Downloaded-Message: true
```
{% endtab %}

{% tab title="Messages.yml" %}
```yaml
Accept-Message: '&aYou have accepted the pack request!'
Declined-Message: '&cYou have declined the resource-pack request!'
Successfuly-Downloaded-Message: '&aSuccessfully downloaded the resource-pack!'
Failed-Downloaded-Message: '&cThere was an error downloading the resourcepack, please
  inform the staff members!'
Error-Message: '&6Error: error on checking request!'
```
{% endtab %}
{% endtabs %}

