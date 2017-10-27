---
id: eticket-checkin
type: ServicePoint
title: E-ticket check in points
description: Check in point at the entrance for ticket verification
exhibition: gif
location:
  building: phl
  room: phl-zaal-000
  position: Net voor de entree van zaal 1
suppliers:
  - name: logicsupply
  - name: tickets25
tags:
  - etickets
  - servicepoint
  - touchscreen
powersupply: paddenstoel-001
components:
  - id: switch-012
    type: hp1820-8g
    ip: 172.16.75.1
    mac: asdasdasdads
  - id: kissbox-012
    type: kissbox-hd1010
    ip: null
    mac: asdsdsdsd
---

# ServicePoint: E-ticket check in points

## General description

General description about the exhibit.

## Support

 * Support: is responsible for 
 * ICT Infra: is responsible for deployment of the OS and browser on the devices and network connectivity.
 * Tickets 25: is responsible for the 

## Technical details

### Components

#### Hardware

* Hardware: 

#### Software

* Ubuntu Linux
* Puppet
* Chrome
* Tickets25.com

### Deployment

Both eticket computers run Ubuntu Linux with a kiosk browser which is configured to open the Tickets25 portal. The software is deployed using Foreman and Puppet. The Puppet manifest which is applied [can be found here](https://github.com/naturalis/puppet-kiosk-minimal).

### Known issues

We've had several reports about the computers not powering off properly. We haven't been able to reproduce the issue.
