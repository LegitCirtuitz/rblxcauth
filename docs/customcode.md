# Running Custom Code #

!!! danger
    This Section Contains Information about Running Custom Code. DO NOT run code unless you know what you are doing.

### Custom Settings
In order to set a new custom setting, follow the steps below.
Firstly, Add the Setting variable in CAuthConfig Located in ``ServersScriptService``.
``` lua
-- under settings, add your desired variable and define it.
-- SETTINGS --
YourVar = true/false

-- Then add it to the return block of the OnServerInvoke block.

GetStatusRF.OnServerInvoke = function(player)
	return 
		GameLoad,
		informCLData,
		master,
		HealthBarGui,
		HealthbarName,
		CheckDebugVersionGui,
		VersionGui,
		EnableCAUTH,
		CauthHidePrint,
		CauthHidePrintTime,
		ShowGameDebug,
		CheckEnabledGuis,
		LogGuiStateChanges,
        YourVar
end
```
After Adding your Variable in the CAuthConfig, add it to Invoke the Server in the Client Code in CAuthClient.

``` lua
-- On Line 23, add it to the back / last part of the Line using the format below.
local GameLoaded1, iCLD, mastere, HBGui, HBCGui, CDV, VersionName, ECAUTH, CHP, CHPT, ShowGD, CEG, LGSC, YourVar = GetStatusRF:InvokeServer()
-- Then Define it in the CAuth() function and then in the mastere if statement.
if Yourvar == value then
    -- put your code here
end
```
And its that Simple to add your own setting in CAuth.

### Preloading Fonts
!!! info
    see [Fonts](fonts.md) for the default Preloaded fonts in CAuth.

Preloading Fonts is extremely simple. It only takes 1 line of code.
Just Add your Font into the fonts table. For Example I want the Comic Neue Angular Font.
``` lua
local fonts = {
	Font.new("rbxasset://fonts/families/LegacyArial.json"),
	Font.new("rbxasset://fonts/families/Arial.json"),
	Font.new("rbxasset://fonts/families/ArialBold.json"),
	Font.new("rbxasset://fonts/families/Roboto.json"),
	Font.new("rbxasset://fonts/families/RobotoMono.json"),
	Font.new("rbxasset://fonts/families/SourceSansPro.json"),
	Font.new("rbxasset://fonts/families/SourceSansLight.json"),
	Font.new("rbxasset://fonts/families/GothamSSm.json"),
	Font.new("rbxasset://fonts/families/Nunito.json"),
	Font.new("rbxasset://fonts/families/Oswald.json"),
	Font.new("rbxasset://fonts/families/PatrickHand.json"),
	Font.new("rbxasset://fonts/families/PermanentMarker.json"),
	Font.new("rbxasset://fonts/families/Bangers.json"),
	Font.new("rbxasset://fonts/families/Creepster.json"),
	Font.new("rbxasset://fonts/families/DenkOne.json"),
	Font.new("rbxasset://fonts/families/Fondamento.json"),
	Font.new("rbxasset://fonts/families/FredokaOne.json"),
	Font.new("rbxasset://fonts/families/Guru.json"),
	Font.new("rbxasset://fonts/families/IndieFlower.json"),
	Font.new("rbxasset://fonts/families/Inconsolata.json"),
	Font.new("rbxasset://fonts/families/JosefinSans.json"),
	Font.new("rbxasset://fonts/families/Jura.json"),
	Font.new("rbxasset://fonts/families/Kalam.json"),
	Font.new("rbxasset://fonts/families/LuckiestGuy.json"),
	Font.new("rbxasset://fonts/families/Merriweather.json"),
	Font.new("rbxasset://fonts/families/Michroma.json"),
	Font.new("rbxasset://fonts/families/Migae.json"),
	Font.new("rbxasset://fonts/families/Montserrat.json"),
	Font.new("rbxasset://fonts/families/SpecialElite.json"),
	Font.new("rbxasset://fonts/families/TitilliumWeb.json"),
	Font.new("rbxasset://fonts/families/Ubuntu.json"),
	Font.new("rbxasset://fonts/families/Zekton.json"),
    Font.new("rbxasset://fonts/families/ComicNeueAngular.json") -- Put your font path as a rbxasset file.
}
```
You can refer to [Roblox Fonts](https://create.roblox.com/docs/reference/engine/datatypes/Font) for all fonts.
