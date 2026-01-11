# One Liners

Refrain from using conditions that create a new section:
```vb
if health of player > 5:
	remove 1 from health of player
```
These can cause pyramids and lots of indentation. Which look like garbage.

Instead use:
```vb
health of player > 5
remove 1 from health of player
```

# If... Stop Conditions

This is also fine because it doesn't cause more indentation:
```vb
if health of player <= 5:
	stop
remove 1 from health of player
```

Only use if you're going to add extra things like messages:
```vb
if health of player <= 5:
	send "You're not low enough to use this ability!"
	stop
remove 1 from health of player
```
