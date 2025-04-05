# Tutoriel 1

```package
tutorial_asset_exemple=github:sbergeroncp/tutorial_asset_exemple
```

## @showdialog

Crée l'adaptation vidéoludique du livre Escapades virtuelles.

## Étape 1

Ajoute le bloc ``||scene:définir couleur d'arrière-plan||`` (onglet ``||scene:Scène||``) dans le bloc ``||loops:au démarrage||``.

Clique sur le carré gris et sélectionne la couleur ⬛.

```blocks
scene.setBackgroundColor(15)
```

## Étape 2

Ajoute le bloc ``||game:splash||`` (onglet ``||scene:Scène||``) sous le bloc ``||scene:définir couleur d'arrière-plan||`` .

Appuie sur le ➕ pour ajouter une autre case.

```blocks
scene.setBackgroundColor(15)
game.splash("", "")
```

## Étape 3

Modifie le bloc ``||game:splash||``.

Écris **Escapades** dans la case de gauche.

Écris **virtuelles** dans la case de droite.

```blocks
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
```

## Étape 4

Ajoute le bloc ``||scene:définir image d'arrière-plan||`` (onglet ``||scene:Scène||``) sous le bloc ``||game:splash||``.

Clique sur le carré gris et sélectionne l'image de l'indice.

```blocks
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
```

## Étape 5 

Ajoute le bloc ``||variables:définir mySprite||`` (onglet ``||sprites:Sprites||``) sous le bloc ``||scene:définir image d'arrière-plan||``.

Clique sur le carré gris et sélectionne le personnage de l'indice.

📝 Renomme le personnage ``||variables:perso1||``

```blocks
scene.setBackgroundColor(15)
game.splash("Escapades", "virtuelles")
scene.setBackgroundImage(tutorial_asset_exemple.background2)
let perso1 = sprites.create(tutorial_asset_exemple.perso1, SpriteKind.Player)
```