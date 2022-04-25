# VegCraftForge

A Forge mod for Minecraft 1.12.2 that adds vegan crafting recipes for vanilla Minecraft items. This is based on the data pack [VegCraft](https://github.com/ACascarino/vegcraft) created by [ACascarino](https://github.com/ACascarino). For newer versions of Minecraft, use the original data pack.

## Installation

VegCraftForge currently does not have a mod JAR file that can be used for installation. It is planned to ship this project as a standalone mod one day.

Instead, we rely on modifying the [Uncrafted](https://www.curseforge.com/minecraft/mc-mods/uncrafted) mod. It has great synergy with our mod by providing recipes for vanilla items that normally do not exist. They also support and encourage users to add their own custom recipes.

- [Download](https://www.curseforge.com/minecraft/mc-mods/uncrafted/files/2477473) Uncrafted for Minecraft 1.12.2.
- Create a temporary working directory.

    ```
    mkdir /tmp/vegcraft_build/
    cd /tmp/vegcraft_build/
    ```

- Copy Uncrafted to it and extract it.

    ```
    cp ${HOME}/Downloads/Uncrafted+1.12++\(v.3.0.1\).jar ./
    unzip Uncrafted+1.12++\(v.3.0.1\).jar
    ```

- Download VegCraftForge.

    ```
    git clone https://github.com/lukeshortcloud/vegcraftforge.git
    ```

- Copy the recipes over.

    ```
    cp -r vegcraftforge/data/vegcraft/recipes/*.json assets/uncrafted/recipes/
    ```

- Delete the Uncrafted JAR file and the VegCraftForge files before creating a new JAR.

    ```
    rm -r -f Uncrafted*.jar vegcraftforge
    ```

- Create a new JAR file to use.

    ```
    zip -r Uncrafted+1.12++\(v.3.0.1\)-VegCraftForge.jar ./
    ```

- Place that file in the "mods" folder of the server.

## Recipes

Item | Recipe | Description
---- | ------ | ----------
Blaze Powder | ![Crafting table: top row: glowstone dust, gold nugget, glowstone dust; middle row: nether wart, gunpowder, nether wart; bottom row: glowstone dust, gold nugget, glowstone dust -> blaze powder](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/blaze_powder.png) | Original blaze powder is produced from blaze rods, a drop from Blazes - went with a "firey gold powder" theme
Blaze Rod | ![Crafting table: top row: -, gold nugget, -; middle row: blaze powder, stick, blaze powder; bottom row: -, gold nugget, - -> blaze rod](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/blaze_rod.png) | Original blaze rods are a drop from Blazes - flipped production so powder is now produced first and rods are constituted from powder.
Ender Pearl | Hard / Early-Game Recipe:<br><br>Nether Quartz, Cyan Dye, Nether Quartz<br>Nether Quartz, Bottle o' Enchanting, Nether Quartz<br>Nether Quartz, Nether Quartz, Nether Quartz<br><br>OR<br><br>Easy / Late-Game Recipe:<br><br>Chorus Fruit, Cyan Dye, Glass Pane, Gunpowder | Original ender pearls obtained from endermen - went for a "magic glass orb" theme. Requiring Bottles O' Enchanting forces it to be a late-game item. After you reach the End, ender pearls are plentiful, so an alternative recipe is provided that is slightly easier to obtain and produces more ender pearls.
Cake | Milk, Milk, Milk<br>Sugar, Apple, Sugar<br>Wheat, Wheat, Wheat | Original cake recipe uses eggs; have substituted eggs for an apple globally. Applesauce is a common egg replacement in baking.
Feather | ![Crafting table: shapeless: paper, stick, string -> 4 feathers](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/feather.png) | Firework star "burst" recipe hardcoded to use feathers, so needed an alternate feather recipe - getting the sense of tying paper to a stick as a "paper feather"
Ghast Tear | ![Crafting table: top row: fire charge, gunpowder, glass; middle row: blaze powder, quartz, blaze powder; bottom row: glass, gunpowder, fire charge -> Ghast Tear](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/ghast_tear.png) | Original ghast tears are obtained from killing Ghasts. They are relatively difficult to obtain, so the recipe reflects this.
Gunpowder | Redstone, Sugar, Charcoal, Bone Meal | Gunpowder originally obtained from creepers - went for the idea of "energetic powdery burny stuff".
Ink Sac | Charcoal, Water Bottle | Mixing charcoal and water in a bottle results in a usable ink bottle.
Leather | ![Crafting table: shapeless: 3 rotten flesh, string -> leather](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/leather.png) | Original method of leather production kills cows; new method sews together rotten flesh to make a leather
Milk Bucket | ![Crafting table: shapeless: 3 wheat, bucket, water bucket -> milk bucket](https://raw.githubusercontent.com/ACascarino/vegcraft/master/img/milk_bucket.png) | Original method of milk production uses cows; new method creates "oat milk". Two buckets needed due to bucket duplication glitch.
Pumpkin Pie | Pumpkin, sugar, apple | Original pumpkin pie recipe uses eggs; have substituted eggs for an apple globally. Applesauce is a common egg replacement in baking.
Rotten Flesh | Apple (or Poisonous Potato), Rose Red, Cactus Green, Charcoal | Original rotten flesh production kills zombies; have created an "apple leather" vibe with dye and charcoal. Have also given use to poisonous potatos as a sort of "rotten potato leather".
String | Sugar Canes, Suger Canes | Original string production kills spiders; have gone with sugar canes for string.
