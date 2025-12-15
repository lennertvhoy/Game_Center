# Netwerk Verbindingen Overzicht

Dit document beschrijft de fysieke verbindingen (patching) tussen de verschillende netwerkapparaten.

| Bron Apparaat | Lokale Interface (Poort) | Bestemming Apparaat | Bestemming Interface |
| :--- | :--- | :--- | :--- |
| **GC-Router** | GigabitEthernet0/0 | Personeel-Core-SW | GigabitEthernet0/1 |
| **GC-Router** | GigabitEthernet0/1 | Klant-Core-SW | GigabitEthernet0/1 |
| | | | | |
| **Personeel-Core-SW** | GigabitEthernet0/1 | GC-Router | GigabitEthernet0/0 |
| **Personeel-Core-SW** | FastEthernet0/1 | Personeel-Kassa-SW | FastEthernet0/1 |
| **Personeel-Core-SW** | FastEthernet0/2 | Personeel-Server-SW | FastEthernet0/1 |
| | | | | |
| **Personeel-Kassa-SW** | FastEthernet0/1 | Personeel-Core-SW | FastEthernet0/1 |
| **Personeel-Server-SW** | FastEthernet0/1 | Personeel-Core-SW | FastEthernet0/2 |
| | | | | |
| **Klant-Core-SW** | GigabitEthernet0/1 | GC-Router | GigabitEthernet0/1 |
| **Klant-Core-SW** | FastEthernet0/1 | Klant-Arcade-SW | FastEthernet0/1 |
| **Klant-Core-SW** | FastEthernet0/2 | Klant-Gaming-SW | FastEthernet0/1 |
| | | | | |
| **Klant-Arcade-SW** | FastEthernet0/1 | Klant-Core-SW | FastEthernet0/1 |
| **Klant-Gaming-SW** | FastEthernet0/1 | Klant-Core-SW | FastEthernet0/2 |

## Opmerkingen
*   **Ongebruikte Poorten**: Alle poorten die niet in deze tabel staan vermeld en niet in gebruik zijn voor eindapparaten (PC's, Kassa's), zijn administratief uitgeschakeld (`shutdown`) voor beveiliging.
