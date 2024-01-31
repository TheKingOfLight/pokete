This repo contains some custimasations to the original pokete: ![Pokete](https://github.com/lxgr-linux/pokete)
For changes see bottom:

# Pokete -- Grey Edition

![Example](assets/ss/ss01.png)

[See more example pics](assets/pics.md)
## What is it?
Pokete is a small terminal based game in the style of a very popular and old game by Gamefreak.

## Installation
For Linux, BSD etc. just do this:
```shell
$ git clone https://github.com/lxgr-linux/pokete.git
$ ./pokete/pokete.py
```

You can also install it from the AUR:
```shell
$ buildaur -S pokete-git
```

Or you can just run the AppImage from the release page.

NOTE: In that case you first have to create the `~/.cache/pokete/` folder.

For OSX:
```shell
$ git clone https://github.com/lxgr-linux/pokete.git
$ ./pokete/pokete.py
```

For Windows:

Some windows antivirus may flag the `libplaysound.dll` as malicious. If pokete crashes, please make sure that the .dll exists and is **not** in quarantine!

```shell
git clone https://github.com/lxgr-linux/pokete.git
```
To run just execute `pokete.py`.

If you have problems with your ARCH you maybe need to rebuild the audio module, see [here](playsound/README.md).

## Usage
The game can be run normally without supplying any options.
For non gameplay related usage, use `--help`.
Try it out [online](https://replit.com/@lxgr-linux/pokete).

## How to play
Imagine that you're a Pokete Trainer and you travel around the world to catch/train as many Poketes as possible with the ultimate goal of becoming the best trainer.

First of all you get a starter Pokete (Steini), that you can use to fight battles with other Poketes.
Use W, A, S and D to move around.

When entering the high grass (;), you may be attacked by a wild Pokete. By pressing `1` you can choose between the attacks your Pokete has (as long their AP is over 0). By pressing the according number, or navigating with the `*` cursor to the attack and pressing `Enter` you can use the attack selected. The wild Pokete will fight back, but you can kill it and gain XP to level up your Pokete. If you would like to catch a wild Pokete, you must first weaken it and then throw a Poketeball. With a bit of luck, you can catch it and have it fight for you.

By pressing the `1` key, you can take a look at your current deck. You can see detailed information of your Pokete and your attacks, or rearrange them.
Changes will only be saved by quitting the game using the exit function.

Since you're a Pokete Trainer, you can also fight against other trainers (they appear as an 'a'). He will start a fight with you when you get close enough to him. You can not run from a trainer fight; you either have to win, or lose. These trainer fights give double the XP.

When one of your Poketes is too weak or dies, you can heal it by going into the Pokete Center (the house), talk the the person there and choose the healing option.
Here you can also take a look at all of your Poketes, and not just the six in your team. The ones marked with an `o` are the ones in your deck.

By pressing `e`, a menu will appear where player name, and later other settings, can be changed.

The red balls all over the map are Poketeballs. You'll need these to catch Poketes. Stepping on such a ball will add it to your inventory.

See [How to play](HowToPlay.md).

## Game depth
Not only are there Poketes that are stronger than others, but also Poketes with different types, which are effective against some types and ineffective against others.

| Type    | Effective against            | Ineffective against |
|---------|------------------------------|---------------------|
| Normal  |                              |                     |
| Stone   | Flying, Fire                 | Plant               |
| Plant   | Stone, Ground, Water         | Fire, Ice           |
| Water   | Stone, Flying, Fire          | Plant, Ice          |
| Fire    | Flying, Plant, Undead, Ice   | Stone, Water        |
| Ground  | Normal                       | Flying              |
| Electro | Stone, Flying                | Ground              |
| Flying  | Plant                        | Stone               |
| Undead  | Normal, Ground, Plant, Water | Fire                |
| Ice     | Water, Plant                 | Fire                |

For additional information you can see [wiki](wiki.md) or
[the multi-page wiki](https://lxgr-linux.github.io/pokete/wiki-multi).

## Mods
Mods can be written to extend Pokete. To load a mod, the mod has to be placed in `mods` and mods have to be enabled in the menu.
For an example mod see [example.py](mods/example.py).

## Tips
- When you want to see the next part of a conversation, press any key
- Don't play on full-screen; the game will not run properly
- Don't be offended by the other trainers; they may swear at you

## TODO
- [x] A wizard at the start to set name and starter Pokete
- [ ] More maps
- [x] Types for attacks and Poketes
- [x] Evolving
- [x] More than one Pokete for trainers
- [x] Coloured Poketes
- [x] A store to buy Poketeballs
- [x] Potions
- [x] Intro
- [x] Trading
- [x] Poketedex
- [x] Effects
- [x] Colour codes for types

## Dependencies
Pokete depends on python3 and the `scrap_engine` module.
On Windows `pynput` has to be installed too.

## Documentation
- [Documentation for pokete_classes](https://lxgr-linux.github.io/pokete/doc/pokete_classes/index.html)
- [Documentation for pokete_data](https://lxgr-linux.github.io/pokete/doc/pokete_data/index.html)
- [Documentation for the gen-wiki file](https://lxgr-linux.github.io/pokete/doc/gen_wiki.html "gen_wiki.py")
- [Documentation for the prepare_pages file](https://lxgr-linux.github.io/pokete/doc/prepare_pages.html "prepare_pages.py")
- [Documentation for the pokete_general_use_fns](https://lxgr-linux.github.io/pokete/doc/pokete_general_use_fns.html "pokete_general_use_fns.py")
- [Documentation for the main file "pokete.py"](https://lxgr-linux.github.io/pokete/doc/pokete.html "pokete.py")

## Releases
For release information see [Changelog](Changelog.md).

## Contributing
Feel free to contribute whatever you want to this game.
New Pokete contributions are especially welcome, those are located in /pokete_data/poketes.py

To learn how to add more poketes/types/attacks to the game, see [the development guide](DevGuide.md)

After adding new Poketes and/or attacks you may want to run
```shell
$ ./gen_wiki.py
```

to regenerate the wiki and adding them to it.

## Credits
Music:
- Eric Skiff - Resistor Anthems - Available at [http://EricSkiff.com/music](http://EricSkiff.com/music)
- Marllon Silva (xDeviruchi) - 8-bit-fantasy-adventure-music-pack - Available at [itch.io](https://xdeviruchi.itch.io/8-bit-fantasy-adventure-music-pack)
- SketchyLogic - Map - Available at [opengameart.org](https://opengameart.org/content/nes-shooter-music-5-tracks-3-jingles)
- lxgr-linux - Original game - Available at [pokete](https://github.com/lxgr-linux/pokete)

## Troubleshooting
If you're experiencing problems on Japanese systems take a look at [this](https://gist.github.com/z80oolong/c7523367b798bdda094f859342f4c8be).


## Changes to lxgr-linux original game
- Merged Pull request [#255](https://github.com/lxgr-linux/pokete/pull/255) by ta-mj
  - Skip animation when pressing 'Accept' key
  - Added an archivment ("first Gym Win")
  - Added Attacks
    - heartattack
    - cutearrow
    - 10billon_volt"
    - downpour
    - water_blast
  - Added Poketes
    - rabbitto
    - whitecotten
    - pangsuni
  - Balancing
    - More xp when fighting higher lv. poketes
    - adjusted some probabillity values
    - Increased pokete HP by 1 every 10 lv.
  - Minor spelling improvement
