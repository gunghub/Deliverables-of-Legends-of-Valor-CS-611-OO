CS611 - Legends of Valor
Group members:
Peng Huang          BU ID: U50250882
Yichen Mu           BU ID: U30147159
Shaolin Xie        BU ID: U51803896

This program is a game of Legends of Valor.

1. Compile and run
- (go to the program directory where src lies)
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
- Extra graphic!
- Colorful console!
- Music and sound effects!
- Factory and Observer design pattern!
- Inputs parsed from input files!

4. Coding platform
MacOS


Enjoy the game!

------------Class Hierarchy-------------
Main ----- main class
Game ----- abstract class
    RPGGame ----- abstract class extends Game
        LegendsOfValor ----- class extends RPGGame

Attackable ----- interface
Equipable ----- interface
Usable ----- interface

Item ----- abstract class
    Armor ----- extends Item implements Equipable
    Weapon ----- extends Item implements Equipable, Attackable
    Potion ----- extends Item implements Usable
    Spell ----- extends Item Attackable
        IceSpell ----- extends Spell
        FireSpell ----- extends Spell
        LightningSpell ----- extends Spell

Grid ----- abstract class
    LovMap ----- class extends Grid

CellType ----- enum
Cell ----- abstract class
    PlainCell ----- class extends Cell
    InaccessibleCell ----- class extends Cell
    BushCell ----- class extends Cell
    CaveCell ----- class extends Cell
    KoulouCell ----- class extends Cell
    NexusCell ----- class extends Cell

Nexus - abstract class
    HeroNexus ------ extends Nexus
    Monster Nexus ----- extends Nexus

Lane ----- class that represents a lane

Character ----- abstract class
    Hero ----- abstract class
        Sorcerer ----- extends Hero
        Warrior ----- extendsHero
        Paladin ----- extends Hero
    Monster ----- extends Character
        Exoskeleton ----- extends Monster
        Dragon ----- extends Monster
        Spirit ----- extends Monster

Inventory ----- class contains ArrayList of weapon, armor, spell and HashMap of potion
Markets ----- class that represents the market

Player ----- class
    LegendsPlayer ----- extends Player

Round ----- class represents a round of game

ScannerParser ----- class to parse scanner inputs. All functions are static
FileParser ------ class to parse input files into objects
Printer ------ class to print shop/ heroes/ monsters/ weapon/ spell/ potion/ armor and other info
Colors ------ class for console colors
Factory ----- class to create objects
AudioUtility
Graphhic



