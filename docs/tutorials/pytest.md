# Chase the Pizza

### ~button /#tutorial:tutorials/chase-the-pizza

Try this tutorial!

### ~

## Introduction @unplugged

![Game animation](/static/tutorials/chase-the-pizza.gif)

In this tutorial, you will build a fairly simple game with the goal of eating a pizza before time runs out. When the player eats a slice of pizza, the countdown is restarted.

## Step 1 @fullscreen

Find ``||scene:set background color to||`` in ``||scene:Scene||``. Drag it into the ``||loops:on start||`` and then click on the grey box to select a new background color.

```spy
// @highlight
scene.setBackgroundColor(7)
```

## Step 2 @fullscreen

Find ``||variables:set mySprite to||`` in ``||sprites:Sprites||``. Drag it into the ``||loops:on start||`` **after** ``||scene:set background color to||``.

This will create a new character in the game -- but there is no image to represent this character yet.

```spy
enum SpriteKind {
    Player,
    Enemy,
    Food
}
let mySprite: Sprite = null
scene.setBackgroundColor(7)
// @highlight
mySprite = sprites.create(img`
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
. . . . . . . . . . . . . . . . 
`, SpriteKind.Player)
```
