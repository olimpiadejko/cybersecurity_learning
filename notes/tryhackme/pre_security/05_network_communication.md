# Network Communication (Packets, TCP/IP, Ports, Firewall)

## Packet (Pakiet)

Pakiet to jednostka danych z warstwy 3 modelu OSI (Network).

Zawiera:
- nagłówek IP
- dane (payload)

odpowiada za dostarczenie danych do właściwego urządzenia w sieci  
umożliwia komunikację między różnymi sieciami  

Dane są dzielone na małe pakiety:
- zwiększa to wydajność  
- zmniejsza ryzyko przeciążenia sieci  

---

### IP Packet Header (najważniejsze pola)

- **TTL (Time To Live)**  
  ogranicza liczbę przeskoków (każdy router zmniejsza TTL o 1)

- **Checksum**  
  sprawdza czy dane nie zostały uszkodzone (IPv4)

- **Source IP**  
  adres nadawcy  

- **Destination IP**  
  adres odbiorcy  

---

## Frame (Ramka)

Ramka działa w warstwie 2 (Data Link).

- „opakowuje” pakiet  
- dodaje adresy MAC (nadawcy i odbiorcy)  

działa tylko w sieci lokalnej (LAN)  

---

## How Data Travels (krok po kroku)

1. komputer tworzy pakiet (IP odbiorcy)  
2. pakiet jest opakowany w ramkę  
3. trafia do routera  
4. router usuwa starą ramkę i tworzy nową  
5. pakiet pozostaje ten sam aż do celu  

---

## Encapsulation

Enkapsulacja = dodawanie nagłówków na każdej warstwie OSI

dane „opakowywane” są warstwa po warstwie  

---

## TCP/IP Model

Uproszczona wersja OSI.

Warstwy:
- Application  
- Transport  
- Internet  
- Network Interface  

---

### TCP (Transmission Control Protocol)

- działa w warstwie transportowej  
- zapewnia niezawodność  
- kontroluje kolejność i kompletność danych  

---

### TCP Connection Closing

1. FIN → „kończę”  
2. ACK → potwierdzenie  
3. FIN → druga strona kończy  
4. ACK → finalne potwierdzenie  

---

## UDP/IP

- **UDP** → szybki, brak kontroli błędów  
- **IP** → adresowanie i dostarczenie danych  

### Zastosowania UDP:
- streaming  
- gry online  
- rozmowy  
- DNS  

---

## Ports

Porty określają do jakiej aplikacji trafią dane.

Zakres:
- 0–1024 → well-known ports  
- 1025–49151 → registered  
- 49152–65535 → dynamic  

---

### Common Ports

- 80 → HTTP  
- 443 → HTTPS  
- 21 → FTP  
- 22 → SSH  
- 445 → SMB  
- 3389 → RDP  

---

## Port Forwarding

Pozwala udostępnić usługę z sieci lokalnej do internetu.

Router:
- odbiera ruch (np. port 80)  
- przekazuje go do konkretnego urządzenia w sieci  

---

## Firewall

Firewall to zabezpieczenie sieci.

Sprawdza:
- skąd pochodzi ruch  
- dokąd zmierza  
- jaki port  
- jaki protokół (TCP/UDP)  

analizuje pakiety i decyduje czy je przepuścić  

Działa na:
- warstwie 3 (Network)  
- warstwie 4 (Transport)  

---

### Types of Firewall

- **Stateless**  
  - analizuje każdy pakiet osobno  
  - szybki, ale mniej inteligentny  

- **Stateful**  
  - analizuje całe połączenie  
  - pamięta stan komunikacji  
  - bardziej zaawansowany  

---

## My notes / What I learned
- pakiety przenoszą dane między sieciami  
- ramki działają lokalnie (LAN)  
- enkapsulacja to „opakowywanie” danych  
- TCP jest dokładny, UDP szybki  
- porty kierują dane do aplikacji  
- firewall chroni sieć analizując ruch  
