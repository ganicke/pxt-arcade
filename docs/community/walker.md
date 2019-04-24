# Walker

A sprite walks off of the screen!

https://makecode.com/_hWVH2CMpxEYU

```blocks
enum SpriteKind {
    Player,
    Projectile,
    Enemy,
    Food
}
let walker = sprites.create(img`
    . . 2 2 2 2 . .
    . 2 . . . . 2 .
    . 2 . . . . 2 .
    . . 2 2 2 2 . .
    . . . 2 2 . . .
    . . 2 . . 2 . .
    . 2 . . . . 2 .
    2 2 . . . . 2 2
`, SpriteKind.Player)
game.onUpdateInterval(500, function () {
	walker.x += 10
})
```
