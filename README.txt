Summary:
This train system is heavily inspired by LTN.  When parameters were first released I started working on making my own pull-based train system.  It has been nearly 2 years of updating it off-and-on and its finally in a state I am happy with. 

Features:
--No mods required!
--Pull-based dispatch system
--Centralized depot with refeulling
--Both common and legendary quality sets included
--Grid-aligned rail segments with roboports, large power poles and red+green wires included
--Configurable train limits and provider station priorities.  
--Dynamic priorities for requester stations with Manual option available
--Solid and Fluid trains are handled separately
--Front and Back loading solid-item stations
--Separate requester stations that can handle spoilable items

Not Supported:
--Multi-item trains/stations
--Depot upgrade from common->legendary

Known Issues:
--Legendary Stations assume Legendary Trains.  Mix-and-matching qualities does work but causes trains to spend extra time at stations to get full loads/fully empty
--Spoilable Requester stations have edge-case where if the chest contents are equal loading will stop.  I haven't found a way to remove this edge case AND handle spoilable items without adding more combinators, but items spoiling will force chest contents to change so its not a huge issue.

Requirements:
The following all need to be setup before the train system will work
--A depot with fuel, from the Stations book
--A fuelled train in the depot, from the Stations book
--A provider station with items, from the Stations book
--A requester station that needs items, from the Stations book
--Rails connecting all of the above.  You can use your own rail blueprints but I have included the simple set I use

How to Use:
Rails:
Globally grid-aligned.  Overlay one segment of rails with existing tracks for the red+green wires to attach.  They are not required(or even used) thanks to Radar signals but I included them anyways.

Depots:
No parameters.  Provide a fuel type to the belt.  The Legendary depot uses requester chests with Legendary Nuclear Fuel by default

Trains:
No parameters.  Place in the depot, make sure they get fuelled and are set to automatic

Provider Stations:
3 parameters: Pick your item, set your train limit, set your priority.  Good rule of thumb: Set your train limit to the number of trains that can wait at the station without blocking the main line.
Fluid stations have the same parameters.  If you want more than 2 trains worth of storage, add 4 tanks per additional train.

Requester Stations:
5 parameters: Pick your item and the number of trains to request.  For priority, it defaults to Dynamic Priority, Max 150 with a range of 50(so 100-150).  Change the Manual Priority parameter to 0 to set priority manually, using the Priority Max value.  Priority Range is unused if you select Manual priority.
Spoilable requester stations have the same parameters.  See Known Issues for why they are separate
Fluid stations have the same parameters.  If you want more than 2 trains worth of storage, add 4 tanks per additional train.  