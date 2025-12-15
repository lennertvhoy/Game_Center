# Voorstel Verbeterpunten: Game Center Netwerk

Na onderzoek van de huidige repository (`opdracht.txt`, `Documentatie`, en `Configuratie`), voldoet het project aan de basisvereisten. Er zijn echter een aantal verbeterpunten mogelijk om het netwerk professioneler, veiliger en gebruiksvriendelijker te maken.

## 1. Beveiliging (Security Hardening)
Hoewel de wachtwoorden en encryptie zijn ingesteld, kan de beveiliging worden verhoogd:

-   **Poorten uitschakelen**: In `Netwerk_Documentatie.md` wordt aangeraden ongebruikte poorten uit te schakelen (`shutdown`), maar dit zit nog niet in de config files.
    -   *Actie*: Toevoegen van een `interface range ... shutdown` script.
-   **SSH i.p.v. Telnet**: Momenteel wordt platte tekst (mogelijk Telnet) toegelaten op de VTY lijnen. SSH is veiliger.
    -   *Actie*: Crypto keys genereren en SSH forceren op VTY lijnen.
-   **DNS Lookup**: Om te voorkomen dat de switch/router vastloopt bij een typo (omdat hij dat als domeinnaam probeert op te zoeken), is `no ip domain-lookup` een 'best practice'.

## 2. Netwer Stopologie & Stabiliteit
-   **Expliciete Trunks**: Het netwerk vertrouwt nu op de standaard VLAN 1 configuratie. Het is beter om verbindingen tussen switches expliciet als **Trunk** in te stellen.
    -   *Voordeel*: Betere controle over welk VLAN over welke kabel gaat en voorbereiding op toekomstige uitbreidingen.

## 3. Gebruiksgemak (Quality of Life)
-   **Logging Synchronous**: Voorkomt dat logberichten je typtewerk in de console onderbreken.
    -   *Commando*: `logging synchronous` onder `line console 0`.

## 4. Documentatie
-   **Kabeloverzicht**: De config bestanden specificeren niet welke poort naar welke switch gaat (behalve op de router). Het toevoegen van `description Uplink naar ...` op specifieke switchpoorten maakt het debuggen makkelijker.

---

### Wil je dat ik deze verbeteringen doorvoer?
Ik kan:
1.  De configuratiebestanden updaten met deze 'best practices'.
2.  De documentatie bijwerken om deze wijzigingen te reflecteren.
