---
id: av_king_cobra
type: Exhibit
title: Intro video King Cobra
description: Projectie van video over konings cobra.
exhibition: gif
location:
  building: phl
  room: phl-zaal-001
  position: Nader te bepalen
suppliers:
  - name: second-nature
tags:
  - brightsign
  - video
components:
  - id: av_king_cobra-bs-001
    type: brightsign-hd1010
    ip: 172.16.75.21
    mac: 00:0d:4b:42:01:1c
  - id: av_king_cobra-projector-001
    type: mitsubishi-wd8200u
    ip: 172.16.75.32
    mac: 00:26:92:2f:10:bc
---

# Exhibit: Intro video King Cobra

## General description

Projectie van de King Cobra video in de eerste zaal van de tentoonstelling.

## Technische details

De video wordt afgespeeld op een Brightsign HD1010. Aan de GPIO poort van de
Brightsign player is met een UTP kabel een knoppenbedieningskastje verbonden
waarmee de volgende acties zijn geconfigureerd:

* Input 0: start de video
* Input 1: volume 0 (mute)
* Input 2: volume 50
* Input 3: volume 100
* Input 4: stop de video en toon het Gif logo

Bij het opstarten van de Brightsign player wordt de video gestart en staat het
audio volume op 100.

Het videobestand en de configuratie die worden gebruikt [staan in deze
map](https://drive.google.com/open?id=0B5f_FPhR8B0nSTNBTjl2aWlZYjA)

### Projector

De video wordt geprojecteerd met een Mitsubishi WD8200u projector. De projector
wordt met een UTP kabel direct in de switch van netwerkconnectiviteit voorzien.

Het aan- en uitzetten van de projector gebeurt door middel van 
[Stargazer](../infra/stargazer.md). Het aanzetten van de projector gebeurt op
basis van het inschakelen van de stroom, het uitzetten gebeurt op basis van het
PJLINK protocol.

## Known issues

De netwerkverbinding van de projector is zeer instabiel wanneer deze ingesteld
staat op DHCP. De verbinding gaat met die instelling om de seconde up en down.
Hierdoor werkt het remote uitlezen van de status en het remote uitschakelen van
de projector niet, of zeer onbetrouwbaar. Nadat de configuratie via het
projectormenu is aangepast naar een statische IP instelling is dit probleem
verholpen.
