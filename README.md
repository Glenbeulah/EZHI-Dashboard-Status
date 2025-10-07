# EZHI-Dashboard-Status
## Overview

This code can be used to monitor an EZHI microinverter (Apsystems) status with battery in your HA Dashboard using lovelance mushroom cards and fold-entity-row

## Features

- Battery Monitoring: View battery state (Laden, Entladen, Fehler, Shutdown, Keine Kommunikation) 

- System Monitoring: Summerizes system status (System Status OK, System Status Fehleraktiv)

- Dropdown for all system parameter
- Color and Icon change depending on status

## Before installing this integration, you need to:

- Ensure your APsystems EZHI inverter is connected to your local network
- Set a static IP address for the inverter in your router (recommended)

## HACS (Recommended)

- Add https://github.com/piitaya/lovelace-mushroom for Mushroom cards
- Add https://github.com/thomasloven/lovelace-fold-entity-row for Dropdown
- Add Addon code from configuration.yaml to your configuration.yaml and insert your IP adresse
- Restart Home Assistant
- Add Addon code from dashboard.yaml into your dashboard (example is a stand alone dashboard)

## Sensors (from /getOutputData)

  - batS       sensor.ezhi_battery_status
     - 1 => Leerlauf
     - 2 =>Laden
     - 3 => Entladen
     - 4 => Fehler
     - 5 => Shutdown
     - 6 => Keine Kommunikation 

## Binary sensor (from /getAlarm)

  - BatLTP  Batterie Untertemperatur
  - BatHTP  Batterie Übertemperatur
  - BatCE   Batterie Kommunikationsfehler
  - BatHV   Batterie Überspannung
  - BatLV   Batterie Unterspannung
  - BatHI   Batterie Überstrom
  - BatE    Allgemeiner Batteriefehler
  - DTP     Gerät Übertemperatur
  - EE      Gerätefehler
  - SBS     Batterie Shutdown
  - ACA     AC Fehler
  - OfOI    Off-Grid Überstrom
  - PvHV    PV Überspannung
  - PvOC    PV Überstrom
  - IRDE    IRD Fehler
  - PVWE    PV Verdrahtungsfehler
  - OfGS    Off-Grid Kurzschluss
  
## Troubleshooting

- Ensure the inverter is connected to your network
- Check that the IP address is correct
- Ensure the inverter is powered on 

## License

This project is released under the MIT License.
