# Tutoriel 2

```package
tutorial_asset_exemple=github:sbergeroncp/tutorial_asset_exemple
```

## @showdialog

🎮🎮🎮 Crée l'adaptation vidéoludique du livre Escapades virtuelles. 🎮🎮🎮

## Étape 1

Teste !

```blockconfig.global
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let mySprite = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
scene.cameraShake(5, 1000)
controller.moveSprite(mySprite)
```

```template
scene.setBackgroundColor(10)
game.splash("Escapades virtuelles")
```
