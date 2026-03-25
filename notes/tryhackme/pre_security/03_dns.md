# DNS (Domain Name System)

## What is DNS?
DNS to system nazw domen, który działa jak „książka telefoniczna internetu”.

Zamiast zapamiętywać adresy IP (np. 142.250.74.14), możemy używać nazw domen (np. google.com).  
DNS tłumaczy nazwę domeny na adres IP, dzięki czemu komputer wie, gdzie się połączyć.

---

## Domain Hierarchy

### ROOT (.)
- najwyższy poziom w hierarchii
- zwykle niewidoczny dla użytkownika

---

### TLD (Top-Level Domain)
To końcówka domeny, np.:
- .com
- .edu
- .gov

Rodzaje:
- gTLD (generic) → .com, .gov, .edu
- ccTLD (country) → .pl, .uk, .ca

---

### SLD (Second-Level Domain)
- właściwa nazwa domeny (np. google w google.com)
- maksymalnie 63 znaki

---

### Subdomain
- wszystko przed nazwą domeny
- np. admin.tryhackme.com
- można mieć wiele subdomen
- maksymalna długość całej nazwy: 253 znaki

---

## DNS Records

DNS działa jak baza danych, a rekordy to wpisy w tej bazie.

### Najważniejsze rekordy:

- **A** → domena → IPv4  
  np. google.com → 142.250.74.14  

- **AAAA** → domena → IPv6  

- **CNAME** → alias (przekierowanie na inną domenę)  

- **MX** → serwery poczty  
  - niższa liczba = wyższy priorytet  
  - np. 10 (główny), 20 (zapasowy)

- **TXT** → dodatkowe informacje  
  używane np. do:
  - SPF (kto może wysyłać maile)
  - DMARC (ochrona przed spamem)
  - weryfikacja domeny

---

## How DNS Works (step by step)

1. Komputer sprawdza lokalną pamięć podręczną (cache)  
2. Jeśli brak → zapytanie do Recursive DNS Server  
3. Jeśli brak → zapytanie trafia do:
   - Root DNS
   - TLD DNS
   - Authoritative DNS
4. Serwer autorytatywny zwraca adres IP  
5. Odpowiedź wraca do komputera i strona się ładuje  

---

## TTL (Time To Live)
TTL określa, jak długo odpowiedź DNS jest przechowywana w cache.

Przykład:
TTL = 3600 → 1 godzina  

Po tym czasie zapytanie musi zostać wykonane ponownie.

---

## Tool: nslookup

Służy do sprawdzania rekordów DNS.

Przykłady:
nslookup --type=A google.com
nslookup --type=MX google.com

---

## My notes / What I learned
- DNS tłumaczy nazwy domen na adresy IP
- działa hierarchicznie (Root → TLD → Authoritative)
- rekordy DNS przechowują różne informacje (IP, mail, aliasy)
- TTL wpływa na czas przechowywania danych w cache
- narzędzia jak nslookup pozwalają analizować DNS
