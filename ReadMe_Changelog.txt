---------
Changelog
---------

v0.7.4.0-development (2015-05-05)
---------------------------------
-----General Changes-----
Moved changelog from the general readme file to its own readme file.
Added hyphens underneath version numbers in the changelog.
----Ships-----
Fixed image for Oboroguruma-class stealth freighter in PSD menus.
Lampyridae-class stealth transports now use the correct number (8) of armor segments in PSD.
Adjusted the starting and PSD equipment on the Lampyridae and Oboroguruma.
The locations of the armor segments on the Oboroguruma now correspond to the actual locations of the armor segments on the Oboroguruma
----Items-----
Auxiliary reactors should now shut themselves off automatically if your ship is really low on fuel.
Added Phantom-class reconnaissance auton series (Levels 2, 4, 6, 8, and 10).
Fixed typo in the name of the mark I wraith auton.
Fixed typo in the description of the mark V wraith auton.



v0.7.3.0 (2015-05-01)
---------------------
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
---------------------
Fixed the descriptions for Cabbage Corp brand enhancers to show the correct enhancement from the change in the v0.7.2 update.



v0.7.2 (01/27/2015)
-------------------
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
-------------------
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
-------------------
Initial release