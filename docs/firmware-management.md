# Firmware, OS & Automation Strategy

Een belangrijk onderdeel van netwerkbeheer is zorgen dat alle apparatuur op veilige, ondersteunde firmware draait (*Target OS*) en dat beheersinterfaces snel toegankelijk zijn.

## 1. TFTP Firmware Upgrades & Troubleshooting

Voor het geautomatiseerd en efficiënt upgraden van switches is een dedicated **TFTP-server** ingericht.

* **Troubleshooting Proces:** 
  Bij het laden van nieuwe OS-images traden in eerste instantie time-out errors op tijdens de TFTP-overdracht. Dit is opgelost door:
  1. Ping-tests en netwerkverbindingscontroles uit te voeren.
  2. Firewalls tijdelijk uit te schakelen en poorttoegankelijkheid te controleren.
  3. Bestandspaden te verifiëren en gerichte debugging toe te passen (met behulp van AI-tools).
* **Documentatie:** De exacte stappen en handige troubleshoot-commando's zijn vastgelegd in een interne handleiding om toekomstige upgrades te versnellen.

## 2. Factory Reset & Bootmanager Recovery

Wanneer netwerkapparatuur (zoals HP-switches) na een reset om onbekende inloggegevens vraagt, is een recovery via de **bootmanager** uitgevoerd:
* Toegang verkregen tot de bootmanager om beveiligingsinstellingen te omzeilen.
* Volledige fabrieksreset uitgevoerd en een schone basisconfiguratie toegepast.
* Apparatuur voorzien van fysieke post-its/labels met de nieuwe OS-status en inloggegevens voor het team.

## 3. Alpine Linux & Seriële Console Inrichting

Om netwerkapparatuur lokaal te kunnen beheren via een seriële kabel, zijn console-PC's geconfigureerd met **Alpine Linux**:

* **Architectuur-compatibiliteit:** De 64-bit versie van Alpine Linux is vereist om pakketcompatibiliteit (zoals `picocom`) te garanderen.
* **Offline Uitrol:** `.apk`-installatiebestanden zijn gedownload en via een USB-bootstick offline geïnstalleerd op de werkstations.
* **Seriële Poort Conflict Oplossen (`ttyS0`):**
  Alpine claimde standaard de seriële poort voor een inlogprompt. Dit conflict is als volgt verholpen:
  ```bash
  # Schakel de getty-dienst op ttyS0 uit in /etc/inittab (voeg een # toe):
  # ttyS0::respawn:/sbin/getty-custom 115200 ttyS0

  # Herlaad en sla op via init:
  init q
  lbu commit usb
