# Project Scope & Takenpakket

In dit project was ik medeverantwoordelijk voor het opzetten en operationeel houden van de IT-infrastructuur in het labo en de serverruimte.

## Kernverantwoordelijkheden

### 1. Fysieke Opbouw & Infrastructuur Management
- **Studentenpods & Serverruimte:** Fysiek monteren van routers, switches, verdeelstekkers (PDU's) en opslagplateaus in de racks.
- **Capaciteitsplanning & Rackstructuur:** Racks opgebouwd volgens een structuur geschikt voor 4 studenten per rack (inclusief hoofdlayer), met flexibiliteit om uit te breiden naar 6 studenten.
- **Hardware-onderhoud & Uitbreiding:** Server-PC's voorzien van extra SSD's (schroefloos/kliksysteem) en nieuwe moederbordbatterijen. Routers uitgebreid met extra Ethernet- en seriële poorten.
- **Kabelbeheer & Structurele Netheid:** Het herstructureren en netjes bundelen van bekabeling (met behulp van klittenband/velcro) om storingen te voorkomen en overzicht te behouden.
- **Opruim & Afvoer (Lifecycle):** Scheiden van werkend en defect materiaal; afvoeren van verouderde apparatuur.
- **Lesruimtes klaarmaken:** Installeren van labomateriaal in meerdere leslokalen.

### 2. Netwerkinventarisatie & Automatisering
- **Automatische Inventarisatie:** Schrijven en debuggen van automatisering-scripts (Python / Batch) om de complete netwerkinfrastructuur uit te lezen.
- **Data-conversie:** Scripts geconfigureerd om opgehaalde gegevens automatisch te exporteren naar een centraal Excel-overzicht.
- **Physical Tracking:** Implementatie van QR-codes om hardware fysiek snel te scannen en te identificeren.

### 3. Firmware Lifecycle & Target OS Management
- **TFTP Server Setup:** Inrichten van een TFTP-server om netwerkapparatuur en switches te upgraden naar de nieuwste Target OS-image.
- **Hardware Reset & Bootmanager Recovery:** HP-switches via de bootmanager hersteld naar fabrieksinstellingen wanneer inloggegevens ontbraken.
- **Labeling & Overdracht:** Post-its en labels op apparatuur aangebracht met de nieuwe OS-status en inloggegevens om het team direct te informeren.

### 4. Systeembeheer, Console-PC's & Testing
- **Alpine Linux Console-PC's:** Inrichten van Alpine Linux (64-bit) op console-PC's om via `picocom` en de seriële poort apparatuur te beheren.
- **Probleemoplossing Seriële Poort:** Seriële poortconflicten opgelost door de `getty`-dienst op `ttyS0` in `/etc/inittab` uit te schakelen.
- **Offline Package Deployment:** Zorgen voor offline installatie van benodigde `.apk`-bestanden via USB-stick op systemen zonder internet.
- **Connectiviteitstesten & Troubleshooting:** Uitvoeren van ping-testen, firewall-controles en netwerkdiagnostiek bij time-out problemen.
