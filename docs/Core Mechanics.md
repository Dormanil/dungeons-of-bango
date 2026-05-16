## Core Mechanics

Dungeon Exploration with light randomization and puzzle solving, using 
different types of equipment to push your way through obstacles and delve 
deeper. 

More specifically a grid system like the ones in Mystery Dungeon and Void 
Stranger.

Since we have at least 4 types of weapons in the assets, I want different 
weapons to do different things. A turn system like from a mystery dungeon 
game where a move from you is followed by one from the active enemies. A 
way to make it so enemies can be randomized in every level, maybe allow 
for different things to show up in different rooms instead of enemies, 
like NPCs or items. Some way to generate enemies, like maybe an enemy 
generator of some kind in a room that spawns a set number of them that 
then wanders around while you explore.
### Turns

A turn constitutes one of the actions the player can perform. Switching weapons uses a turn, attacking uses a turn, and moving uses a turn. Certain buffs can gran extra actions the player may use for performing extra movements, or the ability to attack twice in one turn.
### Player Movement

![[Movement.png]]


Movement occurs in a grid environment. The player character can move in any one direction if there are no obstacles in the way. Movement can be slowed by 1 or 2 turns depending on enemy debuffs, but the player may also move twice in one turn depending on if they're buffed or use a special item.
### Enemy Movement

Enemies move in the grid after the player makes their move. Some enemies only move within their room, and some will seek the player vaguely through the map. Enemies can have their movement ranges buffed and debuffed like the player.
### Base Weapons

![[Weapon Ranges.png]]

Since we have at least 4 types of weapons in the assets, I want different 
weapons to do different things. Switching weapons eats up 1 player turn.
#### Sword
One of 4 base weapons. It pierces up to two spaces in front of the player. On a scale of 3, the attack power of its base form would be 1.
#### Bow
One of 4 base weapons. It travels until it hits the first enemy on its path or an obstacle in its path, or the player. On a scale of 3, the attack power of its base form would be 2. Arrows don't move instantaneously, they travel 3 squares upon firing, and 3 squares per turn after.
#### Axe
One of 4 base weapons. Its range covers 3 spaces in front of the player in its base form, hitting any enemy in these 3 spaces. On a sale of 3, the attack power of its base form would be 3. Using it lowers the player's defense by 25%
#### Rod
One of 4 base weapons. Its range can be aimed, targeting an area within 5 spaces in any direction. Aiming a rod attack slows down the player's next turn, letting enemies move one extra time. The area of effect depends on the rod, as does its effects.
### Stats

There are a number of stats that the player and the enemies have. Over the course of the game stats will be raised by better items. There will be no level ups.
#### Hit Points
Base amount of hit points a unit has. May be modified with items or equipment.
#### Strength 
Base strength of a unit, can be modified with weapons
####  Intelligence
Base Magic Strength, cannot crit
#### Defense
Base defense of a unit, can be modified with armor
#### Resilience
Covers debuff resistance
#### Dexterity
Covers base hit rate and crit rate of attacks
#### Luck
Modifies crit rate and hit rate of attacks, makes it more likely to get good outcomes during events.
### Damage, Hit and Crit Formulae

#### Damage Formula

Damage = ((Weapon Attack + Base Strength + Temporary Modifiers + Gear Strength) - (Base Enemy Defense + Enemy Gear Defense)) x crit damage 
#### Crit Rate Formula

Crit rate = (Base Dexterity + Gear Dexterity - (Enemy Base Dexterity + Enemy Gear Dexterity)) x (luck - enemy luck) / 50 
#### Hit Rate Formula

Hit rate = 50 + (Base Dexterity + Gear Dexterity - (Enemy Base Dexterity + Enemy Gear Dexterity)) + (luck - enemy luck) / 2 % 
#### Crit Damage formula

Crit Damage = 2.0 if crit else 1





