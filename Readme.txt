CS611 - Legends of Valor
Group members:
Peng Huang          BU ID: U50250882
Yichen Mu           BU ID: U30147159
Shaolin Xie         BU ID: U51803896

This program is a game of Legends of Valor.

1. Compile and run
Navigate to the directory after downloading the project.
Run the following instructions on command line:
1) cd src
2) javac Main.java
3) cd ..
4) java -classpath src Main

2. Design pattern
We used the Factory design pattern. We used it to create new monsters, heroes, and items(weapons, potion, armors, spells).
This design pattern improves scalability and efficiency of our program.

We also used the Observers Pattern in Lane class, which maintains a set of Heroes to update the lane
utilizing all the heroes' information when necessary.

3. Bonus points
- Colorful console!
- Music and sound effects!
- Factory and Observer design pattern!
- Inputs parsed from input files!

4. Coding platform
MacOS

Enjoy the game!

------------Class Hierarchy-------------
Main ----- main class the entry of the program
Game ----- abstract class for a game
    RPGGame ----- abstract class extends Game
        LegendsOfValor ----- class extends RPGGame where the game algorithm lies

Attackable ----- interface items that are attackable
Equipable ----- interface items that are equipable
Usable ----- interface items that are usable

Item ----- abstract class for an item
    Armor ----- extends Item implements Equipable
    Weapon ----- extends Item implements Equipable, Attackable
    Potion ----- extends Item implements Usable
    Spell ----- extends Item Attackable
        IceSpell ----- extends Spell
        FireSpell ----- extends Spell
        LightningSpell ----- extends Spell

Grid ----- abstract class for the game map
    LovMap ----- class extends Grid where the game map algorithms are implemented

CellType ----- enum for cell types
Cell ----- abstract class represents a cell on the board. Each cell has a type
    PlainCell ----- class extends Cell
    InaccessibleCell ----- class extends Cell
    BushCell ----- class extends Cell
    CaveCell ----- class extends Cell
    KoulouCell ----- class extends Cell
    NexusCell ----- class extends Cell

Nexus - abstract class to implement algorithms for nexus
    HeroNexus ------ extends Nexus which spawn heroes
    Monster Nexus ----- extends Nexus which spawn monsters

Lane ----- class that represents a lane

Character ----- abstract class representing a character in the game
    Hero ----- abstract class extends Character representing a hero character
        Sorcerer ----- extends Hero
        Warrior ----- extendsHero
        Paladin ----- extends Hero
    Monster ----- abstract class extends Character representing a monster character
        Exoskeleton ----- extends Monster
        Dragon ----- extends Monster
        Spirit ----- extends Monster

Inventory ----- class contains weapons, potions, armors, and spells
Markets ----- class that represents the market, where shopping algorithm lies

Player ----- class representing a player
    LegendsPlayer ----- extends Player

Round ----- class represents a round of game

ScannerParser ----- class to parse scanner inputs. All functions are static
FileParser ------ class to parse input files into objects
Printer ------ class to print shop/ heroes/ monsters/ weapon/ spell/ potion/ armor and other info
Colors ------ class for console colors
Factory ----- class to create objects
AudioUtility ------ class to add audios


