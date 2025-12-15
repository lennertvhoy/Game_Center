# README: Game Center Netwerk

Dit document geeft een overzicht van de opgeleverde bestanden voor de netwerkopdracht.

## 📂 Mappenstructuur

Het project is ordelijk onderverdeeld in 2 mappen:

1.  **Documentatie**: Bevat het volledige ontwerp.
2.  **Configuratie**: Bevat de command-line bestanden voor de apparatuur.

## 📄 Documentatie
*   [Netwerk Ontwerp & IP Schema](Documentatie/Netwerk_Documentatie.md)
    *   *Bevat de topologie, IP-adressen tabel en VLAN informatie.*
*   [Fysieke Verbindingen (Patching)](Documentatie/Verbindingen_Tabel.md)
    *   *Tabel met kabelverbindingen tussen alle apparaten.*

## ⚙️ Configuratiebestanden

### Router
*   [GC-Router](Configuratie/Config_GC_Router.txt) (Gateway voor beide netwerken)

### Personeel
*   [Core Switch](Configuratie/Config_Personeel_Core_SW.txt)
*   [Kassa Switch](Configuratie/Config_Personeel_Kassa_SW.txt)
*   [Server Switch](Configuratie/Config_Personeel_Server_SW.txt)

### Klant
*   [Core Switch](Configuratie/Config_Klant_Core_SW.txt)
*   [Arcade Switch](Configuratie/Config_Klant_Arcade_SW.txt)
*   [Gaming Switch](Configuratie/Config_Klant_Gaming_SW.txt)

---
*Alles is geconfigureerd volgens de vereisten uit `opdracht.txt`.*
