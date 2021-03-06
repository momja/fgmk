# Specification

The engine and the editor expects some files, and that they are organized in the
following manner.

Here is how the file tree should be  organized

    game_project_name
    ├── audio
    ├── descriptors
    │   ├── charaset
    │   │   └── charaset1.json
    │   ├── charas.json
    │   ├── feedback.json
    │   ├── hms.json
    │   ├── init.json
    │   ├── items.json
    │   └── levels
    │       ├── ahouse.map.json
    │       └── house.pal.json
    |        ...
    ├── font
    │   └── INFO56_0.ttf
    ├── icon.png
    ├── img
    │   ├── bgimg1.png
    │   ├── charaset.png
    │   ├── faceset.png
    │   ├── monsterset.png
    │   ├── pictures
    │   │   └── example.png
    |   |    ...
    │   ├── printer.png
    │   ├── sys
    │   │   ├── controllers.png
    │   │   ├── keys0.png
    │   │   ├── keysexplainer.png
    │   │   └── pckeys.png
    │   ├── tile.png
    │   └── title.png
    └── index.html


- `audio` (folder) - contains audio files used by the game.

- `descriptors` (folder) - contains all json files, and folders containing json
files.

    - `charaset` (folder) - this folder contains the different jsons that describes the
    animations you use with Charas.

    OBS: right now only a single file that has to be named `charaset1.json` is
    possible. Soon this won't be a requirement.

    - `charas.json` - things that you can place in any the map, they can move and
    trigger actions, and usually represent the non playable characters you interact
    in the game.

    - `feedback.json` - deals with the engine feedback, right now only colision and
    the sound when outputing text. This should be moved inside the engine soon.

    - `hms.json` - Heroes, Monsters and Skills, this file describes all the heroes
    that you can add to the party, all the monsters you can fight against, and the
    skills that they can have.

    - `init.json` - where does the game starts, who is in the party, and some things
    that didn't fit anywhere else.

    - `items.json` - has the description of the items, how do they work, what they
    are.

    - `scriptedbattles.json` - has the description of a scripted battle, what
    monsters are involved and how each script is triggered.

    - `levels` (folder) - this folder contains levels (.map.json files) and possible
    palettes (.pal.json files) to use when designing levels.


- `img` (folder) - this folder contains all the image files in png format.

    - `pictures` (folder) - you can show a picture using action, this folder
    contains possible pictures in png format.

- `font` (folder) - holds the type font for the engine. Currently it MUST be
INFO56_0.

  OBS: Soon the font name will be placed in init.json, so you will be able to
change this.

- `index.html` - this is the engine. It should be placed at the root of the
game project folder.



[*back*](../index.md)
