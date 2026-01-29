Make sure all of your scripts are inside a folder that has the name of your project. 

Ex.
```
plugins/Skript/scripts/Marine SMP/
```

This is to keep things clean. 

Libraries should be placed in a folder named "!Libraries."
```
plugins/Skript/scripts/!Libraries
```
They should be inside the scripts folder, separate from your project. Unless the library is private and not used anywhere else, place the library inside:
```
plugins/Skript/scripts/<your project>/!Libraries
```
Make sure to add "!" at the start of the folder name and at the start of the script names. This is so custom syntax and events load before your actual project code so they can be used.

Code for abilities and whatnot should have their own folder.
Ex. 
```
plugins/Skript/scripts/<your project>/Abilities/SpeedGem.sk
```

Make sure scripts are not too long. If they are, split them into different folders. This is too keep loading times during development low.  