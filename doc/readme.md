# Wynn Armour Documentation

## Helpful Resources
- [Optifine CIT Documentation](https://github.com/sp614x/optifine/blob/master/OptiFineDoc/doc/cit_single.properties)
- [Example Properties Files](./properties_ex/)

## Overview
WynnArmour uses a feature of Optifine called Custom Item Textures (CIT) to change the texture of an item based on it's name.
In order for this to work, each texture must be accompanied by a properties file, which defines:
- The item type (eg, armor or item)
- The item material (eg, chainmail_helmet or leather_chestplate)
- The replacement textures file names
- The custom name of the item to replace.

## Leather Armour
Due to the way that leather armour is handled with dye colors, instead of replacing the items base texture, we replace the overlay texture which does not have the dye color applied to it. The base texture is also replaced with a transparent image to avoid texture clipping issues.

This can be achieved by defining the original texture we want to replace.
Example for items:
```
texture.leather_chestplate=/common/blank.png (the transparent image)
texture.leather_chestplate_overlay=really_cool_icon (the icon image name)
```
Example for armour:
```
texture.leather_layer_1=/common/blank.png (the transparent image)
texture.leather_layer_1_overlay=really_cool_icon (the icon image name)
```
Note: Helmets, Chestplates and Boots use the leather_layer_1 texture while pants use the leather_layer_2 texture.

 

