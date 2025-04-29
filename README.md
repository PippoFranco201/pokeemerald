# Pokémon Emerald

Hello! This is an an all-in-one package to expand the Mauville Game Corner, that, in its current state, isn't configurable.
It uses several unused Emerald flags, vars, and FR/LG tracks to make things work... Please keep this in mind if you would like to use this for your own hack.

More specifically, this adds 4 pinball mini-games, Flappy Bird, Block Stacker, Snake, Blackjack, Voltorb Flip, Plinko, Mauville Derby, and Gacha Machines into the Game Corner.

THIS IS CURRENTLY NOT COMPATIBLE WITH EMERALD EXPANSION!

Big thank you to huderlem (Pokemon Pinball to Emerald), and Pokeabbie (Voltorb Flip from Emerald Rogue). All I really did for these was some graphics, music, and code to work with coins. They deserve the real credits here.
Also thank you to Viperio, who made an initial Snake for Pokemon Emerald that I based my code on.

...

This is a decompilation of Pokémon Emerald.

It builds the following ROM:

* [**pokeemerald.gba**](https://datomatic.no-intro.org/index.php?page=show_record&s=23&n=1961) `sha1: f3ae088181bf583e55daf962a92bb46f4f1d07b7`

To set up the repository, see [INSTALL.md](INSTALL.md).

## FAQ
### `(followers*)` Q: Where are the config settings?
A: Configuration for the follower system is mostly in [event_objects.h](include/constants/event_objects.h):
```c
// If true, follower pokemon will bob up and down
// during their idle & walking animations
#define OW_MON_BOBBING  TRUE

// If true, adds a small amount of overhead
// to OW code so that large (48x48, 64x64) OWs
// will display correctly under bridges, etc.
#define LARGE_OW_SUPPORT TRUE
```

### `(lighting)` Q: How do I mark certain colors in a palette as light-blended?
A: Create a `.pla` file in the same folder as the `.pal` with the same name.

In this file you can enter color indices [0,15]
on separate lines to mark those colors as being light-blended, i.e:

`06.pla:`
```
# A comment
0 # if color 0 is listed, uses it to blend with instead of the default!
1
9
10
```

You might have to `make mostlyclean` or change the `.pal` file to pick up the changes.

## See also

For contacts and other pret projects, see [pret.github.io](https://pret.github.io/).
