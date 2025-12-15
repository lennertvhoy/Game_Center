# Netwerk Verbindingen Overzicht

Dit document beschrijft de fysieke verbindingen (patching) tussen de verschillende netwerkapparaten.

| Bron Apparaat | Lokale Interface (Poort) | Bestemming Apparaat | Bestemming Interface | Type Verbinding |
| :--- | :--- | :--- | :--- | :--- |
| **GC-Router** | GigabitEthernet0/0 | Personeel-Core-SW | GigabitEthernet0/1 | Router-on-a-Stick / Trunk |
| **GC-Router** | GigabitEthernet0/1 | Klant-Core-SW | GigabitEthernet0/1 | Router-on-a-Stick / Trunk |
| | | | | |
| **Personeel-Core-SW** | GigabitEthernet0/1 | GC-Router | GigabitEthernet0/0 | Uplink |
| **Personeel-Core-SW** | GigabitEthernet0/2 | Personeel-Kassa-SW | GigabitEthernet0/1 | Downlink (Trunk) |
| **Personeel-Core-SW** | GigabitEthernet0/3 | Personeel-Server-SW | GigabitEthernet0/1 | Downlink (Trunk) |
| | | | | |
| **Personeel-Kassa-SW** | GigabitEthernet0/1 | Personeel-Core-SW | GigabitEthernet0/2 | Uplink (Trunk) |
| **Personeel-Server-SW** | GigabitEthernet0/1 | Personeel-Core-SW | GigabitEthernet0/3 | Uplink (Trunk) |
| | | | | |
| **Klant-Core-SW** | GigabitEthernet0/1 | GC-Router | GigabitEthernet0/1 | Uplink |
| **Klant-Core-SW** | GigabitEthernet0/2 | Klant-Arcade-SW | GigabitEthernet0/1 | Downlink (Trunk) |
| **Klant-Core-SW** | GigabitEthernet0/3 | Klant-Gaming-SW | GigabitEthernet0/1 | Downlink (Trunk) |
| | | | | |
| **Klant-Arcade-SW** | GigabitEthernet0/1 | Klant-Core-SW | GigabitEthernet0/2 | Uplink (Trunk) |
| **Klant-Gaming-SW** | GigabitEthernet0/1 | Klant-Core-SW | GigabitEthernet0/3 | Uplink (Trunk) |

## Opmerkingen
*   **Trunking**: Alle verbindingen tussen switches en naar de router zijn geconfigureerd om VLAN-verkeer door te laten.
*   **Ongebruikte Poorten**: Alle poorten die niet in deze tabel staan vermeld en niet in gebruik zijn voor eindapparaten (PC's, Kassa's), zijn administratief uitgeschakeld (`shutdown`) voor beveiliging.
