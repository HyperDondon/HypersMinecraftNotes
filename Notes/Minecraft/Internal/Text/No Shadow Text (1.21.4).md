# No Shadows

This requires a 1.21.4+ client and a 1.21.4+ server. This is possible to do with ItemsAdder but you wont be able to add other colors and stuff. You can use ItemsAdder's rainbow text feature with shadows if you have a 1.21.4 server and use the vanilla feature instead of ItemsAdder's.

Here's an example, rainbow text with no shadow. ItemsAdder replaces any text with the color #e6fffe to rainbow. This happens client side using core shaders.

```
/tellraw @a {"text":"custom text example", "color":"#e6fffe", "shadow_color":0}
```