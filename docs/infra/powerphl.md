---
id: powerphl
type: Infrastructure
title: Power supply Pesthuis
description: 
exhibition: gif
location:
  building: phl
suppliers:
  - name: kissbox-europe
tags:
  - power
components:
  - id: powerphl-kissbox-mer
    type: kissbox-general
    ip: 172.16.75.11
    mac: 00:e0:6b:7e:ff:8a
    dataoutlet: Rechtstreeks
  - id: powerphl-kissbox-lift
    type: kissbox-general
    ip: 172.16.75.12
    mac: a00:e0:6b:7e:ff:7
    dataoutlet: MER-M-09
  - id: powerphl-kissbox-ser
    type: kissbox-do4pr
    ip: 172.16.75.13
    mac: 00:e0:6b:7e:ff:4d
    dataoutlet: Rechtstreeks
  - id: powerphl-mpower-studio
    type: mfi-mpower-pro-eu
    ip: 172.16.45.55
    mac: 04:18:d6:54:1c:5d
    dataoutlet: SER-02-07
---

# Infrastructure: Stroomvoorziening Pesthuis

## Algemene omschrijving

Dit document beschrijft de stroomvoorziening in het Pesthuis.

## Support

 * ICT Infra: is verantwoordelijk voor het de aansturing en de netwerkconnectiviteit van de Kissboxen en de mPower stekkerdozen.
 * Vastgoed is verantwoordelijk voor het beheer en onderhoud van alle electravoorzieningen.

## Technische details

Er wordt gebruik gemaakt van in totaal drie Kiss-boxen:

* powerphl-kissbox-mer
  Locatie: MER
  Aantal schakelaars: 12
* powerphl-kissbox-lift
  Locatie: Om de hoek bij de lift van het restaurant
  Aantal schakelaars: 6
* powerphl-kissbox-ser
  Locatie: SER / AV cabine
  Aantal schakelaars: 2

De Kiss-Boxen worden aangestuurd door Stargazer, de controller unit waarmee de gehele tentoonstelling en werkverlichting wordt aangestuurd. [Check hier de code waarmee de kissboxen daadwerkelijk worden aangestuurd.](https://github.com/MakeExpose/stargazer/blob/develop/lib/devices_executor.py#L174)

Naast de Kiss-Boxen wordt in de Studio gebruik gemaakt van een Ubiquity mPower stekkerdoos die aangesloten is op het netwerk en waarmee zes stopcontacten individueel op afstand geschakeld kunnen worden. [Check hier de code waarmee de mPower stekkerdoos wordt aangestuurd vanuit Stargazer.](https://github.com/MakeExpose/stargazer/blob/develop/lib/devices_executor.py#L253)

### Known issues

* De labels op de power outlets blijken lang niet altijd te kloppen.
