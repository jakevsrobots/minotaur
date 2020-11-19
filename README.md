# pet minotaur

a small engine for first person maze games in the browser, with stories powered by inkjs.

## status

in development, not working yet!

## instructions

open the minotaur.html file and edit the content of the top two script tags.

first come the maps:

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
  1 start
  2 minotaur
  # wall
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
  # image: Minotaur.jng
  "oooOOooOOOoo," they say.

  = wall
  # image: stone-wall-texture.jpg
</script>
```

as the player moves through the maze, pet minotaur communicates with the ink story, using it for its world model, state, and most interactions.

## credits

inkjs is a javascript port by yannick lohse of ink by inkle studios. https://github.com/y-lohse/inkjs

this project also uses the parsimmon parser library. https://github.com/jneen/parsimmon
