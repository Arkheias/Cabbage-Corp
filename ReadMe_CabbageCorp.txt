(This file is best viewed with a monospaced font)
==============================================================
       Title:  Cabbage Corp + Cabbage Corporate Command       
==============================================================
Game Version:  1.6b2
 API Version:  26
 Mod Version:  v0.7.4.0-development (Still an alpha release)
Release Date:  2015-05-06
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
