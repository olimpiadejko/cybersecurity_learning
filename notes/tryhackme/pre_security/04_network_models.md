# OSI Model (Open Systems Interconnection)

## What is the OSI Model?

Model OSI (Open Systems Interconnection) opisuje, w jaki sposób dane przemieszczają się w sieci komputerowej. Składa się z **7 warstw**, z których każda pełni określoną funkcję. Dzięki temu różne systemy i technologie mogą się ze sobą komunikować, nawet jeśli zostały stworzone przez różnych producentów.

Przykład: podczas otwierania strony internetowej dane przechodzą przez wszystkie warstwy modelu OSI – od aplikacji użytkownika aż do fizycznej transmisji sygnału.

---

## Mnemonik ułatwiający zapamiętanie

**ALL PEOPLE SEEM TO NEED DATA PROCESSING**  
→ **APSTNDP**

Polska wersja:  
**ALA PROSI SWOJEGO TATĘ NA DOBRE PIEROGI**

---

## 7 Warstw Modelu OSI

### 7. Application (Warstwa aplikacji)
- Bezpośrednia interakcja użytkownika z usługami sieciowymi.
- Określa zasady wymiany danych między aplikacjami.
- **Przykładowe protokoły:** HTTP, HTTPS, DNS, DHCP, FTP, SMTP.

Przykład: wpisanie adresu strony w przeglądarce lub wysłanie e-maila.

---

### 6. Presentation (Warstwa prezentacji)
- Odpowiada za **formatowanie, kompresję i szyfrowanie danych**.
- Zapewnia, że dane są zrozumiałe dla systemu odbiorcy.
- Obsługuje różne kodowania znaków i formaty plików.

Przykład: szyfrowanie SSL/TLS używane w HTTPS.

---

### 5. Session (Warstwa sesji)
- Zarządza **nawiązywaniem, utrzymywaniem i kończeniem sesji** między aplikacjami.
- Umożliwia tworzenie **punktów synchronizacji (checkpoints)**.

Przykład: wznowienie pobierania pliku po przerwaniu połączenia.

---

### 4. Transport (Warstwa transportowa)
- Odpowiada za **dostarczanie danych między aplikacjami** oraz kontrolę jakości transmisji.
- Wykorzystuje **numery portów**.
- **Jednostka danych:** segment (TCP) lub datagram (UDP).

**Główne protokoły:**
- **TCP** – niezawodny, zapewnia kontrolę błędów i kolejność danych.
- **UDP** – szybszy, ale bez gwarancji dostarczenia.

---

### 3. Network (Warstwa sieciowa)
- Odpowiada za **adresowanie logiczne (IP)** i **routing**.
- Wybiera najlepszą trasę dla pakietów.

**Protokoły:**
- IP (IPv4/IPv6)
- ICMP
- Protokoły routingu: **OSPF**, **RIP**, **BGP**

Jednostka danych: **pakiet**

---

### 2. Data Link (Warstwa łącza danych)
- Zapewnia komunikację w obrębie tej samej sieci lokalnej (LAN).
- Wykorzystuje **adresy MAC**.
- Odpowiada za detekcję błędów.

**Przykłady technologii:**
- Ethernet
- Wi-Fi (IEEE 802.11)
- ARP

Jednostka danych: **ramka**

---

### 1. Physical (Warstwa fizyczna)
- Odpowiada za fizyczną transmisję danych w postaci **bitów**.
- Obejmuje wszystkie elementy sprzętowe.

**Przykłady:**
- kable Ethernet
- światłowody
- sygnały elektryczne i radiowe
- złącza i wtyczki

Jednostka danych: **bity**

---

## Jednostki danych w modelu OSI

| Warstwa | Jednostka danych |
|--------|-----------------|
| Application | Data |
| Presentation | Data |
| Session | Data |
| Transport | Segment / Datagram |
| Network | Packet |
| Data Link | Frame |
| Physical | Bits |

---

## Podsumowanie

- Model OSI składa się z **7 warstw**, które opisują proces komunikacji sieciowej.
- Każda warstwa ma określone zadania i współpracuje z innymi.
- Ułatwia projektowanie, analizę i rozwiązywanie problemów sieciowych.
- Jest podstawą wiedzy w cyberbezpieczeństwie i administracji sieci.

---

## My notes / What I learned
- Model OSI pomaga zrozumieć, jak dane przemieszczają się w sieci.
- Każda warstwa pełni określoną funkcję.
- TCP i UDP działają w warstwie transportowej.
- Adresy IP należą do warstwy sieciowej, a MAC do warstwy łącza danych.
- Znajomość modelu OSI jest kluczowa w cyberbezpieczeństwie.
