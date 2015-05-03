(This file is best viewed with a monospaced font)
==============================================================
       Title:  Cabbage Corp + Cabbage Corporate Command       
==============================================================
Game Version:  1.6b2
    API Version:  26
  Mod Version:  v0.7.3.0 (Still an alpha release)
 Release Date:  2015-05-01
           Author:  Arkheias
          License:  CC BY-NC-SA (Creative Commons Attribution-NonCommercial-ShareAlike)
==============================================================

-----------
Description
-----------

This adds a corporate empire known as Cabbage Corp which manufactures/produces weapons, armor, reactors, drives, autons, shields, bok choy, napa Cabbages, green cabbages, red cabbages, kohlrabi, savoy cabbages, brussel sprouts, kale and other various items/devices.  Cabbage Corp runs their own stations and refineries, and each of their devices comes with a Cabbage Corp Toolset so that it can be modified for your survival.  

This is an alpha release, I am currently going back through the mod and rewriting items so they are all nearly perfectly balanced. I got excel sheets for each set of items and everything.  I have tested this out well enough so that nothing should be blowing up on accident, but I haven't actually played through a game using this mod in several months (I started working on it around July 2014).



-----------------------
How to install this mod
-----------------------

Download and extract the mod into your "Extensions" folder, which should be in your Transcendence folder.

*Don't mess with the folder hierarchy


Start the game.


If you don't have Corporate Command installed and don't want new and fancy playerships,
enable "Cabbage Corp".

If you have Corporate Command installed and don't want new and fancy playerships,
enable "Cabbage Corporate Command".


If you don't have Corporate Command installed and want new and fancy playerships,
enable "Cabbage Corp Ships & Stuff".

If you have Corporate Command installed and want new and fancy playerships,
enable "Cabbage Corporate Command Ships & Stuff".


Do not use more than one version at the same time.



------------
Crew Members
------------
Hiring crew members is a way to increase the strength of your ship even after you have run out of device slots.  Crew member's contracts are generally more expensive than the equivalent devices, and crew members can only be hired from Cabbage Corp stations by viewing their special deals.  They are balanced by only being obtainable via paying large amounts of credits and requiring power from your ship for their life support and powered tools.  Ships are also limited in how many crew members they can support due to life support system constraints, which can be increased by installing cargo holds with support for extended life-support systems.  Damage control crews are the only crew members whose job benefits from having multiple crews working side-by-side.

Current crew members that can be hired include:
 -Damage control crews which repair damage to armor.
 -Weapons engineering crews which make energy weapons more powerful and make non-energy weapons fire faster.
 -Shields engineering crews which strengthen shields.

 *I will hopefully eventually enable gunner crews which will make your primary weapons omnidirectional at the cost of a reduced firing-rate.


For custom ships:

To specify the base crew capacity of a ship, add this to it:


	<StaticData>
		<maxAuxCrew>##</maxAuxCrew>
	</StaticData>
</ShipClass>

See CCShips.xml for examples.


To specify the additional crew capacity provided by a device, add the following to it:

	"crewQuarters" 
		;to the device's attributes

	inherit=			"&vtCCCrewQuartersBaseClass;"
		;after  "attribute="
		
	<StaticData>
		<addCrewSpace>##</addCrewSpace>
	</StaticData>
</ItemType>
		;to replace the end of the ItemType definition.

See CCDevices_CargoHolds.xml for examples.


From the default settings:
Player ships:			base crew capacity:

EI500-class freighter		4
Sapphire-class yacht		1
Wolfen-class gunship		0

Osaka-class transport		2

Constellation-class freighter		2
Freyr-class gunship			1
Manticore-class heavy gunship	1

Ships without a defined crew capacity:	(cargo capacity / 50), rounded down

suggested base crew capacity:	(cargo capacity / 50), rounded down, +1 if transport

-------------
Compatibility
-------------

Base game:
Does not overwrite any items, objects or things from the base game though it does add new actions to existing dockscreens.

If you have any Cabbage Corp devices installed on your ship, you can access the Cabbage Corp Toolbox to modify or use them in the case of refineries.

I have added a new action to the arrest screens of corporate stations that will appear if you have a diplomatic ID so that you have the option to undock.  I will eventually change this into an option to bribe away your criminal record, but for now it just lets you undock with an implied claim of diplomatic immunity.


Mining Pack:
Includes an alternative to the magic-omni-refinery (specialized refineries for each fuel ore that create roughly 1.5x more fuel.
-There are also advanced refineries that create assembly versions of fuel rods (3x more efficient than the omni refinery).
Includes a set of continuous mining beams (includes dual, omni, side-mounted and scanning versions).
*These all have the attribute minerGear and will possibly show up in Mining Pack mining stations.

*I will hopefully eventually include mining weapons that don't do damage to enemy ships.  (I'm thinking that they won't actually fire anything, but upon pressing the button to fire them an <OnFireWeapon> event could be used to generate a mining beam from a virtual mining weapon that wouldn't be associated with any ship and would only do EMP damage just so that it counts as weaponsfire and can hit targets.


Black Market Expansion (BME):
Includes an alternative to smuggler's cargo holds.  It's an expensive slotless miscellaneous device with the attribute smugglersHold.  I mention this because I'm not exactly sure how BME changes how your ship is searched for contraband, but this item will still probably help to some extent.
-This also includes a diplomat's cargo hold and military cargo holds.



----------
Changelog
----------

v0.7.3.0 (2015-05-01)
-----General Changes-----
Switched to ISO 8601
Updated deprecated functions.
Watched as other functions became deprecated.
Organized the various modules and resources.
Began plans to separate libraries from items, will likely have at least two libraries: 
 -one for globals, dockscreens and base/virtual items, 
 -the other for items and sovereign information to be used for the playserships that will be kept in a separate extension (and will be dependent on the playership drones (PSD) mod).

-----Stations & Dockscreens----
Added "Buy & Modify" actions to Cabbage Corp stations for standard versions of mining lances, howitzers, repeaters, cargo holds, drives, reactors, and stealth armor.
 *This dockscreen was designed for Transcendence v1.5. I fixed it so that it would still work for v1.6b2 but you are limited to only buying items from this menu, you cannot buy and install items in one step, I think.
 -Dual, omni, aux and scanning versions will not normally appear in Cabbage Corp stations now, but you can buy them by choosing the "Buy & Modify" option.
 -I will eventually replace this with a version based off of Transcendene's newer dockscreens in some future update.
 *This dockscreen was designed for Transcendence v1.5. I fixed it so that it would still work for v1.6b2 but you are limited to only buying items from this menu, you cannot buy and install items in one step, I think
  *(even if they have been further updated such that they have become even worse than the old dockscreens).
Cabbage Corp stations should now actually check for a premium membership ID when using the "Buy & Install" option to determine whether or not they check for a military ID.
Fixed critical bug in shield modification screen that prevented the player from getting back to the cockpit.
 *(I don't think this was even in the previously released version, but it appeared at some point and I had to fix it).
Cabbage Corp Outposts are now hidden. Don't look for them.
Cabbage Corp stations have been moved to their own separate .xml files and updated to use Transcendence v1.6b2's fancy new dockscreens (to some extent).
Cabbage Corp stations now use patrolling autons for defense instead of having the stations be armed.
 *The fact that autons are cheaper than the weapons they carry means that the stations are now generally better defended at a lower cost.  

-----Ships-----
Fixed bug in display of Kraken-class mini-dreadnought.
 *(The unid was previously used for the cover image and I had only updated it in the library .xml, the extension .xml reused the old unid).
Set npc traveler-class ships to guard instead of gateonthreat, did the same with the kraken-class.
Replaced Traveler-class havy transports with Lorry-class stealth transport.  Removed kraken-class mini-dreadnought.
Created the Blacklight-class stealth frigate npc ships (does not appear ingame, I think).
Created the Oborogurama-class stealth freighter.
 -I will add missions and whatnot at a later date.
Created 2 auton series (Levels 2, 4, 6, 8, and 10), levels 4 and higher (Mark II through Mark V autons) support 5 ton armor segments.
 -Wraith-class assault auton
 -Shade-class transport auton
*These autons work well with the Souped up Auton Bay mod, I think.
The two Cabbage Corp versions, "Cabbage Corp" and "Cabbage Corporate Command" (for people with Corporate Command installed) have been separated into two versions with and without playerships.
 -The playerships extensions are dependant on PSD v6.
 -Only one of these four extensions should be selected when starting the game.
Ships now have their facings image organized like the ships from eternity port.  It is much nicer to look at when looking at the raw files.
Ships now have fancy inventory icons (some are fancier than others, I think).
Fixed bug that appeared at some point and may have allowed players to install 5x more crew members than they should have been able to for custom playerships without specified crew capacities.

----Items-----
Replaced Kale series of repeaters. It now has standard, dual, omni, and side-mounted versions.
Updated enhancers
 -Removed general enhancers, and dual enhancers
 -Added 'repeater heat sinks' which speed up Cabbage Corp repeaters.
 -Added 'mining lance capacitors' which increase damage output of Cabbage Corp mining lances.
Created stealth armor series.
Replaced the Sivaya armor series (previously a Novaya ripoff) with a better version
 -Sivaya armor now works as a combination of solar armor and power armor.  
Created a nanofac series, they're like the Corporate Command device but fully modular.
Updated the Siva reactor series and added a completely unrelated auxiliary Siva reactor series.
 -Siva reactors now have a high output mode with a delightful special effect that kicks in if you use it for too long.
 *Aux Siva reactors may occasionally prevent your ship from ever actually running out of fuel, I think this only happens if they are the only device currently enabled but I am too lazy to do further testing.
Added DRADIS modules that increase the perception of ships that install them, so long as said ships are not piloted by the player.
Updated descriptions of Savoy howitzers, and several other items that I forgot to keep track of.
Fixed name of expanded diplomat's cargo hold, dual shields, and several other items that I forgot to keep track of.
Added things man was not meant to know.
Rebalanced the pointless set of CPUs, and several other items that I forgot to keep track of.
Replaced all item masks with .bmp versions because the .jpg versions get screwed up when they appear in the 'use items' menu, the ship masks still appear to work perfectly so they stay as .jpg.
Forgot about a bunch of other changes that I made.



v0.7.2.1 (01/27/2015)
Fixed the descriptions for Cabbage Corp brand enhancers to show the correct enhancement from the change in the v0.7.2 update.



v0.7.2 (01/27/2015)
Replaced autodefense devices.
Rebalanced solar devices (and impulse drives)
Nerfed Cabbage Corp brand enhancers and added fancy graphics to them.
Replaced cargo holds with balanced and simplified versions.
 -'Miner's cargo holds' and 'imitation auton bays' have been combined into 'miner's cargo bays'.  
 -All dual versions of cargo holds are balanced as if a standard cargo hold was just tacked on, instead of having dozens of versions for each possible combination of cargo hold.
 -Cabbage Corp cargo holds now increase crew capacity.
Decreased momentum and recoil on Savoy howitzers.
Added new crew members:
 -Weapons engineers: increases damage output (energy weapons) or fire-rate (matter weapons).  
 -Shields engineers: enhances shields
 -Crew members now have icons.
 -Crew members now have souls.
 *Inherit from &vtCCCrewQuartersBaseClass;, add <StaticData> <addCrewSpace>##</addCrewSpace> </StaticData> and include the attribute crewQuarters to make a device increase crew capacity.
Modified the Cabbage Corp playerships:
 -Decreased the maximum rotation rate (9.0 -> 7.5).
 -Removed launcher from tau ceti ship.
 -Switched armor from heavy titanium to light organic (it's blue).
 -Decreased starting credits.
 -Decreased maximum cargo capacity (300 -> 250)
 -Decreased base cargo capacity (50 -> 10)
 -Added a small cargo hold to player ships to negate the decrease in standard cargo capacity (+40).
Modified stations:
 -Switched to the fancy v1.5 dock services screens.
 -Fixed the custom devices recipe list that was blank because it had items that no longer existed in it.
 -Overhauled and unified the dockscreens.
 *Cabbage Corp IDs and ROMs are no longer spawned on the stations and have to be purchased through a menu.
Added new images for items.
Replaced all instances (that I found in one pass) of the Cabbage attribute (original Cabbage Corp brand identifier) with the cabbageCorp attribute (newer Cabbage Corp brand identifier), though I still need to get around to replacing the semicolons with commas to match the new apparent standard.
 *This means that Cabbage Corp stations should now show all Cabbage Corp items and the Cabbage Corp brand enhancers should enhance all relevant Cabbage Corp devices.  I was previously replacing them as I rebalanced the devices and forgot that the stations were only set to show devices with the old atribute.
Updated cover image
Added credits for public domain stuff and new licensed stuff.



v0.7.1 (01/09/2015)
Added Dual, Omni and side-mounted Savoy howitzers.
Added damage control crew.
 -Created a pseudo-class of devices that simulate having crew members on your ship.
 -Use the base class "&baCCAuxCrewBase;" and add the attribute "auxCrew" to have a device act like a crew member.
 -The maximum amount of crew members a ship can carry defaults to 2, add <StaticData> <maxAuxCrew>###</maxAuxCrew> </StaticData> to a custom ship to override this.
 -Crew members from the this mod can be thought of as being hired on contract for the duration of your journey to the galactic core.
Cabbage Corp stations will now offer to upgrade your shield generator to a Jadeite class deflector of the same level as the current system.
 -There is a 40% chance they will instead offer you a crew member of the same level.
Added credits for the authors of some stuff that I forgot I included and thus forgot to add credits for in the previous release.
Moved resources necessary to making the Cheops-class Warship playable over to its page.
 -Since it's required anyway to play use Cabbage Corp, I didn't see any problem with adding further requirements that you have to include it to play this game.  
 *Only the resources are currently required from the Cheops mod.
 *The CheopsWarshipExtension.xml exists solely to add the Cheops-class warship as a playership.  It will never be required for Cabbage Corp as I am against cluttering the playership selection screen.
 *The CheopsWarshipLibrary.xml is not currently required for Cabbage Corp, but I may eventually decide to move all Cheops related ships/items/whatnot over to this file for OCD purposes, in which case this file and the resources would be required.



v0.7.0 (01/01/2015)
Initial release



---------------------------------------------------------------------
Blender Rotation Code (because this should be more readily available)
---------------------------------------------------------------------

http://forums.kronosaur.com/viewtopic.php?f=5&t=5683&p=51673&hilit=steelwing#p51673

# Transcendence - Render facings for ship model
# by steelwing, edited by RPC, further edited by Arkheias for 120 facings
# Make sure you've got your ship set up facing the right way to start.
# Your ship must be the only selected object.

# Set this for the path and filename to use.  Leave the %i intact, as it's used to number the files.
output_filepath = '//facings2\\facing_%i.png'
# specify render format (make sure the extension above matches)
output_format = 'PNG'

import bpy
from math import radians
# Set output format
bpy.context.scene

#loop for 120 facings
for x in range(1,121,1):
 bpy.context.scene.render.filepath = format(output_filepath % x) # set filename to save to
 bpy.ops.render.render(write_still=True) # perform render
 bpy.ops.transform.rotate(value=(radians(3),)) # rotate to next angle

#After this, use a program such as Irfanview to stitch the facings together into a vertical panorama
#May be beneficial to use a program such as advanced renamer to make sure that all images have the same number of digits in them so that they can appear in the right order without manually sorting them
#i.e., convert 1, 2, 3, ... 9, 10, 11, ... 99, 100, 101, ... to 001, 002, 003, ... 009, 010, 011, ... 099, 100, 101, ...
#something something masks...

---------------------------
*Special Thanks and Credits
---------------------------

George Moromisato - The author of Transcendence.

PM - Made the 120 facing graphics for the Kobol ship (cause I still have no idea how to manipulate the files from TransArt101.zip) and the armor huds that I appropriated for my reinterpretation of the Kobol Ship and the code for the helium fuel converters that I appropriated and rewrote into fuel-ore refinery devices

Star Weaver - Made a working implementation of implantable ID chips... (someone should really make an updated version of that mod, I only included implantable versions of Cabbage Corp IDs).

Kiel Cravatta - Made The original version of the image which I have edited into CCPraclarushHangar.jpg (Google Images reported it as "labeled for reuse with modification" and implied that commercial use was fine too).
	http://kielcravatta.com/

The image used for the cover (CCCabbageCorpCover.jpg) is a derivative of the public domain image "M74: The Perfect Spiral" and a picture of a cabbage.
	http://apod.nasa.gov/apod/ap130811.html
	http://www.dreamstime.com/stock-images-green-cabbage-isolated-image21864594 © Neil Overy | Dreamstime.com
	*Derivatives of this cabbage are also included in other resources

The images and masks (CCCrewMembers.jpg and CCCrewMembersMask.jpg) used for the crew members are derivatives of the "Elite Captains Icons" iconset and the "Elite Soldiers Icons" iconset by IconTexto (Bruno Maia), used under CC BY-NC.
	http://www.iconarchive.com/show/elite-captains-icons-by-icontexto.html
	http://www.iconarchive.com/show/elite-soldiers-icons-by-icontexto.html
	http://www.iconarchive.com/artist/icontexto.html
	http://creativecommons.org/licenses/by-nc/4.0/
