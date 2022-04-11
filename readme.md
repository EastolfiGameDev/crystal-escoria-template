# Game Template

![game-template-overview](https://user-images.githubusercontent.com/6860637/101258948-24c35c80-3726-11eb-8c64-7a201e945f73.png)

> 🌟 You make games, the template handles the boring stuff.

<p>
<a href="https://godotengine.org/download">
  <img alt="Godot Download badge" src="https://img.shields.io/badge/godot-3.4-blue">
</a>

<a href="https://github.com/crystal-bit/godot-game-template/releases">
  <img alt="GitHub release (latest by date)" src="https://img.shields.io/github/v/release/crystal-bit/godot-game-template">
</a>

<a href="https://github.com/crystal-bit/godot-game-template/actions?query=workflow%3A%22godot-ci+export%22">
  <img alt="GitHub workflow status" src="https://img.shields.io/github/workflow/status/crystal-bit/godot-game-template/godot-ci%20export?label=game-export">
</a>

<!-- <a href="https://github.com/crystal-bit/godot-game-template/wiki">
  <img alt="GitHub wiki" src="https://img.shields.io/badge/%F0%9F%93%96-wiki-blueviolet">
</a> -->

<a href="https://crystalbit.itch.io/godot-game-template">
  <img alt="Play store badge" src="https://img.shields.io/badge/HTML5-Itch.io-critical">
</a>

<a href="https://play.google.com/store/apps/details?id=org.crystalbit.godottemplate">
  <img alt="Play store badge" src="https://img.shields.io/badge/Android-PlayStore-green">
</a>
</p>

# Get started

1. 💻 [Create a new repo using this template](https://github.com/crystal-bit/godot-game-template/generate)
2. Clone the new repository locally
3. Open the project in [Godot](https://godotengine.org/download/) (GDScript)
4. Done

Read the [wiki](https://github.com/crystal-bit/godot-game-template/wiki/) to learn more.

## Used by

| Logo                                                                                                                                            | Title                               | Play it!                                                                                                                                                             | Source                                                            |
| ----------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------- |
| ![YouAreUto icon](https://play-lh.googleusercontent.com/lL54YNps-UPuDONDHfy3pmn8_aVUZGMorHJcDArimJWCQKjjNax0QMxpiAWCc5PUPbU=s100-rw)            | **YouAreUto** (2019)                | [Android](https://play.google.com/store/apps/details?id=com.youare.uto), [iOS](https://apps.apple.com/app/brain-game-teaser-youareuto/id1590561597#?platform=iphone) | [GitHub](https://github.com/YouAreUto/YouAreUto)                  |
| ![Defending Todot icon](https://imgur.com/Bn10XAf.png)                                                                                          | **Defending Todot** (2020)          | [HTML5](https://crystal-bit.github.io/defending-todot/)                                                                                                              | [GitHub](https://github.com/crystal-bit/defending-todot)          |
| ![Karooto No Gase icon](https://play-lh.googleusercontent.com/sWgjV9dJxa1jKina0mNbU3fGmqA4zuqtRWXfhn_dfEK6reW90GH1uz0wsai1SG898bOZ=s100-rw)     | **Karooto No Gase** (2021)          | [Android](https://play.google.com/store/apps/details?id=org.calalinta.karootonogase), [Itch.io](https://calalinta.itch.io/)                                          | N/A                                                               |
| ![Godot Game Template Demo](https://play-lh.googleusercontent.com/aOVexQckoyjN2WJp_puq8ifTr2TnWwJ-cNw6iflcH0IpQYp04m_ChTd0jwkCKalz5wVM=s100-rw) | **demo-godot-game-template** (2021) | [Android](https://play.google.com/store/apps/details?id=org.crystalbit.godottemplate)                                                                                | [GitHub](https://github.com/crystal-bit/demo-godot-game-template) |

_Get in contact if you want to be featured here!_

### Changelog

- [changelog.md](./changelog.md)

# Features

- **Continuos Integration**:
  - Automatic desktop build (linux, windows, osx, HTML5)
  - Automatic HTML5 deploy to Github pages
  - Automatic HTML5 deploy to itch.io
  - Automatic Android builds
- **Scenes loading** with graphic transitions (fade-in/out)
  - Send parameters to the new scene
  - Input prevention during scene changes
  - You can still play individual scenes for quick development
  - Singlethread & Multithread
- **Game pause** handling
- `.gitignore`
- Follows official GDScript guidelines (tested with [gdlint](https://github.com/Scony/godot-gdscript-toolkit#gdscript-toolkit))
- Compatible with other Godot addons

# How to

## Change scene

```gd
Game.change_scene("res://scenes/gameplay/gameplay.tscn")
```

![change_scene](https://user-images.githubusercontent.com/6860637/162567110-026c1979-6237-4255-bb2a-97815fc4b0c4.gif)

## Change scene and show progress bar

```gd
Game.change_scene("res://scenes/gameplay/gameplay.tscn", {
  "show_progress_bar": true
})
```

![progress](https://user-images.githubusercontent.com/6860637/162567097-81b5c54e-1ee5-42b9-a583-60764ecff069.gif)

## Change scene and pass parameters

```gd
# you can pass whatever value you like: int, float, dictionary, ...
var params = {
  "level": 4,
  "skin": 'dark'
}
Game.change_scene("res://scenes/gameplay/gameplay.tscn", params)
```

```gd
# gameplay.gd

func pre_start(params):
   print(params.level) # 4
   print(params.skin) # 'dark'
   # setup your scene here
```

To learn more about all the features, read the [wiki](https://github.com/crystal-bit/godot-game-template/wiki/2.-Features). 

## Center a Node2D into the viewport

```gd
$Sprite.position = Game.size / 2
```

## Contributors

Many features were implemented only thanks to the help of:

- [Andrea-Miele](https://github.com/Andrea-Miele)
- [Fahien](https://github.com/Fahien)
- [Andrea1141](https://github.com/Andrea1141)
- [vini-guerrero](https://github.com/vini-guerrero)

Also many tools were already available in the open source community, see the [Thanks](#thanks) section.

## Contributing

Development of new versions is made on the [`dev`](https://github.com/crystal-bit/godot-game-template/tree/dev) branch.

If you want to help the project, create games and feel free to get in touch and report any issue.

![Discord](https://img.shields.io/discord/686600734636376102?logo=discord&logoColor=ffffff&color=7389D8&labelColor=6A7EC2)

You can also join [the Discord server](https://discord.gg/SA6S2Db) (`#godot-game-template` channel).

Before adding new features please open an issue to discuss it with other contributors.

## Thanks

- For support & inspiration:
  - All the [contributors](https://github.com/crystal-bit/godot-game-template/graphs/contributors)
  - Crystal Bit community
  - GameLoop.it
  - Godot Engine Italia
  - Godot Engine
- For their work on free and open source software:
  - [aBARICHELLO](https://github.com/aBARICHELLO/godot-ci)
  - [croconut](https://github.com/croconut/godot-multi-builder)
  - [josephbmanley](https://github.com/josephbmanley)
  - [GDQuest](https://github.com/GDquest)
  - [Scony](https://github.com/Scony)
  - [myood](https://github.com/myood)


# Escoria

# Escoria Demo Game

![](https://raw.githubusercontent.com/godot-escoria/.github/main/design/escoria-logo-small.png)

[![Join our Discord](https://img.shields.io/discord/884336424780984330.svg?label=Join%20our%20Discord&logo=Discord&colorB=7289da&style=for-the-badge)](https://discord.com/invite/jMxJjuBY5Z)

Libre framework for the creation of point-and-click adventure games with the multi-platform game engine [Godot Engine](https://godotengine.org).

Check out the [Escoria documentation](https://docs.escoria-framework.org), especially the Getting Started Guide for further details.

If you want to contribute to the development of Escoria, please read our [Contribution guidelines](https://github.com/godot-escoria/.github/blob/main/CONTRIBUTING.md).

This is the demo game that acts as a testing ground for future Escoria development and a general showcase of its features.

## Art credits

### Characters

- Mark spritesheet by Marco Giorgini - marcogiorgini.com 
  Licence : CC0 Licence
  https://opengameart.org/content/mark-2d-adventure-game-sprite
  with some additions (talk animations) by Julian Murgia
- Worker spritesheet based on Mark spritesheet by Marco Giorgini - marcogiorgini.com 
  Licence: CC0 Licence
  edited by Julian Murgia

### Items

* Generic items by Kenney
* Animal pack redux by Kenney
  Licence: CC0 Licence
  https://www.kenney.nl/assets/generic-items

## Sound credits

* Concrete footstep
  Licence: CC0 Licence
  https://www.kenney.nl/
* “Game Menu Looping” (Licence CC-BY 4.0)
* “Mystical Ocean Puzzle Game” (Licence CC-BY 4.0)
  by Eric Matyas
  www.soundimage.org
  
## Cursors

* Pointers part 4 by "yd"
  Licence: CC0 Licence
  https://opengameart.org/content/pointers-part-4x
  edited by Julian Murgia

## Font

These fonts are provided as an example. Please mind checking the licence before redistributing with your game.

- Caslon Antique 
  https://www.1001fonts.com/caslon-antique-font.html#license
  Licence: Free for personal use - Free for commercial use
  This is the font used in LucasArt's game Curse of Monkey Island.

- Onesize
  https://www.whatfontis.com/Onesize.font
  Licence: Free for personal use
  This is the font used in LucasArt's games The Secret of Monkey Island and Monkey Island 2: Lechuck's Revenge.
