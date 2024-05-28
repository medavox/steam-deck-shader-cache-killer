# Steam Deck: Shader Cache Killer

Script to purge the Steam Deck's `shadercache` & `compatdata` directories

<img src="img/example.jpg" width="100%" />

# Steam Deck: Shader Cache Mover

Script to Symlink selected games Shader Cache & Compat Data to the SD card or External Drive

<img src="img/mover.jpg" width="100%" />

## Problem

With the 64GB verson of the Steam Deck, "Other" can quicky fill your internal SSD, even if you only store Games on the SD card. 
This "Other" is often `Shader Cache` & `CompatData`.


## Solution?

To free up some of the space you can delete the Shader Cache and/or the Compat(ability) Data.
The `zShaderCacheKiller` script aims to make that process a little easier.

Rather than deleting the Shader Cache or the Compat Data, `zShaderCacheMover` will copy & symlink selected games `shadercache` & `compatdata` directotries to the SD card or External Drive where the game is stored, freeing up the Internal Storage.


## Is this safe?

This has had limited testing on one system, USE AT OWN RISK

## What results can I expect?

For me I had 16.2GB of "Other" data, running  `zShaderCacheKiller` dropped this down to ~7GB.

My Back 4 Blood install was also using 3.5GB of Shader Cache, this I did not want to remove. Instead with `zShaderCacheMover` these files are now on my much larger SD card. As I also dual boot with Windows 11, this also saves space as the Shader Cache is now in the same location on the SD card.

## How to use

## Video Guide

https://www.youtube.com/watch?v=SLGvTDGDUcY

## Uninstall

To uninstall simply delete the install folder:

`sudo rm -r /home/deck/.local/share/scawp/SDSCK`

Also remove the `non-steam game` links in `Steam`
