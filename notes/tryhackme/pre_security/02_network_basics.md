# Network Basics

## What is a network?
Sieć to zbiór połączonych ze sobą elementów (np. ludzie, transport, systemy pocztowe).  
W informatyce oznacza to połączenie urządzeń takich jak komputery, telefony czy serwery.

Sieć może składać się z kilku urządzeń lub nawet miliardów (np. Internet).

---

## Internet
Internet to ogromna sieć składająca się z wielu mniejszych sieci.

- Początki: ARPANET (lata 60.)
- 1989: powstanie World Wide Web (WWW)

Internet składa się z:
- sieci prywatnych
- sieci publicznych (łączących inne sieci)

---

## Device Identification

### IP Address
Adres IP to identyfikator urządzenia w sieci.

- składa się z czterech oktetów (IPv4)
- np. 192.168.1.1
- nie może się powtarzać w tej samej sieci

Rodzaje:
- Publiczny → widoczny w internecie
- Prywatny → używany w sieci lokalnej

Przykład:
W domu wiele urządzeń ma różne IP prywatne, ale jedno wspólne IP publiczne.

---

### IPv4
- format: 4 liczby (0–255)
- liczba adresów: 2^32 (~4.3 miliarda)
- obecnie niewystarczające

---

### NAT (Network Address Translation)
Rozwiązanie problemu IPv4:

- wiele urządzeń → jeden publiczny IP
- np. wszystkie urządzenia w domu korzystają z jednego adresu

---

### IPv6
Nowy system adresowania:

- np. 2001:0db8:85a3:0000:0000:8a2e:0370:7334
- liczba adresów: 2^128 (ogromna liczba)
- pozwala na unikalny adres dla każdego urządzenia

---

### MAC Address
Adres MAC to unikalny identyfikator karty sieciowej.

- zapis szesnastkowy (hex)
- np. AA:BB:CC:DD:EE:FF
- pierwsza część → producent
- druga część → unikalny numer

#### MAC Spoofing
Możliwe jest podszywanie się pod inny adres MAC (spoofing), co może pozwolić np. obejść ograniczenia w sieci.

---

## Ping (ICMP)
Ping służy do sprawdzania połączenia między urządzeniami.

Wykorzystuje protokół ICMP:
- wysyła echo request
- odbiera echo reply

Komenda:
ping 8.8.8.8

Pokazuje:
- czy połączenie działa
- czas odpowiedzi (latency)

---

## TCP vs UDP

### TCP (Transmission Control Protocol)
- dokładność > szybkość
- sprawdza czy dane dotarły
- pilnuje kolejności
- retransmisja w razie błędów

#### 3-way handshake:
1. SYN
2. SYN-ACK
3. ACK

Użycie:
- strony WWW
- email
- transfer plików

---

### UDP (User Datagram Protocol)
- szybkość > dokładność
- brak sprawdzania poprawności
- brak kolejności

Użycie:
- gry online
- streaming (YouTube, Netflix)

---

## Delivery (IP + Port)

Aby dane trafiły do konkretnego miejsca:

1. IP → wskazuje urządzenie
2. PORT → wskazuje aplikację

Przykładowe porty:
- 80 → HTTP
- 443 → HTTPS
- 22 → SSH
- 21 → FTP
- 3306 → MySQL

---

## SSL / TLS
SSL (obecnie TLS) zapewnia szyfrowane połączenie między klientem a serwerem.

### Jak działa:
1. Client Hello
2. Server Hello
3. Tworzenie klucza sesji
4. Szyfrowana komunikacja

Bez SSL:
- dane mogą zostać przechwycone

Ikona kłódki w przeglądarce oznacza bezpieczne połączenie.

---

## My notes / What I learned
- Internet to sieć sieci
- IP identyfikuje urządzenie, port identyfikuje aplikację
- TCP jest dokładny, UDP szybki
- NAT pozwala wielu urządzeniom korzystać z jednego IP
- MAC może być spoofowany
- SSL chroni dane podczas transmisji
