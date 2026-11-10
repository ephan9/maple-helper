# Maple Helper

A free Mac overlay for MapleStory Classic World. It works like a screen recording: it watches the game window and shows your stats on top of it. It never touches the game itself.

## What it shows

- EXP per hour, time to next level, and session time
- Gain and loss at a glance: your current EXP/hr and mesos/hr are compared to your usual rate on that map, so you can see right away if you're up or down
- Mesos picked up per hour (+) and potion spend per hour (-)
- Party mode: detects when you're in a party and splits your own kill EXP, shared EXP and party bonus, so you can tell if partying is actually worth it
- Item prices when you hover over an item

## How it avoids what gets accounts flagged

Most overlays that get people banned work from inside the game: they read the game's memory, hook into its process, or read its network traffic. That's exactly what anti-cheat looks for.

Maple Helper doesn't do any of that. It's an ordinary Mac app that runs completely outside the game:

- It sees the game the same way a screen recorder does. It uses macOS screen recording permission (the same one OBS or Zoom asks for) to take a picture of the game window a few times a second. Only the game window is captured.
- It reads the numbers in that picture (EXP bar, kill messages, mesos pickups, item names) with Apple's built-in text recognition, on your Mac.
- It draws its overlay in its own separate window that sits on top of the game.

What it never does:

- Read or change game memory
- Inject code or hook into the game process
- Read or send network packets
- Modify any game files
- Send keyboard or mouse input to the game

The only thing that leaves your computer is the item name when you hover over an item, sent to NiaDB to look up its price.

To be straight with you: Nexon doesn't officially approve any third party tool, so no one can promise how they'll treat one. Maple Helper is built to stay away from everything anti-cheat looks for, but use it at your own discretion.

## Credits

Item price data comes from NiaDB (https://meowdb.com). Thanks to NiaDB for the market data.

Status: in testing, public release coming soon.

Contact: eric@phamilyties.com
