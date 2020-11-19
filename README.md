# pet minotaur

a small engine for first person maze games in the browser, with stories powered
by inkjs.

## status

in development, not working yet!

## instructions

open the minotaur.html file and edit the content of the top two script tags.

first come the maps. you need three blocks of data to define a map: the ascii-art map itself, the key to the map, and some options (optional).

```
<script type="text/minotaur-maps">
  !MAP "start"
  ########
  #    2 #
  #      #
  #  1   #
  ########
  !END

  !KEY "start"
  1 start, walkable
  2 minotaur, bumpable, image: "Minotaur.jpg"
  # wall
  !END

  !OPTIONS "start"
  floor color = 0xa8a8f4
  sky color   = 0xffc922
  !END
</script>
```

next is the story code, written in ink and parsed with inkjs.

```
<script type="text/ink">
  === start

  = start
  welcome to the dungeon.

  = minotaur
  # image: Minotaur.jpg
  "oooOOooOOOoo," they say.

  = wall
  # image: stone-wall-texture.jpg
</script>
```

as the player moves through the maze, pet minotaur communicates with the ink story, using it for its world model, state, and most interactions.

## credits

inkjs is a javascript port by yannick lohse of ink by inkle studios. https://github.com/y-lohse/inkjs

three.js is used for 3d rendering. https://github.com/mrdoob/three.js

this project also uses the parsimmon parser library. https://github.com/jneen/parsimmon
