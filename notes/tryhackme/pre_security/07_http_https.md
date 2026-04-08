# HTTP & HTTPS

## What is HTTP?
HTTP (HyperText Transfer Protocol) to protokół komunikacji między przeglądarką a serwerem.

Jak działa:
- przeglądarka wysyła żądanie (request)
- serwer odsyła odpowiedź (HTML, CSS, obrazy itd.)

❗ HTTP nie jest szyfrowany:
- dane mogą zostać przechwycone
- np. ataki typu sniffing lub Man-in-the-Middle (MITM)

Port: 80

---

## What is HTTPS?
HTTPS to HTTP + szyfrowanie (SSL/TLS).

Zapewnia:
- bezpieczeństwo danych
- pewność, że łączymy się z właściwym serwerem

Port: 443

---

## URL (Uniform Resource Locator)

URL to adres zasobu w internecie.

### Elementy URL:

- **Scheme (schemat)** → np. HTTP, HTTPS, FTP  
- **User** → dane logowania (rzadko używane, niebezpieczne)  
- **Host** → domena lub adres IP  
- **Port** → „drzwi” serwera (domyślnie 80/443)  
- **Path** → lokalizacja zasobu (np. /blog/artykul1)  
- **Query String** → parametry (np. ?id=1)  
- **Fragment** → konkretna sekcja strony (#sekcja)  

❗ Query string może być miejscem ataków (XSS, SQL Injection)

---

## HTTP Request (żądanie)

Przykład:
GET /blog?id=1 HTTP/1.1
Host: example.com

- GET → metoda (co chcemy zrobić)
- /blog?id=1 → zasób
- HTTP/1.1 → wersja protokołu

---

## HTTP Methods

- **GET** → pobieranie danych  
- **POST** → wysyłanie danych (np. formularz)  
- **PUT** → aktualizacja danych  
- **DELETE** → usuwanie danych  

---

## HTTP Status Codes

### Kategorie:
- 100–199 → informacyjne  
- 200–299 → sukces  
- 300–399 → przekierowania  
- 400–499 → błędy klienta  
- 500–599 → błędy serwera  

### Przykłady:
- 200 → OK  
- 201 → utworzono  
- 400 → błędne żądanie  
- 401 → brak autoryzacji  
- 403 → brak dostępu  
- 404 → nie znaleziono  
- 500 → błąd serwera  
- 503 → serwer niedostępny  

---

## HTTP Headers

Nagłówki to dodatkowe informacje wysyłane z requestem lub response.

### Request headers:
- **Host** → jaka strona  
- **User-Agent** → przeglądarka (można fałszować)  
- **Content-Length** → ilość danych  
- **Accept-Encoding** → kompresja  

---

### Response headers:
- **Set-Cookie** → zapis danych w przeglądarce  
- **Cache-Control** → czas przechowywania danych  
- **Content-Type** → typ danych (HTML, JSON itd.)  
- **Content-Encoding** → sposób kompresji  

---

## Cookies

Cookies to dane przechowywane w przeglądarce, które identyfikują użytkownika.

Dlaczego istnieją?
- HTTP jest bezstanowy (nie pamięta użytkownika)

Cookies:
- zawierają token (nie hasło)
- są wysyłane przy każdym żądaniu

❗ zagrożenia:
- kradzież cookies = przejęcie konta
- session hijacking

---

## HTML Injection

HTML Injection to luka w zabezpieczeniach, która występuje, gdy aplikacja wyświetla niefiltrowane dane od użytkownika.

W efekcie:
- użytkownik może wstrzyknąć własny kod HTML (lub JavaScript)
- przeglądarka traktuje dane jako kod, a nie tekst
- możliwa jest zmiana treści strony lub wykonanie złośliwego kodu

---

### How to prevent:

1. **Używaj `textContent` zamiast `innerHTML`**  
   - `innerHTML` → interpretuje dane jako kod  
   - `textContent` → traktuje dane jako zwykły tekst  

2. **Sanityzacja danych (czyszczenie inputu)**  
   Przykład: name.replace(/</g, "<").replace(/>/g, ">");

3. **Walidacja danych**

---
   
## Example Attacks

- SQL Injection:
  GET /blog?id=1 OR 1=1

- Path Traversal:
  GET /../../etc/passwd

- Phishing:
  fałszywe domeny (np. faceb00k-login.com)

---

## My notes / What I learned
- HTTP nie jest bezpieczny, HTTPS dodaje szyfrowanie
- request i response to podstawowa komunikacja w sieci
- URL zawiera wiele elementów (host, path, query itd.)
- metody HTTP określają operacje na danych
- cookies pozwalają serwerowi „pamiętać” użytkownika
- HTML Injection wynika z braku walidacji i filtrowania danych  
