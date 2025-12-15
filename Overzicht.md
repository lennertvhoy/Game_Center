# Project Overzicht: Game Center Netwerk

Dit document geeft een overzicht van de opgeleverde bestanden voor de netwerkopdracht.

## 📂 Mappenstructuur

Het project is ordelijk onderverdeeld in 2 mappen:

1.  **Documentatie**: Bevat het volledige ontwerp.
2.  **Configuratie**: Bevat de command-line bestanden voor de apparatuur.

## 📄 Documentatie
*   [Netwerk Ontwerp & IP Schema](Documentatie/Netwerk_Documentatie.md)
    *   *Bevat de topologie, IP-adressen tabel en VLAN informatie.*

## ⚙️ Configuratiebestanden

### Router
*   [GC-Router](Configuratie/Config_GC_Router.txt) (Gateway voor beide netwerken)

### Personeel (VLAN 10)
*   [Core Switch](Configuratie/Config_Personeel_Core_SW.txt)
*   [Kassa Switch](Configuratie/Config_Personeel_Kassa_SW.txt)
*   [Server Switch](Configuratie/Config_Personeel_Server_SW.txt)

### Klant (VLAN 20)
*   [Core Switch](Configuratie/Config_Klant_Core_SW.txt)
*   [Arcade Switch](Configuratie/Config_Klant_Arcade_SW.txt)
*   [Gaming Switch](Configuratie/Config_Klant_Gaming_SW.txt)

---
*Alles is geconfigureerd volgens de vereisten uit `opdracht.txt`.*
