---------
Changelog
---------

v0.7.5.5 (2016-02-15)
---------------------------------
-----General Changes-----
Updated for Transcendence v1.6.4.
Added catfighter and PhaseMacaw to the credits list.
Removed deprecated information from README files.

-----Dockscreens-----
Changed various dockscreens to match vanilla Transcendence standards.
Fixed bug with closing dockscreens after opening "Cabbage Corp Toolset" dockscreen.

-----Items-----
Changed description of diplomatic identification chip.
Changed diplomatic identification chip to be usable only when uninstalled.
Fixed repairTech of advanced Sivaya armor (changed from 3 to 9).
Fixed regen of 4x-layered hardened Sivaya armor (changed from 55 to 5).



v0.7.5.4 (2016-01-16)
---------------------------------
-----General Changes-----
Fixed changelog.



v0.7.5.3 (2016-01-16)
---------------------------------
-----Globals-----
Changed commenting in global functions.

-----Items-----
Changed all repairer devices to have a lower upper limit for the levels of the armors that they can repair.
Changed all repairer device descriptions.
Changed the outputs of most solar devices.
Changed all solar device descriptions.
Changed descriptions of all advanced ore refineries.
Changed description of Cabbages to adjust for global warming.

-----Resources-----
Changed the resource CCPraclarushHangar.jpg to a derivative of two public domain images to simplify copyright labelling.



v0.7.5.2 (2016-01-09)
---------------------------------
-----Globals-----
Changed the CCDeviceExchange global function to work for all types of enhanced devices.

-----Dockscreens-----
Changed the Cabbage Corp Toolset "Factory Reset" action to be more robust.
Changed the Cabbage Corp Toolset "Factory Reset" action to have a small chance of damaging/disrupting devices.
Changed the Cabbage Corp Toolset "Modify" action to exit the screen after completing.
Changed the Cabbage Corp Toolset "Factory Reset" action to exit the screen after completing.
Fixed bug where the Cabbage Corp Toolset "Factory Reset" action relied on separate item filters.
Fixed bug where the Cabbage Corp Toolset appeared for unidentified items.
Removed armor items from the Cabbage Corp Toolset list.



v0.7.5.1 (2016-01-04)
---------------------------------
-----Ships-----
Added "auton" to the type value for all autons.
Removed "auton" from the class value for all autons.
Removed howitzers from the types of weapons that lampyridae-class ships offer a swivel mount for.

-----Items-----
Added a new icon for the series of shield emitter arrays.
Changed name of "Cabbage Corp system map access ROM" to "system map access ROM".
Changed the "system map access ROM" to charge more credits for higher level systems.
Fixed bug in which the Cabbage Corp system map access ROM charged the wrong amount of credits.
Fixed bug in which replacement emitter coils did not work unless identified first.



v0.7.5.0 (2016-01-01)
---------------------------------
-----General Changes-----
Updated to API v28 for Transcendence v1.6.3 for real this time.
Replaced deprecated functions.

-----Stations-----
Added Cabbage Corp School of Science to the S. Katherines Arcology University Quarter.
Changed the stargate in Othala to actually transport the player back to the main stargate network instead of itself.
Removed the text from the stargate in Othala that mocked the player after trapping them there.

-----Ships-----
Changed the reactors installed on ships due to rebalancing of said reactors (nearly all are higher capacity).
Changed the fireAccuracy value on wraith autons.
Changed the Lorry-class transports to have 10 device slots.
Changed the Lampyridae-class transports to have 11 device slots.

-----Items-----
Added a series of shield emitter arrays.
Added replacement emitter coils for the shield emitter arrays.
Added Heliotrope fuel assembly.
Changed idlePowerUse of Sivaya armor segments to 1/10 the PowerUse value.
-This is in preparation for API 29 (Trancendence v1.7). It will not take effect until then.
Changed the Siva series of reactors to be more balanced.
Changed auxiliary reactors to be cheaper and lighter.
Changed the Kale series of repeaters to fire in a tighter cluster.
Changed the Kale series of repeaters to have more consistent damage.
Changed the descriptions of the Kale M1 and M3 repeaters.
Changed damaged refineries to display more generic text explaining which refinery doesn't work.
Changed plasma drive variants to have slightly more thrust.
Changed descriptions of Cabbage Corp fuel assemblies.
Fixed bug where none of the mining lance capacitors actually enhanced mining lances above level 1.
Removed the Cabbage Corp brand enhancers.
Removed external shield deflectors.



v0.7.4.3 (2015-10-07)
---------------------------------
-----General Changes-----
Updated to API v28 for Transcendence v1.6.3 (nothing had to actually be fixed).
Added new data for various devices to the readme.
Changed the readme to have more consistency.

-----Ships-----
Added 'remaining cargo space' indicator to the dockscreens for Shade-class autons.
Changed maxCargoCapacity on Shade-class autons to be twice the standard cargoCapacity.
Changed <StaticData> name for a ship's base crew capacity from "maxAuxCrew" to "crewCapacity".
Fixed error where docking with any Shade-class auton showed the description "You are docked with a mark I Shade auton."

-----Items-----
Changed auxiliary crew installation checks to be more efficient and readable.
Changed the name of the "diplomat's cargo bay" variations to "diplomat's cargo hold".
Changed descriptions of Shade-class autons.
Changed descriptions of Wraith-class autons.
Changed descriptions of Cabbagium armors.
Changed descriptions of DRADIS modules.
Changed descriptions of auton bays.
Changed descriptions of a miscellaneous item.
Changed descriptions of cargo holds.
Changed the whitespace and commenting standards for various things, not completely updated yet.
Fixed crew quarters uninstallation checks to be correct, efficient and readable.
Fixed crew related installation/uninstallation checks to allow for base crew capacity to be explicitly defined as 0.
Fixed Military crew members so they will no longer be arrested when you dock at commonwealth stations without a military ID.



v0.7.4.2 (2015-08-04)
---------------------
-----Stations-----
Fixed bug where buying a modified item from a Cabbage Corp Station via the "Buy & Modify" button gave you the item for free (or basically free).



v0.7.4.1 (2015-08-04)
---------------------
-----Ships-----
Fixed error in the description of the lorry-class stealth transport that starts in Tau Ceti.

-----Items-----
Added invoke button to Siva reactors when they are being run without containment so that you can quickly restore containment.
Changed unstable Siva reactors to explode sooner once they start overloading.
Changed mining lance enhancers to provide different bonuses depending on the level of the weapon they are enhancing.
Changed the descriptions of mining lance enhancers to match their new effects.
Changed the effect of the mark V repeater heat sink to match the trend of the other heat sinks.
Changed the descriptions of the repeater heat sinks.
Changed really high level enhancers to use the alien unknown device type.
Changed the level 1-4 reactor explosion to do more damage.
Changed the level 11-15 reactor explosions to do plasma damage.
Changed the Cabbage Corp system map access ROM to require more credits for higher level systems.
Fixed values of higher level mining lance enhancers because I forgot to set them correctly when I first created them.
Fixed a bug in the criteria for the mining lance enhancers that would enable them to affect the other unrelated Cabbage Corp energy weapon.



v0.7.4.0 (2015-08-03)
---------------------
-----General Changes-----
Updated to API v27 for Transcendence v1.6.1.
Temporarily removed Playership Drones (PSD) support due to changes in v1.6 making it not work correctly.
Moved changelog from the general readme file to its own readme file.
Added a line of hyphens underneath version numbers in the changelog.
Added version information to extension and library header files.
Changed the general readme into a fancy .pdf file.

-----Stations-----
Removed mass from outpost turrets (they weren't even marked as mobile and (some) stars have gravity now).
Changed Cabbage Corp outposts and their turrets to use image variants that match their asteroid fields.
Updated the Buy & Modify item screen to use the same implementation as the new default item buying screens.
 -It no longer shows items for which the station does not have the resources to make, previously it showed them but deactivated the button to buy them.
 -(The options are all standardized anyway and there is another menu to show all potential custom devices/armor.)

-----Ships-----
The Corporate Command playerships extension now includes the Eridani starting location for playerships in addition to Tau Ceti.
Fixed image for Oboroguruma-class stealth freighter in PSD menus.
Lampyridae-class stealth transports now use the correct number (8) of armor segments in PSD.
Adjusted the starting and PSD equipment on the Lampyridae and Oboroguruma.
The locations of the armor segments on the Oboroguruma now correspond to the actual locations of the armor segments on the Oboroguruma
Reduced device slots on ships because not having a default reactor is no longer adequate justification due to v1.6b5 changes.
 -The Lorry-class now has 9 device slots instead of 10.
 -The Lampyridae-class now has 10 device slots instead of 12.
 -The Oboroguruma-class now has 15 device slots instead of 16.
Increased maximum armor capacity of the Oboroguruma-class to 40 tons from 20 tons.

-----Items-----
Added new image for solar devices.
Added new image for DRADIS devices.
Added new images for autodefense devices.
Added Phantom-class reconnaissance auton series (Levels 2, 4, 6, 8, and 10).
Added Cabbage Corp Tinkerer ID (Will eventually unlock aditional options when modifying Cabbage Corp devices).
Added proto-Cabbagium catalyst.
Added pygmy ostrich horses.
Added Cabbagium armor sets to replace both trinium and organic armor sets.
Added the default hit-effects to the mining lances.
Added miningEquipment attribute to mining lances, refineries and miner's cargo holds so that they will appear in v1.6 mining stations.
Changed the Cabbage Corp Toolset to not appear unless the playership has Cabbage Corp equipment installed (like I originally advertised it).
Added Microsaur scanner effects and scripts.
Added Microsaur condemnation pods and relevant effects.
Changed low level (Levels 1-2) reactors to notRandom.
Changed dual reactors to appear less often (Levels 3-5 veryrare, everything else is notRandom).
Changed auxiliary reactors to now shut themselves off automatically if your ship is really low on fuel.
Changed auxiliary reactors to now be half as efficient when damaged.
Changed auxiliary reactor efficiencies (civilian: 85%, military: 90%, alien: 95%).
Changed unstable reactors to now have custom explosions when they overload.
Changed unstable dual reactors to now explode twice when they overload.
Changed unstable reactor to have a higher chance of exploding at lower levels but a much lower chance at higher levels.
Changed unstable reactors to last slightly longer before exploding, once they start overloading.
Changed cabbages for balance and updated their descriptions.
Changed misc. items to match new whitespace standard.
Changed generic device images to be reorganized into separate file from generic item images.
Changed the damage of most mining lances to be twice as high so that they will work better with the new mining update.
Changed the firing rate of most mining lances to 4 (from 2) to fire half as fast to balance them accordingly.
Changed the level of all scanning mining lances by 1 level higher than their standard versions.
Changed ore scanner effects and scripts by moving them to the appropriate dedicated files.
Changed MiscItems.xml to be split into MiscItems.xml and UsefulItems.xml for usable items.
Fixed typo in the name of the mark I wraith auton.
Fixed typo in the description of the mark V wraith auton.
Fixed typo in the attributes list for the Cabbage Corp premium memberhip ID and changed frequency to notRandom.
Fixed bug where side-mounted repeaters did not actually fire alongside the primary weapon.
Fixed bug where dual repeaters fired both sets of shots from the same location.
Removed trinium armor sets and organic armor sets.
Removed excess spacing in the names of stealth and sivaya armor sets.
Removed minerGear Attribute from mining related devices as it has been replaced by miningEquipment.

-----Known Bugs-----
Mining colonies reset their inventory of miningEquipment labelled devices each time you enter their system
 *They normally have one of every item labelled as miningEquipment but I have added a script that runs when you enter their systems
  that removes all their Cabbage Corp mining devices and replaces them with just a few random Cabbage Corp mining weapons (up to 1d4 devices)
  and a few random Cabbage Corp mining non-weapons (up to 1d4 devices).



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

-----Items-----
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