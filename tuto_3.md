# Tutoriel - Introduction (suite)

```package
tutorial_asset_exemple=github:sbergeroncp/tutorial_asset_exemple
```

```template
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
```

## @showdialog

🎮🎮🎮 Continue de créer l'adaptation vidéoludique du livre Escapades virtuelles. 🎮🎮🎮

## Étape 1

Ajoute le bloc ``||controller:quand bouton A est appuyé||`` (onglet ``||controller:Contrôleur||``) dans la zone de programmation.

Remplace la valeur ``||controller:A|`` par ``||controller:gauche|``.

🎮🎮🎮

```blocks
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
```

## Étape 2

Ajoute le bloc ``||animation:animer||`` (onglet ``||animation:Animation||``) dans le bloc ``||controller:quand bouton gauche est appuyé||`.

Sélectionne la même animation que celle proposée dans l'indice.

🦹‍♀️🧝‍♀️🧛‍🧜‍♀️ Tu peux également prendre un personnage féminin !!! 🦹‍♀️🧝‍♀️🧛‍🧜‍♀

Remplace la valeur ``||animation:500||`` par ``||animation:100||``.

Active la valeur ``||animation:en boucle ON||``.

🎮🎮🎮

```blocks
controller.left.onEvent(ControllerButtonEvent.Pressed, function () {
    animation.runImageAnimation(
    mySprite,
    [img`
        . . . . f f f f f f . . . . . . 
        . . . f 2 f e e e e f f . . . . 
        . . f 2 2 2 f e e e e f f . . . 
        . . f e e e e f f e e e f . . . 
        . f e 2 2 2 2 e e f f f f . . . 
        . f 2 e f f f f 2 2 2 e f . . . 
        . f f f e e e f f f f f f f . . 
        . f e e 4 4 f b e 4 4 e f f . . 
        . . f e d d f 1 4 d 4 e e f . . 
        . . . f d d d d 4 e e e f . . . 
        . . . f e 4 4 4 e e f f . . . . 
        . . . f 2 2 2 e d d 4 . . . . . 
        . . . f 2 2 2 e d d e . . . . . 
        . . . f 5 5 4 f e e f . . . . . 
        . . . . f f f f f f . . . . . . 
        . . . . . . f f f . . . . . . . 
        `,img`
        . . . . . . . . . . . . . . . . 
        . . . . f f f f f f . . . . . . 
        . . . f 2 f e e e e f f . . . . 
        . . f 2 2 2 f e e e e f f . . . 
        . . f e e e e f f e e e f . . . 
        . f e 2 2 2 2 e e f f f f . . . 
        . f 2 e f f f f 2 2 2 e f . . . 
        . f f f e e e f f f f f f f . . 
        . f e e 4 4 f b e 4 4 e f f . . 
        . . f e d d f 1 4 d 4 e e f . . 
        . . . f d d d e e e e e f . . . 
        . . . f e 4 e d d 4 f . . . . . 
        . . . f 2 2 e d d e f . . . . . 
        . . f f 5 5 f e e f f f . . . . 
        . . f f f f f f f f f f . . . . 
        . . . f f f . . . f f . . . . . 
        `,img`
        . . . . f f f f f f . . . . . . 
        . . . f 2 f e e e e f f . . . . 
        . . f 2 2 2 f e e e e f f . . . 
        . . f e e e e f f e e e f . . . 
        . f e 2 2 2 2 e e f f f f . . . 
        . f 2 e f f f f 2 2 2 e f . . . 
        . f f f e e e f f f f f f f . . 
        . f e e 4 4 f b e 4 4 e f f . . 
        . . f e d d f 1 4 d 4 e e f . . 
        . . . f d d d d 4 e e e f . . . 
        . . . f e 4 4 4 e e f f . . . . 
        . . . f 2 2 2 e d d 4 . . . . . 
        . . . f 2 2 2 e d d e . . . . . 
        . . . f 5 5 4 f e e f . . . . . 
        . . . . f f f f f f . . . . . . 
        . . . . . . f f f . . . . . . . 
        `,img`
        . . . . . . . . . . . . . . . . 
        . . . . f f f f f f . . . . . . 
        . . . f 2 f e e e e f f . . . . 
        . . f 2 2 2 f e e e e f f . . . 
        . . f e e e e f f e e e f . . . 
        . f e 2 2 2 2 e e f f f f . . . 
        . f 2 e f f f f 2 2 2 e f . . . 
        . f f f e e e f f f f f f f . . 
        . f e e 4 4 f b e 4 4 e f f . . 
        . . f e d d f 1 4 d 4 e e f . . 
        . . . f d d d d 4 e e e f . . . 
        . . . f e 4 4 4 e d d 4 . . . . 
        . . . f 2 2 2 2 e d d e . . . . 
        . . f f 5 5 4 4 f e e f . . . . 
        . . f f f f f f f f f f . . . . 
        . . . f f f . . . f f . . . . . 
        `],
    100,
    true
    )
})
let mySprite: Sprite = null
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
```

## Étape 3

Duplique le bloc ``||controller:quand bouton gauche est appuyé||``

Remplace la valeur ``||controller:gauche|`` par ``||controller:droite|``.

Remplace la trame du bloc ``||animation:animer||`` par la bonne animation.

## Étape 4

Duplique le bloc ``||controller:quand bouton droite est appuyé||``

Remplace la valeur ``||controller:droite|`` par ``||controller:haut|``.

Remplace la trame du bloc ``||animation:animer||`` par la bonne animation.

## Étape 5

Duplique le bloc ``||controller:quand bouton haut est appuyé||``

Remplace la valeur ``||controller:haut|`` par ``||controller:bas|``.

Remplace la trame du bloc ``||animation:animer||`` par la bonne animation.

## Étape 6

Ajoute le bloc ``||variables:définir mySprite||`` (onglet ``||Sprites:Sprites||``) sous le bloc ``||scroller:déplacer avec les boutons||``.

*** Assure-toi que la valeur ``||variables:définir mySprite2||`` soit sélectionnée. ***

Remplace la valeur ``||Sprites:Player||`` par ``||Sprites:Food /  Nourriture||``.

Clique sur le carré gris pour sélectionner un lutin dans la Galerie.

```blocks

scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)

```

## Étape 5

Ajoute le bloc ``||info:définir le score||`` (onglet ``||info:Info||``) sous le bloc ``||variables:définir mySprite2||``.

La valeur ``||info:0||`` demeure la même.

```blocks

scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)

```

## Étape 6

Glisse le bloc ``||Sprites:quand||`` (onglet ``||Sprites:Sprites||``) dans la zone de programmation.

Remplace la valeur ``||Sprites:Player||`` de droite par la valeur ``||Sprites:Food||``.

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
	
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
    
```

## Étape 7

Ajoute le bloc ``||info:modifier le score||`` dans le bloc ``||Sprites:quand||``.

La valeur ``||info:1||`` du bloc ``||info:modifier le score||`` demeure la même.

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)

})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
```

## Étape 8

Ajoute le bloc ``||Sprites:définir la position||`` (onglet ``||Sprites:Sprites)||`` sous le bloc ``||info:modifier le score||``.

Remplace la valeur ``||variables:mySprite||`` par ``||variables:mySprite2||``.

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    mySprite2.setPosition(0, 0)
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
```

## Étape 9

Remplace les valeurs ``||Sprites:0||`` du bloc ``||Sprites:définir la position||`` par les blocs ``||math:choisir aléatoirement entre||`` (onglet ``||math:Maths||``).

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    mySprite2.setPosition(randint(0, 10), randint(0, 10))
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
    

```

## Étape 10

Modifie le bloc ``||math:choisir aléatoirement entre||`` pour la valeur ``||Sprites:x||``.

Remplace la valeur ``||math:10||`` du bloc ``||math:choisir aléatoirement entre||`` par le bloc ``||scene:largeur de l'écran||``.

Regarde bien l'indice !

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    mySprite2.setPosition(randint(0, scene.screenWidth()), randint(0, 10))
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
```

## Étape 11

Modifie le bloc ``||math:choisir aléatoirement entre||`` pour la valeur ``||Sprites:y||``.

Remplace la valeur ``||math:10||`` du bloc ``||math:choisir aléatoirement entre||`` par le bloc ``||scene:hauteur de l'écran||``.

Regarde bien l'indice.

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    mySprite2.setPosition(randint(0, scene.screenWidth()), randint(0, scene.screenHeight()))
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
```

## Étape 12

Ajoute le bloc ``||info:démarrer le compte à rebours||`` (onglet ``||info:Info||``) sous le bloc ``||Sprites:définir la position||``.

Remplace la valeur ``||info:10||`` par ``||info:3||``.

```blocks

sprites.onOverlap(SpriteKind.Player, SpriteKind.Food, function (sprite, otherSprite) {
    info.changeScoreBy(1)
    mySprite2.setPosition(randint(0, scene.screenWidth()), randint(0, scene.screenHeight()))
    info.startCountdown(3)
})
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
let mySprite2 = sprites.create(tutorial_asset_exemple.food1, SpriteKind.Food)
info.setScore(0)
```