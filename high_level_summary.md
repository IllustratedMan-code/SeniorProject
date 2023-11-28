# Introduction
This document creates a narritive of what has been done on the project thus far. This narritive structure is much more flexible than the assignments,
allowing us to convey important details of the development process not covered by the assignments.
# Semester 1 Summary
## Repo setup
Early on, we decided to heavily make use of the git version control system for the project.
We split the project into two repos, one for the class [assignments](https://github.com/quaternary-game/class-work), 
the other for the actual [project](https://github.com/quaternary-game/quaternary). This was decided to avoid confusion and facilitate good development practices.

We also decided to create a [style guide](https://github.com/quaternary-game/quaternary/blob/main/CONTRIBUTING.md) to enforce guidelines contributions to the project.
This style guide has made it much easier to maintain repo readability, while also opening the project up for outside contributions in the future.
## Investigating tools
We spent a fair amount of time before the project experimenting and aquainting ourselves with the chosen toolset. 
We all completed the introductory [Godot tutorial](https://docs.godotengine.org/en/stable/getting_started/first_2d_game/index.html) 
and evaluated several different art tools, landing on [blender](https://www.blender.org/). This was also the time when the group began to settle into
various roles: Alex became the "sound guy", David became the graphical artist, John was put in charge of maintaining code style, and Connor does a little of everything.

## Making the tentative vision
After many brainstorming sessions, we came up with a ["tentative vision"](https://github.com/quaternary-game/quaternary/issues/1) 
for the game that gives a general overview of the game's structure. This issue acts as a loose specification for new game features and keeps us all on track.
It was decided that the game should be split into the "main" game and "minigames" that could be worked on seperately. 

## Minigames
Alex, David, and Connor were all put in charge of a separate minigame. John was put in charge of investigating and developing the trait system described in the tentative vision.

### Punnett square minigame
Alex completed this one. A player has to fill in the punnett square before the time runs out! 

https://github.com/quaternary-game/class-work/assets/71360172/5010cd4c-20da-40e6-b044-ff522e55e56b

### Build the codons minigame
This minigame is very similar to the Godot tutorial we all completed. This minigame was completed by Connor.
A player has to catch floating nucleotides that correspond to a piece of tRNA.

INSERT VIDEO HERE

### Mutation minigame
This minigame was completed by David. A player has to mutate a strand of DNA to correspond to another one.

https://github.com/quaternary-game/class-work/assets/60514384/10013259-b732-42c1-95d8-7f4354309944

## The Main game
### Art style
David created a few animated "enemies" for the main game using Blender. They were initially created in 3D, then rendered into 2D for the game.  This also defines the artstyle for the rest of the game.
All other assets created will attempt to fit this style.

The enemies are also based off of real organisms!
#### Bacteria
A generic bacteria.

![ezgif-2-f92e1d13cd (1)](https://github.com/quaternary-game/class-work/assets/60514384/2261427e-95c7-496a-8296-b51da9e49ef7)

#### Bacteriophage
A virus that infects bacteria.

![ezgif-4-c455f0e1b9 (1)](https://github.com/quaternary-game/class-work/assets/60514384/f7f5a437-a8f1-4b0a-8880-a8c31d5fea53)

#### Spider (Patu Digua)
[A very small spider](https://en.wikipedia.org/wiki/Patu_digua)

![ezgif-1-64d700638a (1)](https://github.com/quaternary-game/class-work/assets/60514384/76e976a2-4dc2-452d-be30-56d2cdc19325)


### Trait system
John is actively involved as the lead developer of the trait system. It will control the activity of both the player characters and the enemies in the main game. Each organism has a list of traits that effect its behaviors.
Eyes for example would enable the organism to see its surroundings. More detail is given in the [trait brainstorm](https://github.com/quaternary-game/quaternary/issues/3).

#### The problem of performance
The trait system may model many behavior interactions simultaniously, making performance a concern not present in the minigames. 
John is currently investigating the feasibility of web export and the godot extension system. The godot extension system has higher performance,
but is written in C++, making development time longer and more complicated. 

The web export is performant enough for the minigames, but may not be for the main game. For this reason, the team is also investigating the possibility of a 
"demo" website that hosts minigames and smaller levels of the main game for advertising and education purposes.
