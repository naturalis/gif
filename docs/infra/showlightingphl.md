---
id: showlightgif
type: Infrastructure
title: Show verlichting GIF!
description: Aansturing van show verlichting GIF!
exhibition: gif
location:
  building: phl
suppliers:
  - name: kissbox-europe
tags:
  - power
components:
  - id: showlightgif-ecue-001
    type: ecue
    barcode: dt003566
    description: Ecue lighting computer
    ip: 172.16.75.6
    mac: 84:8f:69:f8:ab:02
  - id: showlightgif-butler-001
    type: butler
    description: Butler voor Ecue
    ip: 172.16.75.8
    mac: 00:16:1c:f0:25:29
  - id: showlightgif-butler-002
    type: butler
    description: Butler voor Ecue
    ip: 172.16.75.10
  - id: showlightgif-kissbox-ecue-001
    type: kissbox-general
    description: Kissbox op zolder voor Ecue
    ip: 172.16.75.9
    mac: 00:e0:6b:ff:06:03
---

# Infrastructure: Stroomvoorziening Pesthuis

## Algemene omschrijving

Dit document beschrijft de inrichting en aansturing van de show verlichting van de GIF! tentoonstelling in het Pesthuis.

## Support

 * ICT Infra: is verantwoordelijk voor de netwerkconnectiviteit van de Kissboxen en de Ecue computer.

## Technische details

De aansturing van de showverlichting gebeurt door middel van het lichtprogramma Ecue. Dit programma staat geïnstalleerd op de lichtcomputer die in AV cabine staat. Deze computer is geconfigureerd met Wake on Lan (WoL) en wordt op deze wijze bij het aanzetten van de tentoonstelling door Stargazer aangezet. De computer is geconfigureerd met twee accounts (Exhibit en LocalAdmin). Bij het opstarten logt het Exhibit account automatisch in. [Zie de Stargazer documentatie voor meer details over hoe dit is ingesteld](https://github.com/MakeExpose/stargazer/blob/develop/README.md#windows-device)
De Ecue lichtcomputer is geconfigureerd

Het lichtprogramma bestaat uit een statische look van railspots die zijn aangesloten op conventionele dimmers. Daarnaast is er een doorlopende sequentie van kleurwisselingen met de Elation Sixpar schijnwerpers. Iedere zaal heeft hiervoor zijn eigen sequentie, zijn eigen cuelist.

De e:cue PC wordt door de ICT afdeling iedere dag opgestart. Nadat Windows is opgestart wordt automatisch de e:cue programmer opgestart en deze gebruikt hiervoor het laatst opgeslagen showfile. In dit geval is dit (“Gif v11.shw”)[https://drive.google.com/open?id=0B5f_FPhR8B0nT0pCVHF1b2QycHgxdEVkamNwOFlobGZiTlIw].

Deze showfile start in de zogenaamde kioskmode op, oftewel er is alleen een userscreen met twee knoppen in beeld. De startknop hoeft in principe niet gebruikt te worden aangezien de showfile door middel van de [Initialization Load Show] trigger [Cuelist QL1 Play] vanzelf gaat lopen.

Op het userscreen is verder te zien of het ethernet DMX device, de Butler, online is en of alle cuelisten lopen.

Mocht het nodig zijn het programma aan te passen of iets dergelijks moet de kioskmode verlaten worden. Dit doe je door op de groene e:cue button (linksonder in beeld) te drukken en eerst op [Log in] te klikken. Dan moet het password ingevoerd worden. Daarna, als je ingelogd bent, klik je op de groene e:cue button en dan op [Leave kiosmode].

[Zie dit document voor meer details over de lichtshow.](https://drive.google.com/open?id=0B5f_FPhR8B0na2xFN0hySHVtdUlHTzI5UUs1RjBNd2lzY3NF)

### Known issues

* De Ecue lichtcomputer wordt momenteel bij het opstarten van de tentoonstelling eerst uitgeschakeld omdat in het geval van een stroomonderbreking de computer na het herstel van de stroomvoorziening automatisch opstart. In dat geval geeft de lichtcomputer al een signaal uit voordat de lampen stroom hebben hetgeen leidt tot problemen.
