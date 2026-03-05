# Project Roadmap

This document outlines the development phases for this Open Tibia Server implementation.

## Phase 1 – Core Infrastructure
- Tibia and Open Tibia file format interpreters (`.dat`, `.otb`, `.otbm`, `.pic`, `.spr`)
- TCP socket management for login and game servers
- Packets and communication protocol (with RSA, Xtea, Adler32)
- Task scheduler thread
- Main game dispatcher thread
- Base objects: Vocation, Rank, etc.
- Base structures

## Phase 2 – Client Interaction
- Premium days
- Message of the day
- Waiting list
- Quests and database storage
- Achievements and database storage
- Hotkeys
- Report bug, report rule violation, debug assert
- Health, mana, soul, capacity

## Phase 3 – Character Control
- Login
- Walking and turning
- Changing outfit (database for outfits/addons)
- Logout

## Phase 4 – Player Communication
- Say (with gamemaster and player in-game commands)
- Whisper, yell
- Direct chat
- Channels and private channels
- Rule violation channel

## Phase 5 – Social Systems
- VIP (database for VIPs)
- Safe Trade
- Party system
- Guild system

## Phase 6 – NPC Interaction
- Private NPC system and NPC channel
- Dialogue
- Buy and sell items / trade window
- Travel and bank account

## Phase 7 – Monster Combat Basics
- Combat controls
- Monster spawn/respawn and despawn (anti-luring)
- Loot, experience, level advancement/downgrade
- Magic level and skills advancement/downgrade
- Rooking, drop bag, drop items, AOL
- Bless (database for blesses)
- Walk, change target, select target and attack strategies

## Phase 8 – Combat Mechanics
- Immunity, mitigation, defense and armor
- Damage type and weapon attack modifier
- Sense invisible and paralysable
- Monster becoming invisible
- Rings and amulets charges
- Item duration (database for item attributes)
- Weapon attributes (range, atk, def, arm)
- Ammunition, bow and arrow, wand and rod, two-handed items

## Phase 9 – Game World Interactions
- Look item (sign items, house doors)
- Move item (stackable, hangable, item attributes)
- Rotate item
- Use item (containers, depot lockers, read/write, quest chest, gate of expertise, ladder/sewer)
- Use item with creature (runes)
- Use item with item (tools)
- Mail (send parcel and letter)

## Phase 10 – Housing and Conditions
- House access list and database storage
- Health and mana regeneration
- Soul regeneration
- Drunk and special conditions
- No-logout zone, logout block, protection zone block, protection zone
- Swimming

## Phase 11 – Systems and Security
- Server status info protocol
- Account manager
- Server save and map clean routines
- Experimental multi-protocol support
- Ban/unban, rate limiting, connection limits
- Anti-spam, maintenance info

## Phase 12 – Plugins and Scripting
- C# DLL plugins
- Lua scripting (actions, ammunitions, creaturescripts, globalevents, movements, npcs, raids, runes, spells, talkactions, weapons, monsterattacks)
- Lua debugging with ZeroBrane
- Lua autocomplete intellisense
- Multi-database support (SQLite, MySQL, MSSQL, PostgreSQL, Oracle, InMemory)

## Phase 13 – Party Shared Experience
- **Party shared experience**: When a party enables shared experience, all eligible party members within range receive equal shares of experience when a monster is killed, rather than proportional-to-damage distribution.
- Eligibility conditions for shared experience:
  - Party member must be alive (on a tile, not destroyed)
  - Party member must be within range of the monster kill (same floor, within 30 tiles)
  - At least one party member must have participated in combat

## Future – Remaining TODO Items
- Fight: war icons, splash damage, summon, convince
- Bed mechanics
- Party spells (Enchant Party, Heal Party, Protect Party, Train Party)
- X-Logging
- Missing 8.60 monsters and monster corpses
- More monster loots and attacks configuration
