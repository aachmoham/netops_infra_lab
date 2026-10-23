# NetOps & Infrastructure Lab (`netops-infra-lab`)

Welkom bij de documentatie van het **NetOps & Infrastructure Lab Project**. Dit project omvatte het ontwerpen, opbouwen, inventariseren en onderhouden van netwerklabo's, serverruimtes en netwerkapparatuur.

> **Doel van deze repository:** Het documenteren van mijn praktische ervaring op het gebied van netwerkbeheer, hardware-installatie, procesautomatisering en projectmatig werken binnen een IT-infrastructuuromgeving.

---

## Geleerde & Toegepaste Vaardigheden

- **Netwerk- & Systeembeheer:** Configuratie van routers/switches, firmware-upgrades via TFTP, wachtwoordresets via bootmanager, en uitrol/configuratie van Linux (Ubuntu & Alpine Linux).
- **Infrastructure Architecture & Simulatie:** Fysieke opbouw van serverracks, bekabeling (velcro management), rack-layout planning in Excel en virtualisatie/simulatie in Cisco Packet Tracer (Physical & Logical View).
- **Automatisering & Scripting:** Schrijven van Python/Batch-scripts om netwerkinventarisatie en updates te automatiseren; offline pakketbeheer (.apk) via USB.
- **Troubleshooting & AI-Driven Debugging:** Oplossen van netwerk-timeouts, firewallblokkades, seriële poortconflicten (`/dev/ttyS0` getty-dienst) en hardwarematige pings/connectiviteitstesten.
- **Methodiek & Projectbeheer:** Werken volgens Kanban-principes, gestructureerde taakverdeling, prioritisering en heldere fysieke/digitale documentatie.

---

## Projectoverzicht & Key Achievements

### 1. Fysieke Infrastructuur & Rack-opbouw
- Opzetten van studentenpods en serverruimtes: monteren van routers, switches, verdeelstekkers (PDU's) en opslagplateaus in de racks.
- Structureren van racks voor 4 studenten per rack (met uitbreidingsruimte naar 6 studenten) inclusief een dedicated hoofdlayer.
- Schoonmaken, bekabelen (velcro) en herstructureren van netwerklokalen om downtime en rommel te voorkomen.
- Vóóraf uittekenen van rack-layouts in Excel en vastleggen in praktijkopstellingen.
- Uitbreiden van netwerkapparatuur en server-PC's met extra Ethernet-/seriële poorten, schroefloze SSD's en nieuwe knoopcelbatterijen.

### 2. Netwerkinventarisatie & Automatisering
- Een geautomatiseerd script ontwikkeld om netwerkapparatuur uit te lezen en te verwerken in een centraal overzicht.
- Implementatie van QR-codes om fysiek materiaal sneller te kunnen identificeren en scannen.

### 3. Lifecycle & Firmware Management
- Definieren en installeren van de **Target OS** (meest stabiele firmware) over het netwerk via een geconfigureerde **TFTP-server**.
- Uitvoeren van fabrieksresets en wachtwoordherstel op HP-switches via de bootmanager voor een schone basisconfiguratie.
- Voorzien van heldere status-markeringen (post-its/labels) op geüpdatete en geresette apparatuur inclusief inloggegevens voor het team.

### 4. Systeem- & Seriële Console-inrichting
- Uitrol van **Alpine Linux (64-bit)** op dedicated console-PC's voor seriële verbindingen met netwerkapparatuur.
- Seriële poortconflicten (`ttyS0`) opgelost in `/etc/inittab` en offline installatie van hulpprogramma's (`picocom`) via USB ingericht.

---

## Navigatie door de Documentatie

- [`docs/project-scope.md`](docs/project-scope.md): Gedetailleerd overzicht van mijn specifieke takenpakket.
- [`docs/planning.md`](docs/planning.md): Mijn manier van projectmatig werken en plannen.
- [`docs/rack-architecture.md`](docs/rack-architecture.md): Technisch ontwerp en Packet Tracer simulaties van de fysieke racks.
- [`docs/firmware-management.md`](docs/firmware-management.md): Automatisering, scripting, TFTP-setup en het firmware updateplan.
