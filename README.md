# Mindrot

3D-s pszichológiai horror játék Godot 4.7-ben (Forward+). A projekt még alap állapotban van, a játéktervezés most indul.

## Futtatás

1. A Godot 4.7-ben kattints az **Import** gombra, és válaszd ki a `project.godot` fájlt.
2. Nyomj **F5**-öt. Egyelőre egy helyőrző jelenet indul.

## Projektstruktúra

```text
assets/            Importált tartalom, amit a jelenetek használnak
  audio/           ambience, music, sfx, voice
  fonts/
  materials/
  models/          characters, environment, props
  textures/
  ui/
data/              Játékadatok .tres fájlokban
docs/              Tervezési dokumentumok (a Godot nem importálja)
scenes/            Jelenetek és a hozzájuk tartozó szkriptek
  main/            Belépési pont
  levels/          Pályák
  player/          Játékos
  characters/      NPC-k és lények
  props/           Interaktív tárgyak
  ui/              Menük, HUD
scripts/           Jelenethez nem köthető kód
  autoload/        Globális singletonok
  resources/       Egyedi Resource osztályok
  systems/         Játékrendszerek
shaders/           Közös shaderek és utófeldolgozás
```

## Szabályok

- A jelenet és a saját szkriptje egymás mellé kerül a `scenes/` alatt. A `scripts/` mappába csak az megy, ami nem egyetlen jelenethez tartozik.
- A fájlnevek `snake_case`, az osztálynevek `PascalCase` formájúak, a [GDScript stílusútmutató](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_styleguide.html) szerint.
- A Godot által generált `.import` és `.uid` fájlok a repóba valók, a `.godot/` mappa nem.

## Commitok

A commit üzenetek a [gitmoji](https://gitmoji.dev) formátumot követik: `:emoji: Rövid leírás`.
