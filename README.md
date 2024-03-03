# NimGame Activity Flatpak

The Game of Nim is a two-player mathematical game of strategy. It is typically played with a collection of objects such as stones, sticks, or coins arranged in several heaps. Players take turns removing objects from the heaps according to specific rules. The objective of the game is to avoid being the player to take the last object.

To know more refer https://github.com/SudoSu-bham/NimGame

## How to build

To build this run the following command in terminal

```bash
https://github.com/SudoSu-bham/org.sugarlabs.NimGame.git
cd org.sugarlabs.NimGame
flatpak -y --user install org.gnome.{Platform,Sdk}//44
flatpak-builder --user --force-clean --install build org.sugarlabs.NimGame.json
```


## Check for updates
Install the flatpak external data checker

```bash
flatpak --user install org.flathub.flatpak-external-data-checker
```
To update every Single module to the latest stable version use

```bash
cd org.sugarlabs.NimGame
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.NimGame.json
```
