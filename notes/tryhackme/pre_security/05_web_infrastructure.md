# Web Infrastructure Basics

## Load Balancer

Load Balancer służy do rozdzielania ruchu między wiele serwerów, aby zapobiec przeciążeniu jednego z nich.

Działa jak pośrednik:
- odbiera żądanie
- przekazuje je do jednego z serwerów

### Algorytmy:
- **Round Robin** → każdy serwer dostaje żądania po kolei  
- **Weighted (ważony)** → wybiera najmniej obciążony serwer  

### Funkcje:
- **Health check** → sprawdza czy serwery działają poprawnie  
- **Failover** → jeśli jeden serwer padnie, ruch trafia do innych  

---

## CDN (Content Delivery Network)

CDN to sieć serwerów rozmieszczonych na całym świecie.

Przechowuje:
- obrazy
- CSS
- JavaScript

Działanie:
- użytkownik wysyła żądanie
- CDN wybiera najbliższy serwer
- dane są dostarczane szybciej

👉 zmniejsza obciążenie głównego serwera i przyspiesza stronę

---

## WAF (Web Application Firewall)

WAF to zapora między użytkownikiem a serwerem.

Chroni aplikację przed atakami poprzez analizę żądań.

Sprawdza:
- czy żądanie pochodzi od prawdziwego użytkownika
- czy nie jest to bot
- czy nie ma zbyt wielu zapytań (rate limiting)

Jeśli wykryje zagrożenie:
- blokuje żądanie
- nie przekazuje go do serwera

---

## Web Servers

Serwer WWW to program, który odbiera żądania i wysyła odpowiedzi.

Przykłady:
- Apache
- Node.js

### Virtual Hosts
- jeden serwer może obsługiwać wiele stron
- dopasowanie odbywa się na podstawie domeny

### Root Directory
To miejsce, gdzie znajdują się pliki strony:

- Linux → /var/www/html  
- Windows → C:\inetpub\wwwroot  

Przykład:
example.com/image.jpg → /var/www/html/image.jpg  

---

## How a Website Works (Step by Step)

1. Użytkownik wpisuje adres strony  
2. Komputer sprawdza cache (czy zna IP)  
3. Zapytanie do DNS  
4. DNS zwraca adres IP  
5. Request przechodzi przez WAF i Load Balancer  
6. Połączenie z serwerem (port 80/443)  
7. Serwer odbiera żądanie  
8. Backend komunikuje się z bazą danych  
9. Serwer wysyła odpowiedź  
10. Przeglądarka wyświetla stronę  

---

## My notes / What I learned
- Load Balancer rozdziela ruch między serwery
- CDN przyspiesza ładowanie strony
- WAF chroni przed atakami
- serwer WWW obsługuje żądania i zwraca dane
- cały proces strony obejmuje DNS, serwer i backend
