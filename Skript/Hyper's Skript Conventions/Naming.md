# File Names

File names of scripts should be named according to the PascalCase naming convention.

Ex.
Your main script should be called: Main.sk
Your abilities will be in a script called: Abilities.sk
Your cool utility script should be called: CoolUtil.sk


# Function Names

Functions must be in camelCase
Argument names must be in camelCase and it should the full name. So a player should be called ```player``` not ```p```. Unless it's something long like ```location```, shorten that to ```loc```.

Ex.
```vb
function spawnSkeletion(loc: location):
	spawn a skeleton 1 block above {_loc}
```
```vb
function killAllSkeletons():
	kill all skeletons
```


# Variable Names

Local variables should be named according to the camelCase convention. Global variables should be naming according to the PascalCase convention.

Ex. (I know this code can be way more simplified, this is only to show the convention.)
```vb
function removeLife(player: player):
	set {_lives} to {Lives::%uuid of {_player}%}
	remove 1 from {_lives}
	set {Lives::%uuid of player%} to {_lives}
```


# Custom Syntax

For things that you're going to release publicly, you must include custom syntax. Read the [skript-reflect documentation](https://tpgamesnl.gitbook.io/skript-reflect/advanced/custom-syntax)

Ex.
```vb
player property gem:
	get:
		return getGem(expr-1)
	set:
		setGem(expr-1, change value)
```

These should be used for big projects as well.

